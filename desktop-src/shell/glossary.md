---
description: Página de glosario
ROBOTS: NOINDEX, NOFOLLOW
title: Glosario de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2F463941-A4BA-4b34-B391-7E599E87BEEA
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6ec49f808f6c6dea74d3c8c2ac4408bc5d1a26e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360678"
---
# <a name="shell-glossary"></a><span data-ttu-id="91d7b-103">Glosario de Shell</span><span class="sxs-lookup"><span data-stu-id="91d7b-103">Shell Glossary</span></span>

## <a name="a"></a><span data-ttu-id="91d7b-104">A</span><span class="sxs-lookup"><span data-stu-id="91d7b-104">A</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-105">**correlación**</span><span class="sxs-lookup"><span data-stu-id="91d7b-105">**association**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-106">Asignación de una extensión de nombre de archivo (por ejemplo,. mp3) o un protocolo (por ejemplo, http) a un identificador de programación (ProgID).</span><span class="sxs-lookup"><span data-stu-id="91d7b-106">A mapping of a file name extension (for example, .mp3) or protocol (for example, http) to a programmatic identifier (ProgID).</span></span> <span data-ttu-id="91d7b-107">Esta asignación se almacena en el registro como una configuración por usuario con una reserva por equipo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-107">This mapping is stored in the registry as a per-user setting with a per-computer fallback.</span></span> <span data-ttu-id="91d7b-108">Las aplicaciones que participan en el sistema programas predeterminados establecen la asignación de Asociación de la extensión de nombre de archivo o protocolo para que apunten a las claves de ProgID que poseen.</span><span class="sxs-lookup"><span data-stu-id="91d7b-108">Applications that participate in the Default Programs system set the association mapping for the file name extension or protocol to point to the ProgID keys that they own.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-109">**matriz de asociación**</span><span class="sxs-lookup"><span data-stu-id="91d7b-109">**association array**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-110">Lista ordenada de ubicaciones del registro que se utiliza para almacenar información sobre un tipo de elemento, incluidos los controladores, los verbos y otros atributos, como el icono y el nombre para mostrar del tipo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-110">An ordered list of registry locations used to store information about an item type, including handlers, verbs, and other attributes like the icon and display name of the type.</span></span> <span data-ttu-id="91d7b-111">Por ejemplo, un archivo. jpg tiene la siguiente matriz de asociación en un sistema Windows predeterminado: "HKCR \\ jpgfile", "HKCR \\ SystemFileAssociations \\ . jpg", "HKCR \\ SystemFileAssociations \\ Image", "HKCR \\ \* ", "HKCR \\ AllFileSystemObjects".</span><span class="sxs-lookup"><span data-stu-id="91d7b-111">For example, a .jpg file has the following association array on a default Windows system: "HKCR\\jpgfile", "HKCR\\SystemFileAssociations\\.jpg", "HKCR\\SystemFileAssociations\\image", "HKCR\\\*", "HKCR\\AllFileSystemObjects".</span></span>

</dd> </dl>

## <a name="b"></a><span data-ttu-id="91d7b-112">B</span><span class="sxs-lookup"><span data-stu-id="91d7b-112">B</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-113">**bind**</span><span class="sxs-lookup"><span data-stu-id="91d7b-113">**bind**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-114">Para cargar o asociar código a los datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-114">To load or associate code with data.</span></span> <span data-ttu-id="91d7b-115">Por ejemplo, un controlador puede estar asociado a un origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-115">For example, a handler may be associated with a Shell data source.</span></span>

</dd> </dl>

