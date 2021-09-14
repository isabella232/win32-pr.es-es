---
title: PBM_DELTAPOS mensaje (Commctrl.h)
description: Avanza la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_DELTAPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d0c36bbfdf5a812c8a7ffb2b2cdda6720fb757
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167790"
---
# <a name="pbm_deltapos-message"></a>Mensaje \_ de DELTAPOS de PBM

Avanza la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cantidad para avanzar la posición.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="remarks"></a>Observaciones

Si el incremento da como resultado un valor fuera del intervalo del control, la posición se establece en el límite más cercano.

El comportamiento de este mensaje es indefinido si se envía a un control que tiene el estilo [**\_ MARQUEE de PBS.**](progress-bar-control-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





