---
title: PBM_STEPIT mensaje (Commctrl.h)
description: Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento de paso mediante el envío del \_ mensaje SETSTEP de PBM.
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_STEPIT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0d4aee387e8f929aaaaf19d947422b95ca9528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167733"
---
# <a name="pbm_stepit-message"></a>Mensaje \_ STEPIT de PBM

Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento de paso mediante el envío del [**\_ mensaje SETSTEP de PBM.**](pbm-setstep.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="remarks"></a>Observaciones

Cuando la posición supera el valor de intervalo máximo, este mensaje restablece la posición actual para que el indicador de progreso se inicie de nuevo desde el principio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





