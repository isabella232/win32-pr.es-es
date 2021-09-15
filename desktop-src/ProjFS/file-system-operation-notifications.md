---
title: Notificaciones de operación del sistema de archivos
description: Describe cómo un proveedor puede recibir notificaciones de operaciones del sistema de archivos.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473643"
---
# <a name="file-system-operation-notifications"></a>Notificaciones de operación del sistema de archivos

Además de las devoluciones de llamada necesarias para controlar la enumeración, devolver metadatos de archivo y contenido de archivo, un proveedor puede registrar opcionalmente una devolución de llamada de PRJ_NOTIFICATION_CB en su llamada **[a]()** **[PrjStartVirtualizing]()**.  Esta devolución de llamada recibe notificaciones de operaciones del sistema de archivos realizadas en archivos y directorios debajo de la raíz de virtualización de la instancia.  Algunas de las notificaciones son notificaciones "posteriores a la operación", que le dicen al proveedor que se acaba de completar una operación.  Las demás notificaciones son notificaciones de "operación previa", lo que significa que se notifica al proveedor antes de que se produce la operación.  En una notificación previa a la operación, el proveedor puede vetar la operación devolviendo un código de error de la devolución de llamada.  Esto hace que se produce un error en la operación con el código de error devuelto.

## <a name="how-to-specify-notifications-to-receive"></a>Cómo especificar notificaciones para recibir

