---
title: Método PaintWin
description: Método PaintWin
ms.assetid: e89794e6-c059-4531-a1e3-3a4972e0218d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b30e7a52640255934762943f910e367d76088d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357789"
---
# <a name="paintwin-method"></a><span data-ttu-id="b9c20-103">Método PaintWin</span><span class="sxs-lookup"><span data-stu-id="b9c20-103">PaintWin Method</span></span>

<span data-ttu-id="b9c20-104">El siguiente es el método **PaintWin** de CGUIPAPER de GUIPAPER. CPP.</span><span class="sxs-lookup"><span data-stu-id="b9c20-104">The following is CGuiPaper's **PaintWin** method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::PaintWin(void)
  {
    HRESULT hr = E_FAIL;
    COLORREF crInkColor;
    SHORT nInkWidth;

    if (m_pIPaper && !m_bPainting && !m_bInking)
    {
      m_bPainting = TRUE;
      // Save and restore ink color and width since redraw otherwise
      // ends up changing these values in CGuiPaper.
      crInkColor = m_crInkColor;
      nInkWidth = m_nInkWidth;
      hr = m_pIPaper->Redraw(m_nLockKey);
      m_nInkWidth = nInkWidth;
      m_crInkColor = crInkColor;
      m_bPainting = FALSE;
    }

    return hr;
  }
```



<span data-ttu-id="b9c20-105">**PaintWin** esencialmente llama al método **redraw** del copaper.</span><span class="sxs-lookup"><span data-stu-id="b9c20-105">**PaintWin** essentially calls COPaper's **Redraw** method.</span></span> <span data-ttu-id="b9c20-106">En el ejemplo [StoServe](structured-storage-server-sample--stoserve-.md) , el método **redraw** se mostró para difundir la matriz de datos de tinta completa del copapel a todos los receptores conectados.</span><span class="sxs-lookup"><span data-stu-id="b9c20-106">In the [StoServe](structured-storage-server-sample--stoserve-.md) sample, the **Redraw** method was shown to broadcast COPaper's entire ink data array to all connected sinks.</span></span> <span data-ttu-id="b9c20-107">**PaintWin** llama a un objeto en el lado del servidor para devolver los datos de dibujo al cliente.</span><span class="sxs-lookup"><span data-stu-id="b9c20-107">**PaintWin** calls an object on the server side to send back the drawing data to the client.</span></span>

 

 




