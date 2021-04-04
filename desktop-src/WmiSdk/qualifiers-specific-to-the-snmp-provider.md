---
description: Los calificadores contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP obtiene acceso a un agente SNMP. A continuación se enumeran los calificadores únicos del proveedor SNMP.
ms.assetid: f2ac107c-e201-4670-96d1-883419787377
ms.tgt_platform: multiple
title: Calificadores específicos del proveedor SNMP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: a1405cb4d9609380fdf35d6ce05a0fc9e1255ba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811407"
---
# <a name="qualifiers-specific-to-the-snmp-provider"></a>Calificadores específicos del proveedor SNMP

Los calificadores contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP obtiene acceso a un agente SNMP. A continuación se enumeran los calificadores únicos del proveedor SNMP.

<dt>

<span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress** 
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Dirección de transporte asociada al agente SNMP, como una dirección IP o un nombre DNS. Debe establecer **AgentAddress** en una dirección de host de unidifusión válida o en un nombre de host de dominio que se pueda resolver a través del proceso de resolución de nombres de dominio del sistema operativo. **AgentAddress** no tiene ningún valor predeterminado.

</dd> <dt>

<span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize** 
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Número máximo de solicitudes SNMP pendientes simultáneas que se pueden enviar a este agente mientras aún no se ha recibido una respuesta. Una solicitud SNMP se considera pendiente hasta que se recibe una respuesta PDU o se agota el tiempo de espera. Un tamaño de ventana grande generalmente mejora el rendimiento, pero es posible que algunos agentes no funcionen bien con mucha carga. **AgentFlowControlWindowSize** se puede establecer en 0 para indicar un tamaño de ventana infinito o un entero entre 1 y 2 ^ 32-1. El valor predeterminado es 10. Este calificador es opcional.

</dd> <dt>

<span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName** 
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Cadena de octetos de longitud variable usada por el agente SNMP para autenticar una unidad de datos de protocolo SNMP (PDU) durante una operación de lectura (las siguientes solicitudes SNMP GET/GET NEXT). El nombre de la comunidad debe estar asignado a una cadena Unicode y se limita a caracteres alfanuméricos. El valor predeterminado es público. Este calificador es opcional.

</dd> <dt>

<span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount** 
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Número de veces que se puede reintentar una única solicitud SNMP cuando no hay ninguna respuesta del agente SNMP antes de que se considere que la solicitud ha producido un error. **AgentRetryCount** debe establecerse en un entero comprendido entre 0 y 2 ^ 32-1. El valor predeterminado es 1. Este calificador es opcional.

</dd> <dt>

<span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout** 
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Tiempo en milisegundos antes de que se considere que se ha quitado la unidad de datos de protocolo SNMP (PDU). Es el número de milisegundos que se debe esperar una respuesta a una solicitud SNMP enviada al agente SNMP. **AgentRetryTimeout** debe establecerse en un entero comprendido entre 0 y 2 ^ 32-1. El valor predeterminado es 500. Este calificador es opcional.

</dd> <dt>

<span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion** 
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Versión del protocolo SNMP que se va a utilizar al comunicarse con el agente SNMP. Actualmente, los únicos valores válidos son 1 (para SNMPv1) y 2C (para SNMPv2C). El valor predeterminado es 1. Este calificador es opcional.

</dd> <dt>

<span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport** 
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Protocolo de transporte utilizado para comunicarse con el agente SNMP. Actualmente, los únicos valores válidos son protocolo de Internet (IP) e intercambio de paquetes de Internet (IPX). El valor predeterminado es IP. Este calificador es opcional.

</dd> <dt>

<span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu** 
</dt> <dd>

Tipo de datos: **CIM \_ SINT32**

Número máximo de enlaces de variables contenidos en una sola PDU de SNMP. Cada solicitud SNMP enviada al agente SNMP contiene una o más variables SNMP. Este parámetro especifica el mayor número de variables que se pueden incluir en una única solicitud. **AgentVarBindsPerPdu** se puede establecer en 0 (cero) para que la implementación determine los enlaces de variables óptimos o en un entero entre 1 y 2 ^ 32-1. Tenga en cuenta que aunque el aumento de este valor puede mejorar el rendimiento, algunos agentes y redes no pueden tratar con la solicitud resultante. El valor predeterminado es 10. Este calificador es opcional.

</dd> <dt>

<span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName** 
</dt> <dd>

Tipo de datos **: \_ cadena CIM**

Cadena de octetos de longitud variable usada por el agente SNMP para autenticar una unidad de datos de protocolo SNMP (PDU) durante una operación de escritura (solicitud de conjunto SNMP). El nombre de la comunidad debe estar asignado a una cadena Unicode y se limita a caracteres alfanuméricos. El valor predeterminado es público. Este calificador es opcional.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

 




