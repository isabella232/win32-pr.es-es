---
description: Las constantes de marca de bits PHONESTATUSFLAGS \_ describen una variedad de información de estado del dispositivo de teléfono.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: PHONESTATUSFLAGS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160621"
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



Especifica si se suspende la manipulación de TAPI del dispositivo telefónico. **TRUE si** se suspende, **FALSE en caso** contrario. El uso de un dispositivo de teléfono por parte de una aplicación se puede suspender temporalmente cuando el conmutador desea manipular el teléfono de forma que no pueda tolerar interferencias de la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




