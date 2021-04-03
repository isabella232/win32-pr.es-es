---
title: Mejora de la experiencia de movimiento panorámico Single-Finger
description: Si compila una aplicación destinada a Windows Touch, proporciona automáticamente compatibilidad básica con el movimiento panorámico. Sin embargo, puede usar el \_ mensaje de gestos de WM para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Touch de Windows, movimiento panorámico con un solo dedor
- Windows Touch, movimiento panorámico
- Windows Touch, barras de desplazamiento
- Windows Touch, gestos
- Touch de Windows, mensajes de movimiento panorámico
- Windows Touch, comentarios de límite
- movimiento panorámico con un solo dedo
- movimiento panorámico, un dedo
- movimiento panorámico, comentarios de los límites
- barras de desplazamiento, movimiento panorámico con un solo dedo
- gestos, movimiento panorámico con un solo dedor
- barras de desplazamiento, deshabilitar
- gestos, deshabilitar
- gestos, mensajes de movimiento panorámico
- movimiento panorámico, mensajes de movimiento panorámico
- Comentarios de los límites, movimiento panorámico con un solo dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792165"
---
# <a name="improving-the-single-finger-panning-experience"></a>Mejora de la experiencia de movimiento panorámico Single-Finger

Si compila una aplicación destinada a Windows Touch, proporciona automáticamente compatibilidad básica con el movimiento panorámico. Sin embargo, puede usar el mensaje de [**\_ gestos de WM**](wm-gesture.md) para proporcionar compatibilidad mejorada con el movimiento panorámico con un solo dedo.

## <a name="overview"></a>Información general

Para mejorar la experiencia de movimiento panorámico con un solo dedo, siga estos pasos, como se explica en secciones posteriores de este tema:

-   Cree una aplicación con barras de desplazamiento y con los gestos deshabilitados.
-   Agregar compatibilidad para mensajes de movimiento panorámico de gestos.
-   Habilitar rebote.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Crear una aplicación con barras de desplazamiento y con gestos deshabilitados

Antes de comenzar, debe crear una aplicación con barras de desplazamiento. En la sección [compatibilidad heredada para la panorámica con barras de desplazamiento](legacy-support-for-panning-with-scrollbars.md) se explica este proceso. Si desea empezar con el contenido del ejemplo, vaya a esa sección y cree una aplicación con barras de desplazamiento y, a continuación, deshabilite los gestos. Si ya tiene una aplicación con barras de desplazamiento en funcionamiento, deshabilite los gestos tal y como se describe en esa sección.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Incorporación de compatibilidad personalizada de movimiento panorámico para mensajes de movimiento panorámico

Para admitir mensajes de movimiento panorámico de gestos, debe controlarlos en el método **WndProc** . Los mensajes de gestos se usan para determinar los diferencias horizontales y verticales de los mensajes de pan. Las diferencias se utilizan para actualizar el objeto de barra de desplazamiento, que actualiza la interfaz de usuario.

En primer lugar, actualice la configuración de la versión de Windows en el archivo targetver. h para habilitar Windows Touch. En el código siguiente se muestran los distintos valores de la versión de Windows que deben reemplazarse en targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



A continuación, agregue el archivo UXTheme. h al proyecto y agregue la biblioteca uxtheme. lib a las dependencias adicionales del proyecto.


```C++
#include <uxtheme.h>
```



A continuación, agregue las siguientes variables al principio de la función **WndProc** . Se usarán en los cálculos para la panorámica.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



A continuación, agregue el controlador del mensaje de [**\_ gestos de WM**](wm-gesture.md) para que las barras de desplazamiento se actualicen con deltas basadas en gestos de movimiento panorámico. Esto le ofrece un control mucho más preciso de la panorámica.

En el código siguiente se obtiene la estructura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) de *lParam*, se guarda la última coordenada y de la estructura y se determina el cambio en la posición para actualizar el objeto de barra de desplazamiento. El código siguiente debe colocarse en la instrucción del modificador **WndProc** .


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



Ahora, cuando realice el gesto de panorámica en la ventana, verá el texto desplazarse con inercia. En este punto, es posible que desee cambiar el texto para que tenga más líneas para poder explorar grandes secciones de texto.

## <a name="boundary-feedback-in-wndproc"></a>Comentarios de los límites en WndProc

Los comentarios de los límites son un tipo de comentarios visuales que se conceden a los usuarios cuando llegan al final de un área panorámica. Lo desencadena la aplicación cuando se alcanza un límite. En la implementación de ejemplo anterior del mensaje de [**\_ gestos de WM**](wm-gesture.md) , se usa la condición de finalización del `(si.nPos == si.yPos)` caso de **\_ gestos de WM** para probar que se ha alcanzado el final de una región de movimiento panorámico. Las variables siguientes se utilizan para realizar el seguimiento de los valores y los errores de prueba.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



El caso de gestos de panorámica se actualiza para desencadenar los comentarios de los límites. En el código siguiente se muestra el caso de **\_ pan GID** del controlador de mensajes de [**\_ gestos de WM**](wm-gesture.md) .


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



Ahora la ventana de la aplicación debe tener comentarios sobre los límites cuando un usuario se desplaza más allá de la parte inferior del área de la barra de desplazamiento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Gestos táctiles de Windows](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 