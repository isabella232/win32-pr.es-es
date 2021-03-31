---
title: Ejemplo de Bloc Dete táctil de Windows en C (MTScratchpadWMTouchCS)
description: En el ejemplo de Bloc de entradas táctiles de Windows en C# se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 652124be-01a8-4df4-b590-e5c2ca3f012c
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch, ejemplos de Bloc de pruebas
- Ejemplos de Bloc Dete
ms.topic: article
ms.date: 10/28/2019
ms.openlocfilehash: 2d91c08c55f0d5b29a170a3a01c6ee882fad765f
ms.sourcegitcommit: c7fa8fc137714433c8d18b1bf71e9cf0b5bf5e80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/25/2020
ms.locfileid: "104078487"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Ejemplo de Bloc Dete táctil de Windows (C#)

[En el ejemplo de Bloc de entradas táctiles de Windows en C#](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS) se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se colocó en primer lugar en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en seis colores más: rojo, verde, azul, aguamarina, fucsia y amarillo. La siguiente imagen muestra el aspecto que podría tener la aplicación cuando se ejecuta.

![captura de pantalla que muestra el ejemplo de Bloc Dete táctil de Windows en c Sharp, con líneas onduladas de color negro, verde, azul y rojo en la pantalla](images/mtscratchpadwmtouchcs.png)

En este ejemplo, se crea un formulario táctil para controlar los mensajes de [**WM_TOUCH**](wm-touchdown.md) . Este formulario se hereda para habilitar Windows Touch en la aplicación de Bloc Dete. Cuando los mensajes de **WM_TOUCH** llegan al formulario, se interpretan en puntos y se agregan a la colección de trazos. La colección Strokes se representa en el objeto Graphics. En el código siguiente se muestra cómo se registra el formulario táctil para controlar **WM_TOUCH** mensajes y cómo trata **WM_TOUCH** mensajes.

```CSharp
        private void OnLoadHandler(Object sender, EventArgs e)
        {
            try
            {
                // Registering the window for multi-touch, using the default settings.
                // p/invoking into user32.dll
                if (!RegisterTouchWindow(this.Handle, 0))
                {
                    Debug.Print("ERROR: Could not register window for multi-touch");
                }
            }
            catch (Exception exception)
            {
                Debug.Print("ERROR: RegisterTouchWindow API not available");
                Debug.Print(exception.ToString());
                MessageBox.Show("RegisterTouchWindow API not available", "MTScratchpadWMTouch ERROR",
                    MessageBoxButtons.OK, MessageBoxIcon.Error, MessageBoxDefaultButton.Button1, 0);
            }
        }
(...)
        [PermissionSet(SecurityAction.Demand, Name = "FullTrust")]
        protected override void WndProc(ref Message m)
        {
            // Decode and handle WM_TOUCH message.
            bool handled;
            switch (m.Msg)
            {
                case WM_TOUCH:
                    handled = DecodeTouch(ref m);
                    break;
                default:
                    handled = false;
                    break;
            }

            // Call parent WndProc for default message processing.
            base.WndProc(ref m);

            if (handled)
            {
                // Acknowledge event if handled.
                m.Result = new System.IntPtr(1);
            }
        }
```

En el código siguiente se muestra cómo se interpreta el mensaje Touch de Windows y se agregan los datos a las colecciones de trazos.

```CSharp
        private bool DecodeTouch(ref Message m)
        {
            // More than one touchinput may be associated with a touch message,
            // so an array is needed to get all event information.
            int inputCount = LoWord(m.WParam.ToInt32()); // Number of touch inputs, actual per-contact messages

            TOUCHINPUT[] inputs; // Array of TOUCHINPUT structures
            inputs = new TOUCHINPUT[inputCount]; // Allocate the storage for the parameters of the per-contact messages

            // Unpack message parameters into the array of TOUCHINPUT structures, each
            // representing a message for one single contact.
            if (!GetTouchInputInfo(m.LParam, inputCount, inputs, touchInputSize))
            {
                // Get touch info failed.
                return false;
            }

            // For each contact, dispatch the message to the appropriate message
            // handler.
            bool handled = false; // Boolean, is message handled
            for (int i = 0; i < inputCount; i++)
            {
                TOUCHINPUT ti = inputs[i];

                // Assign a handler to this message.
                EventHandler<WMTouchEventArgs> handler = null;     // Touch event handler
                if ((ti.dwFlags & TOUCHEVENTF_DOWN) != 0)
                {
                    handler = Touchdown;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_UP) != 0)
                {
                    handler = Touchup;
                }
                else if ((ti.dwFlags & TOUCHEVENTF_MOVE) != 0)
                {
                    handler = TouchMove;
                }

                // Convert message parameters into touch event arguments and handle the event.
                if (handler != null)
                {
                    // Convert the raw touchinput message into a touchevent.
                    WMTouchEventArgs te = new WMTouchEventArgs(); // Touch event arguments

                    // TOUCHINFO point coordinates and contact size is in 1/100 of a pixel; convert it to pixels.
                    // Also convert screen to client coordinates.
                    te.ContactY = ti.cyContact/100;
                    te.ContactX = ti.cxContact/100;
                    te.Id = ti.dwID;
                    {
                        Point pt = PointToClient(new Point(ti.x/100, ti.y/100));
                        te.LocationX = pt.X;
                        te.LocationY = pt.Y;
                    }
                    te.Time = ti.dwTime;
                    te.Mask = ti.dwMask;
                    te.Flags = ti.dwFlags;

                    // Invoke the event handler.
                    handler(this, te);

                    // Mark this event as handled.
                    handled = true;
                }
            }

            CloseTouchInputHandle(m.LParam);

            return handled;
        }
    }
```

En el código siguiente se muestra cómo se muestra una colección de trazos.

```CSharp
        public void Draw(Graphics graphics)
        {
            if ((points.Count < 2) || (graphics == null))
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

En el código siguiente se muestra cómo se muestran los objetos de trazo individuales con un objeto gráfico.

```CSharp
        public void Draw(Graphics graphics)
        {
            if(points.Count < 2 || graphics == null)
            {
                return;
            }

            Pen pen = new Pen(color, penWidth);
            graphics.DrawLines(pen, (Point[]) points.ToArray(typeof(Point)));
        }
```

## <a name="related-topics"></a>Temas relacionados

[Ejemplo de Bloc de funciones táctiles de Windows (C++)](windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md), [aplicación de Bloc Dete multitáctil (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [aplicación de Bloc dete multitáctil (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)

