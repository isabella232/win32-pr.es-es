---
title: Mensaje de TDM_SET_MARQUEE_PROGRESS_BAR (commctrl. h)
description: Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea se debe mostrar en modo de marquesina.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_MARQUEE_PROGRESS_BAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a9384826b89d07c6564dc511d4909058871ca3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151049"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>Mensaje de la \_ \_ barra de \_ progreso del conjunto de TDM \_

Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea se debe mostrar en modo de marquesina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Un **booleano** que indica si la barra de progreso se debe mostrar en modo de marquesina. Un valor **true** activa el modo de marquesina y el valor **false** desactiva el modo de marquesina.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Para obtener información sobre el modo de marquesina, vea [control de barra de progreso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