## <a name="c"></a><span data-ttu-id="91d7b-116">C</span><span class="sxs-lookup"><span data-stu-id="91d7b-116">C</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-117">**nombre canónico**</span><span class="sxs-lookup"><span data-stu-id="91d7b-117">**canonical name**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-118">Nombre único de un recurso.</span><span class="sxs-lookup"><span data-stu-id="91d7b-118">The unique name of a resource.</span></span> <span data-ttu-id="91d7b-119">Canonical significa "según las reglas".</span><span class="sxs-lookup"><span data-stu-id="91d7b-119">Canonical means "according to the rules."</span></span> <span data-ttu-id="91d7b-120">Vea también: nombre de verbo canónico.</span><span class="sxs-lookup"><span data-stu-id="91d7b-120">See also: canonical verb name.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-121">**nombre canónico de verbo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-121">**canonical verb name**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-122">Nombre independiente del lenguaje que se puede utilizar mediante programación para hacer referencia a un verbo, independientemente de la cadena localizada en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="91d7b-122">A language-neutral name that can be used programmatically to refer to a verb, regardless of the localized string in the user interface.</span></span> <span data-ttu-id="91d7b-123">Vea también: nombre canónico, verbo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-123">See also: canonical name, verb.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-124">**container**</span><span class="sxs-lookup"><span data-stu-id="91d7b-124">**container**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-125">Un tipo de elemento de Shell que puede contener otros elementos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-125">A type of Shell item that can contain other items.</span></span> <span data-ttu-id="91d7b-126">Los elementos de un contenedor se exponen al espacio de nombres del shell mediante un origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-126">Items in a container are exposed to the Shell namespace by using a Shell data source.</span></span> <span data-ttu-id="91d7b-127">Entre los ejemplos se incluyen carpetas, unidades, servidores de red y archivos comprimidos con una extensión de nombre de archivo. zip.</span><span class="sxs-lookup"><span data-stu-id="91d7b-127">Examples include folders, drives, network servers, and compressed files with a .zip file name extension.</span></span> <span data-ttu-id="91d7b-128">Vea también: origen de datos de Shell, carpeta, elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-128">See also: Shell data source, folder, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-129">**content**</span><span class="sxs-lookup"><span data-stu-id="91d7b-129">**content**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-130">Texto y propiedades asociados a un elemento de shell o a un origen de contenido que se puede indizar.</span><span class="sxs-lookup"><span data-stu-id="91d7b-130">Text and properties associated with a Shell item or a content source that can be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-131">**origen de contenido**</span><span class="sxs-lookup"><span data-stu-id="91d7b-131">**content source**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-132">Un elemento al que puede tener acceso el indizador.</span><span class="sxs-lookup"><span data-stu-id="91d7b-132">An item that can be accessed by the indexer.</span></span> <span data-ttu-id="91d7b-133">Los orígenes de contenido son direccionables mediante una dirección URL y se proporcionan al indizador mediante un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-133">Content sources are addressable by a URL and are provided to the indexer by a protocol handler.</span></span> <span data-ttu-id="91d7b-134">Algunos ejemplos son: archivos y carpetas del sistema de archivos, elementos y carpetas de Microsoft Outlook, registros de base de datos y elementos almacenados de Microsoft SharePoint.</span><span class="sxs-lookup"><span data-stu-id="91d7b-134">Examples include: file system files and folders, Microsoft Outlook items and folders, database records, and Microsoft SharePoint stored items.</span></span> <span data-ttu-id="91d7b-135">Un origen de contenido se puede exponer como elementos de Shell implementando un origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-135">A content source can be exposed as Shell items by implementing a Shell data source.</span></span> <span data-ttu-id="91d7b-136">Vea también: contenido, elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-136">See also: content, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-137">**content view (vista de contenido)**</span><span class="sxs-lookup"><span data-stu-id="91d7b-137">**content view**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-138">Una vista en el explorador de Windows (ofrecida en Windows 7 y versiones posteriores) que muestra el contenido más relevante de cada elemento de la lista en función de su extensión de nombre de archivo o asociación de clase.</span><span class="sxs-lookup"><span data-stu-id="91d7b-138">A view in Windows Explorer (offered in Windows 7 and later) that displays the most relevant content for each item in the list based on its file name extension or Kind association.</span></span> <span data-ttu-id="91d7b-139">La vista de contenido usa una lógica de cambio de tamaño que quita las propiedades cuando se reduce el tamaño de la ventana para asegurarse de que las propiedades más críticas todavía tienen espacio para ser legibles claramente.</span><span class="sxs-lookup"><span data-stu-id="91d7b-139">Content view uses a resizing logic that drops properties when the window size decreases to ensure that the most critical properties still have room to be clearly readable.</span></span> <span data-ttu-id="91d7b-140">Vea también: patrón de diseño, clase, Asociación de clase.</span><span class="sxs-lookup"><span data-stu-id="91d7b-140">See also: layout pattern, Kind, Kind association.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-141">**modo de vista de contenido**</span><span class="sxs-lookup"><span data-stu-id="91d7b-141">**content view mode**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-142">Consulte definición de: vista de contenido.</span><span class="sxs-lookup"><span data-stu-id="91d7b-142">See definition for: content view.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-143">**menú contextual**</span><span class="sxs-lookup"><span data-stu-id="91d7b-143">**context menu**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-144">Este término se usa a veces para hacer referencia al menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-144">This term is sometimes used to mean shortcut menu.</span></span> <span data-ttu-id="91d7b-145">Vea la definición de: menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-145">See definition for: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-146">**controlador del menú contextual**</span><span class="sxs-lookup"><span data-stu-id="91d7b-146">**context menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-147">Este término se usa a veces para hacer referencia al controlador del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-147">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="91d7b-148">Consulte definición de: controlador de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-148">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

