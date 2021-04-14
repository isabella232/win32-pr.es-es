---
title: Puntuaciones de la prueba de posicionamiento táctil
description: Las constantes siguientes identifican las puntuaciones de pruebas de posicionamiento posibles para un objeto, con respecto a otros objetos que forman una intersección con el área de contacto táctil.
ms.assetid: EACDE6DB-ADBD-4F0C-8C31-7321AB6A73EA
topic_type:
- apiref
api_name:
- TOUCH_HIT_TESTING_PROXIMITY_CLOSEST
- TOUCH_HIT_TESTING_PROXIMITY_FARTHEST
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: f6590e7d56c1c9d92f0ff20524b6e4222d8655b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534005"
---
# <a name="touch-hit-testing-scores"></a>Puntuaciones de la prueba de posicionamiento táctil

Las constantes siguientes identifican las puntuaciones de pruebas de posicionamiento posibles para un objeto, con respecto a otros objetos que forman una intersección con el área de contacto táctil.

| Constante o valor | Descripción |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0X0      | El objeto es el destino más probable.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | El objeto es el destino menos probable.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | Winuser. h |
