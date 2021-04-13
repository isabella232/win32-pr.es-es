---
title: Bloc Dete táctil de Windows con el ejemplo de lápiz Real-Time (C#)
description: En el ejemplo de Bloc de entradas táctiles de Windows (MTScratchpadRTStylus) se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch, ejemplos de Bloc de pruebas
- Ejemplos de Bloc Dete
- Touch de Windows, objeto de lápiz en tiempo real (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 4cf9ab2e451dcdcaaee808083ca42c420778f231
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358680"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a><span data-ttu-id="d9254-108">Bloc Dete táctil de Windows con el ejemplo de lápiz Real-Time (C#)</span><span class="sxs-lookup"><span data-stu-id="d9254-108">Windows Touch Scratchpad using the Real-Time Stylus Sample (C#)</span></span>

<span data-ttu-id="d9254-109">En el ejemplo de Bloc de entradas táctiles de Windows ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana.</span><span class="sxs-lookup"><span data-stu-id="d9254-109">The Windows Touch Scratchpad sample ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) shows how to use Windows Touch messages to draw traces of the touch points to a window.</span></span> <span data-ttu-id="d9254-110">El seguimiento del dedo principal, el que se colocó en primer lugar en el digitalizador, se dibuja en negro.</span><span class="sxs-lookup"><span data-stu-id="d9254-110">The trace of the primary finger, the one that was put on the digitizer first, is drawn in black.</span></span> <span data-ttu-id="d9254-111">Los dedos secundarios se dibujan en seis colores más: rojo, verde, azul, aguamarina, fucsia y amarillo.</span><span class="sxs-lookup"><span data-stu-id="d9254-111">Secondary fingers are drawn in six other colors: red, green, blue, cyan, magenta and yellow.</span></span> <span data-ttu-id="d9254-112">En la captura de pantalla siguiente se muestra el aspecto que podría tener la aplicación durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="d9254-112">The following screen shot shows how the application could look while running.</span></span>

![captura de pantalla que muestra el ejemplo de Bloc Dete táctil de Windows con el lápiz en tiempo real en c Sharp, con líneas onduladas de color negro y rojo en la pantalla](images/mtscratchpadrtstyluscs.png)

<span data-ttu-id="d9254-114">En este ejemplo, se crea el objeto del lápiz Real-Time (RTS) y se habilita la compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="d9254-114">For this sample, the Real-Time Stylus (RTS) object is created and support for multiple contact points is enabled.</span></span> <span data-ttu-id="d9254-115">Se agrega un complemento DynamicRenderer al RTS para representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="d9254-115">A DynamicRenderer plug-in is added to the RTS to render content.</span></span> <span data-ttu-id="d9254-116">Un complemento, EventHandlerPlugIn, se implementa para realizar un seguimiento del número de dedos y para cambiar el color que está dibujando el representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="d9254-116">A plug-in, EventHandlerPlugIn, is implemented to track down the number of fingers and to change the color that the dynamic renderer is drawing.</span></span> <span data-ttu-id="d9254-117">Con ambos complementos en la pila de complementos RTS, la aplicación de Bloc Dete táctil de Windows representará el contacto principal en blanco y el resto de los contactos en los distintos colores.</span><span class="sxs-lookup"><span data-stu-id="d9254-117">With both plug-ins in the RTS plug-in stack, the Windows Touch Scratchpad application will render the primary contact in black and the rest of the contacts in the various colors.</span></span>

<span data-ttu-id="d9254-118">En el código siguiente se muestra cómo el EventHandlerPlugIn aumenta y disminuye un recuento del número de contactos y establece el color del representador dinámico.</span><span class="sxs-lookup"><span data-stu-id="d9254-118">The following code shows how the EventHandlerPlugIn increments and decrements a count of the number of contacts and sets the color of the dynamic renderer.</span></span>

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

<span data-ttu-id="d9254-119">En el código siguiente se muestra cómo se crea el RTS con compatibilidad con varios puntos de contacto.</span><span class="sxs-lookup"><span data-stu-id="d9254-119">The following code shows how the RTS is created with multiple contact point support.</span></span>

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

<span data-ttu-id="d9254-120">Una vez que el color del objeto DynamicRenderer ha cambiado y se han dibujado trazos, una llamada a DynamicRenderer:: Refresh hará que aparezcan los nuevos trazos.</span><span class="sxs-lookup"><span data-stu-id="d9254-120">After the DynamicRenderer object's color has changed and strokes have been drawn, a call to DynamicRenderer::Refresh will cause the new strokes to appear.</span></span> <span data-ttu-id="d9254-121">En el código siguiente se muestra cómo se realiza este procedimiento en el método OnPaintHandler.</span><span class="sxs-lookup"><span data-stu-id="d9254-121">The following code shows how this is performed in the OnPaintHandler method.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="d9254-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d9254-122">Related topics</span></span>

<span data-ttu-id="d9254-123">[Aplicación de Bloc Dete multitáctil (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [aplicación de Bloc Dete multitáctil (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)</span><span class="sxs-lookup"><span data-stu-id="d9254-123">[Multi-touch Scratchpad Application (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [Multi-touch Scratchpad Application (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows Touch Samples](windows-touch-samples.md)</span></span>