## <a name="d"></a><span data-ttu-id="91d7b-149">D</span><span class="sxs-lookup"><span data-stu-id="91d7b-149">D</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-150">**controlador de objetos de datos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-150">**data object handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-151">Un controlador que proporciona formatos adicionales del portapapeles para el objeto de datos (IDataObject) de un elemento.</span><span class="sxs-lookup"><span data-stu-id="91d7b-151">A handler that provides additional clipboard formats for the data object (IDataObject) of an item.</span></span> <span data-ttu-id="91d7b-152">Los objetos de datos se utilizan en escenarios de arrastrar y colocar, y de copiar y pegar.</span><span class="sxs-lookup"><span data-stu-id="91d7b-152">Data objects are used in drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-153">**origen de datos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-153">**data source**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-154">Este término se usa a veces para indicar el almacén de datos o el origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-154">This term is sometimes used to mean data store or Shell data source.</span></span> <span data-ttu-id="91d7b-155">Vea la definición de: almacén de datos, origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-155">See definition for: data store, Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-156">**almacén de datos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-156">**data store**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-157">Un repositorio de datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-157">A repository of data.</span></span> <span data-ttu-id="91d7b-158">Un almacén de datos se puede exponer en el modelo de programación de shell como un contenedor mediante un origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-158">A data store can be exposed to the Shell programming model as a container using a Shell data source.</span></span> <span data-ttu-id="91d7b-159">El sistema de Windows Search puede indizar los elementos de un almacén de datos mediante un controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-159">The items in a data store can be indexed by the Windows Search system using a protocol handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-160">**composición de escritorio**</span><span class="sxs-lookup"><span data-stu-id="91d7b-160">**desktop composition**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-161">Característica de Windows Vista que permite dibujar ventanas individuales en superficies fuera de la pantalla en la memoria de vídeo en lugar de que se dibujen directamente en el dispositivo de pantalla principal.</span><span class="sxs-lookup"><span data-stu-id="91d7b-161">A Windows Vista feature that enables individual windows to be drawn to off-screen surfaces in video memory instead of the being drawn directly to the primary display device.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-162">**document**</span><span class="sxs-lookup"><span data-stu-id="91d7b-162">**document**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-163">Un elemento de Shell que contiene texto y para el que se podría implementar la interfaz de IFilter.</span><span class="sxs-lookup"><span data-stu-id="91d7b-163">A Shell item that contains text, and for which the IFilter interface could be implemented.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-164">**quitar controlador**</span><span class="sxs-lookup"><span data-stu-id="91d7b-164">**drop handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-165">Un controlador que permite que un tipo de elemento determinado admita escenarios de arrastrar y colocar, y copiar y pegar.</span><span class="sxs-lookup"><span data-stu-id="91d7b-165">A handler that enables a particular item type to support drag-and-drop and copy/paste scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-166">**destino de colocación**</span><span class="sxs-lookup"><span data-stu-id="91d7b-166">**drop target**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-167">Objeto de datos que se arrastra y se coloca en un archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-167">A data object that is dragged and dropped onto a file.</span></span> <span data-ttu-id="91d7b-168">Vea también: controlador de datos, quitar controlador.</span><span class="sxs-lookup"><span data-stu-id="91d7b-168">See also: data handler, drop handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-169">**verbo dinámico**</span><span class="sxs-lookup"><span data-stu-id="91d7b-169">**dynamic verb**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-170">Verbo que depende del estado de un elemento de shell o del sistema; la apariencia del elemento se basa en el estado y requiere que el código que se está ejecutando determine si el elemento debe aparecer.</span><span class="sxs-lookup"><span data-stu-id="91d7b-170">A verb that depends on the state of a Shell item or of the system; the appearance of the item is state based and requires that the executing code determine whether the item should appear.</span></span> <span data-ttu-id="91d7b-171">Vea también: controlador de menú contextual, verbo estático, verbo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-171">See also: shortcut menu handler, static verb, verb.</span></span>

</dd> </dl>

## <a name="e"></a><span data-ttu-id="91d7b-172">E</span><span class="sxs-lookup"><span data-stu-id="91d7b-172">E</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-173">**Explorador (comando)**</span><span class="sxs-lookup"><span data-stu-id="91d7b-173">**Explorer command**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-174">Objeto que se puede presentar como un botón cerca de la parte superior de la ventana del explorador de Windows que proporciona funcionalidad para los elementos y contenedores de esa ventana.</span><span class="sxs-lookup"><span data-stu-id="91d7b-174">An object that can be presented as a button near the top of the Windows Explorer window that provides functionality for items and containers in that window.</span></span> <span data-ttu-id="91d7b-175">Un origen de datos de Shell proporciona los objetos de comando del explorador de Windows para un elemento contenedor determinado.</span><span class="sxs-lookup"><span data-stu-id="91d7b-175">A Shell data source provides the Windows Explorer command objects for a particular container item.</span></span> <span data-ttu-id="91d7b-176">Los comandos se utilizan a veces como verbos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-176">Commands are sometimes used as verbs.</span></span>

</dd> </dl>

