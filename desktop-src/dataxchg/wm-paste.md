---
title: WM_PASTE mensaje (Winuser.h)
description: Una aplicación envía un mensaje WM PASTE a un control de edición o a un cuadro combinado para copiar el contenido actual del Portapapeles en el control de edición en la posición \_ del cursor de cursor actual. Los datos solo se insertan si el Portapapeles contiene datos en formato CF \_ TEXT.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86b723830ecdd0f8b7e3faa9da9adcb51161b297
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174866"
---
# <a name="wm_paste-message"></a>Mensaje \_ DE WM PASTE

Una aplicación envía un mensaje **WM \_ PASTE** a un control de edición o a un cuadro combinado para copiar el contenido actual del Portapapeles en el control de edición en la posición del cursor de cursor actual. Los datos solo se insertan si el Portapapeles contiene datos en [**formato CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se usa y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve un valor.

## <a name="remarks"></a>Observaciones

Cuando se envía a un cuadro combinado, el control de edición controla el mensaje **\_ WM PASTE.** Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS.**](../controls/combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

