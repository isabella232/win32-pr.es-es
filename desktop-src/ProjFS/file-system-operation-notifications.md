---
title: Notificaciones de operación del sistema de archivos
description: Describe cómo un proveedor puede recibir notificaciones de las operaciones del sistema de archivos.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/04/2018
ms.topic: article
ms.openlocfilehash: 9eae9bde6d56592f371dcd48c24fef96a9eecbdf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792004"
---
# <a name="file-system-operation-notifications"></a><span data-ttu-id="783a1-103">Notificaciones de operación del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="783a1-103">File System Operation Notifications</span></span>

<span data-ttu-id="783a1-104">Además de las devoluciones de llamada necesarias para controlar la enumeración, devolver metadatos de archivo y contenido de archivo, un proveedor puede registrar opcionalmente una **[PRJ_NOTIFICATION_CB]()** devolución de llamada en su llamada a **[PrjStartVirtualizing]()**.</span><span class="sxs-lookup"><span data-stu-id="783a1-104">In addition to required callbacks for handling enumeration, returning file metadata, and file contents, a provider may optionally register a **[PRJ_NOTIFICATION_CB]()** callback in its call to **[PrjStartVirtualizing]()**.</span></span>  <span data-ttu-id="783a1-105">Esta devolución de llamada recibe notificaciones de las operaciones del sistema de archivos realizadas en los archivos y directorios situados debajo de la raíz de virtualización de la instancia.</span><span class="sxs-lookup"><span data-stu-id="783a1-105">This callback receives notifications of file system operations performed on files and directories beneath the instance's virtualization root.</span></span>  <span data-ttu-id="783a1-106">Algunas de las notificaciones son notificaciones "posteriores a la operación", que indican al proveedor que se acaba de completar una operación.</span><span class="sxs-lookup"><span data-stu-id="783a1-106">Some of the notifications are "post-operation" notifications, which tell the provider that an operation has just completed.</span></span>  <span data-ttu-id="783a1-107">Las demás notificaciones son notificaciones de "preoperación", lo que significa que se notifica al proveedor antes de que se produzca la operación.</span><span class="sxs-lookup"><span data-stu-id="783a1-107">The other notifications are "pre-operation" notifications, meaning that the provider is notified before the operation happens.</span></span>  <span data-ttu-id="783a1-108">En una notificación previa a la operación, el proveedor puede vetar la operación devolviendo un código de error de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="783a1-108">In a pre-operation notification the provider can veto the operation by returning an error code from the callback.</span></span>  <span data-ttu-id="783a1-109">Esto hace que se produzca un error en la operación con el código de error devuelto.</span><span class="sxs-lookup"><span data-stu-id="783a1-109">This causes the operation to fail with the returned error code.</span></span>

## <a name="how-to-specify-notifications-to-receive"></a><span data-ttu-id="783a1-110">Cómo especificar las notificaciones que se van a recibir</span><span class="sxs-lookup"><span data-stu-id="783a1-110">How to Specify Notifications to Receive</span></span>

<span data-ttu-id="783a1-111">Si el proveedor proporciona una implementación de **PRJ_NOTIFICATION_CB** cuando inicia una instancia de virtualización, también debe especificar qué notificaciones desea recibir.</span><span class="sxs-lookup"><span data-stu-id="783a1-111">If the provider supplies an implementation of **PRJ_NOTIFICATION_CB** when it starts a virtualization instance, it should also specify which notifications it wishes to receive.</span></span>  <span data-ttu-id="783a1-112">Las notificaciones para las que se puede registrar el proveedor se definen en la enumeración [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) .</span><span class="sxs-lookup"><span data-stu-id="783a1-112">The notifications for which the provider can register are defined in the [PRJ_NOTIFICATION](/windows/win32/api/projectedfslib/ne-projectedfslib-prj_notification) enum.</span></span>

