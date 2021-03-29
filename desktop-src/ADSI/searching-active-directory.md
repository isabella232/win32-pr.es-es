---
title: Buscar Active Directory
description: Una función importante de Active Directory consiste en resolver las consultas de datos para los usuarios, así como los datos de configuración de los equipos y servicios.
ms.assetid: 8427d69b-0974-4adc-9732-790e5d31db7a
ms.tgt_platform: multiple
keywords:
- Buscar Active Directory ADSI
- ADSI ADSI, buscar Active Directory
- consultas ADSI, buscar Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1881872be6092312015f22eba477599ed9394df7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356692"
---
# <a name="searching-active-directory"></a><span data-ttu-id="f4f88-106">Buscar Active Directory</span><span class="sxs-lookup"><span data-stu-id="f4f88-106">Searching Active Directory</span></span>

<span data-ttu-id="f4f88-107">Una función importante de Active Directory consiste en resolver las consultas de datos para los usuarios, así como los datos de configuración de los equipos y servicios.</span><span class="sxs-lookup"><span data-stu-id="f4f88-107">An important function of Active Directory is to resolve data queries for people, as well as configuration data for computers and services.</span></span> <span data-ttu-id="f4f88-108">Para escribir consultas eficaces para Active Directory, resulta útil estar familiarizado con lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f4f88-108">To write efficient queries for Active Directory, it is helpful to be familiar with the following:</span></span>

-   <span data-ttu-id="f4f88-109">Determinar el ámbito de la consulta: ¿debe encontrar el cliente las propiedades de los objetos que pueden encontrarse en cualquier lugar dentro de un bosque, solo dentro de un dominio o en una unidad organizativa (OU) determinada?</span><span class="sxs-lookup"><span data-stu-id="f4f88-109">Determining the scope of the query: Must the client find properties for objects that might be located anywhere within a forest, or only within one domain, or within a given organizational unit (OU)?</span></span>
-   <span data-ttu-id="f4f88-110">Determinar la profundidad de la consulta: ¿la consulta solo debe buscar un nivel o podría cruzarse en otros directorios LDAP?</span><span class="sxs-lookup"><span data-stu-id="f4f88-110">Determining the depth of the query: Must the query only search one level or might it cross into other LDAP directories?</span></span>
-   <span data-ttu-id="f4f88-111">Rendimiento y control de grandes conjuntos de resultados: ¿Cómo debe el cliente controlar eficazmente el potencial de un conjunto de resultados grande?</span><span class="sxs-lookup"><span data-stu-id="f4f88-111">Performance and handling large result sets: How should the client effectively handle the potential of a large result set?</span></span>
-   <span data-ttu-id="f4f88-112">Determinar las mejores consultas: ¿Qué tipo de consultas proporcionan los resultados más eficaces?</span><span class="sxs-lookup"><span data-stu-id="f4f88-112">Determining the best queries: What type of queries provide the most efficient results?</span></span> <span data-ttu-id="f4f88-113">¿Qué tipo de consultas debe evitar el desarrollador?</span><span class="sxs-lookup"><span data-stu-id="f4f88-113">What type of queries should the developer avoid?</span></span>
-   <span data-ttu-id="f4f88-114">Descripción de la sintaxis de las consultas: ADSI admite la sintaxis LDAP tal y como se documenta en RFC 2254, así como un subconjunto de SQL.</span><span class="sxs-lookup"><span data-stu-id="f4f88-114">Understanding the query syntax: ADSI supports both the LDAP syntax as documented in RFC 2254, as well as a subset of SQL.</span></span>
-   <span data-ttu-id="f4f88-115">Elección de interfaces: ADSI proporciona compatibilidad con OLE DB, así como una interfaz de C/C++ denominada [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span><span class="sxs-lookup"><span data-stu-id="f4f88-115">Choice of interfaces: ADSI provides both OLE DB support as well as a C/C++ interface called [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch).</span></span> <span data-ttu-id="f4f88-116">Dado que ADSI funciona para varios espacios de nombres, puede utilizar estas interfaces para consultar otros espacios de nombres, como Exchange, así como Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f4f88-116">Because ADSI works for multiple namespaces, you can use these interfaces for querying other namespaces such as Exchange, as well as Active Directory.</span></span> <span data-ttu-id="f4f88-117">Dado que el objeto de datos ActiveX (ADO) es un modelo de objetos de acceso a datos sencillo que se puede incluir en scripts sobre OLE DB, las interfaces de OLE DB funcionan bien para los programadores de Visual Basic y los escritores de scripts de página web.</span><span class="sxs-lookup"><span data-stu-id="f4f88-117">Because the ActiveX Data Object (ADO) is a simple scriptable data access object model on top of OLE DB, the OLE DB interfaces work well for Visual Basic programmers and webpage script writers.</span></span> <span data-ttu-id="f4f88-118">Las nuevas características de acceso a datos dentro de Visual Studio y las aplicaciones de Office que aprovechan las ventajas de ADO y OLE DB ahora pueden tener acceso a los datos de Active Directory de la misma manera que obtienen acceso a los datos de otros proveedores de OLE DB, como SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f4f88-118">The new data access features within Visual Studio and Office applications that take advantage of ADO and OLE DB can now access Active Directory data in the same way that they access data from other OLE DB providers, such as SQL Server.</span></span> <span data-ttu-id="f4f88-119">Sin embargo, si un desarrollador de C/C++ debe realizar una búsqueda de directorio simple, la interfaz **IDirectorySearch** podría ser más adecuada que las interfaces OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f4f88-119">However, if a C/C++ developer must perform a simple directory search, the **IDirectorySearch** interface might be more appropriate than the OLE DB interfaces.</span></span>

<span data-ttu-id="f4f88-120">En los temas siguientes se describe cómo buscar Active Directory para asegurarse de que la aplicación emite la consulta más eficaz, dados los requisitos del cliente:</span><span class="sxs-lookup"><span data-stu-id="f4f88-120">The following topics describe how to search Active Directory to ensure your application issues the most efficient query, given the requirements of the client:</span></span>

-   [<span data-ttu-id="f4f88-121">Ámbito de la consulta</span><span class="sxs-lookup"><span data-stu-id="f4f88-121">Scope of Query</span></span>](scope-of-query.md)
-   [<span data-ttu-id="f4f88-122">Rendimiento y control de grandes conjuntos de resultados</span><span class="sxs-lookup"><span data-stu-id="f4f88-122">Performance and Handling Large Result Sets</span></span>](performance-and-handling-large-result-sets.md)
-   [<span data-ttu-id="f4f88-123">Sintaxis de filtro de búsqueda</span><span class="sxs-lookup"><span data-stu-id="f4f88-123">Search Filter Syntax</span></span>](search-filter-syntax.md)
-   [<span data-ttu-id="f4f88-124">Interfaces de consulta</span><span class="sxs-lookup"><span data-stu-id="f4f88-124">Query Interfaces</span></span>](query-interfaces.md)
-   [<span data-ttu-id="f4f88-125">Buscar datos binarios</span><span class="sxs-lookup"><span data-stu-id="f4f88-125">Searching Binary Data</span></span>](searching-binary-data.md)
-   [<span data-ttu-id="f4f88-126">Consulta distribuida</span><span class="sxs-lookup"><span data-stu-id="f4f88-126">Distributed Query</span></span>](distributed-query.md)

 

 




