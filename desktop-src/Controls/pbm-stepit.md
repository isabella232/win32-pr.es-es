---
title: Mensaje de PBM_STEPIT (commctrl. h)
description: Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento del paso mediante el envío del mensaje de SETSTEP de PBM \_ .
ms.assetid: fd9947f6-7a48-4207-b691-b7db78eb8a85
keywords:
- PBM_STEPIT controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996732"
---
# <a name="pbm_stepit-message"></a>Mensaje de STEPIT de PBM \_

Avanza la posición actual de una barra de progreso en el incremento de paso y vuelve a dibujar la barra para reflejar la nueva posición. Una aplicación establece el incremento del paso mediante el envío del mensaje de [**\_ SETSTEP de PBM**](pbm-setstep.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="remarks"></a>Observaciones

Cuando la posición supera el valor de intervalo máximo, este mensaje restablece la posición actual para que el indicador de progreso vuelva a empezar desde el principio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





