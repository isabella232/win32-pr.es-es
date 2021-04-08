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
# <a name="inkstart-method"></a><span data-ttu-id="4cafe-103">Método InkStart</span><span class="sxs-lookup"><span data-stu-id="4cafe-103">InkStart Method</span></span>

<span data-ttu-id="4cafe-104">Todos los métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) utilizan construcciones GUI de Win32, como contextos de dispositivo y objetos de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4cafe-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="4cafe-105">Esto ilustra por qué se necesita CGuiPaper como un nivel independiente de encapsulación.</span><span class="sxs-lookup"><span data-stu-id="4cafe-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="4cafe-106">Los aspectos de la GUI del papel del dibujo se controlan en CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="4cafe-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="4cafe-107">El objeto de copapeles solo se envía a datos de tinta.</span><span class="sxs-lookup"><span data-stu-id="4cafe-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="4cafe-108">Otro motivo de diseño para el nivel de encapsulación CGuiPaper es la naturaleza dual de sus métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4cafe-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="4cafe-109">No solo llaman al copaper para grabar los datos de tinta a medida que se producen, sino que también dibujan una imagen visual del dibujo a medida que se produce.</span><span class="sxs-lookup"><span data-stu-id="4cafe-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="4cafe-110">CGuiPaper mantiene una \_ marca m bInkSaving para administrar esta doble naturaleza.</span><span class="sxs-lookup"><span data-stu-id="4cafe-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="4cafe-111">Cuando m \_ bInkSaving es false, la imagen se dibuja en la pantalla, pero los datos no se envían al papel para la grabación.</span><span class="sxs-lookup"><span data-stu-id="4cafe-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="4cafe-112">Este esquema se usa para volver a pintar cuando el usuario no mueve el mouse, pero los datos de tinta de los copapeles se reenvían a CGuiPaper para que se vuelva a dibujar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="4cafe-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="4cafe-113">Se puede indicar a CGuiPaper que establezca la \_ marca m bInkSaving llamando a su método [**InkSaving**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4cafe-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="4cafe-114">En los fragmentos de código de ejemplo siguientes se muestran los métodos **InkStart** de GUIPAPER. CPP Y SINK. CPP.</span><span class="sxs-lookup"><span data-stu-id="4cafe-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="4cafe-115">Método InkStart (GUIPAPER. CPP</span><span class="sxs-lookup"><span data-stu-id="4cafe-115">InkStart Method (GUIPAPER.CPP)</span></span>


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



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="4cafe-116">Método InkStart (receptor. CPP</span><span class="sxs-lookup"><span data-stu-id="4cafe-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="4cafe-117">**StoClien** recibe los datos de dibujo en forma de llamadas a la interfaz **IPaperSink** conectada en su objeto COPaperSink.</span><span class="sxs-lookup"><span data-stu-id="4cafe-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="4cafe-118">Estos métodos se corresponden con los métodos **InkStart**, [**InkDraw**](inkdraw-method.md)y [**InkStop**](cguipaper-methods.md) similares de CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="4cafe-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


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



<span data-ttu-id="4cafe-119">Cuando se llama a **InkStart** en el receptor, llama a CGuiPaper para desactivar el almacenamiento de entradas manuscritas en copapeles.</span><span class="sxs-lookup"><span data-stu-id="4cafe-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="4cafe-120">El copaper no necesita recibir una copia en eco de los datos que envía.</span><span class="sxs-lookup"><span data-stu-id="4cafe-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="4cafe-121">Cuando se llama a [**InkDraw**](inkdraw-method.md) en el receptor, simplemente pasa la llamada a **CGuiPaper:: InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="4cafe-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="4cafe-122">Cuando se llama a [**InkStop**](cguipaper-methods.md) en el receptor, se llama a CGuiPaper para volver a activar el almacenamiento de tinta.</span><span class="sxs-lookup"><span data-stu-id="4cafe-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="4cafe-123">El resultado es una reproducción de los datos de tinta de los copapeles en CGuiPaper para su presentación únicamente.</span><span class="sxs-lookup"><span data-stu-id="4cafe-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="4cafe-124">Puede probar el comportamiento de **StoClien** cuando su **IPaperSink** se desconecta; para ello, elija la opción desconectar en el menú del receptor.</span><span class="sxs-lookup"><span data-stu-id="4cafe-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="4cafe-125">Como experimento, después de desconectar el receptor, elija acerca de en el menú ayuda.</span><span class="sxs-lookup"><span data-stu-id="4cafe-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="4cafe-126">Se mostrará el cuadro de diálogo acerca de, que cubrirá parte del dibujo del **StoClien**.</span><span class="sxs-lookup"><span data-stu-id="4cafe-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="4cafe-127">Haga clic en aceptar en el cuadro de diálogo acerca de.</span><span class="sxs-lookup"><span data-stu-id="4cafe-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="4cafe-128">Observe que la parte del dibujo que se ha tratado ha desaparecido.</span><span class="sxs-lookup"><span data-stu-id="4cafe-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="4cafe-129">Los datos del dibujo no se pierden, pero parte de la imagen es.</span><span class="sxs-lookup"><span data-stu-id="4cafe-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="4cafe-130">El cliente recibió el mensaje de Paint de WM \_ y emitió el método [**IPaper:: redraw**](ipaper--redraw.md) .</span><span class="sxs-lookup"><span data-stu-id="4cafe-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="4cafe-131">Pero como el receptor no estaba conectado, no recibió las llamadas a **IPaperSink** para volver a dibujar el dibujo.</span><span class="sxs-lookup"><span data-stu-id="4cafe-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="4cafe-132">También puede probar este comportamiento al minimizar **StoClien** y, a continuación, restaurarlo.</span><span class="sxs-lookup"><span data-stu-id="4cafe-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="4cafe-133">En este caso, se pierde toda la imagen de dibujo y es necesario volver a pintar.</span><span class="sxs-lookup"><span data-stu-id="4cafe-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="4cafe-134">Para volver a dibujar la imagen de dibujo después de cualquiera de estas pruebas, use el menú de receptor para volver a conectarse y, a continuación, elija volver a [**dibujar**](ipaper--redraw.md) en el menú dibujo.</span><span class="sxs-lookup"><span data-stu-id="4cafe-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




