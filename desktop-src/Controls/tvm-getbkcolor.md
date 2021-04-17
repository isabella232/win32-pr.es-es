---
title: Mensaje de TVM_GETBKCOLOR (commctrl. h)
description: Recupera el color de fondo actual del control. Puede enviar este mensaje explícitamente o mediante la \_ macro GetBkColor de TreeView.
ms.assetid: 1b9eea90-54cd-47b9-befa-ec0128a0230f
keywords:
- TVM_GETBKCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8077bc9655c088aceefe239ed019cc45874d38ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658324"
---
# <a name="tvm_getbkcolor-message"></a>\_Mensaje de GETBKCOLOR TVM

Recupera el color de fondo actual del control. Puede enviar este mensaje explícitamente o mediante la macro [**\_ GetBkColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getbkcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de [**COLORREF**](/windows/desktop/gdi/colorref) que representa el color de fondo actual. Si este valor es-1, el control usa el color del sistema para el color de fondo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ SETBKCOLOR**](tvm-setbkcolor.md)
</dt> </dl>

 

