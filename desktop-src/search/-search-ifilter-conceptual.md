---
description: Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desarrollar controladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8f45892549dc3f392824c31c78884b209d283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082021"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="1951b-103">Desarrollar controladores de filtro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="1951b-103">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="1951b-104">Microsoft Windows Search usa filtros para extraer el contenido de los elementos que se van a incluir en un índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="1951b-104">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="1951b-105">Puede extender Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.</span><span class="sxs-lookup"><span data-stu-id="1951b-105">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="1951b-106">En esta sección se proporciona el marco conceptual que es necesario para implementar un controlador de filtro (una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).</span><span class="sxs-lookup"><span data-stu-id="1951b-106">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="1951b-107">Descripción de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="1951b-107">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="1951b-108">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="1951b-108">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="1951b-109">Devolver propiedades de un controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="1951b-109">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="1951b-110">Controladores de filtro que se distribuyen con Windows</span><span class="sxs-lookup"><span data-stu-id="1951b-110">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="1951b-111">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="1951b-111">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="1951b-112">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="1951b-112">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="1951b-113">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="1951b-113">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="1951b-114">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1951b-114">Additional Resources</span></span>

- <span data-ttu-id="1951b-115">En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="1951b-115">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="1951b-116">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1951b-116">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="1951b-117">Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="1951b-117">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="1951b-118">Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1951b-118">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