## <a name="f"></a><span data-ttu-id="91d7b-177">F</span><span class="sxs-lookup"><span data-stu-id="91d7b-177">F</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-178">**Asociación de archivos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-178">**file association**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-179">Vea la definición de: Asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-179">See definition for: file type association.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-180">**formato de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-180">**file format**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-181">Formato de los datos almacenados en un archivo que tiene una especificación de formato documentada.</span><span class="sxs-lookup"><span data-stu-id="91d7b-181">A format for data stored in a file that has a documented format specification.</span></span> <span data-ttu-id="91d7b-182">Entre los ejemplos se incluyen OLE archivos de ejemplo, OPC, XML, ZIP y otras especificaciones de formato de archivo bien conocidas.</span><span class="sxs-lookup"><span data-stu-id="91d7b-182">Examples include OLE DocFile, OPC, XML, ZIP and other well known file format specifications.</span></span> <span data-ttu-id="91d7b-183">Los creadores de tipos de archivo suelen usar un formato de archivo existente como base de un nuevo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-183">File type creators generally use an existing file format as the basis of a new file type.</span></span> <span data-ttu-id="91d7b-184">Un formato de archivo puede ser simplemente una definición de la que no se crean instancias como un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-184">A file format can be simply a definition that is not instantiated as a file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-185">**controlador de formato de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-185">**file format handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-186">Este término es un sinónimo del controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-186">This term is a synonym for file type handler.</span></span> <span data-ttu-id="91d7b-187">Vea la definición de: controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-187">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-188">**extensión de nombre de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-188">**file name extension**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-189">El indicador principal de un tipo de archivo para los elementos del sistema de archivos, es la parte del nombre de archivo que sigue al punto final.</span><span class="sxs-lookup"><span data-stu-id="91d7b-189">The primary indicator of a file type for file system items, it is the portion of the file name that follows the final dot.</span></span> <span data-ttu-id="91d7b-190">La extensión de nombre de archivo no puede contener espacios ni caracteres que no sean ASCII y solo se aplica a archivos (no carpetas).</span><span class="sxs-lookup"><span data-stu-id="91d7b-190">The file name extension cannot contain spaces or non-ASCII characters and applies only to files (not folders).</span></span> <span data-ttu-id="91d7b-191">Las extensiones de nombre de archivo se comparan utilizando una función de comparación que no distingue entre mayúsculas y minúsculas o la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="91d7b-191">File name extensions are compared using a comparison function that is not sensitive to case or locale.</span></span> <span data-ttu-id="91d7b-192">Vea también: formato de archivo, tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-192">See also: file format, file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-193">**tipo de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-193">**file type**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-194">Un valor de extensión de nombre de archivo determinado, como ". htm" o ". jpg", que define una clase de archivos que son del mismo tipo y tienen un conjunto común de asociaciones.</span><span class="sxs-lookup"><span data-stu-id="91d7b-194">A particular file name extension value, like ".htm" or ".jpg", that defines a class of files that are of the same type and have a common set of associations.</span></span> <span data-ttu-id="91d7b-195">Vea también: Kind, Asociación de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-195">See also: Kind, file type association.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-196">**asociación de tipo de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-196">**file type association**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-197">Para una extensión de nombre de archivo determinada, los elementos de la matriz de asociaciones que definen dónde se pueden registrar los controladores y otros atributos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-197">For a particular file name extension, the association array elements that define where handlers and other attributes can be registered.</span></span> <span data-ttu-id="91d7b-198">Vea también: matriz de asociación, tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-198">See also: association array, file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-199">**Personalización de tipos de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-199">**file type customization**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-200">Asociación que permite a Shell personalizar el modo en que Shell trata un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-200">An association that enables Shell to customize how Shell treats a file type.</span></span> <span data-ttu-id="91d7b-201">Las personalizaciones de tipo de archivo incluyen: especificar la aplicación utilizada para abrir el archivo al hacer doble clic, agregar comandos al menú contextual de un tipo de archivo, especificar un icono personalizado, especificar un tipo de contenido MIME para asociarlo a un tipo de archivo, especificar un tipo percibido y especificar una o varias aplicaciones asociadas por tipo de archivo con el cuadro de diálogo Abrir con.</span><span class="sxs-lookup"><span data-stu-id="91d7b-201">File type customizations include: specifying the application used to open the file when double-clicked, adding commands to the shortcut menu for a file type, specifying a custom icon, specifying a MIME content type to associate with a file type, specifying a perceived type, and specifying one or more applications associated by file type with the Open With dialog box.</span></span> <span data-ttu-id="91d7b-202">Vea también: PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="91d7b-202">See also: PerceivedType.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-203">**controlador de tipo de archivo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-203">**file type handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-204">Un controlador registrado para un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-204">A handler registered for a file type.</span></span> <span data-ttu-id="91d7b-205">Vea también: controlador.</span><span class="sxs-lookup"><span data-stu-id="91d7b-205">See also: handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-206">**directorio**</span><span class="sxs-lookup"><span data-stu-id="91d7b-206">**folder**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-207">Vea la definición de: container.</span><span class="sxs-lookup"><span data-stu-id="91d7b-207">See definition for: container.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-208">**PIDL completo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-208">**full PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-209">PIDL que describe de forma única un objeto relativo a la carpeta del escritorio.</span><span class="sxs-lookup"><span data-stu-id="91d7b-209">A PIDL that uniquely describes an object relative to the desktop folder.</span></span>

</dd> </dl>

## <a name="h"></a><span data-ttu-id="91d7b-210">H</span><span class="sxs-lookup"><span data-stu-id="91d7b-210">H</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-211">**controlador**</span><span class="sxs-lookup"><span data-stu-id="91d7b-211">**handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-212">Objeto COM que proporciona funcionalidad para un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-212">A COM object that provides functionality for a Shell item.</span></span> <span data-ttu-id="91d7b-213">La mayoría de los orígenes de datos de Shell ofrecen un sistema extensible para enlazar controladores a elementos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-213">Most Shell data sources offer an extensible system for binding handlers to items.</span></span> <span data-ttu-id="91d7b-214">Por ejemplo, la carpeta sistema de archivos utiliza el sistema de Asociación para buscar los controladores de un tipo de archivo determinado.</span><span class="sxs-lookup"><span data-stu-id="91d7b-214">For example, the file system folder uses the association system to look up the handlers for a particular file type.</span></span> <span data-ttu-id="91d7b-215">Vea también: Asociación de archivos, tipo de archivo, personalización de tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-215">See also: file association, file type, file type customization.</span></span>

</dd> </dl>

## <a name="i"></a><span data-ttu-id="91d7b-216">I</span><span class="sxs-lookup"><span data-stu-id="91d7b-216">I</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-217">**controlador de iconos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-217">**icon handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-218">Un controlador que proporciona la información necesaria para generar y almacenar en caché un icono para un elemento.</span><span class="sxs-lookup"><span data-stu-id="91d7b-218">A handler that provides the information needed to generate and cache an icon for an item.</span></span> <span data-ttu-id="91d7b-219">El almacén de datos del sistema de archivos admite la carga de un controlador de iconos para un elemento basado en el tipo de archivo, lo que permite a ese controlador proporcionar un icono que se usa para todas las instancias de ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-219">The file system data store supports loading an icon handler for an item based on the file type, enabling that handler to provide an icon that is used for all instances of that file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-220">**controlador recuadro informativo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-220">**infotip handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-221">Un controlador que proporciona texto emergente cuando el usuario mantiene el puntero del mouse sobre un objeto de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="91d7b-221">A handler that provides pop-up text when the user hovers the mouse pointer over a user interface object.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-222">**item**</span><span class="sxs-lookup"><span data-stu-id="91d7b-222">**item**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-223">Vea la definición de: elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-223">See definition for: Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-224">**clase de elemento**</span><span class="sxs-lookup"><span data-stu-id="91d7b-224">**item class**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-225">Vea la definición de: tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-225">See definition for: file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-226">**lista de identificadores de elemento**</span><span class="sxs-lookup"><span data-stu-id="91d7b-226">**item identifier list**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-227">Secuencia de una o varias estructuras SHITEMID que define de forma única un objeto relativo a algún objeto raíz.</span><span class="sxs-lookup"><span data-stu-id="91d7b-227">Sequence of one or more SHITEMID structures that uniquely defines an object relative to some root object.</span></span>

