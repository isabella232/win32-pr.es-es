---
title: Mensaje de PBM_SETMARQUEE (commctrl. h)
description: Establece la barra de progreso en el modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- PBM_SETMARQUEE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9229291113f034924cf9ce8112c0e99376d37932
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996735"
---
# <a name="pbm_setmarquee-message"></a>Mensaje de SETMARQUEE de PBM \_

Establece la barra de progreso en el modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si se activa o desactiva el modo de marquesina.

</dd> <dt>

*lParam* 
</dt> <dd>Tiempo, en milisegundos, entre actualizaciones de animaciones de marquesina. Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **true**.

## <a name="remarks"></a>Observaciones

Use este mensaje si no conoce la cantidad de progreso hasta la finalización, pero quiere indicar que se está realizando el progreso.

Envíe el mensaje de **PBM \_ SETMARQUEE** para iniciar o detener la animación.

> [!Note]  
> Debe establecer el estilo de control en [**la \_ marquesina de PBS**](progress-bar-control-styles.md) antes de intentar iniciar la animación.

 

> [!Note]  
> Este mensaje requiere ComCtl32.dll versión 6,00 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





