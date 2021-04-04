---
title: Ejemplo de Bloc Dete táctil de Windows (C++)
description: En el ejemplo de Bloc Dete táctil de Windows se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana.
ms.assetid: 6c4b4595-1e95-499c-b045-b5ae01aa5a6e
keywords:
- Windows Touch, ejemplos de código
- Windows Touch, código de ejemplo
- Windows Touch, ejemplos de Bloc de pruebas
- Ejemplos de Bloc Dete
ms.topic: article
ms.date: 02/18/2020
ms.openlocfilehash: afdd39e886d97671942b4ff67a74c0da75924fbb
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078570"
---
# <a name="windows-touch-scratchpad-sample-c"></a>Ejemplo de Bloc Dete táctil de Windows (C++)

En el ejemplo de Bloc Dete [táctil de Windows](https://github.com/MicrosoftDocs/win32-pr/blob/master/desktop-src/wintouch/windows-touch-scratchpad-sample--mtscratchpadwmtouch-.md) se muestra cómo usar mensajes táctiles de Windows para dibujar seguimientos de los puntos táctiles en una ventana. El seguimiento del dedo principal, el que se colocó en primer lugar en el digitalizador, se dibuja en negro. Los dedos secundarios se dibujan en seis colores más: rojo, verde, azul, aguamarina, fucsia y amarillo. En la imagen siguiente se muestra el aspecto que podría tener la aplicación durante la ejecución.

![captura de pantalla que muestra el Bloc de las ventanas táctiles de Windows, con garabatos rojo y negro en la pantalla](images/mtscratchpadwmtouch.png)

Para esta aplicación, la ventana se registra como una ventana táctil; los mensajes táctiles se interpretan para agregar puntos táctiles a objetos de trazo y los trazos de tinta se representan en la pantalla en el controlador de mensajes de **WM_PAINT** .

En el código siguiente se muestra cómo se registra la ventana como una ventana táctil.

```C++
    // Register application window for receiving multitouch input. Use default settings.
    if(!RegisterTouchWindow(hWnd, 0))
    {
        MessageBox(hWnd, L"Cannot register application window for multitouch input", L"Error", MB_OK);
        return FALSE;
    }
```

En el código siguiente se muestra cómo se usan los mensajes táctiles para agregar puntos táctiles a trazos de lápiz.

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

En el código siguiente se muestra cómo se dibujan los trazos de lápiz en la pantalla en el controlador de mensajes de **WM_PAINT** .

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

En el código siguiente se muestra cómo el objeto Stroke representa trazos en la pantalla.

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

[Ejemplo de Bloc Dete táctil de Windows (C#)](windows-touch-scratchpad-sample-in-c---mtscratchpadwmtouchcs-.md), [aplicación de Bloc Dete multitáctil (WM_TOUCH/c #)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/CS), [aplicación de Bloc dete multitáctil (WM_TOUCH/C + +)](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/Touch/MTScratchpadWMTouch/cpp), [ejemplos de Windows Touch](windows-touch-samples.md)
