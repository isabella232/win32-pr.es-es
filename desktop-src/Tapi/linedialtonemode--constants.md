---
description: Las \_ constantes de marcador de bits LINEDIALTONEMODE describen diferentes tipos de tonos de marcado. Un tono de marcado especial suele tener un significado especial (como en el mensaje en espera).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Constantes de LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690040"
---
# <a name="linedialtonemode_-constants"></a>Constantes de LINEDIALTONEMODE \_

Las constantes de marcador de bits **LINEDIALTONEMODE \_** describen diferentes tipos de tonos de marcado. Un tono de marcado especial suele tener un significado especial (como en el mensaje en espera).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ externo**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado externo (red pública).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**LINEDIALTONEMODE \_ interno**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado interno, como en una PBX.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**LINEDIALTONEMODE \_ normal**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado normal, que normalmente es un tono continuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**LINEDIALTONEMODE \_ especial**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado especial que indica que una condición determinada (conocida por el conmutador o la red) está actualmente en vigor. Los tonos de marcado especiales suelen usar un tono interrumpido. Al igual que con un tono de marcado normal, esto indica que el conmutador está listo para recibir el número que se va a marcar.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**LINEDIALTONEMODE no \_ disponible**
</dt> <dd> <dl> <dt>



El modo de tono de marcado no está disponible y no se conocerá.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**LINEDIALTONEMODE \_ desconocido**
</dt> <dd> <dl> <dt>



El modo de tono de marcado no se conoce actualmente, pero puede ser conocido más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los 16 bits de orden superior se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Las **\_ constantes LINEDIALTONEMODE** se usan dentro de la estructura de datos [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para una llamada en el estado de marcado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




