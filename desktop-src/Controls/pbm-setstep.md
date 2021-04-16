---
title: Mensaje de PBM_SETSTEP (commctrl. h)
description: Especifica el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de STEPIT de PBM \_ . De forma predeterminada, el incremento de paso se establece en 10.
ms.assetid: 75c1085b-6c7a-4c44-9a12-f9bf21f7d945
keywords:
- PBM_SETSTEP controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658263"
---
# <a name="pbm_setstep-message"></a>Mensaje de SETSTEP de PBM \_

Especifica el incremento de paso de una barra de progreso. El incremento de paso es la cantidad por la que la barra de progreso aumenta su posición actual cada vez que recibe un mensaje de [**\_ STEPIT de PBM**](pbm-stepit.md) . De forma predeterminada, el incremento de paso se establece en 10.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





