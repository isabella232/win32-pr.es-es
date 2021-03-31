---
title: Método InkDraw
description: CGuiPaper también mantiene una \_ marca m bInking. InkStart lo establece en TRUE para indicar que una secuencia de dibujo está en curso. Por ejemplo, el método InkDraw usa esta marca para determinar si debe pintar y guardar los datos de tinta.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418978"
---
# <a name="inkdraw-method"></a><span data-ttu-id="c4195-106">Método InkDraw</span><span class="sxs-lookup"><span data-stu-id="c4195-106">InkDraw Method</span></span>

<span data-ttu-id="c4195-107">CGuiPaper también mantiene una \_ marca m bInking.</span><span class="sxs-lookup"><span data-stu-id="c4195-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="c4195-108">[InkStart](inkstart-method.md) lo establece en **true** para indicar que una secuencia de dibujo está en curso.</span><span class="sxs-lookup"><span data-stu-id="c4195-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="c4195-109">Por ejemplo, el método InkDraw usa esta marca para determinar si debe pintar y guardar los datos de tinta.</span><span class="sxs-lookup"><span data-stu-id="c4195-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="c4195-110">El siguiente es el método InkDraw de GUIPAPER. CPP.</span><span class="sxs-lookup"><span data-stu-id="c4195-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



<span data-ttu-id="c4195-111">Este método no hace nada si m \_ bInking es **false**.</span><span class="sxs-lookup"><span data-stu-id="c4195-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="c4195-112">Esta es la condición cuando el usuario simplemente mueve el mouse sobre la ventana del cliente sin presionar el botón primario del mouse.</span><span class="sxs-lookup"><span data-stu-id="c4195-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="c4195-113">InkDraw es claramente una responsabilidad doble.</span><span class="sxs-lookup"><span data-stu-id="c4195-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="c4195-114">Las llamadas a MoveToEx y lineTo de Win32 se realizan para dibujar imágenes de línea en la pantalla de la interfaz gráfica de usuario (mediante el controlador de contexto de dispositivo mantenido en m \_ HDC).</span><span class="sxs-lookup"><span data-stu-id="c4195-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="c4195-115">Los datos de tinta también se pasan al objeto de copaper para grabar con el método InkDraw de la interfaz [IPaper](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="c4195-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="c4195-116">Cuando m \_ bInkSaving es **false**, InkDraw pinta la imagen de línea, pero no almacena los datos en el copaper.</span><span class="sxs-lookup"><span data-stu-id="c4195-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="c4195-117">Esta condición se usa durante la repintado.</span><span class="sxs-lookup"><span data-stu-id="c4195-117">This condition is used during repainting.</span></span>

 

 




