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
ms.openlocfilehash: 1bf9c6a4c21439f93f3459a5061daf28192081a042cc663a644110a1e54d2c54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986155"
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

## <a name="remarks"></a>Comentarios

Si *wParam está* fuera del intervalo del control, la posición se establece en el límite más cercano.

No envíe este mensaje a un control que tenga el estilo [**\_ PBS MARQUEE.**](progress-bar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





