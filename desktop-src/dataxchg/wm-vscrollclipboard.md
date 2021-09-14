---
title: WM_VSCROLLCLIPBOARD mensaje (Winuser.h)
description: Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en formato CF OWNERDISPLAY y se produce un evento en la barra de desplazamiento vertical del visor \_ del Portapapeles.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126884884"
---
# <a name="wm_vscrollclipboard-message"></a>Mensaje \_ VSCROLLCLIPBOARD de WM

Se envía al propietario del Portapapeles mediante una ventana del visor del Portapapeles cuando el portapapeles contiene datos en formato [**\_ CF OWNERDISPLAY**](standard-clipboard-formats.md) y se produce un evento en la barra de desplazamiento vertical del visor del Portapapeles. El propietario debe desplazarse por la imagen del Portapapeles y actualizar los valores de la barra de desplazamiento.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana del visor del Portapapeles.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo *de lParam* especifica un evento de barra de desplazamiento. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                         | Significado                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_ BOTTOM**</dt> <dt>7</dt> </dl>                      | Desplácese hacia abajo a la derecha.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Desplazamiento final.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Desplácese una línea hacia abajo.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ LINEUP**</dt> <dt>0</dt> </dl>                      | Desplácese una línea hacia arriba.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PAGEDOWN**</dt> <dt>3</dt> </dl>                | Desplácese una página hacia abajo.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PAGEUP**</dt> <dt>2</dt> </dl>                      | Desplácese una página hacia arriba.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Desplácese hasta la posición absoluta. La palabra de orden superior especifica la posición actual.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_ TOP**</dt> <dt>6</dt> </dl>                               | Desplácese a la parte superior izquierda.<br/>                                                                  |



 

La palabra de orden superior de *lParam* especifica la posición actual del cuadro de desplazamiento si la palabra de orden bajo de *lParam* es **SB \_ THUMBPOSITION;** de lo contrario, no se usa la palabra de orden superior *de lParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si una aplicación procesa este mensaje, debe devolver cero.

## <a name="remarks"></a>Observaciones

El propietario del Portapapeles puede usar la [**función ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) para desplazar la imagen en la ventana del visor del Portapapeles e invalidar la región adecuada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

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

 

