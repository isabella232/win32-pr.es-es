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
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Bloc Dete táctil de Windows con el ejemplo de lápiz Real-Time (C#)

En el ejemplo de Bloc de entradas táctiles de Windows ([MTScratchpadRTStylus](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)) se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se colocó en primer lugar en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en seis colores más: rojo, verde, azul, aguamarina, fucsia y amarillo. En la captura de pantalla siguiente se muestra el aspecto que podría tener la aplicación durante la ejecución.

![captura de pantalla que muestra el ejemplo de Bloc Dete táctil de Windows con el lápiz en tiempo real en c Sharp, con líneas onduladas de color negro y rojo en la pantalla](images/mtscratchpadrtstyluscs.png)

En este ejemplo, se crea el objeto del lápiz Real-Time (RTS) y se habilita la compatibilidad con varios puntos de contacto. Se agrega un complemento DynamicRenderer al RTS para representar el contenido. Un complemento, EventHandlerPlugIn, se implementa para realizar un seguimiento del número de dedos y para cambiar el color que está dibujando el representador dinámico. Con ambos complementos en la pila de complementos RTS, la aplicación de Bloc Dete táctil de Windows representará el contacto principal en blanco y el resto de los contactos en los distintos colores.

En el código siguiente se muestra cómo el EventHandlerPlugIn aumenta y disminuye un recuento del número de contactos y establece el color del representador dinámico.

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

En el código siguiente se muestra cómo se crea el RTS con compatibilidad con varios puntos de contacto.

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

Una vez que el color del objeto DynamicRenderer ha cambiado y se han dibujado trazos, una llamada a DynamicRenderer:: Refresh hará que aparezcan los nuevos trazos. En el código siguiente se muestra cómo se realiza este procedimiento en el método OnPaintHandler.

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

## <a name="related-topics"></a>Temas relacionados

[Aplicación de Bloc Dete multitáctil (RTS/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS), [aplicación de Bloc Dete multitáctil (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)
