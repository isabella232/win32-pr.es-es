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
# <a name="qualifiers-specific-to-the-snmp-provider"></a><span data-ttu-id="53308-104">Calificadores específicos del proveedor SNMP</span><span class="sxs-lookup"><span data-stu-id="53308-104">Qualifiers Specific to the SNMP Provider</span></span>

<span data-ttu-id="53308-105">Los calificadores contienen información de contexto específica de la implementación y propiedades de transporte que definen cómo el proveedor SNMP obtiene acceso a un agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-105">Qualifiers contain implementation-specific context information and transport properties that define how the SNMP Provider accesses an SNMP agent.</span></span> <span data-ttu-id="53308-106">A continuación se enumeran los calificadores únicos del proveedor SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-106">The following lists the qualifiers unique to the SNMP Provider.</span></span>

<dt>

<span data-ttu-id="53308-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span><span class="sxs-lookup"><span data-stu-id="53308-107"><span id="AgentAddress_"></span><span id="agentaddress_"></span><span id="AGENTADDRESS_"></span>**AgentAddress**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-108">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="53308-108">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="53308-109">Dirección de transporte asociada al agente SNMP, como una dirección IP o un nombre DNS.</span><span class="sxs-lookup"><span data-stu-id="53308-109">Transport address associated with the SNMP agent, such as an IP address or DNS name.</span></span> <span data-ttu-id="53308-110">Debe establecer **AgentAddress** en una dirección de host de unidifusión válida o en un nombre de host de dominio que se pueda resolver a través del proceso de resolución de nombres de dominio del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53308-110">You should set **AgentAddress** to a valid unicast host address or a domain host name that can be resolved through the operating system's domain-name resolution process.</span></span> <span data-ttu-id="53308-111">**AgentAddress** no tiene ningún valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="53308-111">**AgentAddress** has no default value.</span></span>

</dd> <dt>

