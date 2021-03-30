---
title: Ejemplo de gesto de toque de Windows (MTGestures)
description: En esta sección se describe el ejemplo de gestos táctiles de Windows.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch, gestos
- Windows Touch, ejemplos de gestos
- Ejemplos de gestos
- gestos, código de ejemplo
- gestos, ejemplos de código
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788722"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Ejemplo de gesto de toque de Windows (MTGestures)

En esta sección se describe el ejemplo de gestos táctiles de Windows.

En el ejemplo de gestos táctiles de Windows se muestra cómo usar mensajes de movimiento para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) mediante el control del mensaje de [**WM_GESTURE**](wm-gesture.md) . En la captura de pantalla siguiente se muestra el aspecto del ejemplo cuando se está ejecutando.

![captura de pantalla que muestra el ejemplo de gesto de toque de Windows cuando se está ejecutando, con un rectángulo blanco girado y con contorno negro en la pantalla](images/mtgestures.png)

En este ejemplo, los mensajes de gestos se pasan a un motor de gestos, que después llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos. Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando TAP de dos dedos para habilitar o deshabilitar las líneas diagonales en el cuadro representado. Un usuario realiza el gesto de puntear dos dedos, que genera un mensaje controlado por el programa. Cuando se controla el mensaje, cambiará un valor booleano para representar las diagonales en el objeto de dibujo y, a continuación, el objeto representará las líneas diagonales.

En el código siguiente se muestra cómo se pasan mensajes de gesto al motor de gestos desde el método WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

En el código siguiente se muestra cómo el motor de gestos controla el comando TAP de dos dedos.

```C++
// Two-finger tap command
void CMyGestureEngine::ProcessTwoFingerTap(void)
{
    if(_pcRect)
    {
        _pcRect->ToggleDrawDiagonals();
    }
}
```

En el código siguiente se muestra cómo el objeto de dibujo alterna sus diagonales.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

En el código siguiente se muestra cómo el objeto representa las líneas diagonales en su método draw.

```C++
    if(_bDrawDiagonals)
    {
        // draw diagonals
        MoveToEx(hdc,ptRect[0].x,ptRect[0].y,NULL);
        LineTo(hdc,ptRect[2].x,ptRect[2].y);
        MoveToEx(hdc,ptRect[1].x,ptRect[1].y,NULL);
        LineTo(hdc,ptRect[3].x,ptRect[3].y);
    }
```

## <a name="related-topics"></a>Temas relacionados

[Aplicación de gestos multitáctil (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicación de gestos múltiples táctiles (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)
