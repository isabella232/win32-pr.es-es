---
title: Extender el índice (características heredadas del entorno de Windows)
description: Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de Windows Search.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad766d6fa1c00649f7cbdc3118039ed50f13491
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149837"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="eb909-103">Extender el índice (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="eb909-103">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="eb909-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="eb909-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="eb909-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="eb909-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="eb909-106">Se desaconseja encarecidamente el uso de y el desarrollo de las versiones 2. x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eb909-106">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="eb909-107">WDS se puede extender para indizar el contenido de los nuevos tipos de archivo y almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="eb909-107">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="eb909-108">Actualmente, WDS 2. x contiene filtros para más de 200 tipos de elementos (incluidos los elementos de texto no cifrado como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolo y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="eb909-108">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="eb909-109">Si ya tiene implementaciones de filtro instaladas para los nuevos tipos de archivo, WDS puede usar las interfaces de filtro existentes para indizar estos datos.</span><span class="sxs-lookup"><span data-stu-id="eb909-109">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="eb909-110">Los complementos de WDS 2. x permiten al índice atravesar y analizar nuevos datos y estructuras de datos para agregar información al catálogo de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="eb909-110">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="eb909-111">Estos complementos también pueden extender el shell de Windows para asociar iconos y controladores de menú contextual con los nuevos tipos de archivo y almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="eb909-111">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="eb909-112">Para incluir nuevos tipos de archivo en el catálogo de WDS, un complemento debe implementar la interfaz de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter).</span><span class="sxs-lookup"><span data-stu-id="eb909-112">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="eb909-113">Para incluir nuevos almacenes de datos, un complemento debe ser un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="eb909-113">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="eb909-114">Si el nuevo almacén de datos incluye archivos incrustados o nuevos tipos de archivo, también tendrá que escribir un filtro adecuado.</span><span class="sxs-lookup"><span data-stu-id="eb909-114">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="eb909-115">Los filtros y controladores de protocolo deben escribirse en código nativo debido a posibles problemas de control de versiones de CLR con el proceso en el que se ejecutan todos los complementos.</span><span class="sxs-lookup"><span data-stu-id="eb909-115">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="eb909-116">Agregar tipos de archivo al índice</span><span class="sxs-lookup"><span data-stu-id="eb909-116">Adding File Types to the Index</span></span>

<span data-ttu-id="eb909-117">Los complementos pueden extender WDS para indizar tipos de archivo nuevos o propietarios y asociar cada nuevo tipo de archivo a un icono específico de archivo o menú contextual.</span><span class="sxs-lookup"><span data-stu-id="eb909-117">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="eb909-118">Para ello, puede compilar y registrar un complemento que:</span><span class="sxs-lookup"><span data-stu-id="eb909-118">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="eb909-119">Implementa una interfaz [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para cada tipo de archivo, por lo que WDS puede tener acceso y indizar el texto y los metadatos del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="eb909-119">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="eb909-120">Implementa las interfaces **IExtractIcon** y **IContextMenu** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="eb909-120">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="eb909-121">Para obtener una explicación sobre cómo implementar filtros, consulte [desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="eb909-121">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="eb909-122">Agregar almacenes de datos al índice</span><span class="sxs-lookup"><span data-stu-id="eb909-122">Adding Data Stores to the Index</span></span>

<span data-ttu-id="eb909-123">Los complementos pueden extender WDS para indexar nuevos almacenes de datos y asociar archivos con un icono específico de archivo o un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="eb909-123">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="eb909-124">Para ello, puede compilar y registrar un controlador de protocolo que:</span><span class="sxs-lookup"><span data-stu-id="eb909-124">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="eb909-125">Implementa las interfaces **ISearchProtocol** y **IUrlAccessor** para procesar y enlazar elementos individuales en el origen de contenido.</span><span class="sxs-lookup"><span data-stu-id="eb909-125">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="eb909-126">WDS usa las direcciones URL para identificar de forma única los elementos, independientemente de que estén en el sistema de archivos, dentro de un almacén similar a la base de datos o en la Web.</span><span class="sxs-lookup"><span data-stu-id="eb909-126">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="eb909-127">Implementa la interfaz **IPersistFolder** y partes de la interfaz **IShellFolder** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="eb909-127">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="eb909-128">Para obtener información sobre la implementación de controladores de protocolo, vea [desarrollar controladores de protocolo](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="eb909-128">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="eb909-129">Instrucciones del instalador de complementos</span><span class="sxs-lookup"><span data-stu-id="eb909-129">Add-in Installer Guidelines</span></span>

<span data-ttu-id="eb909-130">La instalación de un complemento debe seguir las siguientes directrices:</span><span class="sxs-lookup"><span data-stu-id="eb909-130">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="eb909-131">El instalador debe utilizar el instalador EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="eb909-131">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="eb909-132">Se deben proporcionar las notas de la versión.</span><span class="sxs-lookup"><span data-stu-id="eb909-132">Release notes must be provided.</span></span>
-   <span data-ttu-id="eb909-133">Se debe crear una entrada **Agregar o quitar programas** para cada complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="eb909-133">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="eb909-134">El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.</span><span class="sxs-lookup"><span data-stu-id="eb909-134">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="eb909-135">Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.</span><span class="sxs-lookup"><span data-stu-id="eb909-135">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="eb909-136">Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo en el complemento predeterminado para ese tipo de archivo o para almacenarlo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="eb909-136">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb909-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb909-137">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="eb909-138">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="eb909-138">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="eb909-139">Desarrollo de complementos de IFilter</span><span class="sxs-lookup"><span data-stu-id="eb909-139">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="eb909-140">Desarrollar controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="eb909-140">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="eb909-141">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="eb909-141">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="eb909-142">**Imaging**</span><span class="sxs-lookup"><span data-stu-id="eb909-142">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
