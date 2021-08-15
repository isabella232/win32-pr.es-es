---
title: WM_COPY mensaje (Winuser.h)
description: Una aplicación envía el mensaje WM COPY a un control de edición o a un cuadro combinado para copiar la selección actual en el Portapapeles \_ en formato CF \_ TEXT.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- WM_COPY mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_COPY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d7774b1e2d52cbe21b8636bcaa1c695f9f49b319280ebc89c74fd652533066b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096755"
---
# <a name="wm_copy-message"></a>Mensaje COPY de WM \_

Una aplicación envía el **mensaje WM \_ COPY** a un control de edición o a un cuadro combinado para copiar la selección actual en el Portapapeles en [**formato CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_COPY                         0x0301
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

Devuelve un valor distinto de cero si se ejecuta correctamente; de lo contrario, cero.

## <a name="remarks"></a>Comentarios

Cuando se envía a un cuadro combinado, su control de edición controla el mensaje COPY de **WM. \_** Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS.**](../controls/combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ PASTE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

