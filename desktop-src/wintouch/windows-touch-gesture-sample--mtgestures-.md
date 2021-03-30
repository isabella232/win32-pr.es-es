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
# <a name="windows-touch-gesture-sample-mtgestures"></a><span data-ttu-id="3506e-110">Ejemplo de gesto de toque de Windows (MTGestures)</span><span class="sxs-lookup"><span data-stu-id="3506e-110">Windows Touch Gesture Sample (MTGestures)</span></span>

<span data-ttu-id="3506e-111">En esta sección se describe el ejemplo de gestos táctiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="3506e-111">This section describes the Windows Touch Gesture sample.</span></span>

<span data-ttu-id="3506e-112">En el ejemplo de gestos táctiles de Windows se muestra cómo usar mensajes de movimiento para traducir, girar y escalar un cuadro representado por el Interfaz de dispositivo gráfico (GDI) mediante el control del mensaje de [**WM_GESTURE**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="3506e-112">The Windows Touch Gesture sample demonstrates how to use gesture messages to translate, rotate, and scale a box rendered by the Graphics Device Interface (GDI) by handling the [**WM_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="3506e-113">En la captura de pantalla siguiente se muestra el aspecto del ejemplo cuando se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3506e-113">The following screen shot shows how the sample looks when it is running.</span></span>

![captura de pantalla que muestra el ejemplo de gesto de toque de Windows cuando se está ejecutando, con un rectángulo blanco girado y con contorno negro en la pantalla](images/mtgestures.png)

<span data-ttu-id="3506e-115">En este ejemplo, los mensajes de gestos se pasan a un motor de gestos, que después llama a métodos en objetos de dibujo para traducir, girar y escalar un objeto que tiene métodos para controlar estos comandos.</span><span class="sxs-lookup"><span data-stu-id="3506e-115">For this sample, gesture messages are passed to a gesture engine, which then calls methods on drawing objects to translate, rotate, and scale an object that has methods for handling these commands.</span></span> <span data-ttu-id="3506e-116">Para ayudar a mostrar cómo funciona el ejemplo, tenga en cuenta los pasos para usar el comando TAP de dos dedos para habilitar o deshabilitar las líneas diagonales en el cuadro representado.</span><span class="sxs-lookup"><span data-stu-id="3506e-116">To help show how the sample works, consider the steps for using the two-finger tap command to enable or disable diagonal lines in the rendered box.</span></span> <span data-ttu-id="3506e-117">Un usuario realiza el gesto de puntear dos dedos, que genera un mensaje controlado por el programa.</span><span class="sxs-lookup"><span data-stu-id="3506e-117">A user performs the two-finger tap gesture, which generates a message that is handled by the program.</span></span> <span data-ttu-id="3506e-118">Cuando se controla el mensaje, cambiará un valor booleano para representar las diagonales en el objeto de dibujo y, a continuación, el objeto representará las líneas diagonales.</span><span class="sxs-lookup"><span data-stu-id="3506e-118">When the message is handled, it will toggle a Boolean for rendering diagonals on the drawing object, and the object will then render the diagonal lines.</span></span>

<span data-ttu-id="3506e-119">En el código siguiente se muestra cómo se pasan mensajes de gesto al motor de gestos desde el método WndProc.</span><span class="sxs-lookup"><span data-stu-id="3506e-119">The following code shows how gesture messages are passed to the gesture engine from the WndProc method.</span></span>

```C++
    case WM_GESTURE:
        // The gesture-processing code is implemented in the CGestureEngine
        // class.
        return g_cGestureEngine.WndProc(hWnd,wParam,lParam);
        break;
```

<span data-ttu-id="3506e-120">En el código siguiente se muestra cómo el motor de gestos controla el comando TAP de dos dedos.</span><span class="sxs-lookup"><span data-stu-id="3506e-120">The following code shows how the gesture engine handles the two-finger tap command.</span></span>

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

<span data-ttu-id="3506e-121">En el código siguiente se muestra cómo el objeto de dibujo alterna sus diagonales.</span><span class="sxs-lookup"><span data-stu-id="3506e-121">The following code shows how the drawing object toggles its diagonals.</span></span>

```C++
void ToggleDrawDiagonals(void){_bDrawDiagonals = !_bDrawDiagonals;}
```

<span data-ttu-id="3506e-122">En el código siguiente se muestra cómo el objeto representa las líneas diagonales en su método draw.</span><span class="sxs-lookup"><span data-stu-id="3506e-122">The following code shows how the object renders diagonal lines in its draw method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="3506e-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3506e-123">Related topics</span></span>

<span data-ttu-id="3506e-124">[Aplicación de gestos multitáctil (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [aplicación de gestos múltiples táctiles (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="3506e-124">[Multi-touch Gestures Application (C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/CS), [Multi-touch Gestures Application (C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTGestures/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
