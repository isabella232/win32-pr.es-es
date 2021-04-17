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
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="ccfc6-103">Cancelar operaciones de e/s pendientes</span><span class="sxs-lookup"><span data-stu-id="ccfc6-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="ccfc6-104">Permitir a los usuarios cancelar las solicitudes de e/s que son lentas o bloqueadas puede mejorar la facilidad de uso y la solidez de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="ccfc6-105">Por ejemplo, si una llamada a la función [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) está bloqueada porque la llamada es a un dispositivo muy lento, al cancelarla se habilita la llamada para que se vuelva a realizar, con nuevos parámetros, sin terminar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="ccfc6-106">Windows Vista extiende las capacidades de cancelación e incluye compatibilidad para cancelar las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="ccfc6-107">**Nota:**  La llamada a la función [**CancelIoEx**](cancelioex-func.md) no garantiza que se cancele una operación de e/s; el controlador que controla la operación debe admitir la cancelación y la operación debe estar en un estado que se pueda cancelar.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="ccfc6-108">Consideraciones de cancelación</span><span class="sxs-lookup"><span data-stu-id="ccfc6-108">Cancellation Considerations</span></span>

<span data-ttu-id="ccfc6-109">Al programar llamadas de cancelación, tenga en cuenta las consideraciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="ccfc6-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="ccfc6-110">No hay ninguna garantía de que los controladores subyacentes admitan correctamente la cancelación.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="ccfc6-111">Al cancelar la e/s asincrónica, cuando no se proporciona ninguna estructura superpuesta a la función [**CancelIoEx**](cancelioex-func.md) , la función intenta cancelar todas las e/s pendientes en el archivo en todos los subprocesos del proceso.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="ccfc6-112">Cada subproceso se procesa individualmente, de modo que, una vez procesado el subproceso, puede iniciar otra e/s en el archivo antes de que todos los demás subprocesos hayan cancelado su e/s para el archivo, lo que provocaría problemas de sincronización.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="ccfc6-113">Al cancelar la e/s asincrónica, no reutilice las estructuras superpuestas con cancelación de destino.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="ccfc6-114">Una vez completada la operación de e/s (ya sea correctamente o con un estado cancelado), el sistema ya no usa la estructura superpuesta y se puede volver a usar.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="ccfc6-115">Al cancelar la e/s sincrónica, al llamar a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) se intenta cancelar cualquier llamada sincrónica actual en el subproceso.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="ccfc6-116">Debe tener cuidado para asegurarse de que la sincronización de las llamadas sea correcta; la llamada incorrecta en una serie de llamadas podría cancelarse.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="ccfc6-117">Por ejemplo, si se llama a la función **CancelSynchronousIo** para una operación sincrónica, x, la operación Y solo se inicia después de que se complete la operación x (normalmente o con un error).</span><span class="sxs-lookup"><span data-stu-id="ccfc6-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="ccfc6-118">Si el subproceso que llamó a la operación X inicia otra llamada sincrónica a X, la llamada de cancelación podría interrumpir esta nueva solicitud de e/s.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="ccfc6-119">Al cancelar la e/s sincrónica, tenga en cuenta que puede existir una condición de carrera siempre que un subproceso se comparta entre diferentes partes de una aplicación, por ejemplo, con un subproceso de grupo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="ccfc6-120">Operaciones que no se pueden cancelar</span><span class="sxs-lookup"><span data-stu-id="ccfc6-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="ccfc6-121">Algunas funciones no se pueden cancelar con la función [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)o [**CancelSynchronousIo**](cancelsynchronousio-func.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfc6-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="ccfc6-122">Algunas de estas funciones se han ampliado para permitir la cancelación (por ejemplo, la función [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) y debe utilizarlas en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="ccfc6-123">Además de admitir la cancelación, estas funciones también tienen devoluciones de llamada integradas que le permiten realizar un seguimiento del progreso de la operación.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="ccfc6-124">Las siguientes funciones no admiten la cancelación:</span><span class="sxs-lookup"><span data-stu-id="ccfc6-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="ccfc6-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile): usar [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="ccfc6-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="ccfc6-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile): uso de [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="ccfc6-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="ccfc6-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa): use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="ccfc6-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="ccfc6-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="ccfc6-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="ccfc6-129">Para obtener más información, vea [instrucciones de finalización/cancelación de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="ccfc6-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="ccfc6-130">Cancelar la e/s asincrónica</span><span class="sxs-lookup"><span data-stu-id="ccfc6-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="ccfc6-131">Puede cancelar la e/s asincrónica desde cualquier subproceso del proceso que emitió la operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="ccfc6-132">Debe especificar el identificador en el que se realizó la e/s y, opcionalmente, la estructura superpuesta que se usó para realizar la e/s.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="ccfc6-133">Puede determinar si se ha producido la cancelación examinando el estado devuelto en la estructura superpuesta o en la devolución de llamada de finalización.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="ccfc6-134">Un estado de **error de \_ operación \_ anulada** indica que la operación se canceló.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="ccfc6-135">En el ejemplo siguiente se muestra una rutina que toma un tiempo de espera e intenta una operación de lectura y la cancela con la función [**CancelIoEx**](cancelioex-func.md) si el tiempo de espera expira.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


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



## <a name="canceling-synchronous-io"></a><span data-ttu-id="ccfc6-136">Cancelar e/s sincrónicas</span><span class="sxs-lookup"><span data-stu-id="ccfc6-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="ccfc6-137">Puede cancelar la e/s sincrónica desde cualquier subproceso del proceso que emitió la operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="ccfc6-138">Debe especificar el identificador del subproceso que está realizando actualmente la operación de e/s.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="ccfc6-139">En el ejemplo siguiente se muestran dos rutinas:</span><span class="sxs-lookup"><span data-stu-id="ccfc6-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="ccfc6-140">La función **SynchronousIoWorker** es un subproceso de trabajo que implementa una e/s sincrónica de archivos, comenzando por una llamada a la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="ccfc6-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="ccfc6-141">Si la rutina se realiza correctamente, la rutina puede ir seguida de operaciones adicionales, que no se incluyen aquí.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="ccfc6-142">La variable global *gCompletionStatus* se puede usar para determinar si todas las operaciones se han realizado correctamente o si se ha producido un error en una operación o se ha cancelado.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="ccfc6-143">La variable global *dwOperationInProgress* indica si la e/s de archivos aún está en curso.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="ccfc6-144">**Nota:**  En este ejemplo, el subproceso de interfaz de usuario también podría comprobar la existencia del subproceso de trabajo.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="ccfc6-145">Las comprobaciones manuales adicionales, que no se incluyen aquí, son necesarias en la función **SynchronousIoWorker** es para asegurarse de que, si se solicitó la cancelación durante los breves períodos entre las llamadas de e/s de archivo, se cancelará el resto de las operaciones.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="ccfc6-146">La función **MainUIThreadMessageHandler** simula el controlador de mensajes dentro del procedimiento de ventana de un subproceso de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="ccfc6-147">El usuario solicita un conjunto de operaciones de archivos sincrónicos haciendo clic en un control, que genera un mensaje de ventana definido por el usuario (en la sección marcada por **WM \_ MYSYNCOPS**).</span><span class="sxs-lookup"><span data-stu-id="ccfc6-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="ccfc6-148">Esto crea un nuevo subproceso mediante la función **CreateFileThread** , que luego inicia la función **SynchronousIoWorker** es.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="ccfc6-149">El subproceso de la interfaz de usuario continúa procesando mensajes mientras el subproceso de trabajo realiza la e/s solicitada.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="ccfc6-150">Si el usuario decide cancelar las operaciones sin finalizar (normalmente al hacer clic en un botón Cancelar), la rutina (en la sección marcada por **WM \_ OnCancel**) llama a la función [**CancelSynchronousIo**](cancelsynchronousio-func.md) con el identificador de subproceso devuelto por la función **CreateFileThread** .</span><span class="sxs-lookup"><span data-stu-id="ccfc6-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="ccfc6-151">La función **CancelSynchronousIo** se devuelve inmediatamente después del intento de cancelación.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="ccfc6-152">Por último, el usuario o la aplicación puede solicitar posteriormente otra operación que depende de si las operaciones de archivo se han completado.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="ccfc6-153">En este caso, la rutina (en la sección marcada por **WM \_ PROCESSDATA**) comprueba primero que las operaciones se han completado y, a continuación, ejecuta las operaciones de limpieza.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="ccfc6-154">**Nota:**  En este ejemplo, como la cancelación podría haber tenido lugar en la secuencia de operaciones, puede ser necesario que el autor de la llamada garantice que el estado es coherente, o al menos entendido, antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="ccfc6-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ccfc6-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ccfc6-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccfc6-156">E/s sincrónica y asincrónica</span><span class="sxs-lookup"><span data-stu-id="ccfc6-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



