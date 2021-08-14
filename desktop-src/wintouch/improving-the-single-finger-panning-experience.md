---
title: Mejora de la Single-Finger de movimiento panorámico
description: Si compila una aplicación que tiene como destino Windows Touch, proporciona automáticamente compatibilidad básica de movimiento panorámico. Sin embargo, puede usar el mensaje WM GESTURE para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo \_ dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Movimiento panorámico táctil con un solo dedo
- Windows Táctil, movimiento panorámico
- Windows Touch,scroll bars
- Windows Touch,flicks
- Windows Mensajes táctiles y de panorámica de gestos
- Windows Comentarios táctiles y límites
- movimiento panorámico con un solo dedo
- movimiento panorámico, con un solo dedo
- movimiento panorámico, comentarios de límites
- barras de desplazamiento, movimiento panorámico con un solo dedo
- gestos, movimiento panorámico con un solo dedo
- barras de desplazamiento, deshabilitar
- flicks,disabling
- gestos, mensajes de panorámica de gestos
- movimiento panorámico, mensajes de desplazamiento panorámico de gestos
- comentarios de límites, movimiento panorámico con un solo dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435448"
---
# <a name="improving-the-single-finger-panning-experience"></a>Mejora de la Single-Finger de movimiento panorámico

Si compila una aplicación que tiene como destino Windows Touch, proporciona automáticamente compatibilidad básica de movimiento panorámico. Sin embargo, puede usar el mensaje [**WM \_ GESTURE**](wm-gesture.md) para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo dedo.

## <a name="overview"></a>Introducción

Para mejorar la experiencia de movimiento panorámico con un solo dedo, siga estos pasos, como se explica en las secciones posteriores de este tema:

-   Cree una aplicación con barras de desplazamiento y con los gestos deshabilitados.
-   Agregue compatibilidad para los mensajes de movimiento de panorámica.
-   Habilitar el salto.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Creación de una aplicación con barras de desplazamiento y con gestos deshabilitados

Antes de comenzar, debe crear una aplicación con barras de desplazamiento. En la [sección Compatibilidad heredada para el movimiento panorámico con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) se explica este proceso. Si desea empezar con el contenido de ejemplo, vaya a esa sección y cree una aplicación con barras de desplazamiento y, a continuación, deshabilite los gestos. Si ya tiene una aplicación con barras de desplazamiento en funcionamiento, deshabilite los gestos como se describe en esa sección.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Agregar compatibilidad de movimiento panorámico personalizado para mensajes de desplazamiento panorámico de gestos

Para admitir mensajes de movimiento de panorámica, debe controlarlos en el **método WndProc.** Los mensajes de gesto se usan para determinar las diferencias horizontales y verticales de los mensajes de desplazamiento horizontal. Las diferencias se usan para actualizar el objeto de barra de desplazamiento, que actualiza la interfaz de usuario.

En primer lugar, actualice Windows configuración de versión del archivo targetver.h para habilitar Windows Touch. El código siguiente muestra las distintas Windows de versión que deben reemplazar a las de targetver.h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



A continuación, agregue el archivo UXTheme.h al proyecto y agregue la biblioteca uxtheme.lib a las dependencias adicionales del proyecto.


```C++
#include <uxtheme.h>
```



A continuación, agregue las siguientes variables a la parte superior de **la función WndProc.** Se usarán en cálculos para el movimiento panorámico.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



A continuación, agregue el controlador para el mensaje [**\_ WM GESTURE**](wm-gesture.md) para que las barras de desplazamiento se actualicen con diferencias basadas en gestos de movimiento panorámico. Esto le proporciona un control mucho más preciso del movimiento panorámico.

El código siguiente obtiene la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) de *lParam,* guarda la última coordenada y de la estructura y determina el cambio de posición para actualizar el objeto de barra de desplazamiento. El código siguiente debe colocarse en la **instrucción switch de WndProc.**


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



Ahora, cuando realice el gesto de desplazamiento horizontal en la ventana, verá el desplazamiento de texto con inercia. En este punto, es posible que desee cambiar el texto para que tenga más líneas para que pueda explorar el movimiento panorámico de secciones grandes de texto.

## <a name="boundary-feedback-in-wndproc"></a>Comentarios de límites en WndProc

Los comentarios de límites son un tipo de comentarios visuales que se dan a los usuarios cuando llegan al final de un área que se puede desplazar. La aplicación la desencadena cuando se alcanza un límite. En la implementación de ejemplo anterior del mensaje [**WM \_ GESTURE,**](wm-gesture.md) la condición final del caso WM GESTURE se usa para probar que se ha alcanzado el final de una región que se puede `(si.nPos == si.yPos)` **\_** desplazar. Las variables siguientes se usan para realizar un seguimiento de los valores y probar los errores.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



El caso del gesto de panorámica se actualiza para desencadenar comentarios de límites. El código siguiente muestra el caso **GID \_ PAN** del controlador [**de mensajes WM \_ GESTURE.**](wm-gesture.md)


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



Ahora, la ventana de la aplicación debe tener comentarios sobre los límites cuando un usuario se desplaza más allá de la parte inferior de la región de la barra de desplazamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows Gestos táctiles](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 