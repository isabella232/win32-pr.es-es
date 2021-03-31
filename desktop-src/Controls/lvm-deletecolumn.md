---
title: Mensaje de LVM_DELETECOLUMN (commctrl. h)
description: Quita una columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro DeleteColumn de ListView.
ms.assetid: 1748a70b-9a13-4753-ac23-55b5652164c2
keywords:
- LVM_DELETECOLUMN controles de mensajes de Windows
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
ms.openlocfilehash: daa9005009ceaf42a01ede4f0f26334ae686c2df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801129"
---
# <a name="lvm_deletecolumn-message"></a>\_Mensaje DELETECOLUMN LVM

Quita una columna de un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ DeleteColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deletecolumn) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la columna que se va a eliminar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

La eliminación de la columna cero de un control de vista de lista solo se admite en ComCtl32.dll versión 6 y posteriores. La versión 5 también admite la eliminación de la columna cero, pero solo después de usar [**CCM \_ SETVERSION**](ccm-setversion.md) para establecer la versión en 5 o posterior. En versiones anteriores a la versión 5, si tiene que eliminar la columna cero, inserte una columna ficticia de longitud cero cero y elimine la columna uno y versiones posteriores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





