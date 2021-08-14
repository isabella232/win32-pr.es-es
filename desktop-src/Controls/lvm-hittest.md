---
title: LVM_HITTEST mensaje (Commctrl.h)
description: Determina qué elemento de vista de lista, si existe, está en una posición especificada. Puede enviar este mensaje explícitamente o mediante la macro ListView \_ HitTest.
ms.assetid: 81df4ed1-30bd-4b63-9cb9-5163cb7cf52c
keywords:
- LVM_HITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81308249992b134dd3fa2bd0bc43ff0074bc3bae7048072ada7d68b0a867a979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958174"
---
# <a name="lvm_hittest-message"></a>Mensaje DE \_ LVM HITTEST

Determina qué elemento de vista de lista, si existe, está en una posición especificada. Puede enviar este mensaje explícitamente o mediante la macro [**ListView \_ HitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_hittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser 0. **Windows Vista.** Debe ser -1 si se van a recuperar los miembros **iGroup** e **iSubItem** de la estructura *lParam.*</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) que contiene la posición de la prueba de posicionamiento y recibe información sobre los resultados de la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento en la posición especificada, si lo hay, o -1 en caso contrario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





