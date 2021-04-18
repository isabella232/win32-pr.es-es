---
title: Glosario del sistema de archivos previsto de Windows
description: Términos especiales usados en ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/21/2020
ms.locfileid: "105720135"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="123d5-103">Glosario del sistema de archivos previsto de Windows</span><span class="sxs-lookup"><span data-stu-id="123d5-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="123d5-104">Términos especiales usados en ProjFS.</span><span class="sxs-lookup"><span data-stu-id="123d5-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="123d5-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**memoria auxiliar**</span><span class="sxs-lookup"><span data-stu-id="123d5-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-106">Datos jerárquicos mantenidos por el proveedor que se proyectan en el sistema de archivos como archivos y directorios.</span><span class="sxs-lookup"><span data-stu-id="123d5-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**marcador de posición modificado**</span><span class="sxs-lookup"><span data-stu-id="123d5-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-108">Archivo o directorio que se ha modificado localmente y que ya no es una caché de su estado en el almacén del proveedor.</span><span class="sxs-lookup"><span data-stu-id="123d5-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="123d5-109">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**archivo/directorio completo**</span><span class="sxs-lookup"><span data-stu-id="123d5-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-111">Un archivo o directorio creado en el sistema de archivos local, o un archivo que se ha modificado, de modo que ya no es una caché de su estado en la memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="123d5-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="123d5-112">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**marcador de posición hidratado**</span><span class="sxs-lookup"><span data-stu-id="123d5-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-114">Archivo cuyo contenido y sus metadatos se han almacenado en memoria caché en el disco.</span><span class="sxs-lookup"><span data-stu-id="123d5-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="123d5-115">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**falso**</span><span class="sxs-lookup"><span data-stu-id="123d5-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-117">Archivo o directorio que no está totalmente presente en el disco.</span><span class="sxs-lookup"><span data-stu-id="123d5-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="123d5-118">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**exclusión**</span><span class="sxs-lookup"><span data-stu-id="123d5-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-120">Marcador de posición oculto especial que representa un elemento que se ha eliminado del sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="123d5-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="123d5-121">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**directorio/archivo virtual**</span><span class="sxs-lookup"><span data-stu-id="123d5-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-123">Archivo o directorio que no existe físicamente en el disco, sino que se proyecta en los resultados de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="123d5-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="123d5-124">Consulte [Estado de la caché en la raíz de virtualización](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="123d5-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instancia de virtualización**</span><span class="sxs-lookup"><span data-stu-id="123d5-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-126">Objeto en memoria que administra la comunicación entre el proveedor y ProjFS para el conjunto de archivos y directorios ubicados en una raíz de virtualización determinada.</span><span class="sxs-lookup"><span data-stu-id="123d5-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="123d5-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**raíz de virtualización**</span><span class="sxs-lookup"><span data-stu-id="123d5-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="123d5-128">Directorio del sistema de archivos en el que se proyectan los datos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="123d5-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->