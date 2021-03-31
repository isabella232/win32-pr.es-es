---
title: Enlazar con el catálogo global
description: El catálogo global es un espacio de nombres que contiene los datos de directorio de todos los dominios de un bosque.
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- Enlazar al anuncio de catálogo global
- Catálogo global (AD), enlazar a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077563"
---
# <a name="binding-to-the-global-catalog"></a><span data-ttu-id="89cdf-105">Enlazar con el catálogo global</span><span class="sxs-lookup"><span data-stu-id="89cdf-105">Binding to the Global Catalog</span></span>

<span data-ttu-id="89cdf-106">El catálogo global es un espacio de nombres que contiene los datos de directorio de todos los dominios de un bosque.</span><span class="sxs-lookup"><span data-stu-id="89cdf-106">The Global Catalog is a namespace that contains directory data for all domains in a forest.</span></span> <span data-ttu-id="89cdf-107">El catálogo global contiene una réplica parcial de cada directorio de dominio.</span><span class="sxs-lookup"><span data-stu-id="89cdf-107">The Global Catalog contains a partial replica of every domain directory.</span></span> <span data-ttu-id="89cdf-108">Contiene una entrada para cada objeto del bosque de empresa, pero no contiene todas las propiedades de cada objeto.</span><span class="sxs-lookup"><span data-stu-id="89cdf-108">It contains an entry for every object in the enterprise forest, but does not contain all the properties of each object.</span></span> <span data-ttu-id="89cdf-109">En su lugar, solo contiene las propiedades especificadas para su inclusión en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-109">Instead, it contains only the properties specified for inclusion in the Global Catalog.</span></span>

<span data-ttu-id="89cdf-110">El catálogo global se almacena en servidores específicos de toda la empresa.</span><span class="sxs-lookup"><span data-stu-id="89cdf-110">The Global Catalog is stored on specific servers throughout the enterprise.</span></span> <span data-ttu-id="89cdf-111">Solo los controladores de dominio pueden servir como servidores de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-111">Only domain controllers can serve as Global Catalog servers.</span></span> <span data-ttu-id="89cdf-112">Los administradores indican si un controlador de dominio determinado contiene un catálogo global mediante el Active Directory el administrador de sitios y servicios.</span><span class="sxs-lookup"><span data-stu-id="89cdf-112">Administrators indicate whether a given domain controller holds a Global Catalog by using the Active Directory Sites and Services Manager.</span></span>

<span data-ttu-id="89cdf-113">Para enlazar con el catálogo global con ADSI, use el moniker "GC:".</span><span class="sxs-lookup"><span data-stu-id="89cdf-113">To bind to the Global Catalog with ADSI, use the "GC:" moniker.</span></span>

<span data-ttu-id="89cdf-114">Hay dos maneras de enlazar con el catálogo global para realizar una búsqueda en un bosque:</span><span class="sxs-lookup"><span data-stu-id="89cdf-114">There are two ways to bind to the Global Catalog to perform a search in a forest:</span></span>

-   <span data-ttu-id="89cdf-115">Enlazar con el objeto raíz de la empresa para buscar en todos los dominios del bosque.</span><span class="sxs-lookup"><span data-stu-id="89cdf-115">Bind to the enterprise root object to search across all domains in the forest.</span></span>
-   <span data-ttu-id="89cdf-116">Enlazar a un objeto específico para buscar ese objeto y sus elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="89cdf-116">Bind to a specific object to search that object and its children.</span></span> <span data-ttu-id="89cdf-117">Por ejemplo, si se enlaza a un dominio que tiene dos dominios debajo en un árbol de dominios del bosque, puede buscar en estos tres dominios.</span><span class="sxs-lookup"><span data-stu-id="89cdf-117">For example, if you bind to a domain that has two domains beneath it in a domain tree in the forest, you can search across those three domains.</span></span> <span data-ttu-id="89cdf-118">Tenga en cuenta que el nombre distintivo del objeto al que se va a enlazar es exactamente el mismo que el nombre distintivo que se usa para enlazar con el espacio de nombres "LDAP:".</span><span class="sxs-lookup"><span data-stu-id="89cdf-118">Be aware that the distinguished name for the object to bind to is exactly the same as the distinguished name used to bind to the "LDAP:" namespace.</span></span> <span data-ttu-id="89cdf-119">Recuerde que "LDAP:" es una réplica completa de un solo dominio y que "GC:" es una réplica parcial de todos los dominios del bosque.</span><span class="sxs-lookup"><span data-stu-id="89cdf-119">Recall that "LDAP:" is a full replica of a single domain and that "GC:" is a partial replica of all domains in the forest.</span></span>

