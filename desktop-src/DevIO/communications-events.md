---
description: Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar cuándo las señales CTS (clear-to-send) y DSR (data-set-ready) cambian de estado.
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 466bd5076405427c7c348c1df3706cb7b5c3edc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164518"
---
# <a name="communications-events"></a>Eventos de comunicaciones

Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar cuándo las señales CTS (clear-to-send) y DSR (data-set-ready) cambian de estado.

Un proceso puede supervisar eventos en un recurso de comunicaciones determinado mediante la [**función SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para crear una máscara de eventos. Para determinar la máscara de eventos actual para un recurso de comunicaciones, un proceso puede usar la [**función GetCommMask.**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) Los valores siguientes especifican eventos que se pueden supervisar.



| Value           | Significado                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EV \_ BREAK**   | Se ha detectado una interrupción en la entrada.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | La señal CTS (clear-to-send) cambió de estado.                                                                                                                                                                                                     |
| **EV \_ DSR**     | La señal DSR (lista para el conjunto de datos) cambió de estado.                                                                                                                                                                                                    |
| **EV \_ ERR**     | Se produjo un error de estado de línea. Los errores de estado de línea **son CE \_ FRAME,** **CE \_ OVERRUN** y **CE \_ RXPARITY.**                                                                                                                                        |
| **EV \_ RING**    | Se ha detectado un indicador de llamada.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | La señal RLSD (receive-line-signal-detect) cambió de estado.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | Se ha recibido y colocado un carácter en el búfer de entrada.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | El carácter de evento se recibió y se colocó en el búfer de entrada. El carácter de evento se especifica en la estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) del dispositivo, que se aplica a un puerto serie mediante la [**función SetCommState.**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) |
| **EV \_ TXEMPTY** | Se envió el último carácter del búfer de salida.                                                                                                                                                                                                 |



 

Una vez especificado un conjunto de eventos, un proceso usa la función [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) para esperar a que se produzca uno de los eventos. **WaitCommEvent se** puede usar de forma sincrónica o como una operación superpuesta. Para obtener información adicional sobre la ejecución de una función como una operación superpuesta, vea [Sincronización de](/windows/desktop/Sync/synchronization).

Cuando se produce uno de los eventos especificados en la máscara de eventos, el proceso completa la operación de espera y establece una variable de máscara de eventos para indicar el tipo de evento detectado. Si se llama a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para un recurso de comunicaciones mientras hay una espera pendiente para ese recurso, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) devuelve un error.

La [**función WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) detecta los eventos que se han producido desde la última llamada a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) **o WaitCommEvent.** Por ejemplo, si especifica el evento **EV \_ RXCHAR** como evento de espera, se satisfará una llamada a **WaitCommEvent** si hay caracteres en el búfer de entrada del controlador que han llegado desde la última llamada a **WaitCommEvent** o **SetCommMask**. Por lo tanto, dado el pseudocódigo siguiente, los caracteres recibidos entre T1 y T2 cumplirán la siguiente llamada a **WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Al supervisar un evento que se produce cuando una señal (CTS, DSR, entre otros) cambia de estado, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) notifica el cambio, pero no el estado actual. Para consultar el estado actual de las señales CTS (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect) y ring indicator, un proceso puede usar la función [**GetCommModemStatus.**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)

 

 
