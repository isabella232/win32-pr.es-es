---
title: Mensaje de TVM_SETITEMHEIGHT (commctrl. h)
description: Establece el alto de los elementos de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemHeight de TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TVM_SETITEMHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114769f689cbf8d9475460e40d205c4282a1a787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996554"
---
# <a name="tvm_setitemheight-message"></a>\_Mensaje de SETITEMHEIGHT TVM

Establece el alto de los elementos de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemHeight de TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo alto de cada elemento en la vista de árbol, en píxeles. El alto inferior a 1 se establecerá en 1. Si este argumento no es par y el control de vista de árbol no tiene el [**estilo \_ NONEVENHEIGHT de TV**](tree-view-control-window-styles.md) , este valor se redondeará al valor par más cercano. Si este argumento es-1, el control volverá a usar su alto predeterminado del elemento.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el alto anterior de los elementos, en píxeles.

## <a name="remarks"></a>Observaciones

El control de vista de árbol usa este valor para el alto de todos los elementos. Para modificar el alto de elementos individuales, vea la descripción del miembro **iIntegral** de la estructura [**TVITEMEX**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





