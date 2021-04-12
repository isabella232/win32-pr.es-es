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
# <a name="windows-touch-gestures-in-c-sample-mtgesturescs"></a><span data-ttu-id="38f0b-110">Gestos táctiles de Windows en el ejemplo de C# (MTGesturesCS)</span><span class="sxs-lookup"><span data-stu-id="38f0b-110">Windows Touch Gestures in C# Sample (MTGesturesCS)</span></span>

<span data-ttu-id="38f0b-111">En esta sección se describe el ejemplo de gestos táctiles de Windows en C#.</span><span class="sxs-lookup"><span data-stu-id="38f0b-111">This section describes the Windows Touch Gestures sample in C#.</span></span>

<span data-ttu-id="38f0b-112">En este ejemplo de gestos táctiles de Windows se muestra cómo usar mensajes de movimiento para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) mediante el control del mensaje de [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="38f0b-112">This Windows Touch Gestures sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="38f0b-113">En la captura de pantalla siguiente se muestra el aspecto del ejemplo cuando se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="38f0b-113">The following screen shot shows how the sample looks when it is running.</span></span>

![captura de pantalla que muestra los gestos táctiles de Windows en el ejemplo de c Sharp cuando se está ejecutando, con un rectángulo blanco con contorno negro centrado en la pantalla](images/mtgesturescs.png)

<span data-ttu-id="38f0b-115">En este ejemplo, los mensajes de gestos se pasan a un motor de gestos que, a continuación, llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos.</span><span class="sxs-lookup"><span data-stu-id="38f0b-115">For this sample, gesture messages are passed to a gesture engine which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="38f0b-116">Para que esto sea posible en C#, se crea una forma especial, TouchableForm, para controlar los mensajes de gestos.</span><span class="sxs-lookup"><span data-stu-id="38f0b-116">To make this possible in C#, a special form, TouchableForm, is created to handle gesture messages.</span></span> <span data-ttu-id="38f0b-117">A continuación, este formulario utiliza los mensajes para realizar cambios en un objeto de dibujo, DrawingObject, para cambiar el modo en que el objeto se representa en el método Paint.</span><span class="sxs-lookup"><span data-stu-id="38f0b-117">This form then uses the messages to make changes on a drawing object, DrawingObject, to change how the object renders in the Paint method.</span></span>

<span data-ttu-id="38f0b-118">Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando pan para traducir el cuadro representado.</span><span class="sxs-lookup"><span data-stu-id="38f0b-118">To help show how the sample works, consider the steps for using the pan command to translate the rendered box.</span></span> <span data-ttu-id="38f0b-119">Un usuario realiza el gesto de panorámica que genera un mensaje de [**WM_GESTURE**](wm-gesture.md) con el identificador de gesto GID_PAN.</span><span class="sxs-lookup"><span data-stu-id="38f0b-119">A user performs the pan gesture which generates a [**WM_GESTURE**](wm-gesture.md) message with the gesture identifier GID_PAN.</span></span> <span data-ttu-id="38f0b-120">El TouchableForm controla estos mensajes y actualiza la posición del objeto de dibujo, y el objeto se representará a su vez traducido.</span><span class="sxs-lookup"><span data-stu-id="38f0b-120">The TouchableForm handles this messages and updates the position of the drawing object, and the object will then render itself translated.</span></span>

<span data-ttu-id="38f0b-121">En el código siguiente se muestra cómo el controlador de gestos recupera los parámetros del mensaje de [**WM_GESTURE**](wm-gesture.md) y, a continuación, realiza la traducción en el cuadro representado a través de una llamada al método move del objeto de dibujo.</span><span class="sxs-lookup"><span data-stu-id="38f0b-121">The following code shows how the gesture handler retrieves parameters from the [**WM_GESTURE**](wm-gesture.md) message and then performs translation on the rendered box through a call to the drawing object's move method.</span></span>

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

<span data-ttu-id="38f0b-122">En el código siguiente se muestra cómo el método move del objeto Drawing actualiza las variables de posición internas.</span><span class="sxs-lookup"><span data-stu-id="38f0b-122">The following code shows how the drawing object's move method updates internal position variables.</span></span>

```CSharp
        public void Move(int deltaX,int deltaY)
        {
            _ptCenter.X += deltaX;
            _ptCenter.Y += deltaY;
        }
```

<span data-ttu-id="38f0b-123">En el código siguiente se muestra cómo se utiliza la posición en el método paint del objeto Drawing.</span><span class="sxs-lookup"><span data-stu-id="38f0b-123">The following code shows how the position is used in the drawing object's paint method.</span></span>

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

<span data-ttu-id="38f0b-124">Los gestos de movimiento panorámico harán que el cuadro dibujado se represente.</span><span class="sxs-lookup"><span data-stu-id="38f0b-124">Pan gestures will cause the drawn box to be rendered translated.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38f0b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="38f0b-125">Related topics</span></span>

<span data-ttu-id="38f0b-126">[Aplicación de gestos multitáctil (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicación de gestos múltiples táctiles (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="38f0b-126">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
