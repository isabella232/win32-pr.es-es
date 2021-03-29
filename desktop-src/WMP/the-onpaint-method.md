---
title: El método OnPaint
description: El método OnPaint
ms.assetid: 4b335362-4430-4b05-8aea-7de8df9cc91f
keywords:
- Complementos de Media Player de Windows, método OnPaint
- complementos, método OnPaint
- Complementos de la interfaz de usuario, método OnPaint
- Complementos de la interfaz de usuario, método OnPaint
- OnPaint (método)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22641c34bb2edab30c1bf97011e893bc1d9d44a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486975"
---
# <a name="the-onpaint-method"></a>El método OnPaint

Se llama al método OnPaint siempre que la ventana del complemento debe dibujarse. Esto sucede cuando la ventana del complemento recibe un mensaje de \_ dibujo de WM, que se asigna al método OnPaint en el mapa de mensajes descrito anteriormente. El asistente proporciona una implementación de este método que pinta el negro de fondo y coloca el nombre del complemento en la ventana del complemento. La única modificación que es necesaria para el complemento de la interfaz de usuario de búsqueda es la eliminación del código que muestra el texto.

El siguiente código se usa para implementar este método:


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

 

 