<span data-ttu-id="53308-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span><span class="sxs-lookup"><span data-stu-id="53308-112"><span id="AgentFlowControlWindowSize_"></span><span id="agentflowcontrolwindowsize_"></span><span id="AGENTFLOWCONTROLWINDOWSIZE_"></span>**AgentFlowControlWindowSize**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-113">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="53308-113">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="53308-114">Número máximo de solicitudes SNMP pendientes simultáneas que se pueden enviar a este agente mientras aún no se ha recibido una respuesta.</span><span class="sxs-lookup"><span data-stu-id="53308-114">Maximum number of concurrently outstanding SNMP requests that can be sent to this agent while a response has not yet been received.</span></span> <span data-ttu-id="53308-115">Una solicitud SNMP se considera pendiente hasta que se recibe una respuesta PDU o se agota el tiempo de espera. Un tamaño de ventana grande generalmente mejora el rendimiento, pero es posible que algunos agentes no funcionen bien con mucha carga.</span><span class="sxs-lookup"><span data-stu-id="53308-115">An SNMP request is considered outstanding until a PDU response has been received or it has timed out. A large window size generally improves performance, but some agents might not work well under a heavy load.</span></span> <span data-ttu-id="53308-116">**AgentFlowControlWindowSize** se puede establecer en 0 para indicar un tamaño de ventana infinito o un entero entre 1 y 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="53308-116">**AgentFlowControlWindowSize** can be set to 0 to indicate an infinite window size or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="53308-117">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="53308-117">The default value is 10.</span></span> <span data-ttu-id="53308-118">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-118">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span><span class="sxs-lookup"><span data-stu-id="53308-119"><span id="AgentReadCommunityName_"></span><span id="agentreadcommunityname_"></span><span id="AGENTREADCOMMUNITYNAME_"></span>**AgentReadCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-120">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="53308-120">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="53308-121">Cadena de octetos de longitud variable usada por el agente SNMP para autenticar una unidad de datos de protocolo SNMP (PDU) durante una operación de lectura (las siguientes solicitudes SNMP GET/GET NEXT).</span><span class="sxs-lookup"><span data-stu-id="53308-121">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a read operation (SNMP GET/GET NEXT requests).</span></span> <span data-ttu-id="53308-122">El nombre de la comunidad debe estar asignado a una cadena Unicode y se limita a caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="53308-122">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="53308-123">El valor predeterminado es público.</span><span class="sxs-lookup"><span data-stu-id="53308-123">The default value is public.</span></span> <span data-ttu-id="53308-124">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-124">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span><span class="sxs-lookup"><span data-stu-id="53308-125"><span id="AgentRetryCount_"></span><span id="agentretrycount_"></span><span id="AGENTRETRYCOUNT_"></span>**AgentRetryCount**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-126">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="53308-126">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="53308-127">Número de veces que se puede reintentar una única solicitud SNMP cuando no hay ninguna respuesta del agente SNMP antes de que se considere que la solicitud ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="53308-127">Number of times a single SNMP request can be retried when there is no response from the SNMP agent before the request is deemed to have failed.</span></span> <span data-ttu-id="53308-128">**AgentRetryCount** debe establecerse en un entero comprendido entre 0 y 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="53308-128">**AgentRetryCount** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="53308-129">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="53308-129">The default value is 1.</span></span> <span data-ttu-id="53308-130">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-130">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="53308-131"><span id="AgentRetryTimeout_"></span><span id="agentretrytimeout_"></span><span id="AGENTRETRYTIMEOUT_"></span>**AgentRetryTimeout**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-132">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="53308-132">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="53308-133">Tiempo en milisegundos antes de que se considere que se ha quitado la unidad de datos de protocolo SNMP (PDU).</span><span class="sxs-lookup"><span data-stu-id="53308-133">Time in milliseconds before the SNMP Protocol Data Unit (PDU) is considered to have been dropped.</span></span> <span data-ttu-id="53308-134">Es el número de milisegundos que se debe esperar una respuesta a una solicitud SNMP enviada al agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-134">This is the number of milliseconds to wait for a response to an SNMP request sent to the SNMP agent.</span></span> <span data-ttu-id="53308-135">**AgentRetryTimeout** debe establecerse en un entero comprendido entre 0 y 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="53308-135">**AgentRetryTimeout** must be set to an integer between 0 and 2^32-1.</span></span> <span data-ttu-id="53308-136">El valor predeterminado es 500.</span><span class="sxs-lookup"><span data-stu-id="53308-136">The default value is 500.</span></span> <span data-ttu-id="53308-137">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-137">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span><span class="sxs-lookup"><span data-stu-id="53308-138"><span id="AgentSNMPVersion_"></span><span id="agentsnmpversion_"></span><span id="AGENTSNMPVERSION_"></span>**AgentSNMPVersion**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-139">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="53308-139">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="53308-140">Versión del protocolo SNMP que se va a utilizar al comunicarse con el agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-140">Version of the SNMP protocol to be used when communicating with the SNMP agent.</span></span> <span data-ttu-id="53308-141">Actualmente, los únicos valores válidos son 1 (para SNMPv1) y 2C (para SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="53308-141">Currently, the only valid values are 1 (for SNMPv1) and 2C (for SNMPv2C).</span></span> <span data-ttu-id="53308-142">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="53308-142">The default value is 1.</span></span> <span data-ttu-id="53308-143">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-143">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span><span class="sxs-lookup"><span data-stu-id="53308-144"><span id="AgentTransport_"></span><span id="agenttransport_"></span><span id="AGENTTRANSPORT_"></span>**AgentTransport**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-145">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="53308-145">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="53308-146">Protocolo de transporte utilizado para comunicarse con el agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-146">Transport protocol used to communicate with the SNMP agent.</span></span> <span data-ttu-id="53308-147">Actualmente, los únicos valores válidos son protocolo de Internet (IP) e intercambio de paquetes de Internet (IPX).</span><span class="sxs-lookup"><span data-stu-id="53308-147">Currently the only valid values are Internet Protocol (IP) and Internet Packet Exchange (IPX).</span></span> <span data-ttu-id="53308-148">El valor predeterminado es IP.</span><span class="sxs-lookup"><span data-stu-id="53308-148">The default value is IP.</span></span> <span data-ttu-id="53308-149">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-149">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span><span class="sxs-lookup"><span data-stu-id="53308-150"><span id="AgentVarBindsPerPdu_"></span><span id="agentvarbindsperpdu_"></span><span id="AGENTVARBINDSPERPDU_"></span>**AgentVarBindsPerPdu**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-151">Tipo de datos: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="53308-151">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="53308-152">Número máximo de enlaces de variables contenidos en una sola PDU de SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-152">Maximum number of variable bindings contained within a single SNMP PDU.</span></span> <span data-ttu-id="53308-153">Cada solicitud SNMP enviada al agente SNMP contiene una o más variables SNMP.</span><span class="sxs-lookup"><span data-stu-id="53308-153">Every SNMP request sent to the SNMP agent contains one or more SNMP variables.</span></span> <span data-ttu-id="53308-154">Este parámetro especifica el mayor número de variables que se pueden incluir en una única solicitud.</span><span class="sxs-lookup"><span data-stu-id="53308-154">This parameter specifies the largest number of variables that can be included in a single request.</span></span> <span data-ttu-id="53308-155">**AgentVarBindsPerPdu** se puede establecer en 0 (cero) para que la implementación determine los enlaces de variables óptimos o en un entero entre 1 y 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="53308-155">**AgentVarBindsPerPdu** can be set to 0 (zero) to cause the implementation to determine the optimal variable bindings or to an integer between 1 and 2^32-1.</span></span> <span data-ttu-id="53308-156">Tenga en cuenta que aunque el aumento de este valor puede mejorar el rendimiento, algunos agentes y redes no pueden tratar con la solicitud resultante.</span><span class="sxs-lookup"><span data-stu-id="53308-156">Note that while increasing this value can improve performance, some agents and networks cannot deal with the resulting request.</span></span> <span data-ttu-id="53308-157">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="53308-157">The default value is 10.</span></span> <span data-ttu-id="53308-158">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-158">This qualifier is optional.</span></span>

</dd> <dt>

<span data-ttu-id="53308-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span><span class="sxs-lookup"><span data-stu-id="53308-159"><span id="AgentWriteCommunityName_"></span><span id="agentwritecommunityname_"></span><span id="AGENTWRITECOMMUNITYNAME_"></span>**AgentWriteCommunityName**</span></span> 
</dt> <dd>

<span data-ttu-id="53308-160">Tipo de datos **: \_ cadena CIM**</span><span class="sxs-lookup"><span data-stu-id="53308-160">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="53308-161">Cadena de octetos de longitud variable usada por el agente SNMP para autenticar una unidad de datos de protocolo SNMP (PDU) durante una operación de escritura (solicitud de conjunto SNMP).</span><span class="sxs-lookup"><span data-stu-id="53308-161">Variable-length octet string that is used by the SNMP agent to authenticate an SNMP Protocol Data Unit (PDU) during a write operation (SNMP SET request).</span></span> <span data-ttu-id="53308-162">El nombre de la comunidad debe estar asignado a una cadena Unicode y se limita a caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="53308-162">The community name must be mapped to a Unicode string and is limited to alphanumeric characters.</span></span> <span data-ttu-id="53308-163">El valor predeterminado es público.</span><span class="sxs-lookup"><span data-stu-id="53308-163">The default value is public.</span></span> <span data-ttu-id="53308-164">Este calificador es opcional.</span><span class="sxs-lookup"><span data-stu-id="53308-164">This qualifier is optional.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53308-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53308-165">Requirements</span></span>



| <span data-ttu-id="53308-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="53308-166">Requirement</span></span> | <span data-ttu-id="53308-167">Value</span><span class="sxs-lookup"><span data-stu-id="53308-167">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="53308-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53308-168">Minimum supported client</span></span><br/> | <span data-ttu-id="53308-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53308-169">Windows Vista</span></span><br/>       |
| <span data-ttu-id="53308-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53308-170">Minimum supported server</span></span><br/> | <span data-ttu-id="53308-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53308-171">Windows Server 2008</span></span><br/> |



 

 




