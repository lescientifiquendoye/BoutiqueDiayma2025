# Boutique Diayma

### Tâche 2 – Projets de la solution
La solution `Diayma.sln` référence un projet : `P2FixAnAppDotNetCode/Diayma.csproj` (application ASP.NET Core MVC).


### 3 – La version du SDK .NET utilisée est 2.0.0

### 6 -  2 bugs trouvés:
1. Il n’y a pas la possibilité de retourner à l’accueil après la validation de l’achat.

2. Le stock n’est pas mis à jour après l’achat.
### Tâche 8 – Parcours avant affichage des produits

## 8 - Flux d'exécution de la page d'accueil :

1. **Program.Main()** → Démarre l'application
2. **Startup.ConfigureServices()** (ligne 20) → Enregistre les services (MVC, ProductService, ProductRepository, Cart, etc.)
3. **Startup.Configure()** → Configure la route par défaut : `{controller=Product}/{action=Index}`
4. **ProductController.Index()** (ligne 15) → Contrôleur appelé pour `/`
5. **ProductService.GetAllProducts()** → Récupère les produits
6. **ProductRepository.GetAllProducts()** → Accède aux données
7. **ProductController.Index()** → Retourne `View(products)`
8. **Views/Product/Index.cshtml** → Affiche la liste des produits
9. **CartSummaryViewComponent.Invoke()** (ligne 12) → Affiche le résumé du panier dans le layout

**Namespaces/Classes/Méthodes principales** :
- `P2FixAnAppDotNetCode.Program.Main()`
- `P2FixAnAppDotNetCode.Startup.ConfigureServices()` / `Configure()`
- `P2FixAnAppDotNetCode.Controllers.ProductController.Index()`
- `P2FixAnAppDotNetCode.Models.Services.ProductService.GetAllProducts()`
- `P2FixAnAppDotNetCode.Models.Repositories.ProductRepository.GetAllProducts()`
- `P2FixAnAppDotNetCode.Components.CartSummaryViewComponent.Invoke()`

**Mode de débogage** : Pas à pas principal (F10) pour suivre le flux, Pas à pas détaillé (F11) pour entrer dans les services.

### Tâche 10 – Lien de téléchargement





