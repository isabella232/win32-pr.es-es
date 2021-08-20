---
description: Las constantes de marca de bits PHONESTATUSFLAGS \_ describen una variedad de información de estado del dispositivo de teléfono.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b42f8e13adfae54c56e44244d04b3961216edb87e29730fec6f689f315380a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060653"
---
# <a name="phonestatusflags_-constants"></a>Constantes \_ PHONESTATUSFLAGS

Las constantes de marca de bits **PHONESTATUSFLAGS \_** describen una variedad de información de estado del dispositivo de teléfono.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ CONECTADO**
</dt> <dd> <dl> <dt>



Especifica si el teléfono está conectado actualmente a TAPI. **TRUE si** está conectado, **FALSE en caso** contrario.


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ SUSPENDIDO**
</dt> <dd> <dl> <dt>



Especifica si se suspende la manipulación de TAPI del dispositivo telefónico. **TRUE si** se suspende, **FALSE en caso** contrario. El uso de un dispositivo telefónico por parte de una aplicación se puede suspender temporalmente cuando el conmutador quiere manipular el teléfono de una manera que no pueda tolerar interferencias de la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




