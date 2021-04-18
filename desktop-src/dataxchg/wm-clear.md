---
title: Mensaje de WM_CLEAR (Winuser. h)
description: Una aplicación envía un mensaje de borrar de WM \_ a un control de edición o un cuadro combinado para eliminar (borrar) la selección actual, si la hay, del control de edición.
ms.assetid: 6730a725-01ec-4821-9ffc-1ea267d665b3
keywords:
- Intercambio de datos de mensajes de WM_CLEAR
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
ms.openlocfilehash: 61a8e325704d1e8b953fe59bfaf4e8fcee62cf40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705149"
---
# <a name="wm_clear-message"></a>\_Mensaje de borrado de WM

Una aplicación envía un mensaje de **\_ Borrar de WM** a un control de edición o un cuadro combinado para eliminar (borrar) la selección actual, si la hay, del control de edición.


```C++
#define WM_CLEAR                        0x0303
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza y debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este mensaje no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La eliminación realizada por el mensaje de **\_ borrado de WM** se puede deshacer enviando el control de edición de un mensaje de [**\_ Deshacer de EM**](../controls/em-undo.md) .

Para eliminar la selección actual y colocar el contenido eliminado en el portapapeles, utilice el mensaje de [**\_ corte de WM**](wm-cut.md) .

Cuando se envía a un cuadro combinado, el mensaje de **\_ borrado de WM** se controla mediante su control de edición. Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**copia de WM \_**](wm-copy.md)
</dt> <dt>

[**cortar de WM \_**](wm-cut.md)
</dt> <dt>

[**pegar de WM \_**](wm-paste.md)
</dt> <dt>

[**deshacer de WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> </dl>

 

