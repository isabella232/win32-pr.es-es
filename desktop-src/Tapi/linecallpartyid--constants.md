---
description: Las \_ constantes de marcador de bits LINECALLPARTYID describen la naturaleza de la información disponible sobre las entidades implicadas en una llamada.
ms.assetid: e2a89f25-15f0-4f3c-9ac8-1e6b72c0d8db
title: Constantes de LINECALLPARTYID_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5dd8cca75fe6e91b97fac63dca6c0fdda554394
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690966"
---
# <a name="linecallpartyid_-constants"></a>Constantes de LINECALLPARTYID \_

Las constantes de marcador de bits **LINECALLPARTYID \_** describen la naturaleza de la información disponible sobre las entidades implicadas en una llamada.

<dl> <dt>

<span id="LINECALLPARTYID_ADDRESS"></span><span id="linecallpartyid_address"></span>**Dirección de LINECALLPARTYID \_**
</dt> <dd> <dl> <dt>



La información del identificador de entidad consta de la dirección de la entidad en formato de dirección canónico o en formato de dirección de marcado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_BLOCKED"></span><span id="linecallpartyid_blocked"></span>**LINECALLPARTYID \_ bloqueado**
</dt> <dd> <dl> <dt>



La información del identificador de entidad no está disponible porque la parte remota la ha bloqueado.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_NAME"></span><span id="linecallpartyid_name"></span>**nombre de LINECALLPARTYID \_**
</dt> <dd> <dl> <dt>



La información del identificador de entidad consta del nombre de la entidad (como, por ejemplo, de un directorio mantenido dentro del conmutador).


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_OUTOFAREA"></span><span id="linecallpartyid_outofarea"></span>**LINECALLPARTYID \_ OUTOFAREA**
</dt> <dd> <dl> <dt>



La información del identificador del autor de la llamada no está disponible porque la red no la propaga todo.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_PARTIAL"></span><span id="linecallpartyid_partial"></span>**LINECALLPARTYID \_ parcial**
</dt> <dd> <dl> <dt>



La información del identificador de entidad es válida, pero solo se limita a la información parcial.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNAVAIL"></span><span id="linecallpartyid_unavail"></span>**LINECALLPARTYID no \_ disponible**
</dt> <dd> <dl> <dt>



La información del identificador de entidad no está disponible y no estará disponible más adelante. Es posible que la información no esté disponible por motivos no especificados. Por ejemplo, la red no entregó la información, por lo que el proveedor de servicios la omitió, etc.


</dt> </dl> </dd> <dt>

<span id="LINECALLPARTYID_UNKNOWN"></span><span id="linecallpartyid_unknown"></span>**LINECALLPARTYID \_ desconocido**
</dt> <dd> <dl> <dt>



Actualmente, la información de identificador de entidad es desconocida, pero se puede conocer más adelante.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Para cada una de las partes posibles implicadas en una llamada, las constantes de **LINECALLPARTYID \_** describen cómo se da formato a la información de identificador de entidad. Esta información se proporciona en la estructura de datos [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




