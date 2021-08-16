---
title: LVM_SUBITEMHITTEST mensaje (Commctrl.h)
description: Determina qué elemento de vista de lista o subelemento se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la \_ macro ListView SubItemHitTest.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SUBITEMHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 341f9b3f84646abe975c6543aef802450496154862353b7bbdd1af2c07c087ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830646"
---
# <a name="lvm_subitemhittest-message"></a>Mensaje \_ LVM SUBITEMHITTEST

Determina qué elemento de vista de lista o subelemento se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la [**\_ macro ListView SubItemHitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser 0. **Windows Vista.** Debe ser -1 si se va a recuperar el miembro **iGroup** de *lParam.*</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) La [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) dentro de **LVHITTESTINFO** debe establecerse en las coordenadas de cliente que se probarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento o subelemento probado, si lo hay, o -1 en caso contrario. Si un elemento o subelemento se encuentra en las coordenadas dadas, los campos de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) se rellenarán con la información de acceso aplicable.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

