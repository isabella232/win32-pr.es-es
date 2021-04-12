---
title: Movimientos táctiles de Windows en el ejemplo de C (MTGesturesCS)
description: En esta sección se describe el ejemplo de gestos táctiles de Windows en C \.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
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
ms.openlocfilehash: e6ffc0e8caf63807d4df80a1b96229f2fa7b5ff9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420253"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Gestos táctiles de Windows en el ejemplo de C# (MTGesturesCS)

En esta sección se describe el ejemplo de gestos táctiles de Windows en C#.

En este ejemplo de gestos táctiles de Windows se muestra cómo usar mensajes de movimiento para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) mediante el control del mensaje de [**WM_GESTURE**](wm-gesture.md) . En la captura de pantalla siguiente se muestra el aspecto del ejemplo cuando se está ejecutando.

![captura de pantalla que muestra los gestos táctiles de Windows en el ejemplo de c Sharp cuando se está ejecutando, con un rectángulo blanco con contorno negro centrado en la pantalla](images/mtgesturescs.png)

En este ejemplo, los mensajes de gestos se pasan a un motor de gestos que, a continuación, llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos. Para que esto sea posible en C#, se crea una forma especial, TouchableForm, para controlar los mensajes de gestos. A continuación, este formulario utiliza los mensajes para realizar cambios en un objeto de dibujo, DrawingObject, para cambiar el modo en que el objeto se representa en el método Paint.

Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando pan para traducir el cuadro representado. Un usuario realiza el gesto de panorámica que genera un mensaje de [**WM_GESTURE**](wm-gesture.md) con el identificador de gesto GID_PAN. El TouchableForm controla estos mensajes y actualiza la posición del objeto de dibujo, y el objeto se representará a su vez traducido.

En el código siguiente se muestra cómo el controlador de gestos recupera los parámetros del mensaje de [**WM_GESTURE**](wm-gesture.md) y, a continuación, realiza la traducción en el cuadro representado a través de una llamada al método move del objeto de dibujo.

```CSharp
            switch (gi.dwID)
            {
                case GID_BEGIN:
                case GID_END:
                    break;
               (...)
                case GID_PAN:
                    switch (gi.dwFlags)
                    {
                        case GF_BEGIN:
                            _ptFirst.X = gi.ptsLocation.x;
                            _ptFirst.Y = gi.ptsLocation.y;
                            _ptFirst = PointToClient(_ptFirst);
                            break;

                        default:
                            // We read the second point of this gesture. It is a
                            // middle point between fingers in this new position
                            _ptSecond.X = gi.ptsLocation.x;
                            _ptSecond.Y = gi.ptsLocation.y;
                            _ptSecond = PointToClient(_ptSecond);

                            // We apply move operation of the object
                            _dwo.Move(_ptSecond.X - _ptFirst.X, _ptSecond.Y - _ptFirst.Y);

                            Invalidate();

                            // We have to copy second point into first one to
                            // prepare for the next step of this gesture.
                            _ptFirst = _ptSecond;
                            break;
                    }
                    break;
```

En el código siguiente se muestra cómo el método move del objeto Drawing actualiza las variables de posición internas.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

En el código siguiente se muestra cómo se utiliza la posición en el método paint del objeto Drawing.

```CSharp
public void Paint(Graphics graphics)
        {
(...)
            for (int j = 0; j < 5; j++)
            {
                int idx = arrPts[j].X;
                int idy = arrPts[j].Y;

                // rotation
                arrPts[j].X = (int)(idx * dCos + idy * dSin);
                arrPts[j].Y = (int)(idy * dCos - idx * dSin);

                // translation
                arrPts[j].X += _ptCenter.X;
                arrPts[j].Y += _ptCenter.Y;
            }
(...)
        }
```

Los gestos de movimiento panorámico harán que el cuadro dibujado se represente.

## <a name="related-topics"></a>Temas relacionados

[Aplicación de gestos multitáctil (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicación de gestos múltiples táctiles (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)
