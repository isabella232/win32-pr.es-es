---
title: Mensaje de SBM_SETSCROLLINFO (Winuser. h)
description: El \_ mensaje SBM SETSCROLLINFO se envía para establecer los parámetros de una barra de desplazamiento.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- SBM_SETSCROLLINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98abbca2d53d4b104caea22954472a17dfd5c1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658289"
---
# <a name="sbm_setscrollinfo-message"></a>\_Mensaje SETSCROLLINFO SBM

El mensaje **SBM \_ SETSCROLLINFO** se envía para establecer los parámetros de una barra de desplazamiento.

Las aplicaciones no deben enviar este mensaje directamente. En su lugar, deben utilizar la función [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Una ventana recibe este mensaje a través de su función [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Las aplicaciones que implementan un control de barra de desplazamiento personalizado deben responder a estos mensajes para que la función **SetScrollInfo** funcione correctamente.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica si la barra de desplazamiento se vuelve a dibujar para reflejar la nueva posición del cuadro de desplazamiento. Si este parámetro es **true**, se vuelve a dibujar la barra de desplazamiento. Si es **false**, la barra de desplazamiento no se vuelve a dibujar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Antes de llamar a [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), establezca el miembro **cbSize** de la estructura en **sizeof**(**SCROLLINFO**), establezca el miembro **fMask** para indicar los parámetros que se van a establecer y especifique los nuevos valores de parámetro en los miembros adecuados.

El miembro **fMask** puede ser uno o varios de los valores siguientes.



| Value                                                                                                                                                                           | Significado                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**SIF \_ DISABLENOSCROLL**</dt> </dl> | Deshabilita la barra de desplazamiento en lugar de quitarla, si los nuevos parámetros de la barra de desplazamiento hacen que la barra de desplazamiento sea innecesaria.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_Página SIF**</dt> </dl>                                  | Establece la página de desplazamiento en el valor especificado en el miembro **nPage** .<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**SIF \_ pos**</dt> </dl>                                     | Establece la posición de desplazamiento en el valor especificado en el miembro **NPOs** . <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**intervalo de SIF \_**</dt> </dl>                               | Establece el intervalo de desplazamiento en el valor especificado en los miembros **nmín.** y **nmáx.** . <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es la posición actual del cuadro de desplazamiento.

## <a name="remarks"></a>Observaciones

Los mensajes que indican la posición de la barra de desplazamiento, [**WM \_ HSCROLL**](wm-hscroll.md) y [**WM \_ VSCROLL**](wm-vscroll.md), proporcionan únicamente 16 bits de datos de posición. Sin embargo, la estructura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada [**por \_ SBM GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)y [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) proporciona 32 bits de datos de posición de la barra de desplazamiento. Puede usar estos mensajes y funciones al procesar los mensajes de **WM \_ HSCROLL** o **WM \_ VSCROLL** para obtener datos de posición de la barra de desplazamiento de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

