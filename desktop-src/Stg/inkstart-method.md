---
title: Método InkStart
description: Todos los métodos InkStart, InkDraw y InkStop utilizan construcciones GUI de Win32, como contextos de dispositivo y objetos de lápiz.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994465"
---
# <a name="inkstart-method"></a>Método InkStart

Todos los métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) utilizan construcciones GUI de Win32, como contextos de dispositivo y objetos de lápiz. Esto ilustra por qué se necesita CGuiPaper como un nivel independiente de encapsulación. Los aspectos de la GUI del papel del dibujo se controlan en CGuiPaper. El objeto de copapeles solo se envía a datos de tinta.

Otro motivo de diseño para el nivel de encapsulación CGuiPaper es la naturaleza dual de sus métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) . No solo llaman al copaper para grabar los datos de tinta a medida que se producen, sino que también dibujan una imagen visual del dibujo a medida que se produce. CGuiPaper mantiene una \_ marca m bInkSaving para administrar esta doble naturaleza. Cuando m \_ bInkSaving es false, la imagen se dibuja en la pantalla, pero los datos no se envían al papel para la grabación.

Este esquema se usa para volver a pintar cuando el usuario no mueve el mouse, pero los datos de tinta de los copapeles se reenvían a CGuiPaper para que se vuelva a dibujar automáticamente. Se puede indicar a CGuiPaper que establezca la \_ marca m bInkSaving llamando a su método [**InkSaving**](cguipaper-methods.md) .

En los fragmentos de código de ejemplo siguientes se muestran los métodos **InkStart** de GUIPAPER. CPP Y SINK. CPP.

## <a name="inkstart-method-guipapercpp"></a>Método InkStart (GUIPAPER. CPP


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a>Método InkStart (receptor. CPP

**StoClien** recibe los datos de dibujo en forma de llamadas a la interfaz **IPaperSink** conectada en su objeto COPaperSink. Estos métodos se corresponden con los métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) similares de CGuiPaper.


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



Cuando se llama a **InkStart** en el receptor, llama a CGuiPaper para desactivar el almacenamiento de entradas manuscritas en copapeles. El copaper no necesita recibir una copia en eco de los datos que envía. Cuando se llama a [**InkDraw**](inkdraw-method.md) en el receptor, simplemente pasa la llamada a **CGuiPaper:: InkDraw**. Cuando se llama a [**InkStop**](cguipaper-methods.md) en el receptor, se llama a CGuiPaper para volver a activar el almacenamiento de tinta. El resultado es una reproducción de los datos de tinta de los copapeles en CGuiPaper para su presentación únicamente.

Puede probar el comportamiento de **StoClien** cuando su **IPaperSink** se desconecta; para ello, elija la opción desconectar en el menú del receptor. Como experimento, después de desconectar el receptor, elija acerca de en el menú ayuda. Se mostrará el cuadro de diálogo acerca de, que cubrirá parte del dibujo del **StoClien**. Haga clic en aceptar en el cuadro de diálogo acerca de. Observe que la parte del dibujo que se ha tratado ha desaparecido. Los datos del dibujo no se pierden, pero parte de la imagen es. El cliente recibió el mensaje de Paint de WM \_ y emitió el método [**IPaper:: redraw**](ipaper--redraw.md) . Pero como el receptor no estaba conectado, no recibió las llamadas a **IPaperSink** para volver a dibujar el dibujo.

También puede probar este comportamiento al minimizar **StoClien** y, a continuación, restaurarlo. En este caso, se pierde toda la imagen de dibujo y es necesario volver a pintar. Para volver a dibujar la imagen de dibujo después de cualquiera de estas pruebas, use el menú de receptor para volver a conectarse y, a continuación, elija volver a [**dibujar**](ipaper--redraw.md) en el menú dibujo.

 

 




