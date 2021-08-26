---
title: LVM_DELETECOLUMN mensaje (Commctrl.h)
description: Quita una columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView DeleteColumn.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_DELETECOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 039ab92028d23a75518237bc6e9723f051f2f6f2de8732e40f2086d027a61873
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920325"
---
# <a name="lvm_deletecolumn-message"></a>Mensaje \_ DELETECOLUMN de LVM

Quita una columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView DeleteColumn.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna que se va a eliminar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

La eliminación de la columna cero de un control de vista de lista solo se admite ComCtl32.dll versión 6 y posteriores. La versión 5 también admite la eliminación de la columna cero, pero solo después de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para establecer la versión en 5 o posterior. En versiones anteriores a la versión 5, si debe eliminar la columna cero, inserte una columna ficticia de longitud cero cero y elimine la columna uno y posteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





