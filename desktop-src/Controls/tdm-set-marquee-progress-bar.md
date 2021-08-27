---
title: TDM_SET_MARQUEE_PROGRESS_BAR mensaje (Commctrl.h)
description: Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea debe mostrarse en modo de marquesina.
ms.assetid: 28b9b519-6b96-4130-936c-b8fe8df86d25
keywords:
- TDM_SET_MARQUEE_PROGRESS_BAR controles de Windows mensaje
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
ms.openlocfilehash: 13262339f7d87ea68755a38a49cc8c327706939d6b18025f350334dfdbe3dd4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104615"
---
# <a name="tdm_set_marquee_progress_bar-message"></a>Mensaje TDM \_ SET \_ MARQUEE \_ PROGRESS \_ BAR

Indica si la barra de progreso hospedada de un cuadro de diálogo de tarea debe mostrarse en modo de marquesina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ En\]
</dt> <dd>

Un **BOOL** que indica si la barra de progreso debe mostrarse en modo de marquesina. Un valor de **TRUE activa** el modo de marquesina y un valor **de FALSE** desactiva el modo de marquesina.

</dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Debe ser cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

Para obtener información sobre el modo de marquesina, vea [Control de barra de progreso](progress-bar-control.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





