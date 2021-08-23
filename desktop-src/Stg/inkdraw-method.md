---
title: InkDraw (método)
description: CGuiPaper también mantiene una marca \_ m bInking. InkStart lo establece en TRUE para indicar que una secuencia de dibujo está en proceso. Por ejemplo, el método InkDraw usa esta marca para determinar si debe pintar y guardar datos de entrada de lápiz.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e146093d23fd16d122da1ea81d1c99bdf06ed926d5cb4dba2f1d77b747b2058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662765"
---
# <a name="inkdraw-method"></a>InkDraw (método)

CGuiPaper también mantiene una marca \_ m bInking. [InkStart lo](inkstart-method.md) establece en **TRUE para** indicar que una secuencia de dibujo está en proceso. Por ejemplo, el método InkDraw usa esta marca para determinar si debe pintar y guardar datos de entrada de lápiz.

A continuación se muestra el método InkDraw de GUIPAPER. Cpp.


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



Este método no hace nada si m \_ bInking es **FALSE.** Esta es la condición cuando el usuario simplemente mueve el mouse sobre la ventana del cliente sin presionar el botón izquierdo del mouse.

InkDraw claramente tiene una doble responsabilidad. Las llamadas a MoveToEx y LineTo de Win32 se realizan para dibujar imágenes de línea en la pantalla de la GUI (mediante el identificador de contexto del dispositivo que se mantiene en m \_ hDC). Los datos de entrada de lápiz también se pasan al objeto COPaper para su grabación mediante el método InkDraw de la interfaz [IPaper.](ipaper-methods.md) Cuando m \_ bInkSaving es **FALSE,** InkDraw pinta la imagen de línea, pero no almacena los datos en COPaper. Esta condición se usa durante el repintado.

 

 




