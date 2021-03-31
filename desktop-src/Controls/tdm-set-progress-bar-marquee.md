---
title: Mensaje de TDM_SET_PROGRESS_BAR_MARQUEE (commctrl. h)
description: Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea, y establece la velocidad del marco.
ms.assetid: df947171-a916-4db9-abe0-57a3bf11037f
keywords:
- TDM_SET_PROGRESS_BAR_MARQUEE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TDM_SET_PROGRESS_BAR_MARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f73d3d4308d2e3f963c015b6e36f385902bea6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079708"
---
# <a name="tdm_set_progress_bar_marquee-message"></a>Mensaje de marquesina de la \_ \_ barra de progreso establecida \_ en TDM \_

Inicia y detiene la presentación de marquesina de la barra de progreso en un cuadro de diálogo de tarea, y establece la velocidad del marco.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* \[ de\]
</dt> <dd>

Un **booleano** que indica si se debe activar o desactivar la pantalla de marquesina. Use **true** para activar la presentación de marquesina o **false** para desactivarla.

</dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Un **uint** que especifica el tiempo, en milisegundos, entre las actualizaciones de la animación de marquesina. Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.

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



 

 





