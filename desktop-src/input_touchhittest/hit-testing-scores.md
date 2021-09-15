---
title: Puntuaciones de pruebas de impacto táctil
description: Las constantes siguientes identifican las posibles puntuaciones de prueba de acceso para un objeto, en relación con otros objetos que intersecan con el área de contacto táctil.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569165"
---
# <a name="touch-hit-testing-scores"></a>Puntuaciones de pruebas de impacto táctil

Las constantes siguientes identifican las posibles puntuaciones de prueba de acceso para un objeto, en relación con otros objetos que intersecan con el área de contacto táctil.

| Constante o valor | Descripción |
|---|---|
| **TOUCH_HIT_TESTING_PROXIMITY_CLOSEST** 0x0      | El objeto es el destino más probable.<br/>  |
| **TOUCH_HIT_TESTING_PROXIMITY_FARTHEST** 0xFFF | El objeto es el destino menos probable.<br/> |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | Winuser.h |
