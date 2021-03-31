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
# <a name="inkdraw-method"></a>Método InkDraw

CGuiPaper también mantiene una \_ marca m bInking. [InkStart](inkstart-method.md) lo establece en **true** para indicar que una secuencia de dibujo está en curso. Por ejemplo, el método InkDraw usa esta marca para determinar si debe pintar y guardar los datos de tinta.

El siguiente es el método InkDraw de GUIPAPER. CPP.


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



Este método no hace nada si m \_ bInking es **false**. Esta es la condición cuando el usuario simplemente mueve el mouse sobre la ventana del cliente sin presionar el botón primario del mouse.

InkDraw es claramente una responsabilidad doble. Las llamadas a MoveToEx y lineTo de Win32 se realizan para dibujar imágenes de línea en la pantalla de la interfaz gráfica de usuario (mediante el controlador de contexto de dispositivo mantenido en m \_ HDC). Los datos de tinta también se pasan al objeto de copaper para grabar con el método InkDraw de la interfaz [IPaper](ipaper-methods.md) . Cuando m \_ bInkSaving es **false**, InkDraw pinta la imagen de línea, pero no almacena los datos en el copaper. Esta condición se usa durante la repintado.

 

 




