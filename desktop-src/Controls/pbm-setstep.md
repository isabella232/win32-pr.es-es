---
title: PBM_SETSTEP mensaje (Commctrl.h)
description: Especifica el incremento de paso para una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje \_ STEPIT de PBM. De forma predeterminada, el incremento de paso se establece en 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP controles de Windows mensaje
topic_type:
- apiref
api_name:
- PBM_SETSTEP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1240d09aeadcd7994187704d0b5a4630ab1b7afb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127167734"
---
# <a name="pbm_setstep-message"></a>Mensaje \_ SETSTEP de PBM

Especifica el incremento de paso para una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un [**mensaje \_ STEPIT de PBM.**](pbm-stepit.md) De forma predeterminada, el incremento de paso se establece en 10.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Nuevo incremento de paso.

</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el incremento del paso anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





