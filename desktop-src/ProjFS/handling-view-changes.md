---
title: Control de cambios de vista
description: Describe cómo actualizar la vista de cliente de la memoria auxiliar de un proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 1d5a709752f92b7449d2ccc38f67c4417edf8d62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077871"
---
# <a name="handling-view-changes"></a><span data-ttu-id="f0586-103">Control de cambios de vista</span><span class="sxs-lookup"><span data-stu-id="f0586-103">Handling View Changes</span></span>

<span data-ttu-id="f0586-104">A medida que se abren archivos y directorios en la raíz de virtualización, el proveedor crea marcadores de posición en el disco y, a medida que se leen los archivos, los marcadores de posición se hidratan con el contenido.</span><span class="sxs-lookup"><span data-stu-id="f0586-104">As files and directories under the virtualization root are opened, the provider creates placeholders on disk, and as files are read the placeholders are hydrated with contents.</span></span>  <span data-ttu-id="f0586-105">Estos marcadores de posición representan el estado de la memoria auxiliar en el momento en que se crearon.</span><span class="sxs-lookup"><span data-stu-id="f0586-105">These placeholders represent the state of the backing store at the time they were created.</span></span>  <span data-ttu-id="f0586-106">Estos elementos almacenados en caché, combinados con los elementos proyectados por el proveedor en enumeraciones, constituyen la "vista" del cliente de la memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f0586-106">These cached items, combined with the items projected by the provider in enumerations, constitute the client's "view" of the backing store.</span></span>  <span data-ttu-id="f0586-107">De vez en cuando, es posible que el proveedor desee actualizar la vista del cliente, ya sea debido a cambios en la memoria auxiliar o debido a una acción explícita realizada por el usuario para cambiar su vista.</span><span class="sxs-lookup"><span data-stu-id="f0586-107">From time to time the provider may wish to update the client's view, whether because of changes in the backing store, or because of explicit action taken by the user to change their view.</span></span>

> <span data-ttu-id="f0586-108">Si el proveedor actualiza la vista de forma proactiva, a medida que cambia la memoria auxiliar, se recomienda que los cambios de la vista sean relativamente poco frecuentes.</span><span class="sxs-lookup"><span data-stu-id="f0586-108">If the provider updates the view proactively, as the backing store changes, it is recommended that view changes be relatively infrequent.</span></span>  <span data-ttu-id="f0586-109">Esto se debe a que un cambio de vista en un elemento que se ha abierto y, por tanto, tenía un marcador de posición creado en el disco, requiere que el elemento en disco se actualice o se elimine para reflejar el cambio de vista.</span><span class="sxs-lookup"><span data-stu-id="f0586-109">This is because a view change to an item that has been opened, and therefore had a placeholder created on disk, requires that the on-disk item be either updated or deleted to reflect the view change.</span></span>  <span data-ttu-id="f0586-110">Las actualizaciones frecuentes pueden dar lugar a una actividad adicional en el disco que puede afectar negativamente al rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="f0586-110">Frequent updates may result in extra disk activity that can negatively impact system performance.</span></span>

## <a name="item-versioning"></a><span data-ttu-id="f0586-111">Control de versiones de elementos</span><span class="sxs-lookup"><span data-stu-id="f0586-111">Item Versioning</span></span>

