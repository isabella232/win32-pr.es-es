---
description: Las \_ constantes de marcador de bits PHONESTATUSFLAGS describen una variedad de información de estado de dispositivo de teléfono.
ms.assetid: e94da591-49ab-4932-8621-0a62b8a55dd6
title: Constantes de PHONESTATUSFLAGS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969c2553274037797bdf9abea3e8bdbc1cd8d018
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679229"
---
# <a name="phonestatusflags_-constants"></a>Constantes de PHONESTATUSFLAGS \_

Las constantes de marcador de bits **PHONESTATUSFLAGS \_** describen una variedad de información de estado de dispositivo de teléfono.

<dl> <dt>

<span id="PHONESTATUSFLAGS_CONNECTED"></span><span id="phonestatusflags_connected"></span>**PHONESTATUSFLAGS \_ conectado**
</dt> <dd> <dl> <dt>



Especifica si el teléfono está conectado actualmente a TAPI. **True** si está conectado; en caso contrario, **false** .


</dt> </dl> </dd> <dt>

<span id="PHONESTATUSFLAGS_SUSPENDED"></span><span id="phonestatusflags_suspended"></span>**PHONESTATUSFLAGS \_ suspendido**
</dt> <dd> <dl> <dt>



Especifica si la manipulación de TAPI del dispositivo telefónico está suspendida. **True** si se suspende, **false** en caso contrario. El uso de una aplicación de un dispositivo telefónico se puede suspender temporalmente cuando el conmutador desea manipular el teléfono de forma que no pueda tolerar interferencias de la aplicación.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




