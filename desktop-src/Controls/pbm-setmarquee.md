---
title: PBM_SETMARQUEE mensaje (Commctrl.h)
description: Establece la barra de progreso en modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.
ms.assetid: 6501bcb9-a711-470f-874f-f3484d3613b6
keywords:
- PBM_SETMARQUEE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167757"
---
# <a name="pbm_setmarquee-message"></a>Mensaje \_ SETMARQUEE de PBM

Establece la barra de progreso en modo de marquesina. Esto hace que la barra de progreso se mueva como una marquesina.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si se debe activar o desactivar el modo de marquesina.

</dd> <dt>

*lParam* 
</dt> <dd>Tiempo, en milisegundos, entre actualizaciones de animación de marquesina. Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Observaciones

Use este mensaje si no conoce la cantidad de progreso hacia la finalización, pero desea indicar que se está avanzando.

Envíe el **mensaje \_ SETMARQUEE** de PBM para iniciar o detener la animación.

> [!Note]  
> Debe establecer el estilo de control en [**PBS \_ MARQUEE antes**](progress-bar-control-styles.md) de intentar iniciar la animación.

 

> [!Note]  
> Este mensaje requiere ComCtl32.dll versión 6.00 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





