---
description: El registro de un tipo de archivo es el primer paso para crear una asociación de archivo, que hace que ese tipo de archivo &\# 0034; conocido&\# 0034; en el shell. Sin embargo, sin controladores de tipo de archivo, el shell no puede exponer información al usuario desde y sobre el archivo.
ms.assetid: c0c5c3ef-35ff-4ab6-bb8a-1f0640109d50
title: Controladores de tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cba365b6eb704def7644002b8a87c3842b62aa77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907849"
---
# <a name="file-type-handlers"></a><span data-ttu-id="5b421-104">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-104">File Type Handlers</span></span>

<span data-ttu-id="5b421-105">El [registro de un tipo de archivo](fa-how-work.md) es el primer paso para crear una asociación de archivo, que hace que ese tipo de archivo sea "conocido" en el shell.</span><span class="sxs-lookup"><span data-stu-id="5b421-105">[Registering a file type](fa-how-work.md) is the first step in creating a file association, which makes that file type "known" to the Shell.</span></span> <span data-ttu-id="5b421-106">Sin embargo, sin controladores de tipo de archivo, el shell no puede exponer información al usuario desde y sobre el archivo.</span><span class="sxs-lookup"><span data-stu-id="5b421-106">However, without file type handlers, the Shell is unable to expose information to the user from and about the file.</span></span>

