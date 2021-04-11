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
# <a name="how-to-start-and-stop-a-printing-thread"></a>Cómo: iniciar y detener un subproceso de impresión

En este tema se describe cómo iniciar y detener el subproceso de procesamiento del trabajo de impresión.

## <a name="overview"></a>Información general

Para evitar que las actividades de impresión bloqueen la respuesta de la interfaz de usuario, cree un subproceso independiente para procesar el trabajo de impresión. El subproceso que se inicia cuando se inicia el programa, es el subproceso que controla los mensajes de ventana que resultan de la interacción del usuario y, por tanto, es el subproceso de la interfaz de usuario. El programa debe procesar estos mensajes sin retraso para que la interfaz de usuario responda a la entrada del teclado y del mouse del usuario de manera oportuna. Para que el programa pueda responder a estos mensajes rápidamente, se limita la cantidad de procesamiento que se puede realizar durante cualquier mensaje. Cuando una solicitud de usuario requiere un procesamiento extensivo, un subproceso diferente debe realizar ese procesamiento para permitir que el programa controle la interacción posterior del usuario.

El procesamiento de datos en un subproceso independiente requiere que el programa coordine el funcionamiento del subproceso de la interfaz de usuario y el subproceso de procesamiento. Por ejemplo, mientras el subproceso de procesamiento está procesando los datos, el subproceso principal no debe modificar los datos. Una manera de administrar esto es a través de objetos de sincronización seguros para subprocesos, como semáforos, eventos y exclusiones mutuas.

Al mismo tiempo, se debe evitar cierta interacción del usuario mientras se ejecuta el subproceso de procesamiento. En el programa de ejemplo, los datos de la aplicación están protegidos y la interacción con el usuario se limita al hacer que el procesamiento del trabajo de impresión sea administrado por el cuadro de diálogo de progreso modal. Un cuadro de diálogo modal impide que el usuario interactúe con la ventana principal del programa, lo que evita que el usuario modifique los datos del programa de la aplicación mientras se imprimen los datos.

La única acción que el usuario puede realizar mientras se está procesando un trabajo de impresión es cancelar el trabajo de impresión. Esta restricción se señaliza al usuario mediante la forma cursor. Cuando el cursor está sobre el botón **Cancelar** , se muestra un cursor de flecha, que indica que el usuario puede hacer clic en este botón. Cuando el cursor está sobre cualquier otra parte del área de la ventana del programa, se muestra un cursor de espera, que indica que el programa está ocupado y no puede responder a los datos proporcionados por el usuario.

## <a name="creating-the-printing-thread-procedure"></a>Crear el procedimiento de subproceso de impresión

Se recomienda incluir estas características durante el procesamiento de impresión.

-   **El procesamiento de impresión se divide en pasos**

    Puede dividir el procesamiento de impresión en pasos de procesamiento discretos que puede interrumpir si el usuario hace clic en el botón **Cancelar** . Esto resulta útil porque el procesamiento de impresión puede incluir operaciones de uso intensivo del procesador. Dividir este procesamiento en pasos puede impedir que el procesamiento de impresión bloquee o retrase otros subprocesos o procesos. Interrumpir el procesamiento en pasos lógicos también permite finalizar correctamente el procesamiento de impresión en cualquier momento, de modo que el cierre de un trabajo de impresión antes de que haya terminado no dejará ningún recurso huérfano.

    Esta es una lista de ejemplos de pasos de impresión.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Comprobar si hay un evento de cancelación entre pasos**

    Cuando el usuario hace clic en el botón **Cancelar** , el subproceso de la interfaz de usuario indica el evento de cancelación. El subproceso de procesamiento debe comprobar periódicamente el evento de cancelación para saber cuándo un usuario hizo clic en el botón **Cancelar** . Las instrucciones [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) realizan esta comprobación y también proporcionan a otros programas una oportunidad de ejecutarse para que el procesamiento del trabajo de impresión no se bloquee ni retrase otros subprocesos o procesos.

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

    

-   **Enviar actualizaciones de estado al subproceso de la interfaz de usuario**

    Como cada paso de procesamiento de impresión, el subproceso de procesamiento de impresión envía mensajes de actualización al cuadro de diálogo progreso de impresión para que pueda actualizar la barra de progreso. Tenga en cuenta que el cuadro de diálogo progreso de la impresión se está ejecutando en el subproceso de la interfaz de usuario.

    En el ejemplo de código siguiente se muestra una de las llamadas a mensajes de actualización.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Iniciar el subproceso de impresión

El subproceso de procesamiento de impresión se ejecuta hasta que se devuelve la función PrintThreadProc. En los pasos siguientes se inicia el subproceso de impresión.

1.  **Preparar los datos y los elementos de la interfaz de usuario para imprimirlos.**

    Antes de iniciar el subproceso de procesamiento de impresión, debe inicializar los elementos de datos que describen el trabajo de impresión y los elementos de la interfaz de usuario. Estos elementos incluyen el estado del cursor, de modo que el cursor de espera se muestre correctamente. También debe configurar la barra de progreso para reflejar el tamaño del trabajo de impresión. Estos pasos de preparación se describen en detalle en [Cómo: recopilar información del trabajo de impresión del usuario](preparing-to-print.md).

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

    Llame a [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para iniciar el subproceso de procesamiento.

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

    

3.  **Compruebe si el procesamiento de impresión no se pudo iniciar.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) devuelve un identificador al subproceso creado si el subproceso se ha creado correctamente. La función PrintThreadProc que se inició en el nuevo subproceso comprueba algunas condiciones antes de iniciar el procesamiento real del trabajo de impresión. Si detecta errores en estas comprobaciones, PrintThreadProc podría devolver sin procesar ningún dato de trabajo de impresión. El subproceso de la interfaz de usuario puede comprobar si el subproceso de procesamiento se inició correctamente esperando en el identificador de subproceso durante un período de tiempo que sea mayor que el necesario para realizar las pruebas iniciales, pero que no sea más largo de lo necesario. Cuando finaliza el subproceso, se señala el identificador al subproceso. El código comprueba el estado del subproceso durante un breve período de tiempo después de iniciar el subproceso de procesamiento. La función [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) devuelve cuando se produce el tiempo de espera o se señala el identificador del subproceso. Si la función **WaitForSingleObject** devuelve un estado de **objeto de espera \_ \_ 0** , el subproceso se cerró pronto y, por lo tanto, debe cerrar el cuadro de diálogo de progreso de la impresión, como se muestra en el ejemplo de código siguiente.

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

Cuando el usuario hace clic en el botón **Cancelar** del cuadro de diálogo progreso de la impresión, se notifica al subproceso de impresión para que pueda dejar de procesar el trabajo de impresión de forma ordenada. Aunque el botón **Cancelar** y el evento **quitEvent** son aspectos importantes de este procesamiento, debe diseñar la secuencia de procesamiento completa para que se interrumpa correctamente. Esto significa que los pasos de la secuencia no deben dejar ningún recurso asignado que no se libere si un usuario cancela la secuencia antes de que se completara.

En el ejemplo de código siguiente se muestra cómo el programa de ejemplo comprueba el **quitEvent** antes de procesar cada página del documento que se está imprimiendo. Si el **quitEvent** está señalado o se detectó un error, el procesamiento de impresión se detiene.


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



 

 
