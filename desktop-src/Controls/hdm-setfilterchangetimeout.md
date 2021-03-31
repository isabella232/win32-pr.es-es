---
title: Mensaje de HDM_SETFILTERCHANGETIMEOUT (commctrl. h)
description: Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y el envío de una notificación de FILTERCHANGE de HDN \_ . Puede enviar este mensaje explícitamente o utilizar la \_ macro header SetFilterChangeTimeout.
ms.assetid: 9bc8e0e7-d7c1-4dd6-9d39-6ae937f19d60
keywords:
- HDM_SETFILTERCHANGETIMEOUT controles de mensajes de Windows
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
ms.openlocfilehash: 9876634d12cd15001c296151694cb755ed1b34e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079621"
---
# <a name="hdm_setfilterchangetimeout-message"></a>HDM \_ SETFILTERCHANGETIMEOUT

Establece el intervalo de tiempo de espera entre el momento en que se produce un cambio en los atributos de filtro y el envío de una notificación de [ \_ FILTERCHANGE de HDN](hdn-filterchange.md) . Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ SetFilterChangeTimeout**](/windows/desktop/api/Commctrl/nf-commctrl-header_setfilterchangetimeout) .

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[HDN \_ FILTERCHANGE](hdn-filterchange.md)
</dt> </dl>

 

 