<span data-ttu-id="f0586-112">Para permitir el mantenimiento de varias vistas, ProjFS proporciona la **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span><span class="sxs-lookup"><span data-stu-id="f0586-112">To support maintaining multiple views, ProjFS provides the **[PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.</span></span>  <span data-ttu-id="f0586-113">Un proveedor utiliza este struct independiente en las llamadas a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** y se inserta en los structs **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** y **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** .</span><span class="sxs-lookup"><span data-stu-id="f0586-113">A provider uses this struct standalone in calls to **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)**, and it is embedded in the **[PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** and **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.</span></span>  <span data-ttu-id="f0586-114">**PRJ_PLACEHOLDER_VERSION_INFO**. El campo ContentID es donde el proveedor almacena hasta 128 bytes de información de versión para un archivo o directorio.</span><span class="sxs-lookup"><span data-stu-id="f0586-114">The **PRJ_PLACEHOLDER_VERSION_INFO**.ContentID field is where the provider stores up to 128 bytes of version information for a file or directory.</span></span>  <span data-ttu-id="f0586-115">Después, el proveedor puede asociar internamente este valor a algún valor que identifique una vista determinada.</span><span class="sxs-lookup"><span data-stu-id="f0586-115">The provider may then internally associate this value to some value that identifies a particular view.</span></span>

<span data-ttu-id="f0586-116">Por ejemplo, un proveedor que virtualiza un repositorio de control de código fuente puede optar por usar un hash del contenido de un archivo para que sirva como ContentID y podría usar marcas de tiempo para identificar vistas del repositorio en varios puntos en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0586-116">For example, a provider that virtualizes a source control repository might choose to use a hash of a file's contents to serve as the ContentID, and it might use timestamps to identify views of the repository at various points in time.</span></span>  <span data-ttu-id="f0586-117">Las marcas de tiempo pueden ser las horas en las que se realizaron confirmaciones en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="f0586-117">The timestamps might be the times that commits to the repository were performed.</span></span>

<span data-ttu-id="f0586-118">Con el ejemplo de un repositorio con índice de marca de tiempo, un flujo típico para usar ContentID de un elemento podría ser:</span><span class="sxs-lookup"><span data-stu-id="f0586-118">Using the example of a timestamp-indexed repository, a typical flow for using an item's ContentID might be:</span></span>

1. <span data-ttu-id="f0586-119">El cliente establece una vista especificando la marca de tiempo en la que se presenta el contenido del repositorio.</span><span class="sxs-lookup"><span data-stu-id="f0586-119">The client establishes a view by specifying the timestamp at which to present the repository contents.</span></span>  <span data-ttu-id="f0586-120">Esto se llevaría a cabo a través de una interfaz implementada por el proveedor, no a través de una API de ProjFS.</span><span class="sxs-lookup"><span data-stu-id="f0586-120">This would be done through some interface implemented by the provider, not via a ProjFS API.</span></span>  <span data-ttu-id="f0586-121">Por ejemplo, el proveedor puede tener una herramienta de línea de comandos que se puede usar para indicar al proveedor qué desea ver el usuario.</span><span class="sxs-lookup"><span data-stu-id="f0586-121">For example, the provider may have a command-line tool that could be used to tell the provider which view the user desires.</span></span>
1. <span data-ttu-id="f0586-122">Cuando el cliente crea un identificador para un archivo o directorio virtualizado, el proveedor crea un marcador de posición para él, usando los metadatos del sistema de archivos de la memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f0586-122">When the client creates a handle to a virtualized file or directory, the provider creates a placeholder for it, using file system metadata from the backing store.</span></span>  <span data-ttu-id="f0586-123">El conjunto determinado de metadatos que utiliza se identifica mediante el valor de ContentID asociado a la marca de tiempo de la vista deseada.</span><span class="sxs-lookup"><span data-stu-id="f0586-123">The particular set of metadata it uses is identified by the ContentID value associated with the timestamp of the desired view.</span></span>  <span data-ttu-id="f0586-124">Cuando el proveedor llama a **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para escribir la información del marcador de posición, proporciona el elemento contentid en el miembro versionInfo del argumento _placeholderInfo_ .</span><span class="sxs-lookup"><span data-stu-id="f0586-124">When the provider calls **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** to write the placeholder information, it supplies the ContentID in the VersionInfo member of the _placeholderInfo_ argument.</span></span>  <span data-ttu-id="f0586-125">A continuación, el proveedor debe registrar que se ha creado un marcador de posición para ese archivo o directorio en esta vista.</span><span class="sxs-lookup"><span data-stu-id="f0586-125">The provider should then record that a placeholder for that file or directory was created in this view.</span></span>
1. <span data-ttu-id="f0586-126">Cuando el cliente Lee un marcador de posición, se invoca la devolución de llamada del **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f0586-126">When the client reads from a placeholder, the provider's **[PRJ_GET_FILE_DATA_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** callback is invoked.</span></span>  <span data-ttu-id="f0586-127">El miembro VersionInfo del parámetro _callbackData_ contiene el proveedor contentid especificado en **PrjWritePlaceholderInfo** cuando creó el marcador de posición de archivo.</span><span class="sxs-lookup"><span data-stu-id="f0586-127">The _callbackData_ parameter's VersionInfo member contains the ContentID the provider specified in **PrjWritePlaceholderInfo** when it created the file placeholder.</span></span>  <span data-ttu-id="f0586-128">El proveedor utiliza ese ContentID para recuperar el contenido correcto del archivo desde su memoria auxiliar.</span><span class="sxs-lookup"><span data-stu-id="f0586-128">The provider uses that ContentID to retrieve the correct contents of the file from its backing store.</span></span>
1. <span data-ttu-id="f0586-129">El cliente solicita un cambio de vista especificando una nueva marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0586-129">The client requests a view change by specifying a new timestamp.</span></span>  <span data-ttu-id="f0586-130">Para cada marcador de posición que creó el proveedor en la vista anterior, si existe una versión diferente de ese archivo en la nueva vista, el proveedor puede reemplazar el marcador de posición en disco por uno actualizado cuyos ContentID esté asociado a la nueva marca de tiempo llamando a **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span><span class="sxs-lookup"><span data-stu-id="f0586-130">For each placeholder the provider created in the previous view, if a different version of that file exists in the new view the provider may replace the placeholder on disk with an updated one whose ContentID is associated with the new timestamp by calling **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.</span></span>  <span data-ttu-id="f0586-131">Como alternativa, el proveedor puede eliminar el marcador de posición mediante una llamada a **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** para que la nueva vista del archivo se proyecte en enumeraciones.</span><span class="sxs-lookup"><span data-stu-id="f0586-131">Alternatively, the provider may delete the placeholder by calling **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** so that the new view of the file will be projected in enumerations.</span></span>  <span data-ttu-id="f0586-132">Si el archivo no existe en la vista nueva, el proveedor debe eliminarlo llamando a **PrjDeleteFile**.</span><span class="sxs-lookup"><span data-stu-id="f0586-132">If the file does not exist in the new view, the provider must delete it by calling **PrjDeleteFile**.</span></span>

<span data-ttu-id="f0586-133">Tenga en cuenta que el proveedor debe asegurarse de que, cuando el cliente Enumere un directorio, el proveedor suministre el contenido que se corresponda con la vista del cliente.</span><span class="sxs-lookup"><span data-stu-id="f0586-133">Note that the provider must ensure that when the client enumerates a directory, the provider will supply the contents that correspond to the client's view.</span></span>  <span data-ttu-id="f0586-134">Por ejemplo, el proveedor podría usar el miembro VersionInfo del parámetro _callbackData_ de las devoluciones de llamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** y **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** para recuperar el contenido del directorio sobre la marcha.</span><span class="sxs-lookup"><span data-stu-id="f0586-134">For example, the provider could use the VersionInfo member of the _callbackData_ parameter of the **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** and **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** callbacks to retrieve directory contents on the fly.</span></span>  <span data-ttu-id="f0586-135">Como alternativa, podría crear una estructura de directorios para esa vista en su memoria auxiliar como parte del establecimiento de la vista y, a continuación, simplemente enumerar esa estructura.</span><span class="sxs-lookup"><span data-stu-id="f0586-135">Alternatively it could build a directory structure for that view in its backing store as part of establishing the view, and then simply enumerate that structure.</span></span>

> <span data-ttu-id="f0586-136">Siempre que se invoca una devolución de llamada de proveedor para un marcador de posición o un archivo parcial, la información de versión que el proveedor especificó al crear el elemento se proporciona en el miembro VersionInfo del parámetro _callbackData_ de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="f0586-136">Whenever a provider callback is invoked for a placeholder or partial file, the version information the provider specified when creating the item is provided in the VersionInfo member of the callback's _callbackData_ parameter.</span></span>

## <a name="updating-the-view"></a><span data-ttu-id="f0586-137">Actualización de la vista</span><span class="sxs-lookup"><span data-stu-id="f0586-137">Updating the View</span></span>

<span data-ttu-id="f0586-138">A continuación se muestra una función de ejemplo que ilustra cómo un proveedor puede actualizar la vista local cuando el usuario especifica una nueva marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="f0586-138">Below is a sample function illustrating how a provider might update the local view when the user specifies a new timestamp.</span></span>  <span data-ttu-id="f0586-139">La función recupera una lista de los marcadores de posición creados por el proveedor para la vista del que el usuario ha cambiado y actualiza el estado de la caché local en función del estado de cada marcador de posición en la nueva vista.</span><span class="sxs-lookup"><span data-stu-id="f0586-139">The function retrieves a list of the placeholders the provider created for the view the user has just changed from, and updates the local cache state based on each placeholder's state in the new view.</span></span>  <span data-ttu-id="f0586-140">Para mayor claridad, esta rutina omite ciertas complejidades de tratar con el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="f0586-140">For clarity, this routine omits certain complexities of dealing with the file system.</span></span>  <span data-ttu-id="f0586-141">Por ejemplo, en la vista anterior podría haber existido un directorio determinado con algunos archivos o directorios, pero, en la nueva vista, es posible que ya no exista el directorio (y su contenido).</span><span class="sxs-lookup"><span data-stu-id="f0586-141">For example, in the old view a given directory may have existed with some files or directories in it, but in the new view that directory (and its contents) may no longer exist.</span></span>  <span data-ttu-id="f0586-142">Para evitar que se produzcan errores en esta situación, el proveedor debe actualizar el estado del archivo y los directorios bajo la raíz de virtualización en un modo de prioridad a la profundidad.</span><span class="sxs-lookup"><span data-stu-id="f0586-142">To avoid encountering errors in such a situation the provider should update the state of the file and directories beneath the virtualization root in a depth-first fashion.</span></span>

```C++
typedef struct MY_ON_DISK_PLACEHOLDER MY_ON_DISK_PLACEHOLDER;

typedef struct MY_ON_DISK_PLACEHOLDER {
    MY_ON_DISK_PLACEHOLDER* Next;
    PWSTR RelativePath;
} MY_ON_DISK_PLACEHOLDER;

HRESULT
MyViewUpdater(
    _In_ PRJ_CALLBACK_DATA callbackData,
    _In_ time_t newViewTime
    )
{
    HRESULT hr = S_OK;

    // MyGetOnDiskPlaceholders is a routine the provider might implement to produce
    // a pointer to a list of the placeholders the provider has created in the view.
    MY_ON_DISK_PLACEHOLDER* placeholder = MyGetOnDiskPlaceholders();
    while (placeholder != NULL)
    {
        // MyGetProjectedFileInfo is a routine the provider might implement to
        // determine whether a given file exists in its backing store at a
        // particular timestamp.  If it does, the routine returns a pointer to
        // a PRJ_PLACEHOLDER_INFO struct populated with information about the
        // file.
        PRJ_PLACEHOLDER_INFO* newViewPlaceholderInfo = NULL;
        UINT32 newViewPlaceholderInfoSize = 0;

        newViewPlaceholderInfo = MyGetProjectedFileInfo(placeholder->RelativePath,
                                                 newViewTime,
                                                 &newViewPlaceholderInfoSize);
        if (newViewPlaceholderInfo == NULL)
        {
            // The file no longer exists in the new view.  We want to remove its
            // placeholder from the local cache.
            PRJ_UPDATE_FAILURE_CAUSES deleteFailureReason;
            hr = PrjDeleteFile(callbackData->NamespaceVirtualizationContext,
                               placeholder->RelativePath,
                               PRJ_UPDATE_ALLOW_DIRTY_METADATA
                               | PRJ_UPDATE_ALLOW_DIRTY_DATA
                               | PRJ_UPDATE_ALLOW_TOMBSTONE,
                               &deleteFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not delete [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", deleteFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error deleting [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyRemovePlaceholderData is a routine the provider might implement
            // to remove an item from its list of placeholders it has created in
            // the view.
            MyRemovePlaceholderData(placeholder);
        }
        else
        {
            // The file exists in the new view.  Its local cache state may need
            // to be updated, for example if its content is different in this view.
            // As an optimization, the provider may compare the file's ContentID
            // in the new view (stored in newViewPlaceholderInfo->ContentId) with
            // the ContentID it had in the old view.  If they are the same, calling
            // PrjUpdateFileIfNeeded would not be needed.
            PRJ_UPDATE_FAILURE_CAUSES updateFailureReason;
            hr = PrjUpdateFileIfNeeded(callbackData->NamespaceVirtualizationContext,
                                       placeholder->RelativePath,
                                       newViewPlaceholderInfo,
                                       newViewPlaceholderInfoSize,
                                       PRJ_UPDATE_ALLOW_DIRTY_METADATA
                                       | PRJ_UPDATE_ALLOW_DIRTY_DATA
                                       | PRJ_UPDATE_ALLOW_TOMBSTONE,
                                       &updateFailureReason);

            if (hr == HRESULT_FROM_WIN32(ERROR_FILE_SYSTEM_VIRTUALIZATION_INVALID_OPERATION))
            {
                wprintf(L"Could not update [%ls].\n", placeholder->RelativePath);
                wprintf(L"Failure reason: 0x%x", updateFailureReason);
                return hr;
            }
            else
            {
                wprintf(L"Error updating [%ls]: 0x%08x",
                        placeholder->RelativePath,
                        hr);
                return hr;
            }

            // MyUpdatePlaceholderData is a routine the provider might implement
            // to update information about a placeholder it has created in the view.
            MyUpdatePlaceholderData(placeholder, newViewPlaceholderInfo);
        }

        placeholder = placeholder->Next;
    }

    return hr;
}
```