---
description: En este tema se describe cómo iniciar y detener el subproceso de procesamiento del trabajo de impresión.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Cómo: Iniciar y detener un subproceso de impresión'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468523"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Cómo: Iniciar y detener un subproceso de impresión

En este tema se describe cómo iniciar y detener el subproceso de procesamiento del trabajo de impresión.

## <a name="overview"></a>Información general

Para evitar que las actividades de impresión bloqueen la respuesta de la interfaz de usuario, cree un subproceso independiente para procesar el trabajo de impresión. El subproceso que se inicia cuando se inicia el programa es el subproceso que controla los mensajes de ventana que resultan de la interacción del usuario y, por tanto, es el subproceso de la interfaz de usuario. El programa debe procesar estos mensajes sin retraso para que la interfaz de usuario responda a la entrada del mouse y el teclado del usuario de forma oportuna. Para que el programa pueda responder a estos mensajes rápidamente, la cantidad de procesamiento que se puede realizar durante cualquier mensaje es limitada. Cuando una solicitud de usuario requiere un procesamiento exhaustivo, un subproceso diferente debe realizar ese procesamiento para permitir que el programa controle la interacción posterior del usuario.

El procesamiento de datos en un subproceso independiente requiere que el programa coordine el funcionamiento del subproceso de interfaz de usuario y el subproceso de procesamiento. Por ejemplo, mientras el subproceso de procesamiento procesa los datos, el subproceso principal no debe modificar los datos. Una manera de administrar esto es mediante objetos de sincronización seguros para subprocesos, como semáforos, eventos y exclusiones mutuas.

Al mismo tiempo, se debe evitar alguna interacción del usuario mientras se ejecuta el subproceso de procesamiento. En el programa de ejemplo, los datos de la aplicación están protegidos y la interacción del usuario está limitada por la administración del procesamiento del trabajo de impresión mediante el cuadro de diálogo progreso modal. Un cuadro de diálogo modal impide que el usuario interactúe con la ventana principal del programa, lo que impide que el usuario modifique los datos del programa de aplicación mientras se imprimen los datos.

La única acción que el usuario puede realizar mientras se procesa un trabajo de impresión es cancelar el trabajo de impresión. Esta restricción se señala al usuario mediante la forma del cursor. Cuando el cursor está sobre el **botón Cancelar,** se muestra un cursor de flecha, que indica que el usuario puede hacer clic en este botón. Cuando el cursor está sobre cualquier otra parte del área de ventana del programa, se muestra un cursor de espera, que indica que el programa está ocupado y no puede responder a la entrada del usuario.

## <a name="creating-the-printing-thread-procedure"></a>Crear el procedimiento de subproceso de impresión

Se recomienda incluir estas características durante el procesamiento de impresión.

-   **El procesamiento de impresión se divide en pasos**

    Puede dividir el procesamiento de impresión en pasos de procesamiento discretos que puede interrumpir si el usuario hace clic en **el botón** Cancelar. Esto es útil porque el procesamiento de impresión puede incluir operaciones que consumen muchos procesadores. Dividir este procesamiento en pasos puede impedir que el procesamiento de impresión bloquee o retrase otros subprocesos o procesos. Dividir el procesamiento en pasos lógicos también permite finalizar correctamente el procesamiento de impresión en cualquier momento, por lo que finalizar un trabajo de impresión antes de que haya finalizado no dejará ningún recurso huérfano.

    Esta es una lista de ejemplo de pasos de impresión.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Comprobación de un evento de cancelación entre pasos**

    Cuando el usuario hace clic en el **botón Cancelar,** el subproceso de la interfaz de usuario señala el evento de cancelación. El subproceso de procesamiento debe comprobar periódicamente el evento de cancelación para saber cuándo un usuario hizo clic en **el botón** Cancelar. Las [**instrucciones WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) realizan esta comprobación y también ofrecen a otros programas la oportunidad de ejecutarse para que el procesamiento del trabajo de impresión no bloquee ni retrase otros subprocesos o procesos.

    En el ejemplo de código siguiente se muestra una de las pruebas para ver si se ha producido el evento de cancelación.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Envío de actualizaciones de estado al subproceso de la interfaz de usuario**

    Como cada paso de procesamiento de impresión, el subproceso de procesamiento de impresión envía mensajes de actualización al cuadro de diálogo progreso de impresión para que pueda actualizar la barra de progreso. Tenga en cuenta que el cuadro de diálogo progreso de impresión se está ejecutando en el subproceso de la interfaz de usuario.

    En el ejemplo de código siguiente se muestra una de las llamadas de mensaje de actualización.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Iniciar el subproceso de impresión

