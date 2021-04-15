---
title: Mensaje de LVM_SUBITEMHITTEST (commctrl. h)
description: Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la \_ macro SubItemHitTest de ListView.
ms.assetid: 1468febb-af0d-4c04-b0b1-cda5ec77aa2c
keywords:
- LVM_SUBITEMHITTEST controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489257"
---
# <a name="lvm_subitemhittest-message"></a>\_Mensaje SUBITEMHITTEST LVM

Determina qué elemento o subelemento de vista de lista se encuentra en una posición determinada. Puede enviar este mensaje explícitamente o mediante la macro [**\_ SubItemHitTest de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_subitemhittest) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser 0. **Windows Vista.** Debe ser-1 si se va a recuperar el miembro **iGroup** de *lParam* .</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) . La estructura de [**punto**](/previous-versions//dd162805(v=vs.85)) dentro de **LVHITTESTINFO** debe establecerse en las coordenadas de cliente en las que se va a realizar la prueba de posicionamiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del elemento o subelemento probado, si existe, o-1 en caso contrario. Si un elemento o subelemento está en las coordenadas especificadas, los campos de la estructura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) se rellenarán con la información de aciertos correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