</dd> </dl>

## <a name="k"></a><span data-ttu-id="91d7b-228">K</span><span class="sxs-lookup"><span data-stu-id="91d7b-228">K</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-229">**Variante**</span><span class="sxs-lookup"><span data-stu-id="91d7b-229">**Kind**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-230">Propiedad que proporciona un nombre de clase fácil de usar y que se puede asociar a una lista de propiedades y un modelo de diseño.</span><span class="sxs-lookup"><span data-stu-id="91d7b-230">A property that provides a user-friendly Kind name, and can be associated with a list of properties and a layout pattern.</span></span> <span data-ttu-id="91d7b-231">La clase se presentó en Windows Vista para expresar una noción más descriptiva para el usuario final del tipo de archivo y se definió como una propiedad de cadena de varios valores (valores de cadena canónico), por lo que puede tener un valor de tipo "audio, vídeo" o "vínculo; documento".</span><span class="sxs-lookup"><span data-stu-id="91d7b-231">Kind was introduced in Windows Vista to express a more end-user friendly notion of file type and it was defined to be a multi-value string property (canonical string values), thus you can have an "audio;video" or "link;document" Kind value.</span></span> <span data-ttu-id="91d7b-232">Algunos nombres de tipo descriptivos ya están asociados a propiedades y patrones de diseño.</span><span class="sxs-lookup"><span data-stu-id="91d7b-232">Some user-friendly Kind names are already associated with properties and layout patterns.</span></span> <span data-ttu-id="91d7b-233">Por ejemplo, los elementos asociados a Kind. Picture y los elementos asociados a Kind.Document muestran propiedades diferentes incluso cuando están en la misma vista.</span><span class="sxs-lookup"><span data-stu-id="91d7b-233">For example, items associated with Kind.Picture and items associated with Kind.Document display different properties even when they are in the same view.</span></span> <span data-ttu-id="91d7b-234">Cada tipo de elemento puede asociarse a uno de cuatro patrones de diseño únicos que definen el número de propiedades que se muestran para cada elemento y su diseño.</span><span class="sxs-lookup"><span data-stu-id="91d7b-234">Each item Kind can be associated with one of four unique layout patterns that define the number of properties displayed for each item and their layout.</span></span> <span data-ttu-id="91d7b-235">Vea también: Asociación de clase, vista de contenido, patrón de diseño.</span><span class="sxs-lookup"><span data-stu-id="91d7b-235">See also: Kind association, content view, layout pattern.</span></span>

</dd> </dl>

## <a name="l"></a><span data-ttu-id="91d7b-236">L</span><span class="sxs-lookup"><span data-stu-id="91d7b-236">L</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-237">**patrón de diseño**</span><span class="sxs-lookup"><span data-stu-id="91d7b-237">**layout pattern**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-238">Una de varias formas de mostrar propiedades.</span><span class="sxs-lookup"><span data-stu-id="91d7b-238">One of several arrangements for displaying properties.</span></span> <span data-ttu-id="91d7b-239">En Windows 7 y versiones posteriores, cuando se registra un nuevo tipo de archivo, puede usar la vista de contenido para registrar una lista de propiedades personalizadas y un patrón de diseño para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-239">In Windows 7 and later, when you are registering a new file type, you can use the content view to register a custom property list and layout pattern for your file type.</span></span> <span data-ttu-id="91d7b-240">Puede elegir entre cuatro patrones de diseño diferentes: alfa (para los resultados de búsqueda de documentos que contienen fragmentos de código), beta (para los resultados de búsqueda por correo electrónico con fragmentos de código), gamma (similar a alfa pero con un diseño de dos líneas en lugar de cuatro) y Delta (para mostrar muchas propiedades más cortas, como con música e imágenes).</span><span class="sxs-lookup"><span data-stu-id="91d7b-240">You can choose from four different layout patterns: Alpha (for document search results that contain code snippets), Beta (for email search results with code snippets), Gamma (similar to Alpha but with a two-line layout instead of four), and Delta (for showing many shorter properties, such as with music and pictures).</span></span> <span data-ttu-id="91d7b-241">Vea también: vista de contenido, clase, Asociación de clase.</span><span class="sxs-lookup"><span data-stu-id="91d7b-241">See also: content view, Kind, Kind association.</span></span>

</dd> </dl>

## <a name="m"></a><span data-ttu-id="91d7b-242">M</span><span class="sxs-lookup"><span data-stu-id="91d7b-242">M</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-243">**controlador de metadatos**</span><span class="sxs-lookup"><span data-stu-id="91d7b-243">**metadata handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-244">Este término se usa a veces para indicar el controlador de propiedad.</span><span class="sxs-lookup"><span data-stu-id="91d7b-244">This term is sometimes used to mean property handler.</span></span> <span data-ttu-id="91d7b-245">Vea la definición de: controlador de propiedades.</span><span class="sxs-lookup"><span data-stu-id="91d7b-245">See definition for: property handler.</span></span>

</dd> </dl>

## <a name="n"></a><span data-ttu-id="91d7b-246">N</span><span class="sxs-lookup"><span data-stu-id="91d7b-246">N</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-247">**extensión de espacio de nombres**</span><span class="sxs-lookup"><span data-stu-id="91d7b-247">**namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-248">Vea la definición de: origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-248">See definition for: Shell data source.</span></span>

