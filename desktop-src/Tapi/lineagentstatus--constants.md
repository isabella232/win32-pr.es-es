---
description: Las constantes LINEAGENTSTATUS enumera el estado de actualización de los miembros de la estructura \_ LINEAGENTSTATUS de un agente.
ms.assetid: 068a2b24-a430-4cf5-b70d-5574e981a899
title: LINEAGENTSTATUS_ constantes (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d792fc31c1d56afaa483a9aa6890db1f52398d7107ef944cf53352734044b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682045"
---
# <a name="lineagentstatus_-constants"></a>LineAGENTSTATUS \_ (Constantes)

Las **constantes LINEAGENTSTATUS \_ enumera** el estado de actualización de los miembros de la estructura [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) de un agente.

<dl> <dt>

<span id="LINEAGENTSTATUS_ACTIVITY"></span><span id="lineagentstatus_activity"></span>**ACTIVIDAD \_ LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



Se ha actualizado el miembro **dwActivityID,** **dwActivitySize** o **dwActivityOffset** de [**LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_ACTIVITYLIST"></span><span id="lineagentstatus_activitylist"></span>**LINEAGENTSTATUS \_ ACTIVITYLIST**
</dt> <dd> <dl> <dt>



[**LineAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist) se ha actualizado. La aplicación puede llamar a [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_CAPSCHANGE"></span><span id="lineagentstatus_capschange"></span>**LINEAGENTSTATUS \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Se han actualizado las funcionalidades de [**LINEAGENTCAPS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) La aplicación puede llamar a [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUP"></span><span id="lineagentstatus_group"></span>**LINEAGENTSTATUS \_ GROUP**
</dt> <dd> <dl> <dt>



[**LineAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUPLIST"></span><span id="lineagentstatus_grouplist"></span>**LINEAGENTSTATUS \_ GROUPLIST**
</dt> <dd> <dl> <dt>



[**LineAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist) se ha actualizado. La aplicación puede llamar a [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_NEXTSTATE"></span><span id="lineagentstatus_nextstate"></span>**LINEAGENTSTATUS \_ NEXTSTATE**
</dt> <dd> <dl> <dt>



Se ha actualizado el miembro **dwNextState** [**de LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_STATE"></span><span id="lineagentstatus_state"></span>**ESTADO DE \_ LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



Se **ha actualizado el** miembro [**dwState de LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDNEXTSTATES"></span><span id="lineagentstatus_validnextstates"></span>**LINEAGENTSTATUS \_ VALIDNEXTSTATES**
</dt> <dd> <dl> <dt>



Se ha actualizado el miembro **dwValidNextStates** [**de LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDSTATES"></span><span id="lineagentstatus_validstates"></span>**LINEAGENTSTATUS \_ VALIDSTATES**
</dt> <dd> <dl> <dt>



Se ha actualizado el miembro **dwValidStates** [**de LINEAGENTSTATUS.**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist)
</dt> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist)
</dt> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)
</dt> <dt>

[**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)
</dt> <dt>

[**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)
</dt> </dl>

 

 




