---
title: WM_HSCROLLCLIPBOARD mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1066760fe4fb6f2d0c7449fe8f726f41e0e3530610dd3fe7790c369d4821f88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914856"
---
# <a name="wm_hscrollclipboard-message"></a>Mensaje \_ DE WM HSCROLLCLIPBOARD

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles. Esto ocurre cuando el Portapapeles contiene datos en formato [**\_ CF OWNERDISPLAY**](standard-clipboard-formats.md) y se produce un evento en la barra de desplazamiento horizontal del visor del Portapapeles. El propietario debe desplazarse por la imagen del Portapapeles y actualizar los valores de la barra de desplazamiento.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del Portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo *de lParam* especifica un evento de barra de desplazamiento. Este parámetro puede ser uno de los valores siguientes. La palabra de orden superior de *lParam* especifica la posición actual del cuadro de desplazamiento si la palabra de orden bajo de *lParam* es **SB \_ THUMBPOSITION;** de lo contrario, no se usa la palabra de orden superior.



| Valor                                                                                                                                                                                                                         | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Desplazamiento final.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_ LEFT**</dt> <dt>6</dt> </dl>                            | Desplácese a la parte superior izquierda.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_ RIGHT**</dt> <dt>7</dt> </dl>                         | Desplácese hacia abajo a la derecha.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> <dt>0</dt> </dl>                | Se desplaza a la izquierda por una unidad.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> <dt>1</dt> </dl>             | Se desplaza a la derecha por una unidad.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> <dt>2</dt> </dl>                | Se desplaza a la izquierda por el ancho de la ventana.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ PAGERIGHT**</dt> <dt>3</dt> </dl>             | Se desplaza a la derecha por el ancho de la ventana.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Desplácese hasta la posición absoluta. La palabra de orden superior especifica la posición actual.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Comentarios

El propietario del Portapapeles puede usar la [**función ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para desplazar la imagen en la ventana del visor del Portapapeles e invalidar la región adecuada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

