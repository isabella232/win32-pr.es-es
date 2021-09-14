---
title: SBM_GETSCROLLINFO mensaje (Winuser.h)
description: El mensaje \_ SBM GETSCROLLINFO se envía para recuperar los parámetros de una barra de desplazamiento.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO controles de Windows mensaje
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167077"
---
# <a name="sbm_getscrollinfo-message"></a>Mensaje SBM \_ GETSCROLLINFO

El **mensaje \_ SBM GETSCROLLINFO** se envía para recuperar los parámetros de una barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben usar la [**función GetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) Una ventana recibe este mensaje a través de su [*función WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que **la función GetScrollInfo** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Antes de llamar [**a GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), establezca el miembro **cbSize** de la estructura en **sizeof**(**SCROLLINFO**) y establezca el miembro **fMask** para especificar los parámetros de la barra de desplazamiento que se recuperarán. Antes de devolver, el mensaje copia los parámetros especificados en los miembros adecuados de la estructura .

El **miembro fMask** puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                      | Significado                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ ALL**</dt> </dl>                | Combinación de SIF \_ PAGE, SIF \_ POS, SIF \_ RANGE y SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**PÁGINA \_ SIF**</dt> </dl>             | Copia la página de desplazamiento en el miembro nPage.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ POS**</dt> </dl>                | Copia la posición de desplazamiento en el miembro nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**INTERVALO DE \_ SIF**</dt> </dl>          | Copia el intervalo de desplazamiento en los miembros nMin y nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**SIF \_ TRACKPOS**</dt> </dl> | Copia la posición actual del seguimiento del cuadro de desplazamiento en el miembro nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el mensaje recuperó algún valor, el valor devuelto es **TRUE**; de lo contrario, es **FALSE.**

## <a name="remarks"></a>Observaciones

Los mensajes que indican la posición de la barra de desplazamiento, [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md), proporcionan solo 16 bits de datos de posición. Sin embargo, la estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por **SBM \_ GETSCROLLINFO,** [**SBM \_ SETSCROLLINFO,**](sbm-setscrollinfo.md) [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)y [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) proporciona 32 bits de datos de posición de la barra de desplazamiento. Puede usar estos mensajes y funciones al procesar los mensajes **WM \_ HSCROLL** o **WM \_ VSCROLL** para obtener datos de posición de la barra de desplazamiento de 32 bits.

Para obtener la posición de 32 bits del cuadro de desplazamiento (thumb) durante un código de solicitud SB THUMBTRACK en un mensaje \_ [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL,**](wm-vscroll.md) envíe **SBM \_ GETSCROLLINFO** con el valor TRACKPOS de SIF en el miembro \_ **fMask** de la [**estructura SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) El mensaje devuelve la posición de seguimiento del cuadro de desplazamiento en el **miembro nTrackPos** de la **estructura SCROLLINFO.** Esto le permite obtener la posición del cuadro de desplazamiento a medida que el usuario la mueve. Como alternativa, puede usar la [**función GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para obtener la misma información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

