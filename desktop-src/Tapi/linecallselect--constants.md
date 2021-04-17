---
description: Las \_ constantes de marcador de bits LINECALLSELECT describen qué llamadas se van a seleccionar.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Constantes de LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681088"
---
# <a name="linecallselect_-constants"></a>Constantes de LINECALLSELECT \_

Las constantes de marcador de bits **LINECALLSELECT \_** describen qué llamadas se van a seleccionar.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**Dirección de LINECALLSELECT \_**
</dt> <dd> <dl> <dt>



Selecciona la llamada en la dirección especificada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_llamada a LINECALLSELECT**
</dt> <dd> <dl> <dt>



Selecciona las llamadas relacionadas a la llamada especificada. Por ejemplo, las entidades de una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



Selecciona las llamadas relacionadas al identificador de llamada especificado. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 3,0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



Selecciona llamadas en el identificador de dispositivo especificado. Esta marca solo se expone a las aplicaciones que negocian una versión de TAPI de 2,1 o superior. Las aplicaciones deben considerar el uso de la \_ constante de línea LINECALLSELECT en lugar de esta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**\_línea LINECALLSELECT**
</dt> <dd> <dl> <dt>



Selecciona llamadas en el dispositivo de línea especificado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Sin extensibilidad. Todos los 32 bits están reservados.

Esta constante se usa en [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) y para especificar una selección (ámbito) de las llamadas que se solicitan.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




