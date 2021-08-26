---
title: Windows Touch Scratchpad mediante el Real-Time stylus (C#)
description: Revise un ejemplo Windows C# de Touch Scratchpad (MTScratchpadRTStylus), que muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 8e80672f-0780-4dec-a9b4-afec0f7782ad
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch,Scratchpad samples
- Ejemplos de Scratchpad
- Windows Objeto Touch,Real-time Stylus (RTS)
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: a76f7a66f8bc26b7e1cad8f1fa71d9703f0c0da1ad1452a078b374a0f1603238
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055855"
---
# <a name="windows-touch-scratchpad-using-the-real-time-stylus-sample-c"></a>Windows Touch Scratchpad mediante el Real-Time stylus (C#)

En Windows ejemplo de Touch Scratchpad[(MTScratchpadRTStylus)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS)se muestra cómo usar los mensajes de Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, cian, rojo, rojo y amarillo. En la siguiente captura de pantalla se muestra el aspecto de la aplicación mientras se ejecuta.

![captura de pantalla que muestra el ejemplo de scratchpad táctil de Windows con el lápiz óptico en tiempo real en c sharp, con ondulaciones de color negro y rojo en la pantalla](images/mtscratchpadrtstyluscs.png)

En este ejemplo, se crea el Real-Time Stylus (RTS) y se habilita la compatibilidad con varios puntos de contacto. Se agrega un complemento DynamicRenderer al RTS para representar el contenido. Se implementa un complemento, EventHandlerPlugIn, para realizar un seguimiento del número de dedos y cambiar el color que está dibujando el representador dinámico. Con ambos complementos en la pila de complementos RTS, la aplicación Windows Touch Scratchpad representará el contacto principal en negro y el resto de los contactos en los distintos colores.

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

El código siguiente muestra cómo se crea rts con compatibilidad con varios puntos de contacto.

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

Aplicación Scratchpad multi touch [(RTS/C#),](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/CS) [aplicación scratchpad multi touch (RTS/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadRTStylus/cpp), [Windows touch samples](windows-touch-samples.md)
