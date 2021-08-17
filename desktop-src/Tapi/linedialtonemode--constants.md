---
description: Las constantes de marca de bits DELINEIALTONEMODE \_ describen diferentes tipos de tono de marcado. Un tono de marcado especial suele tener un significado especial (como con el mensaje en espera).
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: LINEDIALTONEMODE_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b51ac15da6c1cba2b1b4e5b51710f04ba54549d2e08f4e9b50a20c543c305d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309965"
---
# <a name="linedialtonemode_-constants"></a>CONSTANTIALTONEMODE \_ (Constantes)

Las constantes de marca de bits **DELINEIALTONEMODE \_** describen diferentes tipos de tono de marcado. Un tono de marcado especial suele tener un significado especial (como con el mensaje en espera).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**LINEDIALTONEMODE \_ EXTERNAL**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcación externo (red pública).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**DELINEIALTONEMODE \_ INTERNAL**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcación interno, como dentro de UN ELEMENTO DE CONTROL DE ACCESO DIRECTO.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**DELINEIALTONEMODE \_ NORMAL**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado normal, que normalmente es un tono continuo.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**DELINEIALTONEMODE \_ SPECIAL**
</dt> <dd> <dl> <dt>



Se trata de un tono de marcado especial que indica que una determinada condición (conocida por el conmutador o la red) está actualmente en vigor. Los tonos de marcado especiales suelen usar un tono interrumpido. Al igual que con un tono de marcado normal, esto indica que el conmutador está listo para recibir el número que se va a marcar.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**UNAVAIL DE LA PROPIEDAD DELINEIALTONEMODE \_**
</dt> <dd> <dl> <dt>



El modo de tono de marcado no está disponible y no se conocerá.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**DESCONOCIADO DE LA PROPIEDAD \_ DELINEIALTONEMODE**
</dt> <dd> <dl> <dt>



El modo de tono de marcado no se conoce actualmente, pero puede conocerse más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los 16 bits de orden alto se pueden asignar para extensiones específicas del dispositivo. Los 16 bits de orden inferior están reservados.

Las **constantes DELINEIALTONEMODE \_ se** usan dentro de la estructura de datos [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) para una llamada en estado dialtone.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