Si el proveedor proporciona una implementación de **PRJ_NOTIFICATION_CB** cuando inicia una instancia de virtualización, también debe especificar qué notificaciones desea recibir.  Las notificaciones para las que el proveedor puede registrarse se definen en [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enumeración.

Cuando el proveedor especifica las notificaciones que desea recibir, lo hace mediante una matriz de una o [varias estructuras PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) datos.  Definen "asignaciones de notificaciones".  Una asignación de notificaciones es un emparejamiento entre un directorio, denominado "raíz de notificación" y un conjunto de notificaciones, expresado como una máscara de bits, que ProjFS debe enviar para ese directorio y sus descendientes.  También se puede establecer una asignación de notificaciones para un único archivo.  Un archivo o directorio especificado en una asignación de notificación no tiene que existir ya en el momento en que el proveedor llama a **PrjStartVirtualizing**, el proveedor puede especificar cualquier ruta de acceso y la asignación se aplicará a él si alguna vez se crea.

Si el proveedor especifica varias asignaciones de notificaciones y algunas son descendientes de otras, las asignaciones deben especificarse en profundidad descendente.  Las asignaciones de notificaciones en niveles más profundos reemplazan a las de nivel superior para sus descendientes.

Si el proveedor no especifica un conjunto de asignaciones de notificaciones, ProjFS enviará de forma predeterminada PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED y PRJ_NOTIFY_FILE_OVERWRITTEN para todos los archivos y directorios debajo de la raíz de virtualización.

El fragmento de código siguiente muestra cómo registrar un conjunto de notificaciones al iniciar una instancia de virtualización.

```C++
PRJ_CALLBACKS callbackTable;

// Supply required callbacks.
callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
callbackTable.GetFileDataCallback = MyGetFileDataCallback;

// The rest of the callbacks are optional.  We want notifications, so specify
// our notification callback.
callbackTable.QueryFileNameCallback = nullptr;
callbackTable.NotificationCallback = MyNotificationCallback;
callbackTable.CancelCommandCallback = nullptr;

// Assume the provider has created a new virtualization root at C:\VirtRoot and
// initialized it with this layout:
//
//     C:\VirtRoot
//     +--- baz
//     \--- foo
//          +--- subdir1
//          \--- subdir2
//
// The provider wants these notifications:
// * Notification of new file/directory creates for all locations within the
//   virtualization root that are not subject to one of the following more
//   specific notification mappings.
// * Notification of new file/directory creates, file opens, post-renames, and
//   pre- and post-deletes for C:\VirtRoot\foo
// * No notifications for C:\VirtRoot\foo\subdir1
PRJ_STARTVIRTUALIZING_OPTIONS startOpts = {};
PRJ_VIRTUALIZATION_MAPPING notificationMappings[3];

// Configure default notifications - notify of new files for most of the tree.
notificationMappings[0].NotificationRoot = L"";
notificationMappings[0].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED;

// Override default notifications - notify of new files, opened files, and file
// deletes for C:\VirtRoot\foo and its descendants.
notificationMappings[1].NotificationRoot = L"foo";
notificationMappings[1].NotificationBitMask = PRJ_NOTIFY_NEW_FILE_CREATED |
                                              PRJ_NOTIFY_FILE_OPENED |
                                              PRJ_NOTIFY_PRE_DELETE |
                                              PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED |
                                              PRJ_NOTIFY_FILE_RENAMED;

// Override all notifications for C:\VirtRoot\foo\subdir1 and its descendants.
notificationMappings[2].NotificationRoot = L"foo\\subdir1";
notificationMappings[2].NotificationBitMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;

startOpts.NotificationMappings = notificationMappings;
startOpts.NotificationMappingsCount = ARRAYSIZE(notificationMapping);

// Start the instance and provide our notification mappings.
HRESULT hr;
PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
hr = PrjStartVirtualizing(rootName,
                          &callbackTable,
                          nullptr,
                          &startOpts,
                          &instanceHandle);
if (FAILED(hr))
{
    wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
    return;
}
```

## <a name="receiving-notifications"></a>Recibir notificaciones

ProjFS envía notificaciones de operaciones del sistema de archivos llamando a la devolución de llamada **PRJ_NOTIFICATION_CB** del proveedor.  Lo hace para cada operación para la que se ha registrado el proveedor.  Si, como en el ejemplo anterior, el proveedor se registró para PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, y una aplicación creó un nuevo archivo en la raíz de notificación, ProjFS llamaría a la  devolución de llamada **PRJ_NOTIFICATION_CB** con el nombre de ruta de acceso del nuevo archivo y el parámetro de notificación establecido en PRJ_NOTIFICATION_NEW_FILE_CREATED.

ProjFS envía las notificaciones de la lista siguiente antes de que se lleve a cabo la operación del sistema de archivos asociada.  Si el proveedor devuelve un código de error de la devolución PRJ_NOTIFICATION_CB **de** llamada, se producirá un error en la operación del sistema de archivos y se devolverá el código de error especificado por el proveedor.

* PRJ_NOTIFICATION_PRE_DELETE: el archivo está a punto de eliminarse.
* PRJ_NOTIFICATION_PRE_RENAME: se va a cambiar el nombre del archivo.
* PRJ_NOTIFICATION_PRE_SET_HARDLINK: se va a crear un vínculo duro para el archivo.
* PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: un archivo está a punto de expandirse de un marcador de posición a un archivo completo, lo que indica que es probable que se modifique su contenido.

ProjFS envía las notificaciones de la lista siguiente una vez completada la operación del sistema de archivos asociada.

* PRJ_NOTIFICATION_FILE_OPENED: se ha abierto un archivo existente.
  * Aunque esta notificación se envía una vez abierto el archivo, el proveedor puede devolver un código de error.  En respuesta, ProjFS cancelará la apertura y devolverá el error al autor de la llamada.
* PRJ_NOTIFICATION_NEW_FILE_CREATED: se ha creado un nuevo archivo.
* PRJ_NOTIFICATION_FILE_OVERWRITTEN: se ha sobrescrito un archivo existente, por ejemplo  llamando a [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) con la marca _CREATE_ALWAYS dwCreationDisposition._
* PRJ_NOTIFICATION_FILE_RENAMED: se ha cambiado el nombre de un archivo.
* PRJ_NOTIFICATION_HARDLINK_CREATED: se [ha creado un vínculo](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) duro para un archivo.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: se ha cerrado un identificador de archivo y no se modificó el contenido del archivo ni se eliminó el archivo.
* PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: se ha cerrado un identificador de archivo y se ha modificado el contenido del archivo.
* PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: se ha cerrado un identificador de archivo y el archivo se eliminó como parte del cierre del identificador.

Para obtener más información sobre cada notificación, consulte la documentación de **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.

El **PRJ_NOTIFICATION_CB** de devolución de llamada _notificationParameters_ especifica parámetros adicionales para determinadas notificaciones.  Si un proveedor recibe una notificación PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, PRJ_NOTIFICATION_FILE_OVERWRITTEN o PRJ_NOTIFICATION_FILE_RENAMED, el proveedor puede especificar un nuevo conjunto de notificaciones que se recibirán para el archivo. Para obtener más información, consulte la documentación de **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.

En el ejemplo siguiente se muestran ejemplos sencillos de cómo un proveedor podría procesar las notificaciones para las que se registró en el fragmento de código anterior.

```C++
#include <windows.h>

HRESULT
MyNotificationCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ BOOLEAN isDirectory,
    _In_ PRJ_NOTIFICATION notification,
    _In_opt_z_ PCWSTR destinationFileName,
    _Inout_ PRJ_NOTIFICATION_PARAMETERS* operationParameters
    )
{
    HRESULT hr = S_OK;

    switch (notification)
    {
    case PRJ_NOTIFY_NEW_FILE_CREATED:

        wprintf(L"A new %ls was created at [%ls].\n",
                isDirectory ? L"directory" : L"file",
                callbackData->FilePathName);

        // Let's stop getting notifications inside newly-created directories.
        if (isDirectory)
        {
            operationParameters->PostCreate.NotificationMask = PRJ_NOTIFY_SUPPRESS_NOTIFICATIONS;
        }
        break;

    case PRJ_NOTIFY_FILE_OPENED:

        wprintf(L"Handle opened to %ls [%ls].\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_PRE_DELETE:

        wprintf(L"Attempt to delete %ls [%ls]: ",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);

        // MyAllowDelete is a routine the provider might implement to decide
        // whether to allow a given file/directory to be deleted.
        if (!MyAllowDelete(callbackData->FilePathName, isDirectory))
        {
            wprintf(L"DENIED\n");
            hr = HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED);
        }
        else
        {
            wprintf(L"ALLOWED\n");
        }
        break;

    case PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED:

        wprintf(L"The %ls [%ls] was deleted.\n",
                isDirectory ? L"directory": L"file",
                callbackData->FilePathName);
        break;

    case PRJ_NOTIFY_FILE_RENAMED:

        if (wcslen(callbackData->FilePathName) == 0)
        {
            // If callbackData->FilePathName is an empty string, then the item
            // that was renamed was originally in a location not under the
            // virtualization root.
            wprintf(L"A %ls was renamed into the virtualization root,\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its new location is [%ls].\n",
                    destinationFileName);
        }
        else if (wcslen(destinationFileName) == 0)
        {
            // If destinationFileName is an empty string, then the item that was
            // renamed is now in a location not under the virtualization root.
            wprintf(L"A %ls was renamed out of the virtualization root.\n",
                    isDirectory ? L"directory": L"file");
            wprintf(L"Its original location was [%ls].\n",
                    callbackData->FilePathName);
        }
        else
        {
            // If both names are specified, both the new and old names are under
            // the virtualization root (it is never the case that nether name is
            // specified).
            wprintf(L"A %ls [%ls] was renamed.\n",
                    isDirectory ? L"directory": L"file",
                    callbackData->FilePathName);
            wprintf(L"Its new name is [%ls].\n", destinationFileName);
        }
        break;

    default:
        wprintf(L"Unrecognized notification: 0x%08x");
    }

    // Note that this may be a failure code from MyAllowDelete().
    return hr;
}
```