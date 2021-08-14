---
title: PBM_SETMARQUEE mensaje (Commctrl.h)
description: Establece la barra de progreso en modo de marquesina. Esto hace que la barra de progreso se mueva como un marco.
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
ms.openlocfilehash: f724f87faa6e989fddb17e8d6fb3b115dd04859ea426addb7d4c0b893aff407a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986145"
---
# <a name="pbm_setmarquee-message"></a>Mensaje \_ SETMARQUEE de PBM

Establece la barra de progreso en modo de marquesina. Esto hace que la barra de progreso se mueva como un marco.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica si se debe activar o desactivar el modo de marquesina.

</dd> <dt>

*lParam* 
</dt> <dd>Tiempo, en milisegundos, entre las actualizaciones de animación de marquesinas. Si este parámetro es cero, la animación de marquesina se actualiza cada 30 milisegundos.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Siempre devuelve **TRUE.**

## <a name="remarks"></a>Comentarios

Use este mensaje si no conoce la cantidad de progreso hacia la finalización, pero quiere indicar que se está avanzando.

Envíe el **mensaje \_ SETMARQUEE** de PBM para iniciar o detener la animación.

> [!Note]  
> Debe establecer el estilo de control en [**PBS \_ MARQUEE antes**](progress-bar-control-styles.md) de intentar iniciar la animación.

 

> [!Note]  
> Este mensaje requiere ComCtl32.dll versión 6.00 o posterior.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





