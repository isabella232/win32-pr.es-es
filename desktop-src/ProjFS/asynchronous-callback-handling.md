---
title: Finalización de devolución de llamada asincrónica
description: Describe cómo el proveedor puede atender las devoluciones de llamada de forma asincrónica.
ms.assetid: <GUID-GOES-HERE>
ms.date: 10/12/2018
ms.topic: article
ms.openlocfilehash: 8ec23f5ea6e8ec55be2eaa2811d9dee8b1870edc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676465"
---
# <a name="asynchronous-callback-handling"></a>Control asincrónico de devolución de llamada

Cuando un cliente interactúa con los archivos y directorios situados debajo de la raíz de virtualización del proveedor, estas interacciones suelen dar lugar a que se invoquen las devoluciones de llamada del proveedor.  ProjFS invoca devoluciones de llamada de proveedor mediante el envío de un mensaje desde el modo kernel a la biblioteca de modo de usuario ProjFS, donde un subproceso de trabajo recibe el mensaje y llama a la devolución de llamada adecuada.  Una vez devuelta la devolución de llamada, el subproceso de trabajo espera a que llegue otro mensaje desde el modo kernel.  Si todos los subprocesos de trabajo están ocupados ejecutando el código de devolución de llamada del proveedor, cualquier e/s de cliente que desencadene una devolución de llamada se bloquea hasta que un subproceso de trabajo esté disponible para recibir el mensaje e invocar la devolución de llamada pertinente.  Cuando se inicia un proveedor, puede especificar el número de subprocesos de trabajo que desea que ProjFS cree en las devoluciones de llamada de servicio mediante el parámetro _Options_ de **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)**.  Un proveedor puede mejorar la eficacia de los subprocesos de trabajo de recepción de mensajes mediante el mantenimiento de sus devoluciones de llamada de forma asincrónica.

> Si el proveedor no especifica el parámetro _Options_ para **PrjStartVirtualizing**, o si especifica 0 para el miembro ConcurrentThreadCount del parámetro _Options_ , ProjFS usará el número de procesadores lógicos del sistema para el valor de ConcurrentThreadCount.
>
> Si el proveedor no especifica el parámetro _Options_ para **PrjStartVirtualizing**, o si especifica 0 para el miembro PoolThreadCount del parámetro _Options_ , ProjFS usará dos veces el valor de ConcurrentThreadCount para el valor de PoolThreadCount.

Un proveedor devuelve las devoluciones de llamada de forma asincrónica mediante la devolución de HRESULT_FROM_WIN32 (ERROR_IO_PENDING) de sus devoluciones de llamada y, posteriormente, su finalización con **[PrjCompleteCommand](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjcompletecommand)**.  Un proveedor que procesa las devoluciones de llamada de forma asincrónica también debe admitir la cancelación de devolución de llamada implementando el **[PRJ_CANCEL_COMMAND_CB](/windows/desktop/api/projectedfslib/nc-projectedfslib-prj_cancel_command_cb)** devolución de llamada.

Cuando ProjFS llama a la devolución de llamada de un proveedor, identifica la invocación específica de la devolución de llamada mediante el miembro CommandID del parámetro _callbackData_ de la devolución de llamada.  Si el proveedor decide procesar esa devolución de llamada de forma asincrónica, debe almacenar el valor del miembro CommandID y devolver HRESULT_FROM_WIN32 (ERROR_IO_PENDING) de la devolución de llamada.  Una vez que el proveedor ha terminado de procesar la devolución de llamada, llama a **PrjCompleteCommand**, pasando el identificador almacenado en el parámetro _CommandID_ .  Esto indica a ProjFS qué invocación de devolución de llamada se ha completado.

Un proveedor que implementa la devolución de llamada de **PRJ_CANCEL_COMMAND_CB** debe realizar un seguimiento de las devoluciones de llamada que todavía no se han completado.  Si el proveedor recibe esta devolución de llamada, indica que se ha cancelado la e/s que causó una de esas devoluciones de llamada, ya sea de forma explícita o porque el subproceso que se emitió ha finalizado. El proveedor debe cancelar el procesamiento de la invocación de devolución de llamada identificada por CommandID lo antes posible.

> Aunque ProjFS invocará **PRJ_CANCEL_COMMAND_CB** para un determinado CommandID solo después de que se invoque la devolución de llamada que se va a cancelar, la cancelación y la invocación original pueden ejecutarse simultáneamente en un proveedor multiproceso.  El proveedor debe ser capaz de controlar correctamente esta situación.

El ejemplo siguiente es una versión del ejemplo que se proporciona para el tema [enumeración de archivos y directorios](enumerating-files-and-directories.md) , modificado para ilustrar el control de devolución de llamada asincrónica.

