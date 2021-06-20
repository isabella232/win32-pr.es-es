---
title: Windows Touch Scratchpad con Real-Time stylus sample (C#)
description: Revise un ejemplo de C# de Windows Touch Scratchpad (MTScratchpadRTStylus), que muestra cómo usar mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Ejemplos de Windows Touch y Scratchpad
- Ejemplos de Scratchpad
- Objeto Windows Touch,Real-Time Stylus (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 3c30d3543024a48394ddd7b9b2b06a05b61f5025
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406318"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="c0828-108">Windows Touch Scratchpad con Real-Time stylus sample (C#)</span><span class="sxs-lookup"><span data-stu-id="c0828-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="c0828-109">El ejemplo de Windows Touch Scratchpad[(MTScratchpadRTStylus)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)muestra cómo usar mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="c0828-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="c0828-110">El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro.</span><span class="sxs-lookup"><span data-stu-id="c0828-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="c0828-111">Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, aguaz, rojo y amarillo.</span><span class="sxs-lookup"><span data-stu-id="c0828-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="c0828-112">En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="c0828-112">The following screen shot shows how the application could look while running.</span></span>

![captura de pantalla que muestra el ejemplo de scratchpad táctil de Windows con el lápiz óptico en tiempo real en c sharp, con ondulados de color negro y rojo en la pantalla](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="c0828-114">En este ejemplo, se crea Real-Time stylus (RTS) y se habilita la compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="c0828-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="c0828-115">Se agrega un complemento DynamicRenderer al RTS para representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="c0828-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="c0828-116">Se implementa un complemento, EventHandlerPlugIn, para realizar un seguimiento del número de dedos y cambiar el color que está dibujando el representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="c0828-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="c0828-117">Con ambos complementos en la pila del complemento RTS, la aplicación Windows Touch Scratchpad representará el contacto principal en negro y el resto de los contactos en los distintos colores.</span><span class="sxs-lookup"><span data-stu-id="c0828-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="c0828-118">El código siguiente muestra cómo EventHandlerPlugIn incrementa y disminuye un recuento del número de contactos y establece el color del representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="c0828-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

```CSharp
        public void StylusDown(RealTimeStylus sender, StylusDownData data)
        {
            // Set new stroke color to the DrawingAttributes of the DynamicRenderer
            // If there are no fingers down, this is a primary contact
            dynamicRenderer.DrawingAttributes.Color = touchColor.GetColor(cntContacts == 0);

            ++cntContacts;  // Increment finger-down counter
        }

        public void StylusUp(RealTimeStylus sender, StylusUpData data)
        {
            --cntContacts;  // Decrement finger-down counter
        }
```

<span data-ttu-id="c0828-119">El código siguiente muestra cómo se crea el RTS con compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="c0828-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            // Create RealTimeStylus object and enable it for multi-touch
            realTimeStylus = new RealTimeStylus(this);
            realTimeStylus.MultiTouchEnabled = true;

            // Create DynamicRenderer and event handler, and add them to the RTS object as synchronous plugins
            dynamicRenderer = new DynamicRenderer(this);
            eventHandler = new EventHandlerPlugIn(this.CreateGraphics(), dynamicRenderer);
            realTimeStylus.SyncPluginCollection.Add(eventHandler);
            realTimeStylus.SyncPluginCollection.Add(dynamicRenderer);

            // Enable RTS and DynamicRenderer object, and enable auto-redraw of the DynamicRenderer
            realTimeStylus.Enabled = true;
            dynamicRenderer.Enabled = true;
            dynamicRenderer.EnableDataCache = true;
        }
```

<span data-ttu-id="c0828-120">Una vez que el color del objeto DynamicRenderer ha cambiado y se han dibujado trazos, una llamada a DynamicRenderer::Refresh hará que aparezcan los nuevos trazos.</span><span class="sxs-lookup"><span data-stu-id="c0828-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="c0828-121">El código siguiente muestra cómo se realiza en el método OnPaintHandler.</span><span class="sxs-lookup"><span data-stu-id="c0828-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

```CSharp
        private void OnPaintHandler(object sender, PaintEventArgs e)
        {
            // Erase the background
            Brush brush = new SolidBrush(SystemColors.Window);
            e.Graphics.FillRectangle(brush, ClientRectangle);

            // Ask DynamicRenderer to redraw itself
            dynamicRenderer.Refresh();
        }
```

## <a name="related-topics"></a><span data-ttu-id="c0828-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c0828-122">Related topics</span></span>

<span data-ttu-id="c0828-123">[Aplicación scratchpad multi touch (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [aplicación de scratchpad multi touch (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="c0828-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
