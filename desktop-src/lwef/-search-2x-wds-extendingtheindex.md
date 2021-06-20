---
title: Extender el índice (características heredadas del entorno de Windows)
description: Obtenga información sobre cómo ampliar el índice en Windows Desktop Search 2.x. En el caso de las versiones de Windows posteriores a Windows XP y Windows Server 2003, use Windows Search en su lugar.
ms.assetid: vs|search|~\search\wds2x\extending_index_ovr.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63408cfe1efeb8da4d6a4540cc57b99ea56ae935
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407358"
---
# <a name="extending-the-index-legacy-windows-environment-features"></a><span data-ttu-id="dd55c-104">Extender el índice (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="dd55c-104">Extending the Index (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="dd55c-105">Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dd55c-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="dd55c-106">En versiones posteriores, use [Windows Search](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="dd55c-106">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="dd55c-107">Se desaconseja encarecidamente el uso y el desarrollo para las versiones 2.x de Microsoft Windows Desktop Search (WDS) en favor de [Windows Search](../search/-search-3x-wds-overview.md).</span><span class="sxs-lookup"><span data-stu-id="dd55c-107">The use of and development for the 2.x versions of Microsoft Windows Desktop Search (WDS) is strongly discouraged in favor of [Windows Search](../search/-search-3x-wds-overview.md).</span></span>

<span data-ttu-id="dd55c-108">WDS se puede extender para indexar el contenido de nuevos tipos de archivo y almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="dd55c-108">WDS can be extended to index the contents of new file types and data stores.</span></span> <span data-ttu-id="dd55c-109">Actualmente, WDS 2.x contiene filtros para más de 200 tipos de elementos (incluidos elementos de texto no cifrado como HTML, XML y archivos de código fuente) y usa la misma tecnología de controlador de protocolos y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)que SharePoint Services.</span><span class="sxs-lookup"><span data-stu-id="dd55c-109">Currently, WDS 2.x contains filters for over 200 types of items (including plaintext items such as HTML, XML, and source code files) and uses the same [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)and protocol handler technology as SharePoint Services.</span></span> <span data-ttu-id="dd55c-110">Si ya tiene implementaciones de filtro instaladas para los nuevos tipos de archivo, WDS puede usar las interfaces de filtro existentes para indexar estos datos.</span><span class="sxs-lookup"><span data-stu-id="dd55c-110">If you already have filter implementations installed for your new file types, WDS can use the existing filter interfaces to index this data.</span></span>

