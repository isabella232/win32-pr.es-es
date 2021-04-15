---
title: Cómo controlar el clip AVI
description: En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip Audio-Video intercalado (AVI) asociado.
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488596"
---
# <a name="how-to-control-the-avi-clip"></a>Cómo controlar el clip AVI

En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip Audio-Video intercalado (AVI) asociado.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Controles de Windows](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Programación de la interfaz de usuario de Windows
-   Archivos AVI

## <a name="instructions"></a>Instrucciones


Cree una función que toma como parámetros un identificador del control Animation y una marca que indica la acción que se va a realizar en el clip AVI asociado.

En el siguiente ejemplo de C++, la función llama a una de las tres macros de control de animación ([**animar \_ reproducir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**animar \_ detener**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)y [**animar \_ cerrar**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) en función del valor del parámetro *nAcción* . El identificador del control de animación que está asociado al clip AVI se pasa a través del parámetro *hwndAnim* .


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los controles de animación](animation-control-overview.md)
</dt> <dt>

[Referencia de control de animación](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usar controles de animación](using-animation-control.md)
</dt> <dt>

[Animation (control)](animation-control-reference.md)
</dt> </dl>

 

 




