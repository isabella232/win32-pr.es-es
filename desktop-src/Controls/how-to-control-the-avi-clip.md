---
title: Cómo controlar el clip AVI
description: En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip asociado Audio-Video intercalado (AVI).
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061918"
---
# <a name="how-to-control-the-avi-clip"></a>Cómo controlar el clip AVI

En este tema se muestra cómo usar las macros de control de animación para reproducir, detener y cerrar un clip asociado Audio-Video intercalado (AVI).

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Requisitos previos

-   C/C++
-   Windows Interfaz de usuario programación
-   Archivos AVI

## <a name="instructions"></a>Instructions


Cree una función que toma como parámetros un identificador para el control de animación y una marca que indica la acción que se va a realizar en el clip AVI asociado.

La función del siguiente ejemplo de C++ llama a una de las tres macros de control de animación [**(Animar \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play)reproducción , Animar detener [**, \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop)Animar cerrar [**) \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)en función del valor del *parámetro nAction.* El identificador del control de animación asociado al clip AVI se pasa a través del *parámetro hwndAnim.*


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

[Referencia de controles de animación](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Usar controles de animación](using-animation-control.md)
</dt> <dt>

[Control de animación](animation-control-reference.md)
</dt> </dl>

 

 




