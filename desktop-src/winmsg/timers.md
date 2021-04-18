---
description: En este tema se describen los temporizadores. Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707225"
---
# <a name="timers"></a>Temporizadores

Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.

### <a name="in-this-section"></a>En esta sección



| Nombre                                   | Descripción                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Acerca de los temporizadores](about-timers.md)       | Describe cómo crear, identificar, establecer y eliminar temporizadores.<br/>                                                     |
| [Usar temporizadores](using-timers.md)       | Describe cómo crear y destruir temporizadores, y cómo usar un temporizador para interceptar la entrada del mouse a intervalos especificados.<br/> |
| [Referencia del temporizador](timer-reference.md) | Contiene la referencia de la API.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Funciones de temporizador



| Nombre                           | Descripción                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Destruye el temporizador especificado. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Crea un temporizador con el valor de tiempo de espera especificado.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Función de devolución de llamada definida por la aplicación que procesa los mensajes [**\_ del temporizador de WM**](wm-timer.md) . El tipo **TIMERPROC** define un puntero a esta función de devolución de llamada. [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) es un marcador de posición para el nombre de la función definida por la aplicación. <br/> |



 

### <a name="timer-notifications"></a>Notificaciones del temporizador



| Nombre                          | Descripción                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**temporizador de WM \_**](wm-timer.md) | Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador. El mensaje se expone mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . <br/> |



 

 

 
