---
title: HDM_SETFILTERCHANGETIMEOUT mensaje (Commctrl.h)
description: Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y la publicación de una notificación \_ FILTERCHANGE de HDN. Puede enviar este mensaje explícitamente o usar la macro \_ SetFilterChangeTimeout de encabezado.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_SETFILTERCHANGETIMEOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b5f8df12a7f30baa5f8b7d4bf15698b30cfbb6619fb71a81d4977b259c318b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435865"
---
# <a name="hdm_setfilterchangetimeout-message"></a>Mensaje \_ SETFILTERCHANGETIMEOUT de HDM

Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y la publicación de una [notificación \_ FILTERCHANGE de HDN.](hdn-filterchange.md) Puede enviar este mensaje explícitamente o usar la macro [**\_ SetFilterChangeTimeout de**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

El valor del tiempo de espera, en milisegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del control de filtro que se está modificando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





