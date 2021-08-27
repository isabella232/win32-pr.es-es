---
description: En este tema se de abordan los temporizadores. Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd8eced20e7d8b1eca5ec8a952f10798f92f1650db3c77bca76aca756cdd569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110704"
---
# <a name="timers"></a>Temporizadores

Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.

### <a name="in-this-section"></a>En esta sección



| Nombre                                   | Descripción                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los temporizadores](about-timers.md)       | Describe cómo crear, identificar, establecer y eliminar temporizadores.<br/>                                                     |
| [Uso de temporizadores](using-timers.md)       | Describe cómo crear y destruir temporizadores y cómo usar un temporizador para capturar la entrada del mouse a intervalos especificados.<br/> |
| [Referencia del temporizador](timer-reference.md) | Contiene la referencia de API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Funciones de temporizador



| Nombre                           | Descripción                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Destruye el temporizador especificado. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Crea un temporizador con el valor de tiempo de espera especificado.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Función de devolución de llamada definida por la aplicación que procesa [**mensajes WM \_ TIMER.**](wm-timer.md) El **tipo TIMERPROC** define un puntero a esta función de devolución de llamada. [*TimerProc es*](/windows/win32/api/winuser/nc-winuser-timerproc) un marcador de posición para el nombre de la función definida por la aplicación. <br/> |



 

### <a name="timer-notifications"></a>Notificaciones de temporizador



| Nombre                          | Descripción                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**TEMPORIZADOR \_ WM**](wm-timer.md) | Se publica en la cola de mensajes del subproceso de instalación cuando expira un temporizador. La función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) publica el mensaje. <br/> |



 

 

 
