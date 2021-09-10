---
title: Procesamiento de mensajes de mensajes
description: Procesamiento de mensajes de mensajes
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- sms, mensajes
- MM_JOY1MOVE mensaje
- MM_JOY1BUTTONDOWN mensaje
- MM_JOY1BUTTONUP mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371167"
---
# <a name="processing-joystick-messages"></a>Procesamiento de mensajes de mensajes

En el ejemplo siguiente se muestra cómo una aplicación podría responder a movimientos y cambios en los estados del botón. Cuando cambia de posición, la aplicación mueve el cursor y, si se presiona cualquiera de los botones, dibuja un hueco de viñeta en el escritorio. Cuando se presiona un botón de botones, la aplicación dibuja un hueco en el escritorio y reproduce un sonido continuamente hasta que se libera un botón. Los mensajes que se van a ver [**son \_ MMMOV1MOVE,**](mm-joy1move.md) [**MM MM \_ SOAP1BUTTONDOWN**](mm-joy1buttondown.md)y [**\_ MMMUT1BUTTONUP.**](mm-joy1buttonup.md)


```C++
case MM_JOY1MOVE :                     // changed position 
    if((UINT) wParam & (JOY_BUTTON1 | JOY_BUTTON2)) 
        DrawFire(hWnd); 
    DrawSight(lParam);                 // calculates new cursor position 
    break; 
case MM_JOY1BUTTONDOWN :               // button is down 
    if((UINT) wParam & JOY_BUTTON1) 
    { 
        PlaySound(lpButton1, SND_LOOP | SND_ASYNC | SND_MEMORY); 
        DrawFire(hWnd); 
    } 
    else if((UINT) wParam & JOY_BUTTON2) 
    { 
        PlaySound(lpButton2, SND_ASYNC | SND_MEMORY |  SND_LOOP); 
        DrawFire(hWnd); 
    } 
    break; 
case MM_JOY1BUTTONUP :                 // button is up 
    sndPlaySound(NULL, 0);             // stops the sound 
    break; 

```



 

 