<span data-ttu-id="783a1-113">Cuando el proveedor especifica las notificaciones que desea recibir, lo hace mediante una matriz de una o varias estructuras de [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) .</span><span class="sxs-lookup"><span data-stu-id="783a1-113">When the provider specifies the notifications it wishes to receive, it does so using an array of one or more [PRJ_NOTIFICATION_MAPPING](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) structures.</span></span>  <span data-ttu-id="783a1-114">Estos definen "asignaciones de notificaciones".</span><span class="sxs-lookup"><span data-stu-id="783a1-114">These define "notification mappings".</span></span>  <span data-ttu-id="783a1-115">Una asignación de notificación es un emparejamiento entre un directorio, denominado "raíz de la notificación", y un conjunto de notificaciones, expresado como máscara de bits, que ProjFS debe enviar para ese directorio y sus descendientes.</span><span class="sxs-lookup"><span data-stu-id="783a1-115">A notification mapping is a pairing between a directory, referred to as a "notification root", and a set of notifications, expressed as a bit mask, which ProjFS should send for that directory and its descendants.</span></span>  <span data-ttu-id="783a1-116">También se puede establecer una asignación de notificación para un único archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-116">A notification mapping can also be established for a single file.</span></span>  <span data-ttu-id="783a1-117">No es necesario que un archivo o directorio especificado en una asignación de notificaciones exista ya en el momento en que el proveedor llama a **PrjStartVirtualizing**, el proveedor puede especificar cualquier ruta de acceso y la asignación se aplicará en caso de que se haya creado.</span><span class="sxs-lookup"><span data-stu-id="783a1-117">A file or directory specified in a notification mapping does not have to exist already at the time the provider calls **PrjStartVirtualizing**, the provider can specify any path and the mapping will apply to it if it is ever created.</span></span>

<span data-ttu-id="783a1-118">Si el proveedor especifica varias asignaciones de notificaciones y otras son descendientes de otras, las asignaciones se deben especificar en profundidad descendente.</span><span class="sxs-lookup"><span data-stu-id="783a1-118">If the provider specifies multiple notification mappings, and some are descendants of others, the mappings must be specified in descending depth.</span></span>  <span data-ttu-id="783a1-119">Las asignaciones de notificaciones en niveles más profundos invalidan las más importantes para sus descendientes.</span><span class="sxs-lookup"><span data-stu-id="783a1-119">Notification mappings at deeper levels override higher-level ones for their descendants.</span></span>

<span data-ttu-id="783a1-120">Si el proveedor no especifica un conjunto de asignaciones de notificaciones, ProjFS le enviará de forma predeterminada PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED y PRJ_NOTIFY_FILE_OVERWRITTEN de todos los archivos y directorios situados debajo de la raíz de virtualización.</span><span class="sxs-lookup"><span data-stu-id="783a1-120">If the provider does not specify a set of notification mappings, ProjFS will default to sending it PRJ_NOTIFY_FILE_OPENED, PRJ_NOTIFY_NEW_FILE_CREATED, and PRJ_NOTIFY_FILE_OVERWRITTEN for all files and directories beneath the virtualization root.</span></span>

<span data-ttu-id="783a1-121">El siguiente fragmento de código muestra cómo registrar un conjunto de notificaciones al iniciar una instancia de virtualización.</span><span class="sxs-lookup"><span data-stu-id="783a1-121">The following code snippet illustrates how to register a set of notifications when starting a virtualization instance.</span></span>

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

## <a name="receiving-notifications"></a><span data-ttu-id="783a1-122">Recibir notificaciones</span><span class="sxs-lookup"><span data-stu-id="783a1-122">Receiving Notifications</span></span>

