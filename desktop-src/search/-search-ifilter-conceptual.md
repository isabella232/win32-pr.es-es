---
description: Obtenga información sobre cómo desarrollar controladores de filtros en Windows Search. La búsqueda usa filtros para extraer elementos para su inclusión en un índice de texto completo.
ms.assetid: 7b24986b-972d-4674-846b-f856b908edf4
title: Desarrollar controladores de filtro para Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa86c0a1e41ababf6f00db72a26784beb93e1879
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988864"
---
# <a name="developing-filter-handlers-for-windows-search"></a><span data-ttu-id="b212d-104">Desarrollar controladores de filtro para Windows Search</span><span class="sxs-lookup"><span data-stu-id="b212d-104">Developing Filter Handlers for Windows Search</span></span>

<span data-ttu-id="b212d-105">Microsoft Windows Search filtros para extraer el contenido de los elementos para su inclusión en un índice de texto completo.</span><span class="sxs-lookup"><span data-stu-id="b212d-105">Microsoft Windows Search uses filters to extract the content of items for inclusion in a full-text index.</span></span> <span data-ttu-id="b212d-106">Puede ampliar los Windows Search para indexar tipos de archivo nuevos o propietarios escribiendo filtros para extraer el contenido y controladores de propiedades para extraer las propiedades de los archivos.</span><span class="sxs-lookup"><span data-stu-id="b212d-106">You can extend Windows Search to index new or proprietary file types by writing filters to extract the content, and property handlers to extract the properties of files.</span></span>

<span data-ttu-id="b212d-107">En esta sección se proporciona el marco conceptual necesario para implementar un controlador de filtro (una implementación de la [**interfaz IFilter).**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="b212d-107">This section provides the conceptual framework that is necessary for implementing a filter handler (an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface).</span></span>

- [<span data-ttu-id="b212d-108">Descripción de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="b212d-108">Understanding Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)
- [<span data-ttu-id="b212d-109">Procedimientos recomendados para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="b212d-109">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)
- [<span data-ttu-id="b212d-110">Devolver propiedades de un controlador de filtros</span><span class="sxs-lookup"><span data-stu-id="b212d-110">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)
- [<span data-ttu-id="b212d-111">Controladores de filtro que se envían con Windows</span><span class="sxs-lookup"><span data-stu-id="b212d-111">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)
- [<span data-ttu-id="b212d-112">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="b212d-112">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)
- [<span data-ttu-id="b212d-113">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="b212d-113">Registering Filter Handlers</span></span>](-search-ifilter-registering-filters.md)
- [<span data-ttu-id="b212d-114">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="b212d-114">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)

## <a name="additional-resources"></a><span data-ttu-id="b212d-115">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="b212d-115">Additional Resources</span></span>

- <span data-ttu-id="b212d-116">El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub,](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)muestra cómo crear una clase base de IFilter para implementar la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="b212d-116">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>
- <span data-ttu-id="b212d-117">Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b212d-117">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="b212d-118">Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="b212d-118">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="b212d-119">Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Registro de aplicaciones.](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b212d-119">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>
