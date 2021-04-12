---
description: Describe los errores del proveedor SNMP de WMI de 221 a 230.
ms.assetid: 50ca7a6b-2367-464b-98af-b65b0fab42c4
ms.tgt_platform: multiple
title: Errores de 221 a 230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89dc0fc15d039bca5f1d8740996928b3586fc61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276258"
---
# <a name="errors-221-through-230"></a><span data-ttu-id="eabaf-103">Errores de 221 a 230</span><span class="sxs-lookup"><span data-stu-id="eabaf-103">Errors 221 through 230</span></span>

<span data-ttu-id="eabaf-104">Describe los errores del proveedor SNMP de WMI de 221 a 230.</span><span class="sxs-lookup"><span data-stu-id="eabaf-104">Describes WMI SNMP provider errors 221 through 230.</span></span>

[<span data-ttu-id="eabaf-105">Error irrecuperable 222</span><span class="sxs-lookup"><span data-stu-id="eabaf-105">Fatal Error 222</span></span>](#fatal-error-222)

[<span data-ttu-id="eabaf-106">Error irrecuperable 223</span><span class="sxs-lookup"><span data-stu-id="eabaf-106">Fatal Error 223</span></span>](#fatal-error-223)

[<span data-ttu-id="eabaf-107">Error irrecuperable 224</span><span class="sxs-lookup"><span data-stu-id="eabaf-107">Fatal Error 224</span></span>](#fatal-error-224)

[<span data-ttu-id="eabaf-108">Error irrecuperable 225</span><span class="sxs-lookup"><span data-stu-id="eabaf-108">Fatal Error 225</span></span>](#fatal-error-225)

[<span data-ttu-id="eabaf-109">Error irrecuperable 226</span><span class="sxs-lookup"><span data-stu-id="eabaf-109">Fatal Error 226</span></span>](#fatal-error-226)

[<span data-ttu-id="eabaf-110">Error irrecuperable 227</span><span class="sxs-lookup"><span data-stu-id="eabaf-110">Fatal Error 227</span></span>](#fatal-error-227)

[<span data-ttu-id="eabaf-111">Error irrecuperable 228</span><span class="sxs-lookup"><span data-stu-id="eabaf-111">Fatal Error 228</span></span>](#fatal-error-228)

[<span data-ttu-id="eabaf-112">Error irrecuperable 229</span><span class="sxs-lookup"><span data-stu-id="eabaf-112">Fatal Error 229</span></span>](#fatal-error-229)

[<span data-ttu-id="eabaf-113">ADVERTENCIA 230</span><span class="sxs-lookup"><span data-stu-id="eabaf-113">Warning 230</span></span>](#warning-230)

## <a name="fatal-error-222"></a><span data-ttu-id="eabaf-114">Error irrecuperable 222</span><span class="sxs-lookup"><span data-stu-id="eabaf-114">Fatal Error 222</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222,> irrecuperable: " <fileName> : <\# de línea>: no se permite el tipo de notificación en la SMI de SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-115"><span id="_222__Fatal_____fileName___line____NOTIFICATION-TYPE_not_allowed_in_SNMPv1_SMI_"></span><span id="_222__fatal_____filename___line____notification-type_not_allowed_in_snmpv1_smi_"></span><span id="_222__FATAL_____FILENAME___LINE____NOTIFICATION-TYPE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<222, Fatal>: "<fileName>:<line\#>: NOTIFICATION-TYPE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-116">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-116">Module syntax error.</span></span> <span data-ttu-id="eabaf-117">Ha usado el tipo de notificación específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-117">You have used the SNMPv2C-specific NOTIFICATION-TYPE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-223"></a><span data-ttu-id="eabaf-118">Error irrecuperable 223</span><span class="sxs-lookup"><span data-stu-id="eabaf-118">Fatal Error 223</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223,> irrecuperable: " <fileName> : <línea \#>: no se permite la identidad del módulo en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-119"><span id="_223__Fatal_____fileName___line____MODULE-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_223__fatal_____filename___line____module-identity_not_allowed_in_snmpv1_smi_"></span><span id="_223__FATAL_____FILENAME___LINE____MODULE-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<223, Fatal>: "<fileName>:<line\#>: MODULE-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-120">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-120">Module syntax error.</span></span> <span data-ttu-id="eabaf-121">Ha usado la identidad del módulo específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-121">You have used the SNMPv2C-specific MODULE IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-224"></a><span data-ttu-id="eabaf-122">Error irrecuperable 224</span><span class="sxs-lookup"><span data-stu-id="eabaf-122">Fatal Error 224</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224,> irrecuperable: " <fileName> : <línea \#>: no se permite la identidad del objeto en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-123"><span id="_224__Fatal_____fileName___line____OBJECT-IDENTITY_not_allowed_in_SNMPv1_SMI_"></span><span id="_224__fatal_____filename___line____object-identity_not_allowed_in_snmpv1_smi_"></span><span id="_224__FATAL_____FILENAME___LINE____OBJECT-IDENTITY_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<224, Fatal>: "<fileName>:<line\#>: OBJECT-IDENTITY not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-124">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-124">Module syntax error.</span></span> <span data-ttu-id="eabaf-125">Ha usado el objeto-IDENTITY específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-125">You have used the SNMPv2C-specific OBJECT-IDENTITY in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-225"></a><span data-ttu-id="eabaf-126">Error irrecuperable 225</span><span class="sxs-lookup"><span data-stu-id="eabaf-126">Fatal Error 225</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225,> irrecuperable: " <fileName> : <línea \#>: no se permite la Convención de texto en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-127"><span id="_225__Fatal_____fileName___line____TEXTUAL-CONVENTION_not_allowed_in_SNMPv1_SMI_"></span><span id="_225__fatal_____filename___line____textual-convention_not_allowed_in_snmpv1_smi_"></span><span id="_225__FATAL_____FILENAME___LINE____TEXTUAL-CONVENTION_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<225, Fatal>: "<fileName>:<line\#>: TEXTUAL-CONVENTION not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-128">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-128">Module syntax error.</span></span> <span data-ttu-id="eabaf-129">Ha usado la Convención TEXTUAL específica de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-129">You have used the SNMPv2C-specific TEXTUAL-CONVENTION in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-226"></a><span data-ttu-id="eabaf-130">Error irrecuperable 226</span><span class="sxs-lookup"><span data-stu-id="eabaf-130">Fatal Error 226</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226,> irrecuperable: " <fileName> : <línea \#>: no se permite el grupo de objetos en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-131"><span id="_226__Fatal_____fileName___line____OBJECT-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_226__fatal_____filename___line____object-group_not_allowed_in_snmpv1_smi_"></span><span id="_226__FATAL_____FILENAME___LINE____OBJECT-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<226, Fatal>: "<fileName>:<line\#>: OBJECT-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-132">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-132">Module syntax error.</span></span> <span data-ttu-id="eabaf-133">Ha usado el grupo de objetos específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-133">You have used the SNMPv2C-specific OBJECT-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-227"></a><span data-ttu-id="eabaf-134">Error irrecuperable 227</span><span class="sxs-lookup"><span data-stu-id="eabaf-134">Fatal Error 227</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227,> irrecuperable: " <fileName> : <\# de línea>: no se permite el grupo de notificaciones en la SMI de SNMPv1"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-135"><span id="_227__Fatal_____fileName___line____NOTIFICATION-GROUP_not_allowed_in_SNMPv1_SMI_"></span><span id="_227__fatal_____filename___line____notification-group_not_allowed_in_snmpv1_smi_"></span><span id="_227__FATAL_____FILENAME___LINE____NOTIFICATION-GROUP_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<227, Fatal>: "<fileName>:<line\#>: NOTIFICATION-GROUP not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-136">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-136">Module syntax error.</span></span> <span data-ttu-id="eabaf-137">Ha usado el grupo de NOTIFICAciones específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-137">You have used the SNMPv2C-specific NOTIFICATION-GROUP in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-228"></a><span data-ttu-id="eabaf-138">Error irrecuperable 228</span><span class="sxs-lookup"><span data-stu-id="eabaf-138">Fatal Error 228</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228,> irrecuperable: " <fileName> : <de línea \#>: no se permite el módulo de compatibilidad en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-139"><span id="_228__Fatal_____fileName___line____MODULE-COMPLIANCE_not_allowed_in_SNMPv1_SMI_"></span><span id="_228__fatal_____filename___line____module-compliance_not_allowed_in_snmpv1_smi_"></span><span id="_228__FATAL_____FILENAME___LINE____MODULE-COMPLIANCE_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<228, Fatal>: "<fileName>:<line\#>: MODULE-COMPLIANCE not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-140">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-140">Module syntax error.</span></span> <span data-ttu-id="eabaf-141">Ha usado la compatibilidad con el módulo específico de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-141">You have used the SNMPv2C-specific MODULE-COMPLIANCE in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="fatal-error-229"></a><span data-ttu-id="eabaf-142">Error irrecuperable 229</span><span class="sxs-lookup"><span data-stu-id="eabaf-142">Fatal Error 229</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229,> irrecuperable: " <fileName> : <línea \#>: no se permiten funciones del agente en SNMPv1 SMI"**</span><span class="sxs-lookup"><span data-stu-id="eabaf-143"><span id="_229__Fatal_____fileName___line____AGENT-CAPABILITIES_not_allowed_in_SNMPv1_SMI_"></span><span id="_229__fatal_____filename___line____agent-capabilities_not_allowed_in_snmpv1_smi_"></span><span id="_229__FATAL_____FILENAME___LINE____AGENT-CAPABILITIES_NOT_ALLOWED_IN_SNMPV1_SMI_"></span>**<229, Fatal>: "<fileName>:<line\#>: AGENT-CAPABILITIES not allowed in SNMPv1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-144">Error de sintaxis de módulo.</span><span class="sxs-lookup"><span data-stu-id="eabaf-144">Module syntax error.</span></span> <span data-ttu-id="eabaf-145">Ha usado las capacidades del agente específicas de SNMPv2C en la MIB, pero ha especificado el modificador **/v1** , que requiere una compatibilidad estricta con la sintaxis SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="eabaf-145">You have used the SNMPv2C-specific AGENT-CAPABILITIES in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

## <a name="warning-230"></a><span data-ttu-id="eabaf-146">ADVERTENCIA 230</span><span class="sxs-lookup"><span data-stu-id="eabaf-146">Warning 230</span></span>

<dl> <dt>

<span data-ttu-id="eabaf-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, ADVERTENCIA>: " <fileName> : <línea \#>: ' <the wrong token> ' utilizada. Se supone ':: = ' "**</span><span class="sxs-lookup"><span data-stu-id="eabaf-147"><span id="_230__Warning_____fileName___line______the_wrong_token___used._Assuming________"></span><span id="_230__warning_____filename___line______the_wrong_token___used._assuming________"></span><span id="_230__WARNING_____FILENAME___LINE______THE_WRONG_TOKEN___USED._ASSUMING________"></span>**<230, Warning>: "<fileName>:<line\#>: '<the wrong token>' used. Assuming '::=' "**</span></span>
</dt> <dd>

<span data-ttu-id="eabaf-148">Se ha utilizado el token ": =", "::" o "=" en lugar de ":: =".</span><span class="sxs-lookup"><span data-stu-id="eabaf-148">The token ":=", "::", or "=" has been used instead of "::=".</span></span>

</dd> </dl>

 

 