<span data-ttu-id="5b421-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5b421-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5b421-108">Convertir un tipo de archivo en Shell</span><span class="sxs-lookup"><span data-stu-id="5b421-108">Make a File Type Known to Shell</span></span>](#make-a-file-type-known-to-shell)
-   [<span data-ttu-id="5b421-109">Descripciones del controlador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-109">File Type Handler Descriptions</span></span>](#file-type-handler-descriptions)
-   [<span data-ttu-id="5b421-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b421-110">Related topics</span></span>](#related-topics)

## <a name="make-a-file-type-known-to-shell"></a><span data-ttu-id="5b421-111">Convertir un tipo de archivo en Shell</span><span class="sxs-lookup"><span data-stu-id="5b421-111">Make a File Type Known to Shell</span></span>

<span data-ttu-id="5b421-112">En la siguiente captura de pantalla del explorador de Windows, el archivo de imagen desierto. conocido aparece en la biblioteca de **imágenes** de Shell y está asociado únicamente a la aplicación Paint.</span><span class="sxs-lookup"><span data-stu-id="5b421-112">In the following screen shot of Windows Explorer, the image file Desert.known appears in the Shell **Pictures** library, and is associated only with the Paint application.</span></span>

![captura de pantalla que muestra que el explorador abre una imagen sin tipo de archivo](images/file-assoc/fileassoc-filetypehandler.png)

<span data-ttu-id="5b421-114">El archivo desierto. know en la captura de pantalla anterior no tiene la siguiente funcionalidad habilitada por un controlador de tipo de archivo:</span><span class="sxs-lookup"><span data-stu-id="5b421-114">The Desert.known file in the preceding screen shot lacks the following functionality that is enabled by a file type handler:</span></span>

-   <span data-ttu-id="5b421-115">Miniatura o vista previa</span><span class="sxs-lookup"><span data-stu-id="5b421-115">Thumbnail or preview</span></span>
-   <span data-ttu-id="5b421-116">Verbos específicos de la imagen en el menú contextual, como:</span><span class="sxs-lookup"><span data-stu-id="5b421-116">Image-specific verbs in the shortcut menu, such as:</span></span>
    -   <span data-ttu-id="5b421-117">Rotar vista previa</span><span class="sxs-lookup"><span data-stu-id="5b421-117">Rotate Preview</span></span>
    -   <span data-ttu-id="5b421-118">Establecer como fondo de escritorio</span><span class="sxs-lookup"><span data-stu-id="5b421-118">Set as Desktop Background</span></span>
    -   <span data-ttu-id="5b421-119">Impresión</span><span class="sxs-lookup"><span data-stu-id="5b421-119">Print</span></span>
-   <span data-ttu-id="5b421-120">Propiedades específicas de la imagen en el panel de **detalles** , como:</span><span class="sxs-lookup"><span data-stu-id="5b421-120">Image-specific properties in the **Details** pane, such as:</span></span>
    -   <span data-ttu-id="5b421-121">Fecha de creación</span><span class="sxs-lookup"><span data-stu-id="5b421-121">Date Taken</span></span>
    -   <span data-ttu-id="5b421-122">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="5b421-122">Tags</span></span>
    -   <span data-ttu-id="5b421-123">Rating</span><span class="sxs-lookup"><span data-stu-id="5b421-123">Rating</span></span>
-   <span data-ttu-id="5b421-124">Indexación del texto del archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-124">Indexing of file text</span></span>

<span data-ttu-id="5b421-125">En la siguiente captura de pantalla, el mismo archivo (desierto. known) tiene la extensión. jpg, que es un tipo de archivo registrado con controladores de tipo de archivo asociados, por lo que se muestra una imagen en miniatura y más propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b421-125">In the following screen shot, the same file (Desert.known) has the .jpg extension, which is a registered file type that has associated file type handlers, so a thumbnail image and more properties are shown.</span></span>

![imagen con un tipo de archivo registrado y controladores de tipo de archivo asociados](images/file-assoc/fileassoc-filetypehandler-2ndex.png)

## <a name="file-type-handler-descriptions"></a><span data-ttu-id="5b421-127">Descripciones del controlador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-127">File Type Handler Descriptions</span></span>

<span data-ttu-id="5b421-128">La funcionalidad proporcionada por cada controlador de tipo de archivo se muestra en la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b421-128">The functionality provided by each file type handler is listed in the following table:</span></span>



| <span data-ttu-id="5b421-129">Controlador</span><span class="sxs-lookup"><span data-stu-id="5b421-129">Handler</span></span>                                                      | <span data-ttu-id="5b421-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5b421-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b421-131">Menú contextual</span><span class="sxs-lookup"><span data-stu-id="5b421-131">Shortcut menu</span></span>](context-menu-handlers.md)                   | <span data-ttu-id="5b421-132">Un controlador de menú contextual, que a veces se denomina controlador de menú contextual, es un controlador de tipo de archivo que agrega comandos a un menú contextual existente.</span><span class="sxs-lookup"><span data-stu-id="5b421-132">A shortcut menu handler, sometimes referred to as a context menu handler, is a file type handler that adds commands to an existing context menu.</span></span> <span data-ttu-id="5b421-133">Estos controladores están asociados a un tipo de archivo determinado y se les llama cada vez que se muestra un menú contextual para un miembro del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="5b421-133">These handlers are associated with a particular file type and are called any time a context menu is displayed for a member of the file type.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5b421-134">Miniatura</span><span class="sxs-lookup"><span data-stu-id="5b421-134">Thumbnail</span></span>](thumbnail-providers.md)                         | <span data-ttu-id="5b421-135">Un controlador que proporciona una imagen para representar un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="5b421-135">A handler that provides an image to represent a Shell item.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="5b421-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5b421-136">Property</span></span>](../properties/building-property-handlers-properties.md) | <span data-ttu-id="5b421-137">Un controlador de propiedades que proporciona acceso a las propiedades de los elementos de búsqueda de Windows, el explorador de Windows y otras aplicaciones que necesitan tener acceso a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="5b421-137">A property handler that provides access to item properties for Windows Search, the Windows Explorer and other applications that need to access properties.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5b421-138">Versión preliminar</span><span class="sxs-lookup"><span data-stu-id="5b421-138">Preview</span></span>](preview-handlers.md)                              | <span data-ttu-id="5b421-139">Un controlador que genera rápidamente una vista simplificada de solo lectura del elemento que se va a mostrar en el panel de vista previa del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="5b421-139">A handler that quickly produces a read-only, simplified view of the item to be displayed in the Windows Explorer preview pane.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="5b421-140">Filtros</span><span class="sxs-lookup"><span data-stu-id="5b421-140">Filters</span></span>](../search/-search-3x-wds-extidx-filters.md)              | <span data-ttu-id="5b421-141">Un filtro, una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , que examina documentos en busca de texto y propiedades (también denominados atributos).</span><span class="sxs-lookup"><span data-stu-id="5b421-141">A filter, an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface, that scans documents for text and properties (also called attributes).</span></span> <span data-ttu-id="5b421-142">Extrae fragmentos de texto de estos documentos, filtrando el formato incrustado y conservando la información sobre la posición del texto.</span><span class="sxs-lookup"><span data-stu-id="5b421-142">It extracts chunks of text from these documents, filtering out embedded formatting and retaining information about the position of the text.</span></span> <span data-ttu-id="5b421-143">También extrae fragmentos de valores, que son propiedades de un documento completo o de partes bien definidas de un documento.</span><span class="sxs-lookup"><span data-stu-id="5b421-143">It also extracts chunks of values, which are properties of an entire document or of well defined parts of a document.</span></span> <span data-ttu-id="5b421-144">**IFilter** proporciona la base para la creación de aplicaciones de nivel superior como indexadores de documentos y visores independientes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5b421-144">**IFilter** provides the foundation for building higher-level applications such as document indexers and application-independent viewers.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5b421-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b421-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b421-146">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="5b421-146">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="5b421-147">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-147">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="5b421-148">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="5b421-148">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="5b421-149">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="5b421-149">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="5b421-150">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="5b421-150">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="5b421-151">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="5b421-151">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="5b421-152">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="5b421-152">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="5b421-153">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="5b421-153">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
