---
title: El método OnPaint
description: El método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Reproductor de Windows Media complementos,método OnPaint
- complementos, método OnPaint
- complementos de interfaz de usuario, método OnPaint
- Complementos de interfaz de usuario, método OnPaint
- OnPaint (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5e121cdaeac1c7589e58b1613a8d25bdff4f44f6db2375bcbdc34da20929e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001955"
---
# <a name="the-onpaint-method"></a>El método OnPaint

Se llama al método OnPaint cada vez que la ventana del complemento debe pintarse a sí misma. Esto sucede cuando la ventana del complemento recibe un mensaje WM PAINT, que se asigna al método OnPaint en el mapa de mensajes descrito \_ anteriormente. El asistente proporciona una implementación de este método que pinta el fondo negro y coloca el nombre del complemento en la ventana del complemento. La única modificación necesaria para el complemento de la interfaz de usuario de búsqueda es la eliminación del código que muestra el texto.

Para implementar este método se usa el código siguiente:


```C++
LRESULT OnPaint(UINT nMsg, WPARAM wParam, 
                         LPARAM lParam, BOOL& bHandled)
{
    PAINTSTRUCT ps;

    HDC hDC = BeginPaint(&ps);

    RECT rc;
    GetClientRect(&rc);

    HBRUSH hNewBrush = ::CreateSolidBrush( RGB(0, 0, 0) );

    if (hNewBrush)
    {
        ::FillRect(hDC, &rc, hNewBrush );
        ::DeleteObject( hNewBrush );
    }

    EndPaint(&ps);
    return 0;
}

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