```C++
typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

typedef struct MY_ENUM_ENTRY {
    MY_ENUM_ENTRY* Next;
    PWSTR Name;
    BOOLEAN IsDirectory;
    INT64 FileSize;
} MY_ENUM_ENTRY;

typedef struct MY_ENUM_SESSION {
    GUID EnumerationId;
    PWSTR SearchExpression;
    USHORT SearchExpressionMaxLen;
    BOOLEAN SearchExpressionCaptured;
    MY_ENUM_ENTRY* EnumHead;
    MY_ENUM_ENTRY* LastEnumEntry;
    BOOLEAN EnumCompleted;
} MY_ENUM_SESSION;

typedef struct MY_ENUM_PARAMS {
    GUID EnumerationId;
    PRJ_DIR_ENTRY_BUFFER_HANDLE DirEntryBufferHandle;
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT NamespaceVirtualizationContext;
    INT32 CommandId;
    PRJ_CALLBACK_DATA_FLAGS Flags;
    WCHAR SearchExpression[1];
} MY_ENUM_PARAMS;

// Prototype for the enumeration worker routine.  In this example this is a
// ThreadProc.  See https://msdn.microsoft.com/library/windows/desktop/ms686736.aspx
DWORD WINAPI MyGetEnumCallbackWorker(_In_ LPVOID parameter);

#define ROLLBACK_NONE           0
#define ROLLBACK_PARAM_ALLOC    1
#define ROLLBACK_TRACK_ENUM     2

HRESULT
MyGetEnumCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData,
    _In_ const GUID* enumerationId,
    _In_opt_z_ PCWSTR searchExpression,
    _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
    )
{
    UINT rollback = ROLLBACK_NONE;

    // This example creates a thread to run the enumeration in.  The provider
    // can access callbackData only while the callback is running, so we copy
    // out the fields that the worker thread will need.
    MY_ENUM_PARAMS* enumParams = NULL;
    size_t bufSize = sizeof(MY_ENUM_PARAMS);

    // Allocate enough space for the parameter buffer and the search expression
    // string plus a terminating NULL character.
    if (searchExpression != NULL)
    {
        bufSize += (wcslen(searchExpression) + 1) * sizeof(WCHAR);
    }
    else
    {
        // We'll store "*" as the search expression in this case.
        bufSize += 2 * sizeof(WCHAR);
    }

    enumParams = (MY_ENUM_PARAMS*) calloc(1, bufSize);

    if (enumParams == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // enumParams allocated.
    rollback = ROLLBACK_PARAM_ALLOC;

    // Copy the search expression into our parameter buffer.
    if (searchExpression != NULL)
    {
        wcsncpy_s(enumParams->SearchExpression,
                  wcslen(searchExpression),
                  searchExpression,
                  wcslen(searchExpression));
    }
    else
    {
        wcsncpy_s(enumParams->SearchExpression, 1, "*", 1);
    }

    // Copy the other parameters into our parameter buffer.
    enumParams->EnumerationId = enumerationId;
    enumParams->DirEntryBufferHandle = dirEntryBufferHandle;
    enumParams->NamespaceVirtualizationContext = callbackData->NamespaceVirtualizationContext
    enumParams->CommandId = callbackData->CommandId;
    enumParams->Flags = callbackData->Flags;

    // MyTrackEnumForCancellation is a routine the provider might implement to
    // track active enumeration callbacks in case they are cancelled.  It stores
    // the CommandId for the callback in some structure.
    hr = MyTrackEnumForCancellation(callbackData->CommandId);

    if (FAILED(hr))
    {
        goto RollbackOnError;
    }

    // Enum callback tracked.
    rollback = ROLLBACK_TRACK_ENUM;

    // Create the worker thread.
    HANDLE workerThread = NULL;
    workerThread = CreateThread(NULL,
                                0,
                                MyGetEnumCallbackWorker,
                                enumParams,
                                0
                                NULL);

    // We'll treat failure to create the thread as a low-resources error.
    if (workerThread == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto RollbackOnError;
    }

    // Return pending to signal that we'll complete the enumeration later.
    return HRESULT_FROM_WIN32(ERROR_IO_PENDING);

RollbackOnError:

    // Clean up manually.  Note the fall-through structure of the switch, and that
    // we clean up in reverse order.
    switch(rollback)
    {
    case ROLLBACK_TRACK_ENUM:
        // MyUntrackEnumForCancellation removes the CommandId for the callback
        // from the structure that MyTrackEnumForCancellation put it in.
        MyUntrackEnumForCancellation(callbackData->CommandId);

    case ROLLBACK_PARAM_ALLOC:
        free(enumParams);

    default:
        break;
    }

    return hr;
}

DWORD
WINAPI
MyGetEnumCallbackWorker(
    _In_ LPVOID parameter
)
{
    HRESULT hr = S_OK;
    MY_ENUM_PARAMS* enumParams = (MY_ENUM_PARAMS*) parameter;

    // MyCheckEnumForCancellation is a routine the provider might implement to
    // check whether a pended enumeration callback has been cancelled.  Even
    // though the enumeration has been cancelled, ProjFS will still call the
    // provider's end-enumeration callback.  This allows general cleanup, such
    // as tearing down the enumeration session, to always happen in that callback.
    if (MyCheckEnumForCancellation(enumParams->CommandId))
    {
        // The operation has been cancelled.  Clean up and get out.
        free(enumParams);
        return 0;
    }

    // MyGetEnumSession is a routine the provider might implement to find
    // information about the enumeration session that it first stored
    // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
    //
    // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
    // already retrieved a list of the items in the backing store located at
    // callbackData->FilePathName, sorted them using PrjFileNameCompare()
    // to determine collation order, and stored the list in session->EnumHead.
    MY_ENUM_SESSION* session = NULL;
    session = MyGetEnumSession(enumParams->EnumerationId);

    if (session == NULL)
    {
        hr = HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        goto CompleteCallback;
    }

    if (!session->SearchExpressionCaptured ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        if (wcsncpy_s(session->SearchExpression,
                      session->SearchExpressionMaxLen,
                      enumParams->SearchExpression,
                      wcslen(enumParams->SearchExpression)))
        {
            // Failed to copy the search expression; perhaps the provider
            // could try reallocating session->SearchExpression.
        }

        session->SearchExpressionCaptured = TRUE;
    }

    MY_ENUM_ENTRY* enumHead = NULL;

    // We have to start the enumeration from the beginning if we aren't
    // continuing an existing session or if the caller is requesting a restart.
    if (((session->LastEnumEntry == NULL) &&
         !session->EnumCompleted) ||
        (enumParams->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
    {
        // Ensure that if the caller is requesting a restart we reset our
        // bookmark of how far we got in the enumeration.
        session->LastEnumEntry = NULL;

        // In case we're restarting ensure we don't think we're done.
        session->EnumCompleted = FALSE;

        // We need to start considering items from the beginning of the list
        // retrieved from the backing store.
        enumHead = session->EnumHead;
    }
    else
    {
        // We are resuming an existing enumeration session.  Note that
        // session->LastEnumEntry may be NULL.  That is okay; it means
        // we got all the entries the last time this callback was invoked.
        // Returning S_OK without adding any new entries to the
        // enumParams->DirEntryBufferHandle buffer signals ProjFS that the
        // enumeration has returned everything it can.
        enumHead = session->LastEnumEntry;
    }

    if (enumHead == NULL)
    {
        // There are no items to return.  Remember that we've returned everything
        // we can.
        session->EnumCompleted = TRUE;
    }
    else
    {
        MY_ENUM_ENTRY* thisEntry = enumHead;
        while (thisEntry != NULL)
        {
            // We'll insert the entry into the return buffer if it matches
            // the search expression captured for this enumeration session.
            if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
            {
                PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                fileBasicInfo.FileSize = thisEntry->FileSize;

                // Format the entry for return to ProjFS.
                if (S_OK != PrjFillDirEntryBuffer(thisEntry->Name,
                                                  &fileBasicInfo,
                                                  enumParams->DirEntryBufferHandle))
                {
                    // We couldn't add this entry to the buffer; remember where we left
                    // off for the next time we're called for this enumeration session.
                    session->LastEnumEntry = thisEntry;
                    hr = S_OK;

                    goto CompleteCallback;
                }
            }

            thisEntry = thisEntry->Next;
        }

        // We reached the end of the list of entries; remember that we've returned
        // everything we can.
        session->EnumCompleted = TRUE;
    }

CompleteCallback:

    // Signal ProjFS that we've completed this callback.  Since this is an enumeration
    // we use the extendedParameters parameter to PrjCompleteCommand.
    PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS extendedParams = {};
    extendedParams.CommandType = PRJ_COMPLETE_COMMAND_TYPE_ENUMERATION;
    extendedParams.enumeration.DirEntryBufferHandle = enumParams->DirEntryBufferHandle;

    PrjCompleteCommand(enumParams->NamespaceVirtualizationContext,
                       enumParams->CommandId,
                       hr,
                       &extendedParams);

    MyUntrackEnumForCancellation(enumParams->CommandId);

    free(enumParams);

    // ThreadProc returns 0 on successful completion.
    return 0;
}
```

Y este es un breve ejemplo PRJ_CANCEL_COMMAND_CB que funciona con el código de ejemplo anterior.

```C++
void
MyCancelCommandCallback(
    _In_ const PRJ_CALLBACK_DATA* callbackData
)
{
    // MyMarkEnumForCancellation is a routine the provider might implement to
    // mark a pended enumeration callback as cancelled.  If the given CommandId
    // is not found, it is not an error.  It may not yet have been tracked or
    // it may already have completed and been untracked.
    MyMarkEnumForCancellation(callbackData->CommandId);
}
```