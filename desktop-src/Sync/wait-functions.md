---
description: Las funciones wait permiten a un subproceso bloquear su propia ejecución.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funciones wait
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: f5a21b0d95a316b926fcaad037004edc8c418246
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160689"
---
# <a name="wait-functions"></a>Funciones wait

*Las funciones wait* permiten a un subproceso bloquear su propia ejecución. Las funciones de espera no se devuelven hasta que se cumplen los criterios especificados. El tipo de función wait determina el conjunto de criterios utilizados. Cuando se llama a una función de espera, comprueba si se han cumplido los criterios de espera. Si no se cumplen los criterios, el subproceso que realiza la llamada entra en el estado de espera hasta que se cumplen las condiciones de los criterios de espera o hasta que transcurre el intervalo de tiempo de espera especificado.

-   [Funciones de espera de un solo objeto](#single-object-wait-functions)
-   [Funciones de espera de varios objetos](#multiple-object-wait-functions)
-   [Funciones de espera que se pueden alertar](#alertable-wait-functions)
-   [Funciones de espera registradas](#registered-wait-functions)
-   [Esperar una dirección](#waiting-on-an-address)
-   [Funciones wait e intervalos de tiempo de espera](#wait-functions-and-time-out-intervals)
-   [Funciones wait y objetos de sincronización](#wait-functions-and-synchronization-objects)
-   [Funciones Wait y Creación de Windows](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funciones de espera de un solo objeto

Las [**funciones SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) requieren un identificador para un objeto de sincronización. Estas funciones devuelven cuando se produce una de las siguientes situaciones:

-   El objeto especificado está en estado señalado.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer **en INFINITE para** especificar que la espera no se va a tiempo de espera.

La [**función SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permite que el subproceso que realiza la llamada establezca de forma atómica el estado de un objeto en señalado y espere a que el estado de otro objeto se establezca en signaled.

## <a name="multiple-object-wait-functions"></a>Funciones de espera de varios objetos

Las [**funciones WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permiten al subproceso que realiza la llamada especificar una matriz que contiene uno o varios identificadores de objeto de sincronización. Estas funciones devuelven cuando se produce una de las siguientes situaciones:

-   El estado de cualquiera de los objetos especificados se establece en signaled o los estados de todos los objetos se han establecido en signaled. Puede controlar si uno o todos los estados se usarán en la llamada de función.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer **en INFINITE para** especificar que la espera no se va a tiempo de espera.

Las [**funciones MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permiten especificar objetos de evento de entrada en la matriz de identificadores de objeto. Esto se hace cuando se especifica el tipo de entrada que se va a esperar en la cola de entrada del subproceso. Por ejemplo, un subproceso podría usar **MsgWaitForMultipleObjects** para bloquear su ejecución hasta que el estado de un objeto especificado se haya establecido en signaled y haya entrada de mouse disponible en la cola de entrada del subproceso. El subproceso puede usar las [**funciones GetMessage,**](/windows/win32/api/winuser/nf-winuser-getmessage) [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) para recuperar la entrada.

Al esperar a que se señalen los estados de todos los objetos, estas funciones de varios objetos no modifican los estados de los objetos especificados hasta que se han establecido los estados de todos los objetos. Por ejemplo, se puede señalar el estado de un objeto de exclusión mutua, pero el subproceso que realiza la llamada no obtiene la propiedad hasta que los estados de los otros objetos especificados en la matriz también se hayan establecido en señalados. Mientras tanto, algún otro subproceso puede obtener la propiedad del objeto mutex, estableciendo así su estado en nonsignaled.

Al esperar a que el estado de un único objeto se establezca en señalizado, estas funciones de varios objetos comprueban los identificadores de la matriz en orden a partir del índice 0, hasta que se señale uno de los objetos. Si se señalizan varios objetos, la función devuelve el índice del primer identificador de la matriz cuyo objeto se señalizó.

## <a name="alertable-wait-functions"></a>Funciones de espera que se pueden alertar

Las funciones [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) difieren de las otras funciones de espera, ya que opcionalmente pueden realizar una operación de espera que permite alertas.  En una operación de espera de alerta, la función puede devolver cuando se cumplen las condiciones especificadas, pero también puede devolver si el sistema pone en cola una rutina de finalización de E/S o un APC para su ejecución por el subproceso en espera. Para obtener más información sobre las operaciones de espera que se pueden alertar y las rutinas de finalización de E/S, vea [Synchronization and Overlapped Input and Output](synchronization-and-overlapped-input-and-output.md). Para obtener más información sobre las API, vea [Llamadas a procedimientos asincrónicos](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funciones de espera registradas

La [**función RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) difiere de las demás funciones de espera en que un subproceso del grupo de subprocesos realiza la operación de [espera.](../procthread/thread-pooling.md) Cuando se cumplen las condiciones especificadas, un subproceso de trabajo del grupo de subprocesos ejecuta la función de devolución de llamada.

De forma predeterminada, una operación de espera registrada es una operación de varias esperas. El sistema restablece el temporizador cada vez que se señala el evento (o transcurre el intervalo de tiempo de espera) hasta que se llama a la función [**UnregisterWaitEx**](unregisterwaitex.md) para cancelar la operación. Para especificar que una operación de espera solo se debe ejecutar una vez, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEONLYONCE**.

Si el subproceso llama a funciones que usan LAS API, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>Esperar una dirección

Un subproceso puede usar la [**función WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) para esperar a que el valor de una dirección de destino cambie de algún valor no deseado a cualquier otro valor. Esto permite que los subprocesos esperen a que un valor cambie sin tener que girar o controlar los problemas de sincronización que pueden surgir cuando el subproceso captura un valor no deseado, pero el valor cambia antes de que el subproceso pueda esperar.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) devuelve cuando el código que modifica el valor de destino señala el cambio llamando a [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) para reactivar un único subproceso en espera o [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) para reactivar todos los subprocesos en espera. Si se especifica un intervalo de tiempo de espera con **WaitOnAddress** y ningún subproceso llama a una función de reactivación, la función devuelve cuando transcurre el intervalo de tiempo de espera. Si no se especifica ningún intervalo de tiempo de espera, el subproceso espera indefinidamente.

## <a name="wait-functions-and-time-out-intervals"></a>Funciones wait e intervalos de tiempo de espera

La precisión del intervalo de tiempo de espera especificado depende de la resolución del reloj del sistema. El reloj del sistema "tics" a una velocidad constante. Si el intervalo de tiempo de espera es menor que la resolución del reloj del sistema, el tiempo de espera puede ser menor que el período de tiempo especificado. Si el intervalo de tiempo de espera es mayor que un tic, pero menor que dos, la espera puede estar entre uno y dos pasos, y así sucesivamente.

Para aumentar la precisión del intervalo de tiempo de espera de las funciones de espera, llame a la función **timeGetDevCaps** para determinar la resolución mínima de temporizador admitida y la función **timeBeginPeriod** para establecer la resolución del temporizador en su mínimo. Tenga cuidado al llamar a **timeBeginPeriod**, ya que las llamadas frecuentes pueden afectar significativamente al reloj del sistema, al uso de energía del sistema y al programador. Si llama a **timeBeginPeriod,** llámelo una vez al principio de la aplicación y asegúrese de llamar a la función **timeEndPeriod** al final de la aplicación.

## <a name="wait-functions-and-synchronization-objects"></a>Funciones wait y objetos de sincronización

Las funciones de espera pueden modificar los estados de algunos tipos de objetos [de sincronización.](synchronization-objects.md) La modificación solo se produce para el objeto u objetos cuyo estado señalado hizo que la función devolvía. Las funciones wait pueden modificar los estados de los objetos de sincronización de la siguiente manera:

-   El recuento de un objeto semáforo se reduce en uno y el estado del semáforo se establece en sin signo si su recuento es cero.
-   Los estados de exclusión mutua, evento de restablecimiento automático y objetos de notificación de cambios se establecen en no con signo.
-   El estado de un temporizador de sincronización se establece en nonsignaled.
-   Los estados de los objetos de entrada de evento de restablecimiento manual, temporizador de restablecimiento manual, proceso, subproceso y consola no se ven afectados por una función de espera.

## <a name="wait-functions-and-creating-windows"></a>Funciones Wait y Creación de Windows

Debe tener cuidado al usar las funciones de espera y el código que crea ventanas directa o indirectamente. Si un subproceso crea ventanas, debe procesar los mensajes. Las difusión de mensajes se envían a todas las ventanas del sistema. Si tiene un subproceso que usa una función de espera sin intervalo de tiempo de espera, el sistema interbloqueará. Dos ejemplos de código que crean ventanas indirectamente son DDE y **la función CoInitialize.** Por lo tanto, si tiene un subproceso que crea ventanas, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx,**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex)en lugar de las otras funciones de espera.

 

 
