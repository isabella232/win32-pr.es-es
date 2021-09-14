---
title: LVM_SUBITEMHITTEST mensaje (Commctrl.h)
description: Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SubItemHitTest.
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
ms.openlocfilehash: c811a3ed85b9eb157920f700b34d5d9c99597e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072329"
---
# <a name="lvm_subitemhittest-message"></a>Mensaje \_ LVM SUBITEMHITTEST

Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SubItemHitTest.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser 0. **Windows Vista.** Debe ser -1 si se va a recuperar el miembro **iGroup** de *lParam.*</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVHITTESTINFO.**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) La [**estructura POINT**](/previous-versions//dd162805(v=vs.85)) dentro de **LVHITTESTINFO** debe establecerse en las coordenadas de cliente que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento o subelemento probado, si lo hay, o -1 en caso contrario. Si un elemento o subelemento se encuentra en las coordenadas dadas, los campos de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) se rellenarán con la información de acceso aplicable.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