El subproceso de procesamiento de impresión se ejecuta hasta que se devuelve la función PrintThreadProc. Los pasos siguientes inician el subproceso de impresión.

1.  **Prepare los datos y los elementos de la interfaz de usuario para la impresión.**

    Antes de iniciar el subproceso de procesamiento de impresión, debe inicializar los elementos de datos que describen el trabajo de impresión y los elementos de la interfaz de usuario. Estos elementos incluyen el estado del cursor, por lo que el cursor de espera se mostrará correctamente. También debe configurar la barra de progreso para reflejar el tamaño del trabajo de impresión. Estos pasos de preparación se describen en detalle [en Cómo: Recopilar](preparing-to-print.md)información del trabajo de impresión del usuario .

    En el ejemplo de código siguiente se muestra cómo configurar la barra de progreso para reflejar el tamaño del trabajo de impresión solicitado por el usuario.

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

    

2.  **Inicie el subproceso de procesamiento de impresión.**

    Llame [**a CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para iniciar el subproceso de procesamiento.

    En el ejemplo de código siguiente se inicia el subproceso de procesamiento.

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

    

3.  **Compruebe si el procesamiento de impresión no se pudo realizar al iniciarse.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) devuelve un identificador al subproceso creado si el subproceso se creó correctamente. La función PrintThreadProc que se inició en el nuevo subproceso comprueba algunas condiciones antes de iniciar el procesamiento real del trabajo de impresión. Si detecta errores en estas comprobaciones, PrintThreadProc podría devolver sin procesar los datos del trabajo de impresión. El subproceso de interfaz de usuario puede comprobar si el subproceso de procesamiento se inició correctamente esperando en el identificador del subproceso durante un período de tiempo mayor del necesario para realizar las pruebas iniciales, pero no más de lo necesario. Cuando se cierra el subproceso, se señala el identificador del subproceso. El código comprueba el estado del subproceso durante un breve período de tiempo después de iniciar el subproceso de procesamiento. La [**función WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) devuelve cuando se agota el tiempo de espera o se señala el identificador del subproceso. Si la **función WaitForSingleObject** devuelve un estado **WAIT OBJECT \_ \_ 0,** el subproceso salió al principio y, por tanto, debería cerrar el cuadro de diálogo progreso de impresión, como se muestra en el ejemplo de código siguiente.

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

    

## <a name="stopping-the-printing-thread"></a>Detener el subproceso de impresión

Cuando el usuario  hace clic en el botón Cancelar del cuadro de diálogo progreso de impresión, se notifica al subproceso de impresión para que pueda detener el procesamiento del trabajo de impresión de forma ordenada. Aunque el **botón Cancelar** y el evento **quitEvent** son aspectos importantes de este procesamiento, debe diseñar toda la secuencia de procesamiento para que se interrumpa correctamente. Esto significa que los pasos de la secuencia no deben dejar ningún recurso asignado que no se libera si un usuario cancela la secuencia antes de que se hubiera completado.

En el ejemplo de código siguiente se muestra cómo el programa de ejemplo comprueba **el quitEvent** antes de que procese cada página del documento que se va a imprimir. Si se **señala el evento quitEvent** o se ha detectado un error, el procesamiento de impresión se detiene.


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



 

 