</dd> </dl>

## <a name="o"></a><span data-ttu-id="91d7b-249">O</span><span class="sxs-lookup"><span data-stu-id="91d7b-249">O</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-250">**Vinculación e incrustación de objetos de base de datos (OLE DB)**</span><span class="sxs-lookup"><span data-stu-id="91d7b-250">**Object Linking and Embedding Database (OLE DB)**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-251">Conjunto estándar de interfaces que proporciona acceso heterogéneo a distintos orígenes de información ubicados en cualquier lugar, como sistemas de archivos, carpetas de correo electrónico y bases de datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-251">A standard set of interfaces that provides heterogeneous access to disparate sources of information located anywhere, such as file systems, email folders, and databases.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-252">**OLE DB**</span><span class="sxs-lookup"><span data-stu-id="91d7b-252">**OLE DB**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-253">Vea la definición de: vinculación de objetos e incrustación de base de datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-253">See definition for: Object Linking and Embedding Database.</span></span>

</dd> </dl>

## <a name="p"></a><span data-ttu-id="91d7b-254">P</span><span class="sxs-lookup"><span data-stu-id="91d7b-254">P</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-255">**PerceivedType**</span><span class="sxs-lookup"><span data-stu-id="91d7b-255">**PerceivedType**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-256">Una amplia categoría de tipos de formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-256">A broad category of file format types.</span></span> <span data-ttu-id="91d7b-257">PerceivedType se presentó en Windows XP y admite un conjunto limitado de tipos de archivo conocidos (entre los que se incluyen imágenes, texto, audio y tipos de archivos comprimidos).</span><span class="sxs-lookup"><span data-stu-id="91d7b-257">PerceivedType was introduced in Windows XP, and supports a limited set of known file types (examples include Image, Text, Audio, and Compressed file types).</span></span> <span data-ttu-id="91d7b-258">Los tipos de archivo, generalmente los tipos de archivo públicos, también pueden tener un tipo percibido.</span><span class="sxs-lookup"><span data-stu-id="91d7b-258">File types, generally public file types, can also have a perceived type.</span></span> <span data-ttu-id="91d7b-259">Por ejemplo, los archivos de imagen Types. bmp,. png,. jpg y. gif también son del tipo percibido, Image.</span><span class="sxs-lookup"><span data-stu-id="91d7b-259">For example, the image file types .bmp, .png, .jpg, and .gif are also of the perceived type, image.</span></span> <span data-ttu-id="91d7b-260">En la capa de programación, PerceivedType se expresa como un entero.</span><span class="sxs-lookup"><span data-stu-id="91d7b-260">At the programming layer, PerceivedType is expressed as an integer.</span></span> <span data-ttu-id="91d7b-261">Dado que hay código que utiliza Kind y PerceivedType, los propietarios de formato de archivo deben registrar ambos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-261">Because there is code that uses Kind and PerceivedType, file format owners must register both.</span></span> <span data-ttu-id="91d7b-262">Por ejemplo, "reproducir todo" depende de PerceivedType.</span><span class="sxs-lookup"><span data-stu-id="91d7b-262">For example "play all" depends on PerceivedType.</span></span> <span data-ttu-id="91d7b-263">Vea también: tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-263">See also: file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-264">**controlador de vista previa**</span><span class="sxs-lookup"><span data-stu-id="91d7b-264">**preview handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-265">Un controlador que genera rápidamente una vista simplificada de solo lectura del elemento de Shell que se va a mostrar en el panel de vista previa del explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="91d7b-265">A handler that quickly produces a read-only, simplified view of the Shell item to be displayed in the Windows Explorer preview pane.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-266">**controlador de propiedades**</span><span class="sxs-lookup"><span data-stu-id="91d7b-266">**property handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-267">Un controlador que traduce los datos almacenados en un archivo en un esquema estructurado reconocido por y al que puede tener acceso el explorador de Windows, Windows Search y otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="91d7b-267">A handler that translates data stored in a file into a structured schema that is recognized by and can be accessed by Windows Explorer, Windows Search, and other applications.</span></span> <span data-ttu-id="91d7b-268">Después, estos sistemas pueden interactuar con el controlador de propiedades para escribir y leer las propiedades del archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-268">These systems can then interact with the property handler to write and read properties to and from the file.</span></span> <span data-ttu-id="91d7b-269">Los datos traducidos incluyen vista de detalles, recuadros informativos, panel de detalles, páginas de propiedades, etc.</span><span class="sxs-lookup"><span data-stu-id="91d7b-269">The translated data includes details view, infotips, details pane, property pages, and so forth.</span></span> <span data-ttu-id="91d7b-270">Cada controlador de propiedad está asociado a un tipo de archivo determinado, identificado por la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-270">Each property handler is associated with a particular file type, identified by the file name extension.</span></span> <span data-ttu-id="91d7b-271">Vea también: sistema de propiedades.</span><span class="sxs-lookup"><span data-stu-id="91d7b-271">See also: property system.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-272">**controlador de la hoja de propiedades**</span><span class="sxs-lookup"><span data-stu-id="91d7b-272">**property sheet handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-273">Un controlador que se usa para crear hojas de propiedades personalizadas con imágenes de interfaz de usuario y controles que permiten la interacción personalizada con un tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-273">A handler that is used to create custom property sheets with UI pictures and controls that permit custom interaction with a file type.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-274">**sistema de propiedades**</span><span class="sxs-lookup"><span data-stu-id="91d7b-274">**property system**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-275">Sistema de lectura y escritura extensible de definiciones de datos que usa propiedades implementadas como pares de nombre y valor.</span><span class="sxs-lookup"><span data-stu-id="91d7b-275">An extensible read/write system of data definitions that uses properties implemented as name-value pairs.</span></span> <span data-ttu-id="91d7b-276">Vea también: controlador de propiedades, elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-276">See also: property handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-277">**valor de propiedad**</span><span class="sxs-lookup"><span data-stu-id="91d7b-277">**property value**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-278">Valor asociado a un nombre de propiedad para un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-278">A value associated with a property name for a Shell item.</span></span> <span data-ttu-id="91d7b-279">Por ejemplo, "autor", "tamaño" y "fecha de toma" son propiedades.</span><span class="sxs-lookup"><span data-stu-id="91d7b-279">For example, "Author", "Size", and "Date Taken" are properties.</span></span> <span data-ttu-id="91d7b-280">Los valores de propiedad se expresan como una estructura PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="91d7b-280">Property values are expressed as a PROPVARIANT structure.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-281">**controlador de protocolo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-281">**protocol handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-282">Un controlador que tiene acceso a los orígenes de contenido y proporciona un objeto IUrlAccessor para el protocolo y la dirección URL especificados.</span><span class="sxs-lookup"><span data-stu-id="91d7b-282">A handler that accesses content sources and provides an IUrlAccessor object for a specified protocol and URL.</span></span> <span data-ttu-id="91d7b-283">Los controladores de protocolo amplían la funcionalidad de búsqueda de Windows y pueden proporcionar notificaciones de cambio a los indizadores.</span><span class="sxs-lookup"><span data-stu-id="91d7b-283">Protocol handlers extend Windows Search functionality, and may provide change notifications to indexers.</span></span> <span data-ttu-id="91d7b-284">Se requieren controladores de protocolo diferentes para indizar tipos específicos de almacenes de datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-284">Different protocol handlers are required to index specific types of data stores.</span></span> <span data-ttu-id="91d7b-285">Para proporcionar una experiencia de usuario razonable, también debe proporcionar un origen de datos de Shell para el almacén de datos, además de implementar el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-285">To provide a reasonable user experience, you must also provide a Shell data source for the data store in addition to implementing your protocol handler.</span></span> <span data-ttu-id="91d7b-286">El controlador de protocolo expone los elementos del almacén de datos al indexador, mientras que el origen de datos del shell expone los elementos del almacén de datos al shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-286">The protocol handler exposes the items in the data store to the indexer, while the Shell data source exposes the items in the data store to the Shell.</span></span>

