---
description: Las constantes de marca de bits LINECALLSELECT \_ describen qué llamadas se van a seleccionar.
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: LINECALLSELECT_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003153"
---
# <a name="linecallselect_-constants"></a>Constantes \_ LINECALLSELECT

Las constantes de marca de bits **LINECALLSELECT \_** describen qué llamadas se van a seleccionar.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT \_ ADDRESS**
</dt> <dd> <dl> <dt>



Selecciona la llamada en la dirección especificada.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT \_ CALL**
</dt> <dd> <dl> <dt>



Selecciona las llamadas relacionadas a la llamada especificada. Por ejemplo, las partes de una llamada de conferencia.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**
</dt> <dd> <dl> <dt>



Selecciona las llamadas relacionadas al identificador de llamada especificado. Esta marca solo se expone a las aplicaciones que negocian una versión TAPI de 3.0 o superior.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**
</dt> <dd> <dl> <dt>



Selecciona las llamadas en el identificador de dispositivo especificado. Esta marca solo se expone a las aplicaciones que negocian una versión tapi de la versión 2.1 o superior. Las aplicaciones deben considerar el uso de la constante LINECALLSELECT \_ LINE en lugar de esta.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ LINE**
</dt> <dd> <dl> <dt>



Selecciona las llamadas en el dispositivo de línea especificado.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Sin extensibilidad. Los 32 bits están reservados.

Esta constante se usa en [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) y para especificar una selección (ámbito) de las llamadas que se solicitan.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



 

 




