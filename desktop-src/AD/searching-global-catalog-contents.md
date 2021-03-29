---
title: Buscar en el catálogo global
description: Active Directory Domain Services también tienen un catálogo global (GC), que contiene una réplica parcial de todos los objetos del directorio.
ms.assetid: 83970563-1a56-4671-b264-56e29939e369
ms.tgt_platform: multiple
keywords:
- Buscar en el catálogo global Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a057330309c12df6d18a209fc3d2adaf42b03005
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773093"
---
# <a name="searching-the-global-catalog"></a><span data-ttu-id="c0483-104">Buscar en el catálogo global</span><span class="sxs-lookup"><span data-stu-id="c0483-104">Searching the Global Catalog</span></span>

<span data-ttu-id="c0483-105">Active Directory Domain Services también tienen un catálogo global (GC), que contiene una réplica parcial de todos los objetos del directorio.</span><span class="sxs-lookup"><span data-stu-id="c0483-105">Active Directory Domain Services also have a global catalog (GC), which contains a partial replica of all objects in the directory.</span></span> <span data-ttu-id="c0483-106">También contiene réplicas parciales del esquema y los contenedores de configuración.</span><span class="sxs-lookup"><span data-stu-id="c0483-106">It also contains partial replicas of the schema and configuration containers.</span></span> <span data-ttu-id="c0483-107">Uno o varios controladores de dominio de un dominio pueden contener una copia del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="c0483-107">One or more domain controllers in a domain can hold a copy of the global catalog.</span></span> <span data-ttu-id="c0483-108">Para obtener más información sobre cómo enlazar a un catálogo global, vea [enlazar con el catálogo global](binding-to-the-global-catalog.md).</span><span class="sxs-lookup"><span data-stu-id="c0483-108">For more information about binding to a global catalog, see [Binding to the Global Catalog](binding-to-the-global-catalog.md).</span></span>

<span data-ttu-id="c0483-109">El catálogo global contiene una réplica de cada objeto en Active Directory Domain Services, pero solo con un número pequeño de sus atributos.</span><span class="sxs-lookup"><span data-stu-id="c0483-109">The global catalog holds a replica of every object in Active Directory Domain Services, but with only a small number of their attributes.</span></span> <span data-ttu-id="c0483-110">Los atributos del catálogo global son los que se usan con más frecuencia en las operaciones de búsqueda, como el nombre y los apellidos de un usuario, los nombres de inicio de sesión, etc.</span><span class="sxs-lookup"><span data-stu-id="c0483-110">The attributes in the global catalog are those most frequently used in search operations, such as a user's first and last names, login names, and so on.</span></span> <span data-ttu-id="c0483-111">Los atributos del catálogo global también incluyen los necesarios para buscar una réplica completa del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0483-111">The global catalog attributes also include those required to locate a full replica of the object.</span></span> <span data-ttu-id="c0483-112">El catálogo global permite a los usuarios encontrar rápidamente objetos de interés sin saber qué dominio los contiene y sin necesidad de un espacio de nombres extendido contiguo en la empresa. es decir, puede buscar en todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="c0483-112">The global catalog allows users to quickly find objects of interest without knowing what domain holds them and without requiring a contiguous extended namespace in the enterprise; that is, you can search the entire forest.</span></span>

<span data-ttu-id="c0483-113">Por lo tanto, si se enlaza a un objeto en el catálogo global, buscará ese objeto y toda la jerarquía debajo de él, sin tener que ir a ningún otro servidor.</span><span class="sxs-lookup"><span data-stu-id="c0483-113">So, if you bind to an object in the global catalog, you will search that object and the entire hierarchy below it — without having to go to any other server.</span></span> <span data-ttu-id="c0483-114">Sin embargo, la búsqueda solo puede utilizar un filtro de consulta que contenga propiedades en el catálogo global y solo puede recuperar propiedades en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="c0483-114">However, the search can only use a query filter containing properties in the global catalog and can retrieve only properties in the global catalog.</span></span>

<span data-ttu-id="c0483-115">La búsqueda en el catálogo global presenta las siguientes ventajas:</span><span class="sxs-lookup"><span data-stu-id="c0483-115">Searching the global catalog has the following benefits:</span></span>

-   <span data-ttu-id="c0483-116">El catálogo global permite buscar en todo el bosque o en cualquier parte del bosque, así como en el esquema y los contenedores de configuración.</span><span class="sxs-lookup"><span data-stu-id="c0483-116">Global catalog enables you to search the entire forest or any part of the forest as well as the schema and configuration containers.</span></span>
-   <span data-ttu-id="c0483-117">El catálogo global permite realizar una búsqueda completa en un solo servidor.</span><span class="sxs-lookup"><span data-stu-id="c0483-117">Global catalog enables you to perform a complete search on a single server.</span></span> <span data-ttu-id="c0483-118">No es necesario realizar referencias ni el seguimiento de la referencia.</span><span class="sxs-lookup"><span data-stu-id="c0483-118">No referrals or referral chasing is required.</span></span>

<span data-ttu-id="c0483-119">La búsqueda en el catálogo global tiene las siguientes desventajas:</span><span class="sxs-lookup"><span data-stu-id="c0483-119">Searching the global catalog has the following disadvantages:</span></span>

-   <span data-ttu-id="c0483-120">El catálogo global contiene un pequeño subconjunto de las propiedades de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="c0483-120">Global catalog contains a small subset of the properties on each object.</span></span> <span data-ttu-id="c0483-121">Si el filtro de consulta incluye propiedades que no están en el catálogo global, la consulta evaluará las expresiones que contienen esas propiedades como false.</span><span class="sxs-lookup"><span data-stu-id="c0483-121">If your query filter includes properties that are not in the global catalog, the query will evaluate the expressions containing those properties as false.</span></span> <span data-ttu-id="c0483-122">Si especifica propiedades de catálogo no globales en la lista de propiedades que se van a devolver, dichas propiedades no se recuperan.</span><span class="sxs-lookup"><span data-stu-id="c0483-122">If you specify non-global catalog properties in the list of properties to return, those properties are not retrieved.</span></span>
-   <span data-ttu-id="c0483-123">Para buscar en el catálogo global, debe haber disponible un controlador de dominio que contenga un catálogo global.</span><span class="sxs-lookup"><span data-stu-id="c0483-123">To search the global catalog, a domain controller that contains a global catalog must be available.</span></span> <span data-ttu-id="c0483-124">Si no hay ninguno disponible, no se puede realizar una búsqueda en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="c0483-124">If one is not available, you cannot perform a global catalog search.</span></span>
-   <span data-ttu-id="c0483-125">El catálogo global es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c0483-125">The global catalog is read-only.</span></span> <span data-ttu-id="c0483-126">Esto significa que no se puede enlazar a un objeto en el catálogo global para crear, modificar o eliminar objetos.</span><span class="sxs-lookup"><span data-stu-id="c0483-126">This means you cannot bind to an object in the global catalog to create, modify, or delete objects.</span></span>

 

 




