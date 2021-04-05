---
title: Mensaje de DTM_CLOSEMONTHCAL (commctrl. h)
description: Cierra un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la macro CloseMonthCal de fecha y hora \_ .
ms.assetid: f60af77f-ec34-4f3d-9427-cda7ac6083bf
keywords:
- DTM_CLOSEMONTHCAL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- DTM_CLOSEMONTHCAL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd79f33576490196bf29fd51316f8ce3daf4ad4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078950"
---
# <a name="dtm_closemonthcal-message"></a>DTM \_ CLOSEMONTHCAL

Cierra un control de selector de fecha y hora (DTP). Envíe este mensaje explícitamente o mediante la [**macro \_ CloseMonthCal de fecha y hora**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_closemonthcal) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Debe ser cero.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero.

## <a name="remarks"></a>Observaciones

Destruye el control y envía una notificación [DTN \_ primer plano](dtn-closeup.md) de que el control se está cerrando en lugar de que el control se esté abriendo (colocando como en la notificación de la [ \_ lista desplegable DTN](dtn-dropdown.md) ) en el elemento primario del control.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[\_lista desplegable DTN](dtn-dropdown.md)
</dt> <dt>

[DTN \_ primer plano](dtn-closeup.md)
</dt> </dl>

 

 





