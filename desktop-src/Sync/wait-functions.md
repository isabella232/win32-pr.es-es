---
description: Las funciones de espera permiten que un subproceso bloquee su propia ejecución.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funciones wait
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: 15bfc37dcd8fe541c14b9a0693c7b743cae6ed3e548c418baf0585f078e6d59a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764969"
---
# <a name="wait-functions"></a>Funciones wait

*Las funciones de* espera permiten que un subproceso bloquee su propia ejecución. Las funciones de espera no se devuelven hasta que se cumplen los criterios especificados. El tipo de función wait determina el conjunto de criterios usados. Cuando se llama a una función de espera, comprueba si se han cumplido los criterios de espera. Si no se cumplen los criterios, el subproceso que realiza la llamada entra en el estado de espera hasta que se cumplen las condiciones de los criterios de espera o hasta que transcurre el intervalo de tiempo de espera especificado.

-   [Funciones de espera de objeto único](#single-object-wait-functions)
-   [Funciones de espera de varios objetos](#multiple-object-wait-functions)
-   [Funciones de espera que se pueden alertar](#alertable-wait-functions)
-   [Funciones de espera registradas](#registered-wait-functions)
-   [Esperando una dirección](#waiting-on-an-address)
-   [Funciones de espera e intervalos de tiempo de espera](#wait-functions-and-time-out-intervals)
-   [Funciones de espera y objetos de sincronización](#wait-functions-and-synchronization-objects)
-   [Funciones wait y creación de Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funciones de espera de objeto único

Las [**funciones SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) requieren un identificador para un objeto de sincronización. Estas funciones devuelven cuando se produce una de las siguientes situaciones:

-   El objeto especificado está en estado señalado.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer en **INFINITE para** especificar que la espera no se va a tiempo de espera.

La [**función SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permite que el subproceso que realiza la llamada establezca de forma atómica el estado de un objeto en señalado y espere a que el estado de otro objeto se establezca en señalado.

## <a name="multiple-object-wait-functions"></a>Funciones de espera de varios objetos

Las funciones [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx,**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex) [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permiten al subproceso que realiza la llamada especificar una matriz que contiene uno o varios identificadores de objeto de sincronización. Estas funciones devuelven cuando se produce una de las siguientes situaciones:

-   El estado de cualquiera de los objetos especificados se establece en señalado o los estados de todos los objetos se han establecido en señalados. Puede controlar si uno o todos los estados se usarán en la llamada de función.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer en **INFINITE para** especificar que la espera no se va a tiempo de espera.

Las [**funciones MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permiten especificar objetos de evento de entrada en la matriz de identificadores de objetos. Esto se hace cuando se especifica el tipo de entrada que se va a esperar en la cola de entrada del subproceso. Por ejemplo, un subproceso podría usar **MsgWaitForMultipleObjects** para bloquear su ejecución hasta que el estado de un objeto especificado se haya establecido en señalado y haya entradas del mouse disponibles en la cola de entrada del subproceso. El subproceso puede usar la [**función GetMessage,**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) para recuperar la entrada.

Al esperar a que los estados de todos los objetos se establezcan en señalados, estas funciones de varios objetos no modifican los estados de los objetos especificados hasta que se hayan establecido los estados de todos los objetos. Por ejemplo, se puede señalar el estado de un objeto de exclusión mutua, pero el subproceso que realiza la llamada no obtiene la propiedad hasta que los estados de los otros objetos especificados en la matriz también se hayan establecido en señalados. Mientras tanto, algún otro subproceso puede obtener la propiedad del objeto mutex, estableciendo así su estado en nonsignaled.

Al esperar a que el estado de un único objeto se establezca en señalado, estas funciones de varios objetos comprueban los identificadores de la matriz en orden a partir del índice 0, hasta que se señala uno de los objetos. Si se señalizan varios objetos, la función devuelve el índice del primer identificador de la matriz cuyo objeto se señaló.

## <a name="alertable-wait-functions"></a>Funciones de espera que se pueden alertar

Las funciones [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait,**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) difieren de las otras funciones de espera en que, opcionalmente, pueden realizar una operación de espera que se puede alertar.  En una operación de espera que se puede alertar, la función puede devolver cuando se cumplen las condiciones especificadas, pero también puede devolver si el sistema pone en cola una rutina de finalización de E/S o un APC para su ejecución por parte del subproceso en espera. Para obtener más información sobre las operaciones de espera que se pueden alertar y las rutinas de finalización de E/S, vea [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md). Para obtener más información sobre las API, vea [Llamadas a procedimiento asincrónico.](asynchronous-procedure-calls.md)

## <a name="registered-wait-functions"></a>Funciones de espera registradas

La [**función RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) difiere de las otras funciones de espera en que la operación de espera la realiza un subproceso del grupo [de subprocesos](../procthread/thread-pooling.md). Cuando se cumplen las condiciones especificadas, un subproceso de trabajo ejecuta la función de devolución de llamada desde el grupo de subprocesos.

De forma predeterminada, una operación de espera registrada es una operación de espera múltiple. El sistema restablece el temporizador cada vez que se señala el evento (o transcurre el intervalo de tiempo de espera) hasta que se llama a la función [**UnregisterWaitEx**](unregisterwaitex.md) para cancelar la operación. Para especificar que una operación de espera se debe ejecutar solo una vez, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEONLYONCE**.

Si el subproceso llama a funciones que usan API, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>Esperando una dirección

Un subproceso puede usar la [**función WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) para esperar a que el valor de una dirección de destino cambie de algún valor no deseado a cualquier otro valor. Esto permite a los subprocesos esperar a que un valor cambie sin tener que girar o controlar los problemas de sincronización que pueden surgir cuando el subproceso captura un valor no deseado, pero el valor cambia antes de que el subproceso pueda esperar.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) devuelve cuando el código que modifica el valor de destino señala el cambio mediante una llamada a [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) para reactivar un único subproceso en espera o [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) para reactivar todos los subprocesos en espera. Si se especifica un intervalo de tiempo de espera con **WaitOnAddress** y ningún subproceso llama a una función de reactivación, la función devuelve cuando transcurre el intervalo de tiempo de espera. Si no se especifica ningún intervalo de tiempo de espera, el subproceso espera indefinidamente.

## <a name="wait-functions-and-time-out-intervals"></a>Funciones de espera e intervalos de tiempo de espera

La precisión del intervalo de tiempo de espera especificado depende de la resolución del reloj del sistema. El reloj del sistema "marca" a una velocidad constante. Si el intervalo de tiempo de espera es menor que la resolución del reloj del sistema, el tiempo de espera puede ser menor que el período de tiempo especificado. Si el intervalo de tiempo de espera es mayor que un tic, pero menor que dos, la espera puede estar en cualquier lugar entre uno y dos tics, y así sucesivamente.

Para aumentar la precisión del intervalo de tiempo de espera de las funciones de espera, llame a la función **timeGetDevCaps** para determinar la resolución mínima de temporizador admitida y la función **timeBeginPeriod** para establecer la resolución del temporizador en su mínimo. Tenga cuidado al llamar **a timeBeginPeriod,** ya que las llamadas frecuentes pueden afectar significativamente al reloj del sistema, al uso de energía del sistema y al programador. Si llama a **timeBeginPeriod,** llámelo una vez al principio de la aplicación y asegúrese de llamar a la función **timeEndPeriod** al final de la aplicación.

## <a name="wait-functions-and-synchronization-objects"></a>Funciones de espera y objetos de sincronización

Las funciones de espera pueden modificar los estados de algunos tipos de objetos [de sincronización.](synchronization-objects.md) La modificación solo se produce para el objeto u objetos cuyo estado señalado ha provocado la devolución de la función. Las funciones wait pueden modificar los estados de los objetos de sincronización de la manera siguiente:

-   El recuento de un objeto semáforo disminuye en uno y el estado del semáforo se establece en sin signo si su recuento es cero.
-   Los estados de exclusión mutua, evento de restablecimiento automático y objetos de notificación de cambios se establecen en no firma.
-   El estado de un temporizador de sincronización se establece en nonsignaled.
-   Los estados de los objetos de entrada de evento de restablecimiento manual, temporizador de restablecimiento manual, proceso, subproceso y consola no se ven afectados por una función de espera.

## <a name="wait-functions-and-creating-windows"></a>Funciones wait y creación de Windows

Debe tener cuidado al usar las funciones de espera y el código que crea ventanas directa o indirectamente. Si un subproceso crea ventanas, debe procesar los mensajes. Las difusiones de mensajes se envían a todas las ventanas del sistema. Si tiene un subproceso que usa una función de espera sin intervalo de tiempo de espera, el sistema interbloqueará. Dos ejemplos de código que crean ventanas indirectamente son DDE y **la función CoInitialize.** Por lo tanto, si tiene un subproceso que crea ventanas, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)en lugar de las otras funciones de espera.

 

 
