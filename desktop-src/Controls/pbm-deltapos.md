---
title: Mensaje de PBM_DELTAPOS (commctrl. h)
description: Hace avanzar la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.
ms.assetid: 92c89434-d50b-45e7-b686-42e9297518b9
keywords:
- PBM_DELTAPOS controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079563"
---
# <a name="pbm_deltapos-message"></a>Mensaje de DELTAPOS de PBM \_

Hace avanzar la posición actual de una barra de progreso en un incremento especificado y vuelve a dibujar la barra para reflejar la nueva posición.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Cantidad que se va a avanzar la posición.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la posición anterior.

## <a name="remarks"></a>Observaciones

Si el incremento da como resultado un valor fuera del intervalo del control, la posición se establece en el límite más cercano.

El comportamiento de este mensaje es indefinido si se envía a un control que tiene el estilo [**de \_ marquesina de PBS**](progress-bar-control-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





