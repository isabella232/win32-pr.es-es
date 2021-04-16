---
description: Puede extender Windows Search para indizar el contenido y las propiedades de los nuevos formatos de archivo y los almacenes de datos mediante interfaces de complementos de datos.
ms.assetid: 69edf316-77a8-4cc5-9af8-fb89f440c9ea
title: Extensión del índice (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a74638dd5366732716335af938c00098cc3991c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705501"
---
# <a name="extending-the-index-windows-search"></a><span data-ttu-id="8d16a-103">Extensión del índice (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="8d16a-103">Extending the Index (Windows Search)</span></span>

<span data-ttu-id="8d16a-104">Puede extender Windows Search para indizar el contenido y las propiedades de los nuevos formatos de archivo y los almacenes de datos mediante [interfaces de complementos de datos](./-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="8d16a-104">You can extend Windows Search to index the contents and properties of new file formats, and data stores using [data add-in interfaces](./-search-data-addins-interfaces-entry-page.md).</span></span> <span data-ttu-id="8d16a-105">Para crear complementos de Windows Search, los desarrolladores de terceros deben implementar primero un almacén de datos de Shell y, a continuación, desarrollar un controlador de protocolo para que Windows Search pueda acceder a los datos para la indexación.</span><span class="sxs-lookup"><span data-stu-id="8d16a-105">To create Windows Search add-ins, third-party developers must first implement a Shell data store, and then develop a protocol handler so that Windows Search can access the data for indexing.</span></span> <span data-ttu-id="8d16a-106">Si tiene un formato de archivo personalizado, debe desarrollar un controlador de filtro para indizar el contenido del archivo y un controlador de propiedades para cada tipo de archivo para indizar las propiedades.</span><span class="sxs-lookup"><span data-stu-id="8d16a-106">If you have a custom file format, you must develop a filter handler to index file contents, and a property handler for every file type to index properties.</span></span>

<span data-ttu-id="8d16a-107">Windows Search admite actualmente la indexación de más de 200 tipos de elementos (como los formatos de archivo. txt,. html y. xml) y puede trabajar con varios tipos de almacenes de datos (como el sistema de archivos NTFS y Microsoft Outlook).</span><span class="sxs-lookup"><span data-stu-id="8d16a-107">Windows Search currently supports the indexing of over 200 types of items (such as .txt, .html, and .xml file formats) and can work with multiple types of data stores (such as the NTFS file system and Microsoft Outlook).</span></span> <span data-ttu-id="8d16a-108">Windows Search usa tecnología de filtros y controladores de protocolo similar a la de SharePoint Server.</span><span class="sxs-lookup"><span data-stu-id="8d16a-108">Windows Search uses filter and protocol handler technology similar to SharePoint Server.</span></span> <span data-ttu-id="8d16a-109">Por lo tanto, si ya tiene implementaciones para el formato de archivo, puede actualizar las implementaciones que se van a inicializar con una secuencia mediante [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) para que el filtro funcione con Windows Search.</span><span class="sxs-lookup"><span data-stu-id="8d16a-109">Hence, if you already have implementations for your file format, you can update the implementations to be initialized with a stream by using [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) so that the filter will work with Windows Search.</span></span>

> [!Note]  
> <span data-ttu-id="8d16a-110">Los controladores de filtro, los controladores de propiedades y los controladores de protocolo deben escribirse en código nativo.</span><span class="sxs-lookup"><span data-stu-id="8d16a-110">Filter handlers, property handlers, and protocol handlers must be written in native code.</span></span> <span data-ttu-id="8d16a-111">Esto se debe a posibles problemas de control de versiones de Common Language Runtime (CLR) con el proceso en el que se ejecutan varios complementos.</span><span class="sxs-lookup"><span data-stu-id="8d16a-111">This is due to potential common language runtime (CLR) versioning issues with the process that multiple add-ins run in.</span></span>

 

<span data-ttu-id="8d16a-112">Esta sección sobre cómo extender el índice con complementos contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="8d16a-112">This section on extending the index with add-ins contains the following topics:</span></span>

-   [<span data-ttu-id="8d16a-113">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="8d16a-113">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)
-   [<span data-ttu-id="8d16a-114">Desarrollar controladores de propiedades para Windows Search</span><span class="sxs-lookup"><span data-stu-id="8d16a-114">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
-   [<span data-ttu-id="8d16a-115">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8d16a-115">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)

## <a name="additional-resources"></a><span data-ttu-id="8d16a-116">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8d16a-116">Additional Resources</span></span>

<span data-ttu-id="8d16a-117">Para ver ejemplos de código relacionados, consulte [ejemplos de código de Windows Search](-search-samples-ovw.md).</span><span class="sxs-lookup"><span data-stu-id="8d16a-117">For related code samples, see [Windows Search Code Samples](-search-samples-ovw.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d16a-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8d16a-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d16a-119">Guía de desarrollo de Windows Search</span><span class="sxs-lookup"><span data-stu-id="8d16a-119">Windows Search Development Guide</span></span>](-search-developers-guide-entry-page.md)
</dt> <dt>

[<span data-ttu-id="8d16a-120">Administración del índice</span><span class="sxs-lookup"><span data-stu-id="8d16a-120">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="8d16a-121">Consulta del índice mediante programación</span><span class="sxs-lookup"><span data-stu-id="8d16a-121">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="8d16a-122">Extensión de recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="8d16a-122">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)
</dt> </dl>

 

 
