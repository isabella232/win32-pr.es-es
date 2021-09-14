---
title: PBM_GETSTEP mensaje (Commctrl.h)
description: Recupera el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje \_ STEPIT de PBM. De forma predeterminada, el incremento de paso se establece en 10.
ms.assetid: 0cf3052a-cf86-4c0e-ad59-ddab7c6e3602
keywords:
- PBM_GETSTEP controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_GETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dcc4adb18d2b60d2936c2cdc7ab79d00389b3ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167770"
---
# <a name="pbm_getstep-message"></a>Mensaje \_ GETSTEP de PBM

Recupera el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje [**\_ STEPIT de PBM.**](pbm-stepit.md) De forma predeterminada, el incremento de paso se establece en 10.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el incremento del paso actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





