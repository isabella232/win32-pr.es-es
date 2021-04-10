---
description: El SDK de Windows Search proporciona un ensamblado de interoperabilidad para trabajar con objetos del modelo de objetos componentes (COM) expuestos por Windows Search y otros programas en las interfaces y clases mediante código administrado.
ms.assetid: 9ade6f55-de65-4f73-9d22-1be819549704
title: Uso de código administrado con datos de shell y Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0a4c0f4182739fe553c21b45bcfc3a3af7a68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153991"
---
# <a name="using-managed-code-with-shell-data-and-windows-search"></a><span data-ttu-id="04fae-103">Uso de código administrado con datos de shell y Windows Search</span><span class="sxs-lookup"><span data-stu-id="04fae-103">Using Managed Code with Shell Data and Windows Search</span></span>

<span data-ttu-id="04fae-104">El SDK de Windows Search proporciona un ensamblado de interoperabilidad para trabajar con objetos del modelo de objetos componentes (COM) expuestos por Windows Search y otros programas en las interfaces y clases mediante código administrado.</span><span class="sxs-lookup"><span data-stu-id="04fae-104">The Windows Search SDK provides an interopability assembly for you to work with Component Object Model (COM) objects that are exposed by Windows Search and other programs against the interfaces and classes using managed code.</span></span> <span data-ttu-id="04fae-105">El ensamblado de interoperabilidad está firmado digitalmente por Microsoft y puede encontrarse con los [ejemplos de Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="04fae-105">The interopability assembly is digitally signed by Microsoft and can be found with the [Windows Search samples](-search-samples-ovw.md).</span></span>

<span data-ttu-id="04fae-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="04fae-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="04fae-107">Uso de la API de Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="04fae-107">Using the Windows API CodePack</span></span>](#using-the-windows-api-codepack)
    -   [<span data-ttu-id="04fae-108">Obtener acceso a los resultados del índice</span><span class="sxs-lookup"><span data-stu-id="04fae-108">Accessing Index Results</span></span>](#accessing-index-results)
    -   [<span data-ttu-id="04fae-109">Aplicación de ejemplo que usa la API de Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="04fae-109">Sample Application Using the Windows API Codepack</span></span>](#sample-application-using-the-windows-api-codepack)
-   [<span data-ttu-id="04fae-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04fae-110">Related topics</span></span>](#related-topics)

## <a name="using-the-windows-api-codepack"></a><span data-ttu-id="04fae-111">Uso de la API de Windows CodePack</span><span class="sxs-lookup"><span data-stu-id="04fae-111">Using the Windows API CodePack</span></span>

<span data-ttu-id="04fae-112">Si está trabajando en el entorno de Microsoft .NET, use el [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) para obtener los resultados de la búsqueda o simplemente examine el espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="04fae-112">If you are working in the Microsoft .NET environment, use the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) to obtain search results, or just browse the namespace.</span></span> <span data-ttu-id="04fae-113">El [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) proporciona una colección de elementos de Shell que básicamente son contenedores en torno a la [interfaz IShellItem](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem)nativa.</span><span class="sxs-lookup"><span data-stu-id="04fae-113">The [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility) provides you with a collection of Shell items that are essentially wrappers around the native [IShellItem Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellitem).</span></span> <span data-ttu-id="04fae-114">Puede recorrer en iteración esta colección y obtener los distintos valores de propiedad de forma similar a como se enumerarían los resultados en una tabla de una consulta de vinculación e incrustación de base de datos (OLE DB).</span><span class="sxs-lookup"><span data-stu-id="04fae-114">You can iterate over this collection and get the various property values in a fashion similar to how you would enumerate the results in a table from an Object Linking and Embedding Database (OLE DB) query.</span></span>

<span data-ttu-id="04fae-115">En el fragmento de código siguiente se muestra cómo recorrer en iteración los elementos de búsqueda y obtener los valores de propiedad para cada uno.</span><span class="sxs-lookup"><span data-stu-id="04fae-115">The following code snippet illustrates how to iterate over Search items and obtain the property values for each.</span></span>


```
foreach (ShellObject so in KnownFolders.SavedSearches)
{
    searchFolder = new ShellSearchFolder(finalSearchCondition, (ShellContainer)so);
    List<ShellObject> items = new List<ShellObject>();
    foreach (ShellObject so2 in searchFolder) items.Add(so2);   
}
```



### <a name="accessing-index-results"></a><span data-ttu-id="04fae-116">Obtener acceso a los resultados del índice</span><span class="sxs-lookup"><span data-stu-id="04fae-116">Accessing Index Results</span></span>

<span data-ttu-id="04fae-117">Puede tener acceso a los resultados del índice a través de OLE DB o del modelo de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="04fae-117">You can access index results through either OLE DB or the Shell data model.</span></span> <span data-ttu-id="04fae-118">Hay ventajas y desventajas con cualquiera de estos enfoques.</span><span class="sxs-lookup"><span data-stu-id="04fae-118">There are advantages and disadvantages with either approach.</span></span> <span data-ttu-id="04fae-119">Una ventaja es que OLE DB y Lenguaje de consulta estructurado (SQL) están familiarizados con los programadores de bases de datos.</span><span class="sxs-lookup"><span data-stu-id="04fae-119">One advantage is that OLE DB and Structured Query Language (SQL) are familiar to database programmers.</span></span> <span data-ttu-id="04fae-120">Otras ventajas son el mejor control sobre el rendimiento cuando se consulta solo el indexador y el acceso a una funcionalidad adicional, como la capacidad de buscar los resultados anteriores en un conjunto de filas nuevo rápidamente.</span><span class="sxs-lookup"><span data-stu-id="04fae-120">Other advantages are better control over performance when querying only the indexer, and access to additional functionality such as the ability to locate previous results in a new rowset quickly.</span></span>

<span data-ttu-id="04fae-121">Las ventajas del modelo de datos de Shell son que abstrae entre diferentes orígenes de información como OpenSearch y proporciona acceso a funcionalidad adicional, como miniaturas y controladores de propiedades.</span><span class="sxs-lookup"><span data-stu-id="04fae-121">Advantages of the Shell data model are that it abstracts across different sources of information such as OpenSearch, and provides access to additional functionality such as thumbnails and property handlers.</span></span> <span data-ttu-id="04fae-122">Además, el modelo de objetos de Shell requiere una compatibilidad especial para los resultados que no son de nombre de archivo, como los elementos de correo y los resultados de OneNote, o para cualquier elemento que resida en el índice del usuario.</span><span class="sxs-lookup"><span data-stu-id="04fae-122">Nor does the Shell object model require special case support for non-filename results such as mail items and OneNote results, nor for any item that resides in the user's index.</span></span> <span data-ttu-id="04fae-123">Tenga en cuenta que en Shell [KNOWNFOLDERID](../shell/knownfolderid.md) es el ámbito de carpeta conocido para el contenido indexado local.</span><span class="sxs-lookup"><span data-stu-id="04fae-123">Note that in Shell [KNOWNFOLDERID](../shell/knownfolderid.md) is the known folder scope for local indexed content.</span></span> <span data-ttu-id="04fae-124">Para obtener más información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="04fae-124">For more information on creating a Shell data source, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="04fae-125">Los orígenes de datos de OpenSearch no se exponen a través de OLE DB para la búsqueda federada en Windows 7 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="04fae-125">OpenSearch data sources are not exposed through OLE DB for federated search in Windows 7 and later.</span></span> <span data-ttu-id="04fae-126">Por esta razón, se recomienda que considere la posibilidad de escribir un proveedor LINQ para el espacio de nombres de Shell en lugar de usar OLE DB para tener acceso a los resultados del indexador.</span><span class="sxs-lookup"><span data-stu-id="04fae-126">For this reason we recommend that you consider writing a LINQ provider for the Shell namespace instead of using OLE DB to access the indexer results.</span></span> <span data-ttu-id="04fae-127">Para obtener más información, vea [Tutorial: crear un proveedor LINQ de IQueryable](/previous-versions/bb546158(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="04fae-127">For more information, see [Walkthrough: Creating an IQueryable LINQ Provider](/previous-versions/bb546158(v=vs.140)).</span></span>

### <a name="sample-application-using-the-windows-api-codepack"></a><span data-ttu-id="04fae-128">Aplicación de ejemplo que usa la API de Windows Codepack</span><span class="sxs-lookup"><span data-stu-id="04fae-128">Sample Application Using the Windows API Codepack</span></span>

<span data-ttu-id="04fae-129">La captura de pantalla siguiente representa un simulacro de una aplicación de ejemplo creada con el [paquete de código de la API de Windows para Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span><span class="sxs-lookup"><span data-stu-id="04fae-129">The following screenshot represents a mock up of a sample application created with the [Windows API Code Pack for Microsoft .NET Framework](https://www.nuget.org/packages/Microsoft.Windows.Compatibility).</span></span>

![captura de pantalla de la aplicación de reproductor de media que muestra mensajes de correo electrónico](images/folderid-searchhome.png)

## <a name="related-topics"></a><span data-ttu-id="04fae-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04fae-131">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="04fae-132">**Vista**</span><span class="sxs-lookup"><span data-stu-id="04fae-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04fae-133">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="04fae-133">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

<span data-ttu-id="04fae-134">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="04fae-134">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="04fae-135">[Interoperabilidad entre lenguajes](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="04fae-135">[Cross-Language Interoperability](/previous-versions/dotnet/netframework-1.1/730f1wy3(v=vs.71))</span></span>
</dt> </dl>

 

 