<span data-ttu-id="89cdf-120">Al igual que con el moniker "LDAP:", puede utilizar el enlace sin servidor o enlazar a un servidor de catálogo global específico.</span><span class="sxs-lookup"><span data-stu-id="89cdf-120">As with the "LDAP:" moniker, you can use serverless binding or bind to a specific Global Catalog server.</span></span> <span data-ttu-id="89cdf-121">Si busca en el bosque actual, use el enlace sin servidor.</span><span class="sxs-lookup"><span data-stu-id="89cdf-121">If searching in the current forest, use serverless binding.</span></span> <span data-ttu-id="89cdf-122">Sin embargo, si realiza búsquedas en otro bosque, especifique un nombre de dominio o un servidor de catálogo global con el que enlazar, como se muestra en los ejemplos siguientes.</span><span class="sxs-lookup"><span data-stu-id="89cdf-122">However, if searching in another forest, specify either a domain name or a Global Catalog server to bind to, such as shown in the following examples.</span></span>

<span data-ttu-id="89cdf-123">Enlazar con el nombre de dominio:</span><span class="sxs-lookup"><span data-stu-id="89cdf-123">Bind using the domain name:</span></span>

``` syntax
GC://fabrikam.com
```

<span data-ttu-id="89cdf-124">Enlazar con el nombre del servidor:</span><span class="sxs-lookup"><span data-stu-id="89cdf-124">Bind using the server name:</span></span>

``` syntax
GC://servername
```

<span data-ttu-id="89cdf-125">También puede enlazar a un objeto específico en el catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-125">You can also bind to a specific object within the Global Catalog.</span></span> <span data-ttu-id="89cdf-126">Para enlazar con el objeto sales del dominio Fabrikam, use el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="89cdf-126">To bind to the sales object in the fabrikam domain, use the following format.</span></span>

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="89cdf-127">O bien, para enlazar al objeto sales del servidor, use el formato siguiente.</span><span class="sxs-lookup"><span data-stu-id="89cdf-127">Or, to bind to the sales object on the server, use the following format.</span></span>

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

<span data-ttu-id="89cdf-128">**Para buscar en todo el bosque**</span><span class="sxs-lookup"><span data-stu-id="89cdf-128">**To search the entire forest**</span></span>

1.  <span data-ttu-id="89cdf-129">Enlazar a la raíz del espacio de nombres del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-129">Bind to the root of the Global Catalog namespace.</span></span>
2.  <span data-ttu-id="89cdf-130">Enumerar el contenedor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-130">Enumerate the Global Catalog container.</span></span> <span data-ttu-id="89cdf-131">El contenedor de catálogos globales contiene un solo objeto que puede usar para buscar en todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="89cdf-131">The Global Catalog container contains a single object that you can use to search the entire forest.</span></span>
3.  <span data-ttu-id="89cdf-132">Use el objeto en el contenedor para realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89cdf-132">Use the object in the container to perform the search.</span></span> <span data-ttu-id="89cdf-133">En C/C++, llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero de [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) en el objeto, de modo que pueda usar la interfaz **IDirectorySearch** para realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89cdf-133">In C/C++, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get an [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) pointer on the object so that you can use the **IDirectorySearch** interface to perform the search.</span></span> <span data-ttu-id="89cdf-134">En Visual Basic, utilice el objeto devuelto de la enumeración en la consulta de ADO.</span><span class="sxs-lookup"><span data-stu-id="89cdf-134">In Visual Basic, use the object returned from the enumeration in your ADO query.</span></span>

<span data-ttu-id="89cdf-135">Para enumerar los servidores de catálogo global de un sitio, realice una búsqueda de subárbol LDAP de "CN = <yoursite> , CN = Sites <DN of the configurationNamingContext> ", usando la siguiente cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="89cdf-135">To enumerate the Global Catalog servers in a site, perform an LDAP subtree search of "cn=<yoursite>,cn=sites,<DN of the configurationNamingContext>", using the following filter string.</span></span>

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

