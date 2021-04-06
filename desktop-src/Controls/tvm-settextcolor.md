---
title: Mensaje de TVM_SETTEXTCOLOR (commctrl. h)
description: Establece el color del texto del control. Puede enviar este mensaje explícitamente o mediante la \_ macro SetTextColor de TreeView.
ms.assetid: eb57dfd5-3e7b-4cda-a659-be9e03470a44
keywords:
- TVM_SETTEXTCOLOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da0049c2666faccce7879146c78ddecc70825e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802648"
---
# <a name="tvm_settextcolor-message"></a>\_Mensaje de SETTEXTCOLOR TVM

Establece el color del texto del control. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetTextColor de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_settextcolor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor de [**COLORREF**](/windows/desktop/gdi/colorref) que contiene el nuevo color de texto. Si este argumento es-1, el control volverá a usar el color del sistema para el color del texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de **COLORREF** que representa el color del texto anterior. Si este valor es-1, el control estaba usando el color del sistema para el color del texto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETTEXTCOLOR**](tvm-gettextcolor.md)
</dt> </dl>

 

