---
title: TVM_SETITEMHEIGHT mensaje (Commctrl.h)
description: Establece el alto de los elementos de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro \_ SetItemHeight de TreeView.
ms.assetid: 23f6f2a4-cdd9-441d-af24-ed40513d2721
keywords:
- TVM_SETITEMHEIGHT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165622"
---
# <a name="tvm_setitemheight-message"></a>Mensaje \_ SETITEMHEIGHT de TVM

Establece el alto de los elementos de la vista de árbol. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemHeight de TreeView.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitemheight)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo alto de cada elemento de la vista de árbol, en píxeles. Las alturas inferiores a 1 se establecerán en 1. Si este argumento no es par y el control de vista de árbol no tiene el estilo [**\_ NONEVENHEIGHT de TVS,**](tree-view-control-window-styles.md) este valor se redondeará hacia abajo al valor par más cercano. Si este argumento es -1, el control volverá a usar su alto de elemento predeterminado.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el alto anterior de los elementos, en píxeles.

## <a name="remarks"></a>Observaciones

El control de vista de árbol usa este valor para el alto de todos los elementos. Para modificar el alto de los elementos individuales, vea la descripción del **miembro iIntegral** de la [**estructura TVITEMEX.**](/windows/win32/api/commctrl/ns-commctrl-tvitemexa)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TVM \_ GETITEMHEIGHT**](tvm-getitemheight.md)
</dt> </dl>

 

 