</dd> </dl>

## <a name="r"></a><span data-ttu-id="91d7b-287">R</span><span class="sxs-lookup"><span data-stu-id="91d7b-287">R</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-288">**PIDL relativo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-288">**relative PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-289">PIDL que es relativo a algún objeto raíz en el espacio de nombres del shell que no sea la carpeta del escritorio.</span><span class="sxs-lookup"><span data-stu-id="91d7b-289">A PIDL that is relative to some root object in the shell namespace other than the desktop folder.</span></span> <span data-ttu-id="91d7b-290">Esta suele ser la carpeta principal del elemento.</span><span class="sxs-lookup"><span data-stu-id="91d7b-290">This is commonly the parent folder of the item.</span></span>

</dd> </dl>

## <a name="s"></a><span data-ttu-id="91d7b-291">S</span><span class="sxs-lookup"><span data-stu-id="91d7b-291">S</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-292">**Origen de datos de Shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-292">**Shell data source**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-293">Componente que se usa para extender el espacio de nombres del shell y exponer los elementos de un almacén de datos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-293">A component that is used to extend the Shell namespace and expose items in a data store.</span></span> <span data-ttu-id="91d7b-294">En el pasado, el origen de datos de Shell se denominaba extensión de espacio de nombres de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-294">In the past, the Shell data source was referred to as the Shell namespace extension.</span></span> <span data-ttu-id="91d7b-295">Vea también: contenedor, controlador, elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-295">See also: container, handler, Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-296">**Extensión de shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-296">**Shell extension**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-297">Este término se usa a veces para indicar el controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-297">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="91d7b-298">Vea la definición de: controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-298">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-299">**Controlador de extensión de Shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-299">**Shell extension handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-300">Este término se usa a veces para indicar el controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-300">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="91d7b-301">Vea la definición de: controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-301">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-302">**Controlador de Shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-302">**Shell handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-303">Este término se usa a veces para indicar el controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-303">This term is sometimes used to mean file type handler.</span></span> <span data-ttu-id="91d7b-304">Vea la definición de: controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-304">See definition for: file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-305">**Elemento de Shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-305">**Shell item**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-306">Un único fragmento de contenido.</span><span class="sxs-lookup"><span data-stu-id="91d7b-306">A single piece of content.</span></span> <span data-ttu-id="91d7b-307">Algunos elementos de Shell son orígenes de contenido y otros no.</span><span class="sxs-lookup"><span data-stu-id="91d7b-307">Some Shell items are content sources, and some are not.</span></span> <span data-ttu-id="91d7b-308">Una carpeta es un origen de contenido, por ejemplo, pero no un archivo. jpg.</span><span class="sxs-lookup"><span data-stu-id="91d7b-308">A folder is a content source, for example, but a .jpg file is not.</span></span> <span data-ttu-id="91d7b-309">Los controladores de tipo de archivo exponen elementos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-309">File type handlers expose Shell items.</span></span> <span data-ttu-id="91d7b-310">En algunos contextos, "Item" se usa para distinguir los contenedores de los no contenedores.</span><span class="sxs-lookup"><span data-stu-id="91d7b-310">In some contexts "item" is used to distinguish containers from noncontainers.</span></span> <span data-ttu-id="91d7b-311">Vea también: contenedor, origen de contenido, controlador de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="91d7b-311">See also: container, content source, file type handler.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-312">**Extensión de espacio de nombres Shell**</span><span class="sxs-lookup"><span data-stu-id="91d7b-312">**Shell namespace extension**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-313">Este término se usa a veces para hacer referencia al origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-313">This term is sometimes used to mean Shell data source.</span></span> <span data-ttu-id="91d7b-314">Vea la definición de: origen de datos de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-314">See definition for: Shell data source.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-315">**menú contextual**</span><span class="sxs-lookup"><span data-stu-id="91d7b-315">**shortcut menu**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-316">Interfaz de usuario que se utiliza para presentar una colección de verbos asociados a un elemento de la interfaz de usuario, como un archivo o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="91d7b-316">A user interface that is used to present a collection of verbs associated with a user interface element, such as a file or folder.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-317">**Controlador del menú contextual**</span><span class="sxs-lookup"><span data-stu-id="91d7b-317">**Shortcut menu handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-318">Un controlador que agrega verbos para un elemento o elementos.</span><span class="sxs-lookup"><span data-stu-id="91d7b-318">A handler that adds verbs for an item or items.</span></span> <span data-ttu-id="91d7b-319">Estos verbos se muestran normalmente en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-319">These verbs are commonly displayed in a shortcut menu.</span></span> <span data-ttu-id="91d7b-320">Vea también: menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-320">See also: shortcut menu.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-321">**PIDL simple**</span><span class="sxs-lookup"><span data-stu-id="91d7b-321">**simple PIDL**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-322">PIDL que se analiza sin comprobación de disco.</span><span class="sxs-lookup"><span data-stu-id="91d7b-322">A PIDL that is parsed without disk verification.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-323">**verbo estático**</span><span class="sxs-lookup"><span data-stu-id="91d7b-323">**static verb**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-324">Un verbo que se aplica a un elemento de Shell sin necesidad de inspeccionar el estado actual de un elemento o sistema.</span><span class="sxs-lookup"><span data-stu-id="91d7b-324">A verb that applies to a Shell item without needing to inspect the current state of an item or system.</span></span> <span data-ttu-id="91d7b-325">Un verbo estático se basa en un registro estático de los elementos asociados de un elemento y no cambia.</span><span class="sxs-lookup"><span data-stu-id="91d7b-325">A static verb is based on a static registration of the associated elements of an item, and does not change.</span></span>

