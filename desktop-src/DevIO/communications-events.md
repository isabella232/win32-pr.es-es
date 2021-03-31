---
description: Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar si las señales CTS (Clear-to-send) y DSR (conjunto de datos preparado) cambian de estado.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153097"
---
# <a name="communications-events"></a>Eventos de comunicaciones

Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar si las señales CTS (Clear-to-send) y DSR (conjunto de datos preparado) cambian de estado.

Un proceso puede supervisar eventos en un recurso de comunicaciones determinado mediante la función [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para crear una máscara de eventos. Para determinar la máscara de eventos actual para un recurso de comunicaciones, un proceso puede utilizar la función [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) . Los valores siguientes especifican los eventos que se pueden supervisar.



| Value           | Significado                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **interrupción de EV \_**   | Se ha detectado una interrupción en la entrada.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | El estado de la señal CTS (Clear-to-send) cambió.                                                                                                                                                                                                     |
| **DSR de EV \_**     | El estado de la señal DSR (preparado para conjuntos de datos) cambió.                                                                                                                                                                                                    |
| **error de EV \_**     | Se produjo un error de estado de línea. Los errores de estado de línea son **\_ fotograma CE**, **\_ saturación de CE** y **\_ RXPARITY de CE**.                                                                                                                                        |
| **\_anillo EV**    | Se ha detectado un indicador de llamada.                                                                                                                                                                                                                    |
| **RLSD de EV \_**    | El estado de la señal RLSD (recepción-línea-señal-detección) cambió.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | Se ha recibido y colocado un carácter en el búfer de entrada.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | El carácter de evento se ha recibido y colocado en el búfer de entrada. El carácter de evento se especifica en la estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) del dispositivo, que se aplica a un puerto serie mediante la función [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) . |
| **EV \_ TXEMPTY** | Se envió el último carácter del búfer de salida.                                                                                                                                                                                                 |



 

Una vez que se especifica un conjunto de eventos, un proceso utiliza la función [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) para esperar a que se produzca uno de los eventos. **WaitCommEvent** se puede utilizar sincrónicamente o como una operación superpuesta. Para obtener información adicional sobre la ejecución de una función como una operación superpuesta, vea [Synchronization](/windows/desktop/Sync/synchronization).

Cuando se produce uno de los eventos especificados en la máscara de eventos, el proceso completa la operación de espera y establece una variable de máscara de eventos para indicar el tipo de evento detectado. Si se llama a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para un recurso de comunicaciones mientras hay una espera pendiente para ese recurso, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) devuelve un error.

La función [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) detecta eventos que se han producido desde la última llamada a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) o **WaitCommEvent**. Por ejemplo, si especifica el evento **EV \_ RXCHAR** como evento de espera, se cumplirá una llamada a **WaitCommEvent** si hay caracteres en el búfer de entrada del controlador que han llegado desde la última llamada a **WaitCommEvent** o **SetCommMask**. Por lo tanto, en el siguiente pseudocódigo, los caracteres recibidos entre T1 y T2 satisfarán la siguiente llamada a **WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Al supervisar un evento que se produce cuando cambia el estado de una señal (CTS, DSR, etc.), [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) informa del cambio, pero no del estado actual. Para consultar el estado actual de las señales CTS (Clear-to-send), DSR (conjunto de datos preparado), RLSD (Receive-line-Signal-detect) y de indicador de anillo, un proceso puede usar la función [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus) .

 

 