<span data-ttu-id="783a1-123">ProjFS envía notificaciones de las operaciones del sistema de archivos llamando a la devolución de llamada del **PRJ_NOTIFICATION_CB** del proveedor.</span><span class="sxs-lookup"><span data-stu-id="783a1-123">ProjFS sends notifications of file system operations by calling the provider's **PRJ_NOTIFICATION_CB** callback.</span></span>  <span data-ttu-id="783a1-124">Lo hace para cada operación para la que el proveedor se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="783a1-124">It does this for each operation the provider has registered for.</span></span>  <span data-ttu-id="783a1-125">Si, como en el ejemplo anterior, el proveedor se registró para PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, y una aplicación creó un nuevo archivo en la raíz de la notificación, ProjFS llamaría a la devolución de llamada de **PRJ_NOTIFICATION_CB** con el nombre de la ruta de acceso del archivo nuevo y el parámetro de _notificación_ establecido en PRJ_NOTIFICATION_NEW_FILE_CREATED.</span><span class="sxs-lookup"><span data-stu-id="783a1-125">If, as in the above example, the provider registered for PRJ_NOTIFY_NEW_FILE_CREATED | PRJ_NOTIFY_FILE_OPENED | PRJ_NOTIFY_PRE_DELETE | PRJ_NOTIFY_FILE_HANDLE_CLOSED_FILE_DELETED | PRJ_NOTIFY_FILE_RENAMED, and an application created a new file in the notification root, ProjFS would call the **PRJ_NOTIFICATION_CB** callback with the new file's path name and the _notification_ parameter set to PRJ_NOTIFICATION_NEW_FILE_CREATED.</span></span>

<span data-ttu-id="783a1-126">ProjFS envía las notificaciones en la lista siguiente antes de que tenga lugar la operación de sistema de archivos asociada.</span><span class="sxs-lookup"><span data-stu-id="783a1-126">ProjFS sends the notifications in the following list before the associated file system operation takes place.</span></span>  <span data-ttu-id="783a1-127">Si el proveedor devuelve un código de error de la devolución de llamada **PRJ_NOTIFICATION_CB** , se producirá un error en la operación del sistema de archivos y se devolverá el código de error especificado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="783a1-127">If the provider returns a failure code from the **PRJ_NOTIFICATION_CB** callback, the file system operation will fail and return the failure code the provider specified.</span></span>

* <span data-ttu-id="783a1-128">PRJ_NOTIFICATION_PRE_DELETE: el archivo está a punto de eliminarse.</span><span class="sxs-lookup"><span data-stu-id="783a1-128">PRJ_NOTIFICATION_PRE_DELETE - The file is about to be deleted.</span></span>
* <span data-ttu-id="783a1-129">PRJ_NOTIFICATION_PRE_RENAME: se va a cambiar el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-129">PRJ_NOTIFICATION_PRE_RENAME - The file is about to be renamed.</span></span>
* <span data-ttu-id="783a1-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK: se va a crear un vínculo físico para el archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-130">PRJ_NOTIFICATION_PRE_SET_HARDLINK - A hard link is about to be created for the file.</span></span>
* <span data-ttu-id="783a1-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL: un archivo se va a expandir desde un marcador de posición a un archivo completo, lo que indica que es probable que se modifique su contenido.</span><span class="sxs-lookup"><span data-stu-id="783a1-131">PRJ_NOTIFICATION_FILE_PRE_CONVERT_TO_FULL - A file is about to be expanded from a placeholder to a full file, which indicates its contents are likely to be modified.</span></span>

<span data-ttu-id="783a1-132">ProjFS envía las notificaciones de la siguiente lista una vez finalizada la operación del sistema de archivos asociada.</span><span class="sxs-lookup"><span data-stu-id="783a1-132">ProjFS sends the notifications in the following list after the associated file system operation has completed.</span></span>

* <span data-ttu-id="783a1-133">PRJ_NOTIFICATION_FILE_OPENED: se ha abierto un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="783a1-133">PRJ_NOTIFICATION_FILE_OPENED - An existing file has been opened.</span></span>
  * <span data-ttu-id="783a1-134">Aunque esta notificación se envía una vez abierto el archivo, el proveedor puede devolver un código de error.</span><span class="sxs-lookup"><span data-stu-id="783a1-134">Even though this notification is sent after the file has been opened, the provider can return a failure code.</span></span>  <span data-ttu-id="783a1-135">En respuesta, ProjFS cancelará la apertura y devolverá el error al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="783a1-135">In response, ProjFS will cancel the open and return the failure to the caller.</span></span>
