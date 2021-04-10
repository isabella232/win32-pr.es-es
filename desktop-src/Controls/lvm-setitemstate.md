---
title: Mensaje de LVM_SETITEMSTATE (commctrl. h)
description: Cambia el estado de un elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro SetItemState de ListView.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2120d6d1d2cd3044368ebb343cdf0fe240d805c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150367"
---
# <a name="lvm_setitemstate-message"></a>\_Mensaje SETITEMSTATE LVM

Cambia el estado de un elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SetItemState de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista. Si este parámetro es-1, el cambio de estado se aplica a todos los elementos.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . El miembro **stateMask** especifica qué bits de estado cambiar y el miembro **State** contiene los nuevos valores de esos bits. Se omiten los demás miembros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve **true** si es correcto o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

El valor de estado de un elemento incluye un conjunto de marcadores de bits que indican el estado del elemento. El valor de estado también puede incluir índices de lista de imágenes que indican la imagen de estado del elemento y la imagen de superposición.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





