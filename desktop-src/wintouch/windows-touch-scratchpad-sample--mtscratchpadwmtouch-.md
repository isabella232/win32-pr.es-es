---
title: Windows Ejemplo de Touch Scratchpad (C++)
description: En Windows ejemplo de Touch Scratchpad se muestra cómo usar Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch,Scratchpad samples
- Ejemplos de Scratchpad
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: 7f3be8c120a935bc1a8d65dfdd8c7ab9894e0360d3415e8c645e5b3afae87012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086260"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Windows Ejemplo de Touch Scratchpad (C++)

En [Windows ejemplo de Touch Scratchpad](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) se muestra cómo usar Windows Touch para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se ha puesto primero en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en otros seis colores: rojo, verde, azul, cian, rojo, rojo y amarillo. En la imagen siguiente se muestra el aspecto de la aplicación mientras se ejecuta.

![captura de pantalla que muestra el scratchpad táctil de Windows, con ondulaciones en rojo y negro en la pantalla](images/mtscratchpadwmtouch.png)

Para esta aplicación, la ventana se registra como una ventana táctil, los mensajes táctiles se interpretan para  agregar puntos táctiles a objetos de trazo y los trazos de lápiz se representan en la pantalla en el controlador de mensajes WM_PAINT de entrada.

El código siguiente muestra cómo se registra la ventana como una ventana táctil.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

El código siguiente muestra cómo se usan los mensajes táctiles para agregar puntos táctiles a trazos de lápiz.

```C++
        // WM_TOUCH message handlers
        case WM_TOUCH:
            {
                // WM_TOUCH message can contain several messages from different contacts
                // packed together.
                // Message parameters need to be decoded:
                unsigned int numInputs = (unsigned int) wParam; // Number of actual per-contact messages
                TOUCHINPUT* ti = new TOUCHINPUT[numInputs]; // Allocate the storage for the parameters of the per-contact messages
                if(ti == NULL)
                {
                    break;
                }
                // Unpack message parameters into the array of TOUCHINPUT structures, each
                // representing a message for one single contact.
                if(GetTouchInputInfo((HTOUCHINPUT)lParam, numInputs, ti, sizeof(TOUCHINPUT)))
                {
                    // For each contact, dispatch the message to the appropriate message
                    // handler.
                    for(unsigned int i=0; i<numInputs; ++i)
                    {
                        if(ti[i].dwFlags & TOUCHEVENTF_DOWN)
                        {
                            OnTouchDownHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_MOVE)
                        {
                            OnTouchMoveHandler(hWnd, ti[i]);
                        }
                        else if(ti[i].dwFlags & TOUCHEVENTF_UP)
                        {
                            OnTouchUpHandler(hWnd, ti[i]);
                        }
                    }
                }
                CloseTouchInputHandle((HTOUCHINPUT)lParam);
                delete [] ti;
            }
            break;
```

El código siguiente muestra cómo se dibujan los trazos de lápiz en la pantalla en el **WM_PAINT** de mensajes.

```C++
        case WM_PAINT:
            hdc = BeginPaint(hWnd, &ps);
            // Full redraw: draw complete collection of finished strokes and
            // also all the strokes that are currently in drawing.
            g_StrkColFinished.Draw(hdc);
            g_StrkColDrawing.Draw(hdc);
            EndPaint(hWnd, &ps);
            break;
```

El código siguiente muestra cómo el objeto de trazo representa trazos en la pantalla.

```C++
void CStroke::Draw(HDC hDC) const
{
    if(m_nCount < 2)
    {
        return;
    }

    HPEN hPen = CreatePen(PS_SOLID, 3, m_clr);
    HGDIOBJ hOldPen = SelectObject(hDC, hPen);
    Polyline(hDC, m_arrData, m_nCount);
    SelectObject(hDC, hOldPen);
    DeleteObject(hPen);
}
```

## <a name="related-topics"></a>Temas relacionados

[Windows Touch Scratchpad sample (C#),](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md) [Multi-touch Scratchpad Application (WM_TOUCH/C#)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [Multi-touch Scratchpad Application (WM_TOUCH/C++)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [Windows Touch Samples](windows-touch-samples.md)
