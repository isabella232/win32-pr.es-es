---
description: En este tema se describe cómo iniciar y detener el subproceso de procesamiento del trabajo de impresión.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Cómo: iniciar y detener un subproceso de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279029"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="72344-103">Cómo: iniciar y detener un subproceso de impresión</span><span class="sxs-lookup"><span data-stu-id="72344-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="72344-104">En este tema se describe cómo iniciar y detener el subproceso de procesamiento del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="72344-105">Información general</span><span class="sxs-lookup"><span data-stu-id="72344-105">Overview</span></span>

<span data-ttu-id="72344-106">Para evitar que las actividades de impresión bloqueen la respuesta de la interfaz de usuario, cree un subproceso independiente para procesar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="72344-107">El subproceso que se inicia cuando se inicia el programa, es el subproceso que controla los mensajes de ventana que resultan de la interacción del usuario y, por tanto, es el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="72344-108">El programa debe procesar estos mensajes sin retraso para que la interfaz de usuario responda a la entrada del teclado y del mouse del usuario de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="72344-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="72344-109">Para que el programa pueda responder a estos mensajes rápidamente, se limita la cantidad de procesamiento que se puede realizar durante cualquier mensaje.</span><span class="sxs-lookup"><span data-stu-id="72344-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="72344-110">Cuando una solicitud de usuario requiere un procesamiento extensivo, un subproceso diferente debe realizar ese procesamiento para permitir que el programa controle la interacción posterior del usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="72344-111">El procesamiento de datos en un subproceso independiente requiere que el programa coordine el funcionamiento del subproceso de la interfaz de usuario y el subproceso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="72344-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="72344-112">Por ejemplo, mientras el subproceso de procesamiento está procesando los datos, el subproceso principal no debe modificar los datos.</span><span class="sxs-lookup"><span data-stu-id="72344-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="72344-113">Una manera de administrar esto es a través de objetos de sincronización seguros para subprocesos, como semáforos, eventos y exclusiones mutuas.</span><span class="sxs-lookup"><span data-stu-id="72344-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="72344-114">Al mismo tiempo, se debe evitar cierta interacción del usuario mientras se ejecuta el subproceso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="72344-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="72344-115">En el programa de ejemplo, los datos de la aplicación están protegidos y la interacción con el usuario se limita al hacer que el procesamiento del trabajo de impresión sea administrado por el cuadro de diálogo de progreso modal.</span><span class="sxs-lookup"><span data-stu-id="72344-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="72344-116">Un cuadro de diálogo modal impide que el usuario interactúe con la ventana principal del programa, lo que evita que el usuario modifique los datos del programa de la aplicación mientras se imprimen los datos.</span><span class="sxs-lookup"><span data-stu-id="72344-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="72344-117">La única acción que el usuario puede realizar mientras se está procesando un trabajo de impresión es cancelar el trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="72344-118">Esta restricción se señaliza al usuario mediante la forma cursor.</span><span class="sxs-lookup"><span data-stu-id="72344-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="72344-119">Cuando el cursor está sobre el botón **Cancelar** , se muestra un cursor de flecha, que indica que el usuario puede hacer clic en este botón.</span><span class="sxs-lookup"><span data-stu-id="72344-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="72344-120">Cuando el cursor está sobre cualquier otra parte del área de la ventana del programa, se muestra un cursor de espera, que indica que el programa está ocupado y no puede responder a los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="72344-121">Crear el procedimiento de subproceso de impresión</span><span class="sxs-lookup"><span data-stu-id="72344-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="72344-122">Se recomienda incluir estas características durante el procesamiento de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="72344-123">**El procesamiento de impresión se divide en pasos**</span><span class="sxs-lookup"><span data-stu-id="72344-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="72344-124">Puede dividir el procesamiento de impresión en pasos de procesamiento discretos que puede interrumpir si el usuario hace clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="72344-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="72344-125">Esto resulta útil porque el procesamiento de impresión puede incluir operaciones de uso intensivo del procesador.</span><span class="sxs-lookup"><span data-stu-id="72344-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="72344-126">Dividir este procesamiento en pasos puede impedir que el procesamiento de impresión bloquee o retrase otros subprocesos o procesos.</span><span class="sxs-lookup"><span data-stu-id="72344-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="72344-127">Interrumpir el procesamiento en pasos lógicos también permite finalizar correctamente el procesamiento de impresión en cualquier momento, de modo que el cierre de un trabajo de impresión antes de que haya terminado no dejará ningún recurso huérfano.</span><span class="sxs-lookup"><span data-stu-id="72344-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="72344-128">Esta es una lista de ejemplos de pasos de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="72344-129">**Comprobar si hay un evento de cancelación entre pasos**</span><span class="sxs-lookup"><span data-stu-id="72344-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="72344-130">Cuando el usuario hace clic en el botón **Cancelar** , el subproceso de la interfaz de usuario indica el evento de cancelación.</span><span class="sxs-lookup"><span data-stu-id="72344-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="72344-131">El subproceso de procesamiento debe comprobar periódicamente el evento de cancelación para saber cuándo un usuario hizo clic en el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="72344-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="72344-132">Las instrucciones [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) realizan esta comprobación y también proporcionan a otros programas una oportunidad de ejecutarse para que el procesamiento del trabajo de impresión no se bloquee ni retrase otros subprocesos o procesos.</span><span class="sxs-lookup"><span data-stu-id="72344-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="72344-133">En el ejemplo de código siguiente se muestra una de las pruebas para ver si se ha producido el evento de cancelación.</span><span class="sxs-lookup"><span data-stu-id="72344-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="72344-134">**Enviar actualizaciones de estado al subproceso de la interfaz de usuario**</span><span class="sxs-lookup"><span data-stu-id="72344-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="72344-135">Como cada paso de procesamiento de impresión, el subproceso de procesamiento de impresión envía mensajes de actualización al cuadro de diálogo progreso de impresión para que pueda actualizar la barra de progreso.</span><span class="sxs-lookup"><span data-stu-id="72344-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="72344-136">Tenga en cuenta que el cuadro de diálogo progreso de la impresión se está ejecutando en el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="72344-137">En el ejemplo de código siguiente se muestra una de las llamadas a mensajes de actualización.</span><span class="sxs-lookup"><span data-stu-id="72344-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="72344-138">Iniciar el subproceso de impresión</span><span class="sxs-lookup"><span data-stu-id="72344-138">Starting the Printing Thread</span></span>

