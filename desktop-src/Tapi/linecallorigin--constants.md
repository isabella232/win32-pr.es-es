---
description: Las \_ constantes LINECALLORIGIN describen el origen de una llamada.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes de LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679339"
---
# <a name="linecallorigin_-constants"></a>Constantes de LINECALLORIGIN \_

Las **constantes \_ LINECALLORIGIN** describen el origen de una llamada.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**Conferencia de LINECALLORIGIN \_**
</dt> <dd> <dl> <dt>



El identificador de llamada es para una llamada de conferencia, es decir, es la conexión de la aplicación al puente de conferencia del conmutador.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externo**
</dt> <dd> <dl> <dt>



La llamada se originó como una llamada entrante en una línea externa.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN \_ entrante**
</dt> <dd> <dl> <dt>



La llamada se originó como una llamada entrante, pero el proveedor de servicios no puede determinar si proviene de otra estación en el mismo conmutador o de una línea externa. Los proveedores de servicios pueden usar esta constante solo cuando se ha negociado la versión 1,4 o posterior de TAPI. De lo contrario, el proveedor de servicios puede sustituir LINECALLORIGIN no \_ disponible.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**
</dt> <dd> <dl> <dt>



La llamada se originó como una llamada entrante en una estación interna al mismo entorno de conmutación.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN de \_ salida**
</dt> <dd> <dl> <dt>



La llamada se originó desde esta estación como una llamada saliente.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN no \_ disponible**
</dt> <dd> <dl> <dt>



El origen de la llamada no está disponible y nunca se conocerá para esta llamada.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ desconocido**
</dt> <dd> <dl> <dt>



Actualmente, el origen de la llamada es desconocido, pero puede ser conocido más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

El origen de una llamada se almacena en el miembro **dwOrigin** de la estructura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) de la llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




