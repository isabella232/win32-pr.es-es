---
title: CMainWindow
description: En el código de ejemplo siguiente se muestra este procedimiento.
ms.assetid: a2998232-db71-48ce-b14b-5e17de147172
keywords:
- CMainWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f67fd2a00bb6f3ab082499e5ca2a4a991a9fb33159a4f43c05923ae393efcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962472"
---
# <a name="cmainwindow"></a>CMainWindow

Microsoft Windows sistema operativo traduce las siguientes acciones de usuario en mensajes de ventana estándar y los envía al procedimiento principal de la **aplicación StoClien:**

-   El usuario hace clic en el botón izquierdo del mouse o en el conmutador de propina de lápiz en los dispositivos de tableta para iniciar una secuencia de dibujo de línea.
-   El usuario hace clic y mantiene presionado el botón y mueve el mouse para dibujar una línea.
-   La secuencia finaliza cuando se libera el botón izquierdo del mouse.

En el código de ejemplo siguiente se muestra este procedimiento.

## <a name="cmainwindowwindowproc-stocliencpp"></a>CMainWindow::WindowProc (STOCLIEN. CPP)


```C++
LRESULT CMainWindow::WindowProc(
            UINT uMsg,
            WPARAM wParam,
            LPARAM lParam)
  {
    LRESULT lResult = FALSE;

    switch (uMsg)
    {
      case WM_CREATE:
        break;

      case WM_ACTIVATE:
        // A mouse click reactivates the paint procedure.
        // This is used to paint a new window when a user
        // selects a portion of the STOCLIEN window that is 
        // visible beneath another window. This message is  
        // sent in the WindowProc handle.
        if (WA_CLICKACTIVE == LOWORD(wParam))
          m_pGuiPaper->PaintWin();
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;

      case WM_SIZE:
        // Handle a resize of this window.
        m_wWidth = LOWORD(lParam);
        m_wHeight = HIWORD(lParam);
        // Inform CGuiPaper of the change.
        m_pGuiPaper->Resize(m_wWidth, m_wHeight);
        break;

      case WM_PAINT:
        // This is a message to repaint the window.
        {
          PAINTSTRUCT ps;

          if(BeginPaint(m_hWnd, &ps))
            EndPaint(m_hWnd, &ps);

          m_pGuiPaper->PaintWin();
        }
        break;

      case WM_LBUTTONDOWN:
        // Start sequence of ink drawing to the paper.
        m_pGuiPaper->InkStart(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_MOUSEMOVE:
        // Draw inking sequence data.
        m_pGuiPaper->InkDraw(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_LBUTTONUP:
        // Stop an ink drawing sequence.
        m_pGuiPaper->InkStop(LOWORD(lParam), HIWORD(lParam));
        break;

      case WM_COMMAND:
        // Dispatch and handle any Menu command messages received.
        lResult = DoMenu(wParam, lParam);
        break;

      case WM_CHAR:
        if (wParam == 0x1b)
        {
          // Exit this application if user presses the ESC key.
          ::PostMessage(m_hWnd, WM_CLOSE, 0, 0);
        }
        break;

      case WM_CLOSE:
        // The user selected Close on the main window System menu
        // or Exit on the File menu.
        // If there is unsaved ink data, then prompt
        // the user. If the user cancels, do not close the window.
        if (IDCANCEL == m_pGuiPaper->AskSave())
          break;
      case WM_QUIT:
        // When exiting the application, close any associated help
        // windows.
        // ::WinHelp(m_hWnd, m_szHelpFile, HELP_QUIT, 0);
      default:
        // If there are any messages that have not been handled,
        // send them to the default window procedure.
        lResult = ::DefWindowProc(m_hWnd, uMsg, wParam, lParam);
        break;
    }

    return(lResult);
  }
```



Una secuencia de dibujo de línea se inicia cuando el mensaje \_ WM LBUTTONDOWN entrega datos de posición del mouse.

CMainWindow tiene un puntero al objeto CGuiPaper y llama al método [**CGuiPaper::InkStart**](cguipaper-methods.md) para iniciar la secuencia de dibujo de línea.

A medida que el mouse se mueve para dibujarse, se proporciona una secuencia de mensajes **\_ WM MOUSEMOVE** independientes que contienen datos de posición del mouse al método [CGuiPaper::InkDraw.](cguipaper-methods.md)

Cuando se libera el botón izquierdo del mouse, se recibe el mensaje **\_ WM LBUTTONUP.** El [método CGuiPaper::InkStop](cguipaper-methods.md) detiene la secuencia de dibujo de línea.

 

 




