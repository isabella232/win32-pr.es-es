---
title: LVM_SETITEMSTATE mensaje (Commctrl.h)
description: Cambia el estado de un elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SetItemState.
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362690"
---
# <a name="lvm_setitemstate-message"></a>Mensaje \_ SETITEMSTATE de LVM

Cambia el estado de un elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SetItemState.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice del elemento de vista de lista. Si este parámetro es -1, el cambio de estado se aplica a todos los elementos.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) El **miembro stateMask** especifica qué bits de estado se cambiarán y el miembro **de** estado contiene los nuevos valores para esos bits. Los demás miembros se omiten.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si envía este mensaje explícitamente, devuelve **TRUE** si se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Observaciones

El valor de estado de un elemento incluye un conjunto de marcas de bits que indican el estado del elemento. El valor de estado también puede incluir índices de lista de imágenes que indican la imagen de estado del elemento y la imagen superpuesta.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





