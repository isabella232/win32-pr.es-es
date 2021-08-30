---
title: SB_SETTEXT mensaje (Commctrl.h)
description: Establece el texto de la parte especificada de una ventana de estado.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT controles de Windows mensaje
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a8ddf0ee02f88b468b0911e64b5308cc2e8784
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479741"
---
# <a name="sb_settext-message"></a>Mensaje \_ SB SETTEXT

Establece el texto de la parte especificada de una ventana de estado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

El [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) de la palabra de orden bajo especifica el índice de base cero de la parte que se establece. Si **loBYTE se** establece en SB SIMPLEID, se supone que la ventana de estado es una barra de estado de modo simple; es decir, una barra de estado con \_ una sola parte.

El [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) de la palabra de orden bajo especifica el tipo de la operación de dibujo. Este parámetro puede ser uno de los valores siguientes.

Se omite la palabra de orden superior *de wParam.*




| Valor | Significado | 
|-------|---------|
| <span id="0"></span><dl><dt><strong>0</strong></dt></dl> | El texto se dibuja con un borde para que aparezca más bajo que el plano de la ventana.<br /> | 
| <span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl><dt><strong>SBT_NOBORDERS</strong></dt></dl> | El texto se dibuja sin bordes.<br /> | 
| <span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl><dt><strong>SBT_OWNERDRAW</strong></dt></dl> | La ventana primaria dibuja el texto. <br /><blockquote>[!Note]<br />Una barra de estado de modo simple no admite el dibujo del propietario.</blockquote><br /> | 
| <span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl><dt><strong>SBT_POPOUT</strong></dt></dl> | El texto se dibuja con un borde para que aparezca más alto que el plano de la ventana.<br /> | 
| <span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl><dt><strong>SBT_RTLREADING</strong></dt></dl> | El texto se mostrará en la dirección opuesta al texto de la ventana primaria.<br /> | 
| <span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl><dt><strong>SBT_NOTABPARSING</strong></dt></dl> | Se omiten los caracteres de tabulación.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el texto que se establecerá. Si *wParam* es SBT \_ OWNERDRAW, este parámetro representa 32 bits de datos. La ventana primaria debe interpretar los datos y dibujar el texto cuando recibe el [**mensaje \_ DRAWITEM de WM.**](wm-drawitem.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

El mensaje invalida la parte de la ventana que ha cambiado, lo que hace que muestre el nuevo texto cuando la ventana recibe a continuación el [**mensaje \_ DE WM PAINT.**](/windows/desktop/gdi/wm-paint)

Las ventanas normales muestran texto de izquierda a derecha (LTR). Windows se puede reflejar *para* mostrar idiomas como hebreo o árabe que leen de derecha a izquierda (RTL). Si se establece SBT \_ RTLREADING, la cadena *lParam* leerá en la dirección opuesta desde el texto de la ventana primaria.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) y **SB \_ SETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SB \_ GETTEXT**](sb-gettext.md)
</dt> </dl>

 