</dd> </dl>

## <a name="t"></a><span data-ttu-id="91d7b-326">T</span><span class="sxs-lookup"><span data-stu-id="91d7b-326">T</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-327">**controlador de miniaturas**</span><span class="sxs-lookup"><span data-stu-id="91d7b-327">**thumbnail handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-328">Un controlador que proporciona una imagen estática para representar un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-328">A handler that provides a static image to represent a Shell item.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-329">**proveedor de miniaturas**</span><span class="sxs-lookup"><span data-stu-id="91d7b-329">**thumbnail provider**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-330">Este término se usa a veces para indicar el controlador de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="91d7b-330">This term is sometimes used to mean thumbnail handler.</span></span> <span data-ttu-id="91d7b-331">Vea la definición de: controlador de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="91d7b-331">See definition for: thumbnail handler.</span></span>

</dd> </dl>

## <a name="u"></a><span data-ttu-id="91d7b-332">U</span><span class="sxs-lookup"><span data-stu-id="91d7b-332">U</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-333">**nombre descriptivo del tipo de usuario**</span><span class="sxs-lookup"><span data-stu-id="91d7b-333">**user friendly kind name**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-334">Vea la definición de: Kind.</span><span class="sxs-lookup"><span data-stu-id="91d7b-334">See definition for: Kind.</span></span>

</dd> </dl>

## <a name="v"></a><span data-ttu-id="91d7b-335">V</span><span class="sxs-lookup"><span data-stu-id="91d7b-335">V</span></span>

<dl> <dt>

<span data-ttu-id="91d7b-336">**Verbo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-336">**verb**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-337">Una acción individual a la que puede llamar un elemento de Shell.</span><span class="sxs-lookup"><span data-stu-id="91d7b-337">An individual action that can be called by a Shell item.</span></span> <span data-ttu-id="91d7b-338">Entre los ejemplos se incluyen abrir e imprimir.</span><span class="sxs-lookup"><span data-stu-id="91d7b-338">Examples include open and print.</span></span> <span data-ttu-id="91d7b-339">Los verbos se conocen a veces como comandos o tareas.</span><span class="sxs-lookup"><span data-stu-id="91d7b-339">Verbs are sometimes referred to as commands or tasks.</span></span> <span data-ttu-id="91d7b-340">Vea también: verbo dinámico, controlador de menú contextual, verbo estático.</span><span class="sxs-lookup"><span data-stu-id="91d7b-340">See also: dynamic verb, shortcut menu handler, static verb.</span></span>

</dd> <dt>

<span data-ttu-id="91d7b-341">**controlador de verbo**</span><span class="sxs-lookup"><span data-stu-id="91d7b-341">**verb handler**</span></span>
</dt> <dd>

<span data-ttu-id="91d7b-342">Este término se usa a veces para hacer referencia al controlador del menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-342">This term is sometimes used to mean shortcut menu handler.</span></span> <span data-ttu-id="91d7b-343">Consulte definición de: controlador de menú contextual.</span><span class="sxs-lookup"><span data-stu-id="91d7b-343">See definition for: shortcut menu handler.</span></span>

</dd> </dl>

 

 



