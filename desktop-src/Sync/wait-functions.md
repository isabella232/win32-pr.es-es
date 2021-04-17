---
description: Las funciones wait permiten que un subproceso bloquee su propia ejecución.
ms.assetid: 9c66c71d-fdfd-42ae-895c-2fc842b5bc7a
title: Funciones de espera
ms.topic: article
ms.date: 06/25/2020
ms.openlocfilehash: f5a21b0d95a316b926fcaad037004edc8c418246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668158"
---
# <a name="wait-functions"></a>Funciones de espera

*Las funciones wait* permiten que un subproceso bloquee su propia ejecución. Las funciones wait no devuelven hasta que se hayan cumplido los criterios especificados. El tipo de función de espera determina el conjunto de criterios que se usan. Cuando se llama a una función wait, comprueba si se han cumplido los criterios de espera. Si no se cumplen los criterios, el subproceso que realiza la llamada entra en el estado de espera hasta que se cumplen las condiciones de los criterios de espera o hasta que transcurre el intervalo de tiempo de espera especificado.

-   [Funciones de espera de un solo objeto](#single-object-wait-functions)
-   [Funciones de espera de varios objetos](#multiple-object-wait-functions)
-   [Funciones de espera de alertas](#alertable-wait-functions)
-   [Funciones de espera registradas](#registered-wait-functions)
-   [Esperar en una dirección](#waiting-on-an-address)
-   [Funciones de espera y intervalos de tiempo de espera](#wait-functions-and-time-out-intervals)
-   [Funciones de espera y objetos de sincronización](#wait-functions-and-synchronization-objects)
-   [Funciones de espera y creación de ventanas](#wait-functions-and-creating-windows)

## <a name="single-object-wait-functions"></a>Funciones de espera de un solo objeto

Las funciones [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) requieren un identificador a un objeto de sincronización. Estas funciones devuelven cuando se produce uno de los siguientes casos:

-   El objeto especificado se encuentra en el estado señalado.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer en **infinito** para especificar que la espera no agotará el tiempo de espera.

La función [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait) permite al subproceso que realiza la llamada establecer atómicamente el estado de un objeto en señalizado y esperar a que el estado de otro objeto se establezca en señalado.

## <a name="multiple-object-wait-functions"></a>Funciones de espera de varios objetos

Las funciones [**WaitForMultipleObjects**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjects), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex), [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects)y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permiten que el subproceso que realiza la llamada especifique una matriz que contenga uno o varios identificadores de objetos de sincronización. Estas funciones devuelven cuando se produce uno de los siguientes casos:

-   El estado de cualquiera de los objetos especificados se establece en señalado o los Estados de todos los objetos se han establecido en señalizado. Puede controlar si se usará uno o todos los Estados en la llamada de función.
-   Transcurre el intervalo de tiempo de espera. El intervalo de tiempo de espera se puede establecer en **infinito** para especificar que la espera no agotará el tiempo de espera.

La función [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) y [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex) permite especificar objetos de eventos de entrada en la matriz de identificadores de objetos. Esto se hace cuando se especifica el tipo de entrada que se va a esperar en la cola de entrada del subproceso. Por ejemplo, un subproceso podría usar **MsgWaitForMultipleObjects** para bloquear su ejecución hasta que el estado de un objeto especificado se haya establecido en señalado y haya una entrada del mouse disponible en la cola de entrada del subproceso. El subproceso puede usar la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessageA**](/windows/win32/api/winuser/nf-winuser-peekmessagea) o [**PeekMessageW**](/windows/win32/api/winuser/nf-winuser-peekmessagew) para recuperar la entrada.

Cuando se espera a que los Estados de todos los objetos se establezcan en señalizado, estas funciones de varios objetos no modifican los Estados de los objetos especificados hasta que se señalan los Estados de todos los objetos. Por ejemplo, se puede señalizar el estado de un objeto mutex, pero el subproceso que realiza la llamada no obtiene la propiedad hasta que los Estados de los demás objetos especificados en la matriz también se hayan establecido en señalizado. Mientras tanto, otro subproceso puede obtener la propiedad del objeto mutex, con lo que se establece su estado en no señalado.

Cuando se espera a que el estado de un solo objeto se establezca en señalizado, estas funciones de varios objetos comprueban los identificadores de la matriz en orden a partir del índice 0 hasta que uno de los objetos está señalado. Si se señalizan varios objetos, la función devuelve el índice del primer identificador de la matriz cuyo objeto se señaló.

## <a name="alertable-wait-functions"></a>Funciones de espera de alertas

Las funciones [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait), [**WaitForMultipleObjectsEx**](/windows/win32/api/synchapi/nf-synchapi-waitformultipleobjectsex)y [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) se diferencian de las demás funciones Wait en que pueden realizar opcionalmente una *operación de espera de alerta*. En una operación de espera de alerta, la función puede devolver cuando se cumplen las condiciones especificadas, pero también puede devolver si el sistema pone en cola una rutina de finalización de e/s o una APC para su ejecución por el subproceso en espera. Para obtener más información sobre las operaciones de espera que se pueden notificar y las rutinas de finalización de e/s, vea [sincronización y entrada y salida superpuestas](synchronization-and-overlapped-input-and-output.md). Para obtener más información sobre APC, vea [llamadas a procedimientos asincrónicos](asynchronous-procedure-calls.md).

## <a name="registered-wait-functions"></a>Funciones de espera registradas

La función [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) difiere de las demás funciones Wait en que un subproceso del [grupo de subprocesos](../procthread/thread-pooling.md)realiza la operación de espera. Cuando se cumplen las condiciones especificadas, un subproceso de trabajo ejecuta la función de devolución de llamada desde el grupo de subprocesos.

De forma predeterminada, una operación de espera registrada es una operación de múltiples esperas. El sistema restablece el temporizador cada vez que se señala el evento (o transcurre el intervalo de tiempo de espera) hasta que se llama a la función [**UnregisterWaitEx**](unregisterwaitex.md) para cancelar la operación. Para especificar que una operación de espera se debe ejecutar una sola vez, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEONLYONCE**.

Si el subproceso llama a las funciones que utilizan APC, establezca el parámetro *dwFlags* de [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) en **WT \_ EXECUTEINPERSISTENTTHREAD**.

## <a name="waiting-on-an-address"></a>Esperar en una dirección

Un subproceso puede usar la función [**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) para esperar a que el valor de una dirección de destino cambie de algún valor no deseado a cualquier otro valor. Esto permite a los subprocesos esperar a que un valor cambie sin tener que girar o controlar los problemas de sincronización que pueden surgir cuando el subproceso captura un valor no deseado, pero el valor cambia antes de que el subproceso pueda esperar.

[**WaitOnAddress**](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress) devuelve cuando el código que modifica el valor de destino indica el cambio llamando a [**WakeByAddressSingle**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle) para reactivar un solo subproceso en espera o [**WakeByAddressAll**](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall) para reactivar todos los subprocesos en espera. Si se especifica un intervalo de tiempo de espera con **WaitOnAddress** y ningún subproceso llama a una función de reactivación, la función devuelve cuando transcurre el intervalo de tiempo de espera. Si no se especifica ningún intervalo de tiempo de espera, el subproceso espera indefinidamente.

## <a name="wait-functions-and-time-out-intervals"></a>Funciones de espera y intervalos de tiempo de espera

La precisión del intervalo de tiempo de espera especificado depende de la resolución del reloj del sistema. El reloj del sistema "TICs" a una velocidad constante. Si el intervalo de tiempo de espera es menor que la resolución del reloj del sistema, la espera puede agotar el tiempo de espera en menos de la cantidad de tiempo especificada. Si el intervalo de tiempo de espera es mayor que un TIC pero menor que dos, la espera puede estar entre uno y dos TICs, etc.

Para aumentar la precisión del intervalo de tiempo de espera de las funciones de espera, llame a la función **timeGetDevCaps** para determinar la resolución de temporizador mínima admitida y la función **timeBeginPeriod** para establecer la resolución del temporizador en el mínimo. Tenga cuidado al llamar a **timeBeginPeriod**, ya que las llamadas frecuentes pueden afectar significativamente al reloj del sistema, al uso de energía del sistema y al programador. Si llama a **timeBeginPeriod**, llámelo una vez al principio de la aplicación y asegúrese de llamar a la función **timeEndPeriod** al final de la aplicación.

## <a name="wait-functions-and-synchronization-objects"></a>Funciones de espera y objetos de sincronización

Las funciones de espera pueden modificar los Estados de algunos tipos de [objetos de sincronización](synchronization-objects.md). La modificación solo se produce para el objeto o los objetos cuyo estado señalado hizo que la función devuelva. Las funciones de espera pueden modificar los Estados de los objetos de sincronización de la siguiente manera:

-   El recuento de un objeto de semáforo disminuye en uno, y el estado del semáforo se establece en no señalado si su recuento es cero.
-   Los Estados de los objetos de exclusión mutua, evento de restablecimiento automático y notificación de cambios se establecen en no señalizado.
-   El estado de un temporizador de sincronización se establece en no señalado.
-   Los Estados de eventos de restablecimiento manual, temporizador de restablecimiento manual, proceso, subproceso y objetos de entrada de consola no se ven afectados por una función de espera.

## <a name="wait-functions-and-creating-windows"></a>Funciones de espera y creación de ventanas

Debe tener cuidado al usar las funciones de espera y el código que crea de forma directa o indirecta Windows. Si un subproceso crea cualquier ventana, debe procesar los mensajes. Las difusiones de mensajes se envían a todas las ventanas del sistema. Si tiene un subproceso que usa una función wait sin ningún intervalo de tiempo de espera, el sistema creará un interbloqueo. Dos ejemplos de código que crea indirectamente ventanas son DDE y la función **CoInitialize** . Por consiguiente, si tiene un subproceso que crea ventanas, use [**MsgWaitForMultipleObjects**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/Winuser/nf-winuser-msgwaitformultipleobjectsex), en lugar de otras funciones de espera.

 

 
