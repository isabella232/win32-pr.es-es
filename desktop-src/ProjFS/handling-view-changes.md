---
title: Control de cambios en la vista
description: Describe cómo actualizar la vista de cliente del almacén de respaldo de un proveedor.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/09/2018
ms.topic: article
ms.openlocfilehash: 99ace7849b8967748f26210d9d6b770e424c349359aa39e828c8ad9af36a65af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792652"
---
# <a name="handling-view-changes"></a>Control de cambios en la vista

A medida que se abren los archivos y directorios de la raíz de virtualización, el proveedor crea marcadores de posición en el disco y, a medida que se leen los archivos, los marcadores de posición se hidratan con contenido.  Estos marcadores de posición representan el estado de la tienda de respaldo en el momento en que se crearon.  Estos elementos almacenados en caché, combinados con los elementos proyectados por el proveedor en enumeraciones, constituyen la "vista" del cliente del almacén de respaldo.  De vez en cuando, es posible que el proveedor quiera actualizar la vista del cliente, ya sea debido a cambios en el almacén de respaldo o a una acción explícita del usuario para cambiar su vista.

> Si el proveedor actualiza la vista de forma proactiva, a medida que cambia el almacén de respaldo, se recomienda que los cambios de vista sean relativamente poco frecuentes.  Esto se debe a que una vista cambia a un elemento que se ha abierto y, por tanto, se ha creado un marcador de posición en el disco, requiere que el elemento en disco se actualice o elimine para reflejar el cambio de vista.  Las actualizaciones frecuentes pueden dar lugar a una actividad de disco adicional que puede afectar negativamente al rendimiento del sistema.

## <a name="item-versioning"></a>Control de versiones de elementos

Para admitir el mantenimiento de varias vistas, ProjFS proporciona **[la PRJ_PLACEHOLDER_VERSION_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info)** struct.  Un proveedor usa esta estructura independiente en las llamadas a **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** y se inserta en los **[structs PRJ_PLACEHOLDER_INFO](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_placeholder_info)** y **[PRJ_CALLBACK_DATA](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callback_data)** structs.  El **PRJ_PLACEHOLDER_VERSION_INFO**. El campo ContentID es donde el proveedor almacena hasta 128 bytes de información de versión para un archivo o directorio.  A continuación, el proveedor puede asociar internamente este valor a algún valor que identifique una vista determinada.

Por ejemplo, un proveedor que virtualiza un repositorio de control de código fuente podría optar por usar un hash del contenido de un archivo para actuar como ContentID, y podría usar marcas de tiempo para identificar vistas del repositorio en varios momentos en el tiempo.  Las marcas de tiempo pueden ser las veces que se realizaron las confirmaciones en el repositorio.

Con el ejemplo de un repositorio indizado por marca de tiempo, un flujo típico para usar contentID de un elemento podría ser:

1. El cliente establece una vista especificando la marca de tiempo en la que se va a presentar el contenido del repositorio.  Esto se haría a través de alguna interfaz implementada por el proveedor, no a través de una API ProjFS.  Por ejemplo, el proveedor puede tener una herramienta de línea de comandos que podría usarse para decir al proveedor qué vista desea el usuario.
1. Cuando el cliente crea un identificador para un archivo o directorio virtualizado, el proveedor crea un marcador de posición para él, mediante metadatos del sistema de archivos del almacén de respaldo.  El conjunto concreto de metadatos que usa se identifica mediante el valor ContentID asociado a la marca de tiempo de la vista deseada.  Cuando el proveedor llama a **[PrjWritePlaceholderInfo](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjwriteplaceholderinfo)** para escribir la información del marcador de posición, proporciona contentID en el miembro VersionInfo del argumento _placeholderInfo._  A continuación, el proveedor debe registrar que se creó un marcador de posición para ese archivo o directorio en esta vista.
1. Cuando el cliente lee de un marcador de posición, se invoca la devolución PRJ_GET_FILE_DATA_CB **[de](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_file_data_cb)** llamada del proveedor.  El miembro VersionInfo del parámetro _callbackData_ contiene el ContentID que el proveedor especificó en **PrjWritePlaceholderInfo** cuando creó el marcador de posición de archivo.  El proveedor usa ese ContentID para recuperar el contenido correcto del archivo de su almacén de respaldo.
1. El cliente solicita un cambio de vista especificando una nueva marca de tiempo.  Para cada marcador de posición que el proveedor creó en la vista anterior, si existe una versión diferente de ese archivo en la nueva vista, el proveedor puede reemplazar el marcador de posición en el disco por uno actualizado cuyo ContentID está asociado a la nueva marca de tiempo llamando a **[PrjUpdateFileIfNeeded](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjupdatefileifneeded)**.  Como alternativa, el proveedor puede eliminar el marcador de posición llamando a **[PrjDeleteFile](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjdeletefile)** para que la nueva vista del archivo se proyecte en enumeraciones.  Si el archivo no existe en la nueva vista, el proveedor debe eliminarlo llamando a **PrjDeleteFile**.

Tenga en cuenta que el proveedor debe asegurarse de que, cuando el cliente enumera un directorio, el proveedor proporcione el contenido correspondiente a la vista del cliente.  Por ejemplo, el proveedor podría usar el miembro VersionInfo del parámetro _callbackData_ de las devoluciones de llamada **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** y **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** para recuperar el contenido del directorio sobre la marcha.  Como alternativa, podría crear una estructura de directorios para esa vista en su almacén de respaldo como parte del establecimiento de la vista y, a continuación, simplemente enumerar esa estructura.

> Cada vez que se invoca una devolución de llamada de proveedor para un marcador de posición o un archivo parcial, la información de versión que el proveedor especificó al crear el elemento se proporciona en el miembro VersionInfo del parámetro _callbackData_ de la devolución de llamada.

## <a name="updating-the-view"></a>Actualización de la vista

A continuación se muestra una función de ejemplo que ilustra cómo un proveedor podría actualizar la vista local cuando el usuario especifica una nueva marca de tiempo.  La función recupera una lista de los marcadores de posición que el proveedor creó para la vista desde la que el usuario acaba de cambiar y actualiza el estado de la caché local en función del estado de cada marcador de posición en la nueva vista.  Para mayor claridad, esta rutina omite ciertas complejidades de tratar con el sistema de archivos.  Por ejemplo, en la vista anterior puede haber existido un directorio determinado con algunos archivos o directorios, pero es posible que en la nueva vista ese directorio (y su contenido) ya no existan.  Para evitar errores en este tipo de situación, el proveedor debe actualizar el estado del archivo y los directorios debajo de la raíz de virtualización de forma por primera vez.

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