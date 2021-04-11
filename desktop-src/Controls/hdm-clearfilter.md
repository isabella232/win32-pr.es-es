---
title: Mensaje de HDM_CLEARFILTER (commctrl. h)
description: Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o utilizar la \_ macro header ClearFilter.
ms.assetid: 74c0265e-68d1-4414-8fd9-20f5f041d4b4
keywords:
- HDM_CLEARFILTER controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150556"
---
# <a name="hdm_clearfilter-message"></a>HDM \_ CLEARFILTER

Borra el filtro de un control de encabezado determinado. Puede enviar este mensaje explícitamente o utilizar la macro [**Header \_ ClearFilter**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearfilter) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Un valor de columna que indica qué filtro se va a borrar.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un entero. **LRESULT** se convierte en un entero que indica **true**(1) o **false**(0).

## <a name="remarks"></a>Observaciones

Si el valor de la columna se especifica como-1, se borran todos los filtros y la notificación de [ \_ FILTERCHANGE de HDN](hdn-filterchange.md) se envía solo una vez.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Encabezado \_ ClearAllFilters**](/windows/desktop/api/Commctrl/nf-commctrl-header_clearallfilters)
</dt> </dl>

 

 





