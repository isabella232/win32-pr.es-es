---
title: El método OnPaint
description: El método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Reproductor de Windows Media complementos, método OnPaint
- complementos, método OnPaint
- complementos de interfaz de usuario, método OnPaint
- Complementos de interfaz de usuario, método OnPaint
- OnPaint (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073207"
---
# <a name="the-onpaint-method"></a>El método OnPaint

Se llama al método OnPaint cada vez que la ventana del complemento debe pintarse a sí misma. Esto sucede cuando la ventana del complemento recibe un mensaje WM PAINT, que se asigna al método OnPaint en el mapa de mensajes descrito \_ anteriormente. El asistente proporciona una implementación de este método que pinta el fondo negro y coloca el nombre del complemento en la ventana del complemento. La única modificación necesaria para el complemento de la interfaz de usuario de búsqueda es la eliminación del código que muestra el texto.

El código siguiente se usa para implementar este método:


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

 

 