* <span data-ttu-id="783a1-136">PRJ_NOTIFICATION_NEW_FILE_CREATED: se ha creado un nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-136">PRJ_NOTIFICATION_NEW_FILE_CREATED - A new file has been created.</span></span>
* <span data-ttu-id="783a1-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN: se ha sobrescrito un archivo existente, por ejemplo llamando a [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) con la marca **CREATE_ALWAYS** _dwCreationDisposition_ .</span><span class="sxs-lookup"><span data-stu-id="783a1-137">PRJ_NOTIFICATION_FILE_OVERWRITTEN - An existing file has been overwritten, for example by calling [CreateFileW](/windows/desktop/api/fileapi/nf-fileapi-createfilew) with the **CREATE_ALWAYS** _dwCreationDisposition_ flag.</span></span>
* <span data-ttu-id="783a1-138">PRJ_NOTIFICATION_FILE_RENAMED: se ha cambiado el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-138">PRJ_NOTIFICATION_FILE_RENAMED - A file has been renamed.</span></span>
* <span data-ttu-id="783a1-139">PRJ_NOTIFICATION_HARDLINK_CREATED: se ha creado un [vínculo físico](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) para un archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-139">PRJ_NOTIFICATION_HARDLINK_CREATED - A [hard link](/windows/desktop/FileIO/hard-links-and-junctions#hard-links) has been created for a file.</span></span>
* <span data-ttu-id="783a1-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION: se ha cerrado un identificador de archivo y no se ha modificado el contenido del archivo, ni se ha eliminado el archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-140">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_NO_MODIFICATION - A file handle has been closed, and the file's content was not modified, nor was the file deleted.</span></span>
* <span data-ttu-id="783a1-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED: se ha cerrado un identificador de archivo y se ha modificado el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-141">PRJ_NOTIFICATION_FILE_HANLDE_CLOSED_FILE_MODIFIED - A file handle has been closed, and the file's content has been modified.</span></span>
* <span data-ttu-id="783a1-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED: se ha cerrado un identificador de archivo y el archivo se ha eliminado como parte del cierre del identificador.</span><span class="sxs-lookup"><span data-stu-id="783a1-142">PRJ_NOTIFICATION_FILE_HANDLE_CLOSED_FILE_DELETED - A file handle has been closed, and the file was deleted as part of closing the handle.</span></span>

<span data-ttu-id="783a1-143">Para obtener más información sobre cada notificación, consulte la documentación de **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span><span class="sxs-lookup"><span data-stu-id="783a1-143">For more details on each notification refer to the documentation for **[PRJ_NOTIFICATION](/windows/desktop/api/projectedfslib/ne-projectedfslib-prj_notification)**.</span></span>

<span data-ttu-id="783a1-144">El parámetro _notificationParameters_ de la devolución de llamada de **PRJ_NOTIFICATION_CB** especifica parámetros adicionales para ciertas notificaciones.</span><span class="sxs-lookup"><span data-stu-id="783a1-144">The **PRJ_NOTIFICATION_CB** callback's _notificationParameters_ parameter specifies extra parameters for certain notifications.</span></span>  <span data-ttu-id="783a1-145">Si un proveedor recibe una notificación PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED o PRJ_NOTIFICATION_FILE_OVERWRITTEN o PRJ_NOTIFICATION_FILE_RENAMED, el proveedor puede especificar un nuevo conjunto de notificaciones que se van a recibir para el archivo.</span><span class="sxs-lookup"><span data-stu-id="783a1-145">If a provider receives a PRJ_NOTIFICATION_FILE_OPENED, PRJ_NOTIFICATION_NEW_FILE_CREATED, or PRJ_NOTIFICATION_FILE_OVERWRITTEN, or PRJ_NOTIFICATION_FILE_RENAMED notification, the provider can specify a new set of notifications to receive for the file.</span></span> <span data-ttu-id="783a1-146">Para obtener más información, consulte la documentación de **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span><span class="sxs-lookup"><span data-stu-id="783a1-146">For further details, refer to the documentation for **[PRJ_NOTIFICATION_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_notification_cb)**.</span></span>

<span data-ttu-id="783a1-147">En el ejemplo siguiente se muestran ejemplos sencillos de cómo un proveedor puede procesar las notificaciones registradas para en el fragmento de código anterior.</span><span class="sxs-lookup"><span data-stu-id="783a1-147">The following sample shows simple examples of how a provider might process the notifications it registered for in the code snippet above.</span></span>

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