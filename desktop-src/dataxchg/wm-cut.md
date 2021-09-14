---
title: WM_CUT mensaje (Winuser.h)
description: Una aplicación envía un mensaje WM CUT a un control de edición o a un cuadro combinado para eliminar (cortar) la selección actual, si la hay, en el control de edición y copiar el texto eliminado en el Portapapeles en formato \_ CF \_ TEXT.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- WM_CUT mensaje Data Exchange
topic_type:
- apiref
api_name:
- WM_CUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a63dfe85fb637636fbabbce5fa139699fd09a65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160490"
---
# <a name="wm_cut-message"></a>Mensaje \_ DE WM CUT

Una aplicación envía un mensaje **WM \_ CUT** a un control de edición o a un cuadro combinado para eliminar (cortar) la selección actual, si la hay, en el control de edición y copiar el texto eliminado en el Portapapeles en formato [**CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_CUT                          0x0300
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

La eliminación realizada por el **mensaje \_ WM CUT** se puede deshacer enviando al control de edición un mensaje EM [**\_ UNDO.**](../controls/em-undo.md)

Para eliminar la selección actual sin colocar el texto eliminado en el Portapapeles, use el [**mensaje WM \_ CLEAR.**](wm-clear.md)

Cuando se envía a un cuadro combinado, su control de edición controla el mensaje **\_ WM CUT.** Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS.**](../controls/combo-box-styles.md)

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

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**WM \_ COPY**](wm-copy.md)
</dt> <dt>

[**WM \_ PASTE**](wm-paste.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**EM \_ UNDO**](../controls/em-undo.md)
</dt> </dl>

 

