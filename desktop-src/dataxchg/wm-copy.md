---
title: Mensaje de WM_COPY (Winuser. h)
description: Una aplicación envía el mensaje de copia de WM \_ a un control de edición o un cuadro combinado para copiar la selección actual en el portapapeles en \_ formato de texto CF.
ms.assetid: dcac3ad3-1e70-4b71-accd-261587224e60
keywords:
- Intercambio de datos de mensajes de WM_COPY
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
ms.openlocfilehash: b298248d75b1d25d1bfef8347347fe2f1a6c7916
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/04/2021
ms.locfileid: "105707574"
---
# <a name="wm_copy-message"></a>Mensaje de copia de WM \_

Una aplicación envía el mensaje de **\_ copia de WM** a un control de edición o un cuadro combinado para copiar la selección actual en el portapapeles en formato de [**\_ texto CF**](standard-clipboard-formats.md) .


```C++
#define WM_COPY                         0x0301
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

Devuelve un valor distinto de cero si es correcto; de lo contrario, es cero.

## <a name="remarks"></a>Observaciones

Cuando se envía a un cuadro combinado, el mensaje de **\_ copia de WM** se controla mediante su control de edición. Este mensaje no tiene ningún efecto cuando se envía a un cuadro combinado con el estilo [**CBS \_ DROPDOWNLIST**](../controls/combo-box-styles.md) .

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

 

