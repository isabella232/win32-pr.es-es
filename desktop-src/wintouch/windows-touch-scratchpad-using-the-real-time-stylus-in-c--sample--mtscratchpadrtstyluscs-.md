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
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch Scratchpad con Real-Time stylus sample (C#)

El ejemplo de Windows Touch Scratchpad[(MTScratchpadRTStylus)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)muestra cómo usar mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, aguaz, rojo y amarillo. En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.

![captura de pantalla que muestra el ejemplo de scratchpad táctil de Windows con el lápiz óptico en tiempo real en c sharp, con ondulados de color negro y rojo en la pantalla](images/mtscratchpadrtstyluscs.png)

En este ejemplo, se crea Real-Time stylus (RTS) y se habilita la compatibilidad con varios puntos de contacto. Se agrega un complemento DynamicRenderer al RTS para representar el contenido. Se implementa un complemento, EventHandlerPlugIn, para realizar un seguimiento del número de dedos y cambiar el color que está dibujando el representador dinámico. Con ambos complementos en la pila del complemento RTS, la aplicación Windows Touch Scratchpad representará el contacto principal en negro y el resto de los contactos en los distintos colores.

El código siguiente muestra cómo EventHandlerPlugIn incrementa y disminuye un recuento del número de contactos y establece el color del representador dinámico.

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

El código siguiente muestra cómo se crea el RTS con compatibilidad con varios puntos de contacto.

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

Una vez que el color del objeto DynamicRenderer ha cambiado y se han dibujado trazos, una llamada a DynamicRenderer::Refresh hará que aparezcan los nuevos trazos. El código siguiente muestra cómo se realiza en el método OnPaintHandler.

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

[Aplicación scratchpad multi touch (RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [aplicación de scratchpad multi touch (RTS/C++),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp) [ejemplos de Windows Touch](windows-touch-samples.md)