<span data-ttu-id="72344-139">El subproceso de procesamiento de impresión se ejecuta hasta que se devuelve la función PrintThreadProc.</span><span class="sxs-lookup"><span data-stu-id="72344-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="72344-140">En los pasos siguientes se inicia el subproceso de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="72344-141">**Preparar los datos y los elementos de la interfaz de usuario para imprimirlos.**</span><span class="sxs-lookup"><span data-stu-id="72344-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="72344-142">Antes de iniciar el subproceso de procesamiento de impresión, debe inicializar los elementos de datos que describen el trabajo de impresión y los elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="72344-143">Estos elementos incluyen el estado del cursor, de modo que el cursor de espera se muestre correctamente.</span><span class="sxs-lookup"><span data-stu-id="72344-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="72344-144">También debe configurar la barra de progreso para reflejar el tamaño del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="72344-145">Estos pasos de preparación se describen en detalle en [Cómo: recopilar información del trabajo de impresión del usuario](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="72344-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="72344-146">En el ejemplo de código siguiente se muestra cómo configurar la barra de progreso para reflejar el tamaño del trabajo de impresión solicitado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="72344-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  <span data-ttu-id="72344-147">**Inicie el subproceso de procesamiento de impresión.**</span><span class="sxs-lookup"><span data-stu-id="72344-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="72344-148">Llame a [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para iniciar el subproceso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="72344-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="72344-149">En el ejemplo de código siguiente se inicia el subproceso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="72344-149">The following code example starts the processing thread.</span></span>

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  <span data-ttu-id="72344-150">**Compruebe si el procesamiento de impresión no se pudo iniciar.**</span><span class="sxs-lookup"><span data-stu-id="72344-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="72344-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) devuelve un identificador al subproceso creado si el subproceso se ha creado correctamente.</span><span class="sxs-lookup"><span data-stu-id="72344-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="72344-152">La función PrintThreadProc que se inició en el nuevo subproceso comprueba algunas condiciones antes de iniciar el procesamiento real del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="72344-153">Si detecta errores en estas comprobaciones, PrintThreadProc podría devolver sin procesar ningún dato de trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="72344-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="72344-154">El subproceso de la interfaz de usuario puede comprobar si el subproceso de procesamiento se inició correctamente esperando en el identificador de subproceso durante un período de tiempo que sea mayor que el necesario para realizar las pruebas iniciales, pero que no sea más largo de lo necesario.</span><span class="sxs-lookup"><span data-stu-id="72344-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="72344-155">Cuando finaliza el subproceso, se señala el identificador al subproceso.</span><span class="sxs-lookup"><span data-stu-id="72344-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="72344-156">El código comprueba el estado del subproceso durante un breve período de tiempo después de iniciar el subproceso de procesamiento.</span><span class="sxs-lookup"><span data-stu-id="72344-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="72344-157">La función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) devuelve cuando se produce el tiempo de espera o se señala el identificador del subproceso.</span><span class="sxs-lookup"><span data-stu-id="72344-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="72344-158">Si la función **WaitForSingleObject** devuelve un estado de **objeto de espera \_ \_ 0** , el subproceso se cerró pronto y, por lo tanto, debe cerrar el cuadro de diálogo de progreso de la impresión, como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="72344-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="72344-159">Detener el subproceso de impresión</span><span class="sxs-lookup"><span data-stu-id="72344-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="72344-160">Cuando el usuario hace clic en el botón **Cancelar** del cuadro de diálogo progreso de la impresión, se notifica al subproceso de impresión para que pueda dejar de procesar el trabajo de impresión de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="72344-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="72344-161">Aunque el botón **Cancelar** y el evento **quitEvent** son aspectos importantes de este procesamiento, debe diseñar la secuencia de procesamiento completa para que se interrumpa correctamente.</span><span class="sxs-lookup"><span data-stu-id="72344-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="72344-162">Esto significa que los pasos de la secuencia no deben dejar ningún recurso asignado que no se libere si un usuario cancela la secuencia antes de que se completara.</span><span class="sxs-lookup"><span data-stu-id="72344-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="72344-163">En el ejemplo de código siguiente se muestra cómo el programa de ejemplo comprueba el **quitEvent** antes de procesar cada página del documento que se está imprimiendo.</span><span class="sxs-lookup"><span data-stu-id="72344-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="72344-164">Si el **quitEvent** está señalado o se detectó un error, el procesamiento de impresión se detiene.</span><span class="sxs-lookup"><span data-stu-id="72344-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
