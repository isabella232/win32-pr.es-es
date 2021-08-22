---
description: Permitir a los usuarios cancelar solicitudes de E/S lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Cancelación de operaciones de E/S pendientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ca0f938420888934dccb28c9837bdff5dd8515bbdeeb1b3acf4078ae558ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534133"
---
# <a name="canceling-pending-io-operations"></a>Cancelación de operaciones de E/S pendientes

Permitir a los usuarios cancelar solicitudes de E/S lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación. Por ejemplo, si se bloquea una llamada a la función [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) porque la llamada es a un dispositivo muy lento, cancelarla permite que la llamada se vuelva a realizar, con nuevos parámetros, sin terminar la aplicación.

Windows Vista amplía las funcionalidades de cancelación e incluye compatibilidad para cancelar operaciones sincrónicas.

**Nota**  Llamar a [**la función CancelIoEx**](cancelioex-func.md) no garantiza que se cancele una operación de E/S; El controlador que está controlando la operación debe admitir la cancelación y la operación debe estar en un estado que se pueda cancelar.

## <a name="cancellation-considerations"></a>Consideraciones de cancelación

Al programar llamadas de cancelación, tenga en cuenta las siguientes consideraciones:

-   No hay ninguna garantía de que los controladores subyacentes admitan correctamente la cancelación.
-   Al cancelar la E/S asincrónica, cuando no se proporciona ninguna estructura superpuesta a la función [**CancelIoEx,**](cancelioex-func.md) la función intenta cancelar todas las E/S pendientes en el archivo en todos los subprocesos del proceso. Cada subproceso se procesa individualmente, por lo que una vez procesado un subproceso, puede iniciar otra E/S en el archivo antes de que todos los demás subprocesos hayan cancelado su E/S para el archivo, lo que provoca problemas de sincronización.
-   Al cancelar E/S asincrónica, no reutilice estructuras superpuestas con cancelación de destino. Una vez completada la operación de E/S (ya sea correctamente o con un estado cancelado), el sistema deja de usar la estructura superpuesta y se puede reutilizar.
-   Al cancelar la E/S sincrónica, la llamada a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) intenta cancelar cualquier llamada sincrónica actual en el subproceso. Debe tener cuidado para asegurarse de que la sincronización de las llamadas es correcta; la llamada incorrecta en una serie de llamadas podría cancelarse. Por ejemplo, si se llama a la función **CancelSynchronousIo** para una operación sincrónica, X, la operación Y solo se inicia una vez completada la operación X (normalmente o con un error). Si el subproceso que llamó a la operación X inicia otra llamada sincrónica a X, la llamada de cancelación podría interrumpir esta nueva solicitud de E/S.
-   Al cancelar la E/S sincrónica, tenga en cuenta que puede existir una condición de carrera siempre que un subproceso se comparta entre diferentes partes de una aplicación, por ejemplo, con un subproceso del grupo de subprocesos.

## <a name="operations-that-cannot-be-canceled"></a>Operaciones que no se pueden cancelar

Algunas funciones no se pueden cancelar mediante la [**función CancelIo,**](cancelio.md) [**CancelIoEx**](cancelioex-func.md)o [**CancelSynchronousIo.**](cancelsynchronousio-func.md) Algunas de estas funciones se han ampliado para permitir la cancelación (por ejemplo, la [**función CopyFileEx)**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) y debe usarlas en su lugar. Además de admitir la cancelación, estas funciones también tienen devoluciones de llamada integradas que le ayudarán a realizar el seguimiento del progreso de la operación. Las siguientes funciones no admiten la cancelación:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile): use [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile): use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa): use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Para obtener más información, vea [Instrucciones de cancelación/finalización de E/S.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

## <a name="canceling-asynchronous-io"></a>Cancelación de E/S asincrónica

Puede cancelar la E/S asincrónica desde cualquier subproceso del proceso que emitió la operación de E/S. Debe especificar el identificador en el que se realizó la E/S y, opcionalmente, la estructura superpuesta que se usó para realizar la E/S. Puede determinar si la cancelación se ha producido examinando el estado devuelto en la estructura superpuesta o en la devolución de llamada de finalización. El estado **ERROR \_ OPERATION \_ ABORTED** indica que se canceló la operación.

En el ejemplo siguiente se muestra una rutina que toma un tiempo de espera e intenta una operación de lectura, cancelándose con la [**función CancelIoEx**](cancelioex-func.md) si expira el tiempo de espera.


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



## <a name="canceling-synchronous-io"></a>Cancelación de E/S sincrónica

Puede cancelar la E/S sincrónica desde cualquier subproceso del proceso que emitió la operación de E/S. Debe especificar el identificador para el subproceso que está realizando actualmente la operación de E/S.

En el ejemplo siguiente se muestran dos rutinas:

-   La **función SynchronousIoWorker** es un subproceso de trabajo que implementa alguna E/S de archivo sincrónica, empezando por una llamada a la [**función CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Si la rutina es correcta, la rutina puede ir seguida de operaciones adicionales, que no se incluyen aquí. La variable global *gCompletionStatus* se puede usar para determinar si todas las operaciones se realizaron correctamente o si se ha cancelado o no una operación. La variable global *dwOperationInProgress* indica si la E/S de archivo todavía está en curso.

    **Nota**  En este ejemplo, el subproceso de interfaz de usuario también podría comprobar la existencia del subproceso de trabajo.

    Se requieren comprobaciones manuales adicionales, que no se incluyen aquí, en la función **SynchronousIoWorker** para asegurarse de que si se solicitó la cancelación durante los breves períodos entre las llamadas de E/S de archivo, se cancelarán el resto de las operaciones.

-   La **función MainUIThreadMessageHandler** simula el controlador de mensajes dentro del procedimiento de ventana de un subproceso de interfaz de usuario. El usuario solicita un conjunto de operaciones de archivo sincrónicas haciendo clic en un control , que genera un mensaje de ventana definido por el usuario ( en la sección marcada por **WM \_ MYSYNCOPS**). Esto crea un nuevo subproceso mediante la **función CreateFileThread,** que luego inicia la función **SynchronousIoWorker.** El subproceso de interfaz de usuario continúa procesando mensajes mientras el subproceso de trabajo realiza la E/S solicitada. Si el usuario decide cancelar las operaciones inconclusas (normalmente haciendo clic en un botón Cancelar), la rutina (en la sección marcada por **WM \_ MYCANCEL)** llama a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) mediante el identificador de subproceso devuelto por la **función CreateFileThread.** La **función CancelSynchronousIo** se devuelve inmediatamente después del intento de cancelación. Por último, el usuario o la aplicación pueden solicitar más adelante alguna otra operación que dependa de si se han completado las operaciones de archivo. En este caso, la rutina (en la sección marcada por **WM \_ PROCESSDATA)** comprueba primero que las operaciones se han completado y, a continuación, ejecuta las operaciones de limpieza.

    **Nota**  En este ejemplo, dado que la cancelación podría haber tenido lugar en cualquier parte de la secuencia de operaciones, puede ser necesario que el autor de la llamada se asegure de que el estado es coherente o, al menos, se entiende antes de continuar.


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

[E/S sincrónica y asincrónica](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



