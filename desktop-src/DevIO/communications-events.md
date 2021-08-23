---
description: Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar cuándo cambian el estado las señales CTS (clear-to-send) y DSR (data-set-ready).
ms.assetid: 5d2a7bf3-a972-474b-b8ca-da3351f1e59c
title: Eventos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bcb257652723a2464ff66c862f574f6aeae621bc6459b55d250f785d0b0895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815495"
---
# <a name="communications-events"></a>Eventos de comunicaciones

Un proceso puede supervisar un conjunto de eventos que se producen en un recurso de comunicaciones. Por ejemplo, una aplicación puede usar la supervisión de eventos para determinar cuándo cambian el estado las señales CTS (clear-to-send) y DSR (data-set-ready).

Un proceso puede supervisar eventos en un recurso de comunicaciones determinado mediante la [**función SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para crear una máscara de eventos. Para determinar la máscara de eventos actual para un recurso de comunicaciones, un proceso puede usar la [**función GetCommMask.**](/windows/desktop/api/Winbase/nf-winbase-getcommmask) Los valores siguientes especifican eventos que se pueden supervisar.



| Valor           | Significado                                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EV \_ BREAK**   | Se ha detectado una interrupción en la entrada.                                                                                                                                                                                                                    |
| **EV \_ CTS**     | La señal CTS (clear-to-send) cambió de estado.                                                                                                                                                                                                     |
| **EV \_ DSR**     | El estado de la señal DSR (data-set-ready) ha cambiado.                                                                                                                                                                                                    |
| **EV \_ ERR**     | Error de estado de línea. Los errores de estado de línea **son CE \_ FRAME,** **CE \_ OVERRUN** y **CE \_ RXPARITY.**                                                                                                                                        |
| **EV \_ RING**    | Se ha detectado un indicador de llamada.                                                                                                                                                                                                                    |
| **EV \_ RLSD**    | El estado de la señal RLSD (receive-line-signal-detect) ha cambiado.                                                                                                                                                                                       |
| **EV \_ RXCHAR**  | Se ha recibido y colocado un carácter en el búfer de entrada.                                                                                                                                                                                          |
| **EV \_ RXFLAG**  | El carácter de evento se recibió y se colocó en el búfer de entrada. El carácter de evento se especifica en la estructura [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) del dispositivo, que se aplica a un puerto serie mediante la [**función SetCommState.**](/windows/desktop/api/Winbase/nf-winbase-setcommstate) |
| **EV \_ TXEMPTY** | Se envió el último carácter del búfer de salida.                                                                                                                                                                                                 |



 

Una vez especificado un conjunto de eventos, un proceso usa la [**función WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) para esperar a que se produzca uno de los eventos. **WaitCommEvent se** puede usar sincrónicamente o como una operación superpuesta. Para obtener información adicional sobre cómo ejecutar una función como una operación superpuesta, vea [Synchronization](/windows/desktop/Sync/synchronization).

Cuando se produce uno de los eventos especificados en la máscara de eventos, el proceso completa la operación de espera y establece una variable de máscara de eventos para indicar el tipo de evento detectado. Si se llama a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) para un recurso de comunicaciones mientras hay una espera pendiente para ese recurso, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) devuelve un error.

La [**función WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) detecta los eventos que se han producido desde la última llamada a [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask) **o WaitCommEvent.** Por ejemplo, si especifica el evento **EV \_ RXCHAR** como un evento de espera, se cumplirá una llamada a **WaitCommEvent** si hay caracteres en el búfer de entrada del controlador que han llegado desde la última llamada a **WaitCommEvent** o **SetCommMask.** Por lo tanto, dado el pseudocódigo siguiente, los caracteres recibidos entre T1 y T2 cumplirán la siguiente llamada **a WaitCommEvent**.


```C++
while (!bFinished) 
{ 
    WaitCommEvent(args)
 
T1: // Read bytes 
    // Process bytes 

T2: 
}
```



Al supervisar un evento que se produce cuando una señal (CTS, DSR, entre otras) cambia de estado, [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent) notifica el cambio, pero no el estado actual. Para consultar el estado actual de cts (clear-to-send), DSR (data-set-ready), RLSD (receive-line-signal-detect) y señales de indicador de anillo, un proceso puede usar la función [**GetCommModemStatus.**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)

 

 
