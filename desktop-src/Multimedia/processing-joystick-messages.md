---
title: Procesamiento de mensajes de joystick
description: Procesamiento de mensajes de joystick
ms.assetid: d21a9d49-1fc0-4899-9083-87c3cf4e0e62
keywords:
- joysticks, mensajes
- Mensaje MM_JOY1MOVE
- Mensaje MM_JOY1BUTTONDOWN
- Mensaje MM_JOY1BUTTONUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f2337d392c0104dcb49839b19c5fb615481ee2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075524"
---
# <a name="processing-joystick-messages"></a>Procesamiento de mensajes de joystick

En el ejemplo siguiente se muestra cómo una aplicación podría responder a los movimientos del joystick y a los cambios en los Estados del botón. Cuando el joystick cambia de posición, la aplicación mueve el cursor y, si se presiona cualquiera de los botones, dibuja un orificio de viñeta en el escritorio. Cuando se presiona un botón del joystick, la aplicación dibuja un orificio en el escritorio y reproduce un sonido continuamente hasta que se suelta un botón. Los mensajes que se van a inspeccionar son [**mm \_ JOY1MOVE**](mm-joy1move.md), [**mm \_ JOY1BUTTONDOWN**](mm-joy1buttondown.md)y [**mm \_ JOY1BUTTONUP**](mm-joy1buttonup.md).


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



 

 




