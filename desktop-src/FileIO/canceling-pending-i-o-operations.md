---
description: Permitir a los usuarios cancelar las solicitudes de e/s que son lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Cancelar operaciones de e/s pendientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688476"
---
# <a name="canceling-pending-io-operations"></a>Cancelar operaciones de e/s pendientes

Permitir a los usuarios cancelar las solicitudes de e/s que son lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación. Por ejemplo, si una llamada a la función [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) está bloqueada porque la llamada es a un dispositivo muy lento, al cancelarla se habilita la llamada para que se vuelva a realizar, con nuevos parámetros, sin terminar la aplicación.

Windows Vista extiende las capacidades de cancelación e incluye compatibilidad para cancelar las operaciones sincrónicas.

**Nota:**  La llamada a la función [**CancelIoEx**](cancelioex-func.md) no garantiza que se cancele una operación de e/s; el controlador que controla la operación debe admitir la cancelación y la operación debe estar en un estado que se pueda cancelar.

## <a name="cancellation-considerations"></a>Consideraciones de cancelación

Al programar llamadas de cancelación, tenga en cuenta las consideraciones siguientes:

-   No hay ninguna garantía de que los controladores subyacentes admitan correctamente la cancelación.
-   Al cancelar la e/s asincrónica, cuando no se proporciona ninguna estructura superpuesta a la función [**CancelIoEx**](cancelioex-func.md) , la función intenta cancelar todas las e/s pendientes en el archivo en todos los subprocesos del proceso. Cada subproceso se procesa individualmente, de modo que, una vez procesado el subproceso, puede iniciar otra e/s en el archivo antes de que todos los demás subprocesos hayan cancelado su e/s para el archivo, lo que provocaría problemas de sincronización.
-   Al cancelar la e/s asincrónica, no reutilice las estructuras superpuestas con cancelación de destino. Una vez completada la operación de e/s (ya sea correctamente o con un estado cancelado), el sistema ya no usa la estructura superpuesta y se puede volver a usar.
-   Al cancelar la e/s sincrónica, al llamar a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) se intenta cancelar cualquier llamada sincrónica actual en el subproceso. Debe tener cuidado para asegurarse de que la sincronización de las llamadas sea correcta; la llamada incorrecta en una serie de llamadas podría cancelarse. Por ejemplo, si se llama a la función **CancelSynchronousIo** para una operación sincrónica, x, la operación Y solo se inicia después de que se complete la operación x (normalmente o con un error). Si el subproceso que llamó a la operación X inicia otra llamada sincrónica a X, la llamada de cancelación podría interrumpir esta nueva solicitud de e/s.
-   Al cancelar la e/s sincrónica, tenga en cuenta que puede existir una condición de carrera siempre que un subproceso se comparta entre diferentes partes de una aplicación, por ejemplo, con un subproceso de grupo de subprocesos.

## <a name="operations-that-cannot-be-canceled"></a>Operaciones que no se pueden cancelar

Algunas funciones no se pueden cancelar con la función [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)o [**CancelSynchronousIo**](cancelsynchronousio-func.md) . Algunas de estas funciones se han ampliado para permitir la cancelación (por ejemplo, la función [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) y debe utilizarlas en su lugar. Además de admitir la cancelación, estas funciones también tienen devoluciones de llamada integradas que le permiten realizar un seguimiento del progreso de la operación. Las siguientes funciones no admiten la cancelación:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile): usar [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile): uso de [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa): use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Para obtener más información, vea [instrucciones de finalización/cancelación de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

## <a name="canceling-asynchronous-io"></a>Cancelar la e/s asincrónica

Puede cancelar la e/s asincrónica desde cualquier subproceso del proceso que emitió la operación de e/s. Debe especificar el identificador en el que se realizó la e/s y, opcionalmente, la estructura superpuesta que se usó para realizar la e/s. Puede determinar si se ha producido la cancelación examinando el estado devuelto en la estructura superpuesta o en la devolución de llamada de finalización. Un estado de **error de \_ operación \_ anulada** indica que la operación se canceló.

En el ejemplo siguiente se muestra una rutina que toma un tiempo de espera e intenta una operación de lectura y la cancela con la función [**CancelIoEx**](cancelioex-func.md) si el tiempo de espera expira.


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a>Cancelar e/s sincrónicas

Puede cancelar la e/s sincrónica desde cualquier subproceso del proceso que emitió la operación de e/s. Debe especificar el identificador del subproceso que está realizando actualmente la operación de e/s.

En el ejemplo siguiente se muestran dos rutinas:

-   La función **SynchronousIoWorker** es un subproceso de trabajo que implementa una e/s sincrónica de archivos, comenzando por una llamada a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Si la rutina se realiza correctamente, la rutina puede ir seguida de operaciones adicionales, que no se incluyen aquí. La variable global *gCompletionStatus* se puede usar para determinar si todas las operaciones se han realizado correctamente o si se ha producido un error en una operación o se ha cancelado. La variable global *dwOperationInProgress* indica si la e/s de archivos aún está en curso.

    **Nota:**  En este ejemplo, el subproceso de interfaz de usuario también podría comprobar la existencia del subproceso de trabajo.

    Las comprobaciones manuales adicionales, que no se incluyen aquí, son necesarias en la función **SynchronousIoWorker** es para asegurarse de que, si se solicitó la cancelación durante los breves períodos entre las llamadas de e/s de archivo, se cancelará el resto de las operaciones.

-   La función **MainUIThreadMessageHandler** simula el controlador de mensajes dentro del procedimiento de ventana de un subproceso de interfaz de usuario. El usuario solicita un conjunto de operaciones de archivos sincrónicos haciendo clic en un control, que genera un mensaje de ventana definido por el usuario (en la sección marcada por **WM \_ MYSYNCOPS**). Esto crea un nuevo subproceso mediante la función **CreateFileThread** , que luego inicia la función **SynchronousIoWorker** es. El subproceso de la interfaz de usuario continúa procesando mensajes mientras el subproceso de trabajo realiza la e/s solicitada. Si el usuario decide cancelar las operaciones sin finalizar (normalmente al hacer clic en un botón Cancelar), la rutina (en la sección marcada por **WM \_ OnCancel**) llama a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) con el identificador de subproceso devuelto por la función **CreateFileThread** . La función **CancelSynchronousIo** se devuelve inmediatamente después del intento de cancelación. Por último, el usuario o la aplicación puede solicitar posteriormente otra operación que depende de si las operaciones de archivo se han completado. En este caso, la rutina (en la sección marcada por **WM \_ PROCESSDATA**) comprueba primero que las operaciones se han completado y, a continuación, ejecuta las operaciones de limpieza.

    **Nota:**  En este ejemplo, como la cancelación podría haber tenido lugar en la secuencia de operaciones, puede ser necesario que el autor de la llamada garantice que el estado es coherente, o al menos entendido, antes de continuar.


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[E/s sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



