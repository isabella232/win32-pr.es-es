---
description: Compatibilidad de Windows 7 con la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows.
ms.assetid: 2014b7ac-4885-4f17-b6d4-5fd95872ed59
title: Búsqueda federada en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d7718bb5215072ceeb8786f5728017ed329e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497080"
---
# <a name="federated-search-in-windows"></a><span data-ttu-id="6b3e0-103">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-103">Federated Search in Windows</span></span>

<span data-ttu-id="6b3e0-104">Compatibilidad de Windows 7 con la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch permite a los usuarios tener acceso a sus datos remotos e interactuar con ellos desde el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="6b3e0-104">Windows 7 support for search federation to remote data stores using OpenSearch technologies enables users to access and interact with their remote data from within Windows Explorer.</span></span>

<span data-ttu-id="6b3e0-105">En la siguiente lista de temas se describe cómo se puede crear un almacén de datos basado en Web que se puede buscar mediante la búsqueda federada de Windows y habilitar la integración enriquecida de los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="6b3e0-105">The following list of topics describe how you can build a web-based data store that can be searched using Windows federated search, and enable rich integration of your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

-   [<span data-ttu-id="6b3e0-106">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-106">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
-   [<span data-ttu-id="6b3e0-107">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-107">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
-   [<span data-ttu-id="6b3e0-108">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-108">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
-   [<span data-ttu-id="6b3e0-109">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="6b3e0-109">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
-   [<span data-ttu-id="6b3e0-110">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-110">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
-   [<span data-ttu-id="6b3e0-111">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-111">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
-   [<span data-ttu-id="6b3e0-112">Esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="6b3e0-112">Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)

## <a name="additional-resources"></a><span data-ttu-id="6b3e0-113">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6b3e0-113">Additional Resources</span></span>

-   <span data-ttu-id="6b3e0-114">En el ejemplo de código [OpenSearch](-search-sample-opensearch.md) se muestra cómo crear un servicio de búsqueda federado mediante el protocolo [OpenSearch](https://github.com/dewitt/opensearch) y un archivo de descriptor de OpenSearch (. osdx) (un conector de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="6b3e0-114">The [OpenSearch](-search-sample-opensearch.md) code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>
-   <span data-ttu-id="6b3e0-115">Para ver una demostración en vídeo sobre la creación de un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) para una base de datos SQL, vea [Windows 7: permite a los usuarios buscar, visualizar y organizar sus datos con las bibliotecas y el explorador](https://channel9.msdn.com/pdc2008/PC16/).</span><span class="sxs-lookup"><span data-stu-id="6b3e0-115">For a video demonstration of creating an [OpenSearch](https://github.com/dewitt/opensearch) web service for a SQL database, see [Windows 7: Empower Users to Find, Visualize and Organize their Data with Libraries and the Explorer](https://channel9.msdn.com/pdc2008/PC16/).</span></span>
-   <span data-ttu-id="6b3e0-116">Si está escribiendo un proveedor de [OpenSearch](https://github.com/dewitt/opensearch) en el lado cliente, consulte:</span><span class="sxs-lookup"><span data-stu-id="6b3e0-116">If you are writing a client-side [OpenSearch](https://github.com/dewitt/opensearch) provider, see:</span></span>
    -   <span data-ttu-id="6b3e0-117">El [desarrollador de OpenSearch guía de procedimientos](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) para obtener más información sobre cómo conectarse a un proveedor del lado cliente mediante el uso de protocolos o API del almacén de datos de su propiedad.</span><span class="sxs-lookup"><span data-stu-id="6b3e0-117">The [OpenSearch Developer How To Guide](https://github.com/dewitt/opensearch/blob/master/mediawiki/Documentation/Developer%20how%20to%20guide.wiki) for more information on connecting to a client-side provider by using a proprietary data store's protocols or APIs.</span></span>
    -   <span data-ttu-id="6b3e0-118">[Información general de la documentación del esquema de Descripción del conector de búsqueda](search-sconn-desc-schema-entry.md) (. searchconnector-MS).</span><span class="sxs-lookup"><span data-stu-id="6b3e0-118">The [Overview of the Search Connector Description Schema](search-sconn-desc-schema-entry.md) (.searchconnector-ms) schema documentation.</span></span>
-   <span data-ttu-id="6b3e0-119">Vea el sitio web del [centro de descarga de Microsoft](https://www.microsoft.com/DOWNLOADS/en/default.aspx) para el siguiente recurso descargable: ejemplo de search Server 2008 Sample: conector de búsqueda federado.</span><span class="sxs-lookup"><span data-stu-id="6b3e0-119">See the [Microsoft Download Center](https://www.microsoft.com/DOWNLOADS/en/default.aspx) website for the following downloadable resource: Search Server 2008 Sample: Federated Search Connector Sample.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b3e0-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b3e0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b3e0-121">Información general sobre Windows Search</span><span class="sxs-lookup"><span data-stu-id="6b3e0-121">Windows Search Overview</span></span>](-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="6b3e0-122">Guía del desarrollador de Windows Search</span><span class="sxs-lookup"><span data-stu-id="6b3e0-122">Windows Search Developer's Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="6b3e0-123">Referencia de Windows Search</span><span class="sxs-lookup"><span data-stu-id="6b3e0-123">Windows Search Reference</span></span>](-search-reference-entry-page.md)
</dt> <dt>

[<span data-ttu-id="6b3e0-124">Ejemplos de código de Windows Search</span><span class="sxs-lookup"><span data-stu-id="6b3e0-124">Windows Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

[<span data-ttu-id="6b3e0-125">Tecnologías de búsqueda relacionadas</span><span class="sxs-lookup"><span data-stu-id="6b3e0-125">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)
</dt> <dt>

[<span data-ttu-id="6b3e0-126">Glosario de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="6b3e0-126">Windows Search Glossary</span></span>](search-glossary.md)
</dt> </dl>

 

 