<span data-ttu-id="dd55c-111">Los complementos de WDS 2.x permiten al índice recorrer y analizar nuevas estructuras de datos y datos para obtener información que se agregue al catálogo en el que se pueden realizar búsquedas.</span><span class="sxs-lookup"><span data-stu-id="dd55c-111">WDS 2.x add-ins enable the index to traverse and parse new data and data structures for information to add to the searchable catalog.</span></span> <span data-ttu-id="dd55c-112">Estos complementos también pueden extender el Shell de Windows para asociar iconos y controladores de menú contextual a los nuevos tipos de archivo y almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="dd55c-112">These add-ins can also extend the Windows Shell to associate icons and context-menu handlers with the new file types and data stores.</span></span> <span data-ttu-id="dd55c-113">Para incluir nuevos tipos de archivo en el catálogo de WDS, un complemento debe implementar la [**interfaz IFilter.**](/windows/desktop/api/filter/nn-filter-ifilter)</span><span class="sxs-lookup"><span data-stu-id="dd55c-113">To include new file types in the WDS catalog, an add-in must implement the [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface.</span></span> <span data-ttu-id="dd55c-114">Para incluir nuevos almacenes de datos, un complemento debe ser un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="dd55c-114">To include new data stores, an add-in must be a protocol handler.</span></span> <span data-ttu-id="dd55c-115">Si el nuevo almacén de datos incluye archivos incrustados o nuevos tipos de archivo, también deberá escribir un filtro adecuado.</span><span class="sxs-lookup"><span data-stu-id="dd55c-115">If the new data store includes embedded files or new file types itself, you will also need to write an appropriate filter as well.</span></span>

> [!Note]
>
> <span data-ttu-id="dd55c-116">Los filtros y los controladores de protocolo deben escribirse en código nativo debido a posibles problemas de control de versiones clr con el proceso en el que se ejecutan todos los complementos.</span><span class="sxs-lookup"><span data-stu-id="dd55c-116">Filters and protocol handlers must be written in native code due to potential CLR versioning issues with the process all add-ins run in.</span></span>

 

## <a name="adding-file-types-to-the-index"></a><span data-ttu-id="dd55c-117">Agregar tipos de archivo al índice</span><span class="sxs-lookup"><span data-stu-id="dd55c-117">Adding File Types to the Index</span></span>

<span data-ttu-id="dd55c-118">Los complementos pueden extender WDS para indexar tipos de archivo nuevos o propietarios y asociar cada nuevo tipo de archivo a un icono o menú contextual específico del archivo.</span><span class="sxs-lookup"><span data-stu-id="dd55c-118">Add-ins can extend WDS to index new or proprietary file types and to associate each new file type with a file-specific icon or context menu.</span></span> <span data-ttu-id="dd55c-119">Para ello, puede compilar y registrar un complemento que:</span><span class="sxs-lookup"><span data-stu-id="dd55c-119">To do this, you can build and register an add-in that:</span></span>

1.  <span data-ttu-id="dd55c-120">Implementa una interfaz [**IFilter para**](/windows/desktop/api/filter/nn-filter-ifilter)cada tipo de archivo para que WDS pueda tener acceso al texto y los metadatos del tipo de archivo e indexarlo.</span><span class="sxs-lookup"><span data-stu-id="dd55c-120">Implements an [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)interface for each file type so WDS can access and index the file type's text and metadata.</span></span>
2.  <span data-ttu-id="dd55c-121">Implementa las interfaces **IExtractIcon** e **IContextMenu** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="dd55c-121">Implements the **IExtractIcon** and **IContextMenu** interfaces to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="dd55c-122">Para obtener una explicación sobre la implementación de filtros, vea [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span><span class="sxs-lookup"><span data-stu-id="dd55c-122">For a discussion on implementing filters, see [Developing IFilter Add-ins](-search-2x-wds-ifilteraddins.md).</span></span>

## <a name="adding-data-stores-to-the-index"></a><span data-ttu-id="dd55c-123">Agregar almacenes de datos al índice</span><span class="sxs-lookup"><span data-stu-id="dd55c-123">Adding Data Stores to the Index</span></span>

<span data-ttu-id="dd55c-124">Los complementos pueden extender WDS para indexar nuevos almacenes de datos y asociar archivos a un icono o menú contextual específico del archivo.</span><span class="sxs-lookup"><span data-stu-id="dd55c-124">Add-ins can extend WDS to index new data stores and to associate files with a file-specific icon or context menu.</span></span> <span data-ttu-id="dd55c-125">Para ello, puede compilar y registrar un controlador de protocolo que:</span><span class="sxs-lookup"><span data-stu-id="dd55c-125">To do this, you can build and register a protocol handler that:</span></span>

1.  <span data-ttu-id="dd55c-126">Implementa las interfaces **ISearchProtocol** **e IUrlAccessor** para procesar y enlazar elementos individuales en el origen de contenido.</span><span class="sxs-lookup"><span data-stu-id="dd55c-126">Implements the **ISearchProtocol** and **IUrlAccessor** interfaces to process and bind individual items in the content source.</span></span> <span data-ttu-id="dd55c-127">WDS usa direcciones URL para identificar de forma única los elementos, independientemente de si están en el sistema de archivos, dentro de un almacén de tipo base de datos o en la Web.</span><span class="sxs-lookup"><span data-stu-id="dd55c-127">WDS uses URLs to uniquely identify items, whether those items are in the file system, inside a database-like store, or on the Web.</span></span>
2.  <span data-ttu-id="dd55c-128">Implementa la **interfaz IPersistFolder** y las partes de la interfaz **IShellFolder** para agregar iconos y menús contextuales para una mayor integración y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="dd55c-128">Implements the **IPersistFolder** interface and portions of the **IShellFolder** interface to add icons and context menus for greater integration and usability.</span></span>

<span data-ttu-id="dd55c-129">Para obtener una explicación sobre la implementación de controladores de protocolo, vea [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span><span class="sxs-lookup"><span data-stu-id="dd55c-129">For a discussion on implementing protocol handlers, see [Developing Protocol Handlers](-search-2x-wds-phaddins.md).</span></span>

## <a name="add-in-installer-guidelines"></a><span data-ttu-id="dd55c-130">Instrucciones del instalador del complemento</span><span class="sxs-lookup"><span data-stu-id="dd55c-130">Add-in Installer Guidelines</span></span>

<span data-ttu-id="dd55c-131">La instalación de un complemento debe seguir las instrucciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="dd55c-131">Installation of an add-in should follow the following guidelines:</span></span>

-   <span data-ttu-id="dd55c-132">El instalador debe usar el instalador EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="dd55c-132">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="dd55c-133">Se deben proporcionar notas de la versión.</span><span class="sxs-lookup"><span data-stu-id="dd55c-133">Release notes must be provided.</span></span>
-   <span data-ttu-id="dd55c-134">Se **debe crear una entrada Agregar** o quitar programas para cada complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="dd55c-134">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="dd55c-135">El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.</span><span class="sxs-lookup"><span data-stu-id="dd55c-135">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="dd55c-136">Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.</span><span class="sxs-lookup"><span data-stu-id="dd55c-136">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="dd55c-137">Si un complemento más reciente ha sobrescrito el complemento anterior, debe haber la capacidad de restaurar la funcionalidad del complemento anterior y convertirla en el complemento predeterminado para ese tipo de archivo o almacén de nuevo.</span><span class="sxs-lookup"><span data-stu-id="dd55c-137">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type or store again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd55c-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dd55c-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dd55c-139">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dd55c-139">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dd55c-140">Desarrollo de complementos de IFilter</span><span class="sxs-lookup"><span data-stu-id="dd55c-140">Developing IFilter Add-ins</span></span>](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[<span data-ttu-id="dd55c-141">Desarrollo de controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="dd55c-141">Developing Protocol Handlers</span></span>](-search-2x-wds-phaddins.md)
</dt> <dt>

<span data-ttu-id="dd55c-142">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="dd55c-142">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="dd55c-143">**Ifilter**</span><span class="sxs-lookup"><span data-stu-id="dd55c-143">**IFilter**</span></span>](/windows/desktop/api/filter/nn-filter-ifilter)
</dt> </dl>

 

 
