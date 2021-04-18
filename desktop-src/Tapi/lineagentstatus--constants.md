---
description: Las \_ constantes LINEAGENTSTATUS muestran el estado de actualización de los miembros de la estructura LINEAGENTSTATUS para un agente.
ms.assetid: 068a2b24-a430-4cf5-b70d-5574e981a899
title: Constantes de LINEAGENTSTATUS_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1fb7afb2703a50d97d0423662a10c92743beb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681094"
---
# <a name="lineagentstatus_-constants"></a>Constantes de LINEAGENTSTATUS \_

Las **\_ constantes LINEAGENTSTATUS** muestran el estado de actualización de los miembros de la estructura [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) para un agente.

<dl> <dt>

<span id="LINEAGENTSTATUS_ACTIVITY"></span><span id="lineagentstatus_activity"></span>**\_actividad LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



Se ha actualizado el miembro **dwActivityID**, **dwActivitySize** o **dwActivityOffset** en [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) .


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_ACTIVITYLIST"></span><span id="lineagentstatus_activitylist"></span>**LINEAGENTSTATUS \_ ACTIVITYLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist) se ha actualizado. La aplicación puede llamar a [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_CAPSCHANGE"></span><span id="lineagentstatus_capschange"></span>**LINEAGENTSTATUS \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Las capacidades de [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) se han actualizado. La aplicación puede llamar a [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUP"></span><span id="lineagentstatus_group"></span>**\_Grupo LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUPLIST"></span><span id="lineagentstatus_grouplist"></span>**LINEAGENTSTATUS \_ GROUPLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist) se ha actualizado. La aplicación puede llamar a [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) para obtener la lista actualizada.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_NEXTSTATE"></span><span id="lineagentstatus_nextstate"></span>**LINEAGENTSTATUS \_ NEXTSTATE**
</dt> <dd> <dl> <dt>



El miembro **dwNextState** de [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_STATE"></span><span id="lineagentstatus_state"></span>**Estado de LINEAGENTSTATUS \_**
</dt> <dd> <dl> <dt>



El miembro **dwState** de [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDNEXTSTATES"></span><span id="lineagentstatus_validnextstates"></span>**LINEAGENTSTATUS \_ VALIDNEXTSTATES**
</dt> <dd> <dl> <dt>



El miembro **dwValidNextStates** de [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDSTATES"></span><span id="lineagentstatus_validstates"></span>**LINEAGENTSTATUS \_ VALIDSTATES**
</dt> <dd> <dl> <dt>



El miembro **dwValidStates** de [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) se ha actualizado.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



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

 

 




