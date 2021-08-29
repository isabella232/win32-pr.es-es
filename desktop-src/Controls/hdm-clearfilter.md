---
title: HDM_CLEARFILTER mensaje (Commctrl.h)
description: Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o usar la \_ macro ClearFilter de encabezado.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER controles de Windows mensaje
topic_type:
- apiref
api_name:
- HDM_CLEARFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8b5117f7f4781bd957bf83b647cc9e4ca73cd85bda4d1a900f44c86945eca7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436265"
---
# <a name="hdm_clearfilter-message"></a>Mensaje \_ CLEARFILTER de HDM

Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o usar la macro [**\_ ClearFilter de**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) encabezado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de columna que indica qué filtro se va a borrar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero. LRESULT **se** convierte en un entero que indica **TRUE**(1) o **FALSE**(0).

## <a name="remarks"></a>Observaciones

Si el valor de columna se especifica como -1, se borran todos los filtros y la [notificación \_ FILTERCHANGE](hdn-filterchange.md) de HDN solo se envía una vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Encabezado \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





