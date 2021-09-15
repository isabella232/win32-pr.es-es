---
title: Windows Ejemplo de gesto táctil (MTGestures)
description: En esta sección se describe el Windows touch gesture.
ms.assetid: 04166c9c-5de7-409e-9d5e-dd210a3a3f11
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Táctil, gestos
- Windows Touch,Gesture samples
- Ejemplos de gestos
- gestures,sample code
- gestos, ejemplos de código
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 0e01d97e844af37caeb5c33f3cb780601da4629d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359582"
---
# <a name="windows-touch-gesture-sample-mtgestures"></a>Windows Ejemplo de gesto táctil (MTGestures)

En esta sección se describe el Windows touch gesture.

El ejemplo Windows touch gesture muestra cómo usar mensajes de gesto para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) controlando el mensaje [**WM_GESTURE.**](wm-gesture.md) En la siguiente captura de pantalla se muestra el aspecto del ejemplo cuando se ejecuta.

![captura de pantalla que muestra el ejemplo de gesto táctil de windows cuando se ejecuta, con un rectángulo blanco girado y de contorno negro en la pantalla](images/mtgestures.png)

En este ejemplo, los mensajes de gesto se pasan a un motor de gestos, que llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos. Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando pulsar con dos dedos para habilitar o deshabilitar las líneas diagonales en el cuadro representado. Un usuario realiza el gesto de pulsar con dos dedos, que genera un mensaje que controla el programa. Cuando se controla el mensaje, alterna un booleano para representar diagonales en el objeto de dibujo y, a continuación, el objeto representará las líneas diagonales.

El código siguiente muestra cómo se pasan los mensajes de gesto al motor de gestos desde el método WndProc.

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

El código siguiente muestra cómo el motor de gestos controla el comando pulsar con dos dedos.

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

El código siguiente muestra cómo el objeto de dibujo alterna sus diagonales.

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

El código siguiente muestra cómo el objeto representa líneas diagonales en su método draw.

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

[Aplicación de gestos multi táctil (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)Aplicación de gestos multi táctil [(C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows touch samples](windows-touch-samples.md)
