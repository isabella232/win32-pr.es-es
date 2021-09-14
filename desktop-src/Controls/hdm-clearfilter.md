---
title: HDM_CLEARFILTER mensaje (Commctrl.h)
description: Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o usar la macro \_ ClearFilter de encabezado.
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
ms.openlocfilehash: 3b1184432517761a567cd76bdd488e4593b1e999
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061999"
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

Devuelve un entero. El **LRESULT** se convierte en un entero que indica **TRUE**(1) o **FALSE**(0).

## <a name="remarks"></a>Observaciones

Si el valor de columna se especifica como -1, se borran todos los filtros y la notificación [ \_ FILTERCHANGE](hdn-filterchange.md) de HDN se envía solo una vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Encabezado \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





