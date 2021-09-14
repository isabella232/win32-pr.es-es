---
title: PBM_SETPOS mensaje (Commctrl.h)
description: Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición.
ms.assetid: 9ebeaa19-0f42-4af7-85d8-aae22498fd6f
keywords:
- PBM_SETPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a157f6a220f4932d39d13f08df79afa99d7348
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167749"
---
# <a name="pbm_setpos-message"></a>Mensaje \_ DE PBM SETPOS

Establece la posición actual de una barra de progreso y vuelve a dibujar la barra para reflejar la nueva posición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Entero con signo que se convierte en la nueva posición.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="remarks"></a>Observaciones

Si *wParam está* fuera del intervalo del control, la posición se establece en el límite más cercano.

No envíe este mensaje a un control que tenga el estilo [**\_ PBS MARQUEE.**](progress-bar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





