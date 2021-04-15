---
title: Mensaje de WM_CUT (Winuser. h)
description: Una aplicación envía un mensaje de corte de WM \_ a un control de edición o un cuadro combinado para eliminar (cortar) la selección actual, si existe, en el control de edición y copiar el texto eliminado en el portapapeles en \_ formato de texto CF.
ms.assetid: 6ac45589-3e34-491c-9562-e072ddc478f9
keywords:
- Intercambio de datos de mensajes de WM_CUT
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676721"
---
# <a name="wm_cut-message"></a>Mensaje de corte de WM \_

Una aplicación envía un mensaje de **\_ corte de WM** a un control de edición o un cuadro combinado para eliminar (cortar) la selección actual, si existe, en el control de edición y copiar el texto eliminado en el portapapeles en formato de [**\_ texto CF**](standard-clipboard-formats.md) .


```C++
#define WM_CUT                          0x0300
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

La eliminación realizada por el mensaje de **\_ corte de WM** se puede deshacer enviando el control de edición de un mensaje de [**\_ Deshacer de EM**](../controls/em-undo.md) .

Para eliminar la selección actual sin colocar el texto eliminado en el portapapeles, utilice el mensaje de [**\_ borrado de WM**](wm-clear.md) .

Cuando se envía a un cuadro combinado, el mensaje de **\_ corte de WM** se controla mediante su control de edición. Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .

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

[**\_borrado de WM**](wm-clear.md)
</dt> <dt>

[**copia de WM \_**](wm-copy.md)
</dt> <dt>

[**pegar de WM \_**](wm-paste.md)
</dt> <dt>

[**deshacer de WM \_**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Vista**
</dt> <dt>

[Portapapeles](clipboard.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**deshacer EM \_**](../controls/em-undo.md)
</dt> </dl>

 

