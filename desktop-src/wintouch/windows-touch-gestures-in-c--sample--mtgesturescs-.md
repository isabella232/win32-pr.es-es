---
title: Windows Gestos táctiles en el ejemplo de C (MTGesturesCS)
description: En esta sección se describe Windows ejemplo de gestos táctiles en C\.
ms.assetid: 4b2d70bb-47e4-4448-97e2-6f6e29d1dfdf
keywords:
- Windows Touch,ejemplos de código
- Windows Touch, código de ejemplo
- Windows Táctil, gestos
- Windows Touch,Ejemplos de gestos
- Ejemplos de gestos
- gestos, código de ejemplo
- gestos, ejemplos de código
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: ac3a7c0772ad7329d14d9909b55f8a60ef6e7d7473a06fcba921297117a00b6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089914"
---
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a>Windows Gestos táctiles en el ejemplo de C# (MTGesturesCS)

En esta sección se describe Windows ejemplo de gestos táctiles en C#.

En Windows ejemplo de gestos táctiles se muestra cómo usar mensajes de gesto para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) controlando el mensaje [**WM_GESTURE.**](wm-gesture.md) En la siguiente captura de pantalla se muestra el aspecto del ejemplo cuando se ejecuta.

![captura de pantalla que muestra los gestos táctiles de las ventanas en c sharp sample when it is running, with a black-outlined white rectangle centered on the screen](images/mtgesturescs.png)

En este ejemplo, los mensajes de gesto se pasan a un motor de gestos que, a continuación, llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos. Para que esto sea posible en C#, se crea un formulario especial, TouchableForm, para controlar los mensajes de gesto. A continuación, este formulario usa los mensajes para realizar cambios en un objeto de dibujo, DrawingObject, para cambiar el modo en que el objeto se representa en Paint método.

Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando pan para traducir el cuadro representado. Un usuario realiza el gesto de panorámica que genera un mensaje [**de**](wm-gesture.md) WM_GESTURE con el identificador de gesto GID_PAN. TouchableForm controla estos mensajes y actualiza la posición del objeto de dibujo y, a continuación, el objeto se representará a sí mismo traducido.

El código siguiente muestra cómo el controlador de gestos recupera los parámetros del mensaje [**de WM_GESTURE y, a**](wm-gesture.md) continuación, realiza la traducción en el cuadro representado mediante una llamada al método de movimiento del objeto de dibujo.

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

El código siguiente muestra cómo el método de movimiento del objeto de dibujo actualiza las variables de posición internas.

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

El código siguiente muestra cómo se usa la posición en el método paint del objeto de dibujo.

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

Los gestos de panorámica harán que el cuadro dibujado se represente traducido.

## <a name="related-topics"></a>Temas relacionados

[Aplicación de gestos multi touch (C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS)Aplicación de gestos multi táctil [(C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows touch samples](windows-touch-samples.md)