<span data-ttu-id="89cdf-136">Este filtro usa el **bit de la \_ regla de coincidencia LDAP \_ \_ \_ y** el operador de regla de coincidencia (1.2.840.113556.1.4.803) para buscar objetos **nTDSDSA** que tengan el bit de orden inferior establecido en la máscara de bits del atributo **Options** .</span><span class="sxs-lookup"><span data-stu-id="89cdf-136">This filter uses the **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule operator (1.2.840.113556.1.4.803) to find **nTDSDSA** objects that have the low-order bit set in the bitmask of the **options** attribute.</span></span> <span data-ttu-id="89cdf-137">El bit de orden inferior, que corresponde a la constante de **\_ \_ \_ GC nTDSDSA is** Defined en ntdsapi. h, identifica el objeto **nTDSDSA** de un servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-137">The low-order bit, which corresponds to the **NTDSDSA\_OPT\_IS\_GC** constant defined in Ntdsapi.h, identifies the **nTDSDSA** object of a Global Catalog server.</span></span> <span data-ttu-id="89cdf-138">Para obtener más información sobre las reglas de coincidencia, consulte [Sintaxis de filtro de búsqueda](/windows/desktop/ADSI/search-filter-syntax).</span><span class="sxs-lookup"><span data-stu-id="89cdf-138">For more information about matching rules, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

<span data-ttu-id="89cdf-139">El elemento primario del objeto **nTDSDSA** es el objeto Server y la propiedad **DnsHostName** del objeto Server es el nombre DNS del servidor de catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-139">The parent of the **nTDSDSA** object is the server object, and the **dNSHostName** property of the server object is the DNS name of the Global Catalog server.</span></span>

<span data-ttu-id="89cdf-140">No puede usar las \# constantes de definición como **nTDSDSA \_ OPC \_ es \_** el bit de la regla de coincidencia de GC y **LDAP, \_ \_ \_ \_ y** directamente en una cadena de filtro de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="89cdf-140">You cannot use \#define constants such as **NTDSDSA\_OPT\_IS\_GC** and **LDAP\_MATCHING\_RULE\_BIT\_AND** directly in a search filter string.</span></span> <span data-ttu-id="89cdf-141">Sin embargo, puede usar estas constantes como argumentos para una función como [**swprintf \_ s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) para insertar los valores constantes en una cadena de filtro.</span><span class="sxs-lookup"><span data-stu-id="89cdf-141">However, you could use these constants as arguments to a function such as [**swprintf\_s**](/windows/win32/api/winuser/nf-winuser-wsprintfa) to insert the constant values into a filter string.</span></span>

<span data-ttu-id="89cdf-142">El catálogo global no representa la estructura de árbol de todo el bosque.</span><span class="sxs-lookup"><span data-stu-id="89cdf-142">The global catalog does not represent the entire forest tree structure.</span></span> <span data-ttu-id="89cdf-143">Por ejemplo, podría esperar que el ejemplo de código siguiente enumerara todos los dominios del bosque y todos los objetos secundarios de cada dominio.</span><span class="sxs-lookup"><span data-stu-id="89cdf-143">For example, you might expect that the following code example would enumerate all of the domains in the forest and all child objects of each domain.</span></span> <span data-ttu-id="89cdf-144">En realidad, lo que realmente hace es enumerar todos los dominios del bosque, pero ninguno de los objetos de dominio enumerados contiene elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="89cdf-144">In reality, what it actually does is enumerate all of the domains in the forest, but none of the enumerated domain objects contain any children.</span></span> <span data-ttu-id="89cdf-145">Se trata de una limitación del catálogo global.</span><span class="sxs-lookup"><span data-stu-id="89cdf-145">This is a limitation of the global catalog.</span></span>


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="89cdf-146">Para corregir esto, es necesario enlazar con cada objeto de dominio y, a continuación, enumerar los objetos secundarios de cada dominio.</span><span class="sxs-lookup"><span data-stu-id="89cdf-146">To correct this, it is necessary to bind to each domain object and then enumerate the child objects of each domain.</span></span> <span data-ttu-id="89cdf-147">En el ejemplo de código siguiente se muestra la técnica adecuada.</span><span class="sxs-lookup"><span data-stu-id="89cdf-147">The proper technique is shown in the following code example.</span></span>


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



<span data-ttu-id="89cdf-148">Para obtener más información y ejemplos de código que muestren cómo buscar en todo el bosque, vea el [código de ejemplo para buscar en un bosque](example-code-for-searching-a-forest.md).</span><span class="sxs-lookup"><span data-stu-id="89cdf-148">For more information and code examples that show how to search an entire forest, see [Example Code for Searching a Forest](example-code-for-searching-a-forest.md).</span></span>

 

 