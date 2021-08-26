---
title: WM_CLEAR mensaje (Winuser.h)
description: Una aplicación envía un mensaje WM CLEAR a un control de edición o a un cuadro combinado para eliminar (borrar) la selección actual, si la \_ hay, del control de edición.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- WM_CLEAR mensaje Datos Exchange
topic_type:
- apiref
api_name:
- WM_CLEAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6820a9134f112b51474cd5b73e8545583cb02969b02a1bd1428138ebf1049dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029115"
---
# <a name="wm_clear-message"></a>Mensaje CLEAR de WM \_

Una aplicación envía un mensaje **\_ WM CLEAR** a un control de edición o a un cuadro combinado para eliminar (borrar) la selección actual, si la hay, del control de edición.


```C++
#define WM_CLEAR                        0x0303
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

## <a name="remarks"></a>Comentarios

La eliminación realizada por el **mensaje WM \_ CLEAR** se puede deshacer enviando al control de edición un [**mensaje EM \_ UNDO.**](../controls/em-undo.md)

Para eliminar la selección actual y colocar el contenido eliminado en el Portapapeles, use el [**mensaje WM \_ CUT.**](wm-cut.md)

Cuando se envía a un cuadro combinado, el control de edición controla el mensaje CLEAR de **WM. \_** Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**\_ DROPDOWNLIST de CBS.**](../controls/combo-box-styles.md)

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

[**WM \_ COPY**](wm-copy.md)
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

 

