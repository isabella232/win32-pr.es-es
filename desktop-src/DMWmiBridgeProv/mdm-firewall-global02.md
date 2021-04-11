---
title: MDM_Firewall_Global02 (clase)
description: La \_ clase Global02 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.
ms.assetid: 387a60c6-6dc9-4710-a1e3-0468ac004395
keywords:
- MDM_Firewall_Global02 (clase)
- MDM_Firewall_Global02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_Global02
- MDM_Firewall_Global02.InstanceID
- MDM_Firewall_Global02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cef2a8b11585848ac10035528db176b78d2e66b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274517"
---
# <a name="mdm_firewall_global02-class"></a><span data-ttu-id="e1338-105">\_Clase Global02 de Firewall de MDM \_</span><span class="sxs-lookup"><span data-stu-id="e1338-105">MDM\_Firewall\_Global02 class</span></span>

<span data-ttu-id="e1338-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e1338-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e1338-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e1338-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e1338-108">La \_ clase Global02 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="e1338-108">The MDM\_Firewall\_Global02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="e1338-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e1338-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1338-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1338-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_Global02
{
  string  InstanceID;
  string  ParentID;
  sint32  PolicyVersionSupported;
  sint32  CurrentProfiles;
  boolean DisableStatefulFtp;
  sint32  SaIdleTime;
  sint32  PresharedKeyEncoding;
  sint32  IPsecExempt;
  sint32  CRLcheck;
  string  PolicyVersion;
  string  BinaryVersionSupported;
  boolean OpportunisticallyMatchAuthSetPerKM;
  sint32  EnablePacketQueue;
};
```

## <a name="members"></a><span data-ttu-id="e1338-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1338-111">Members</span></span>

<span data-ttu-id="e1338-112">La **clase \_ \_ Global02 de Firewall de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e1338-112">The **MDM\_Firewall\_Global02** class has these types of members:</span></span>

-   [<span data-ttu-id="e1338-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1338-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1338-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1338-114">Properties</span></span>

<span data-ttu-id="e1338-115">La **clase \_ \_ Global02 de Firewall de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e1338-115">The **MDM\_Firewall\_Global02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e1338-116">BinaryVersionSupported</span><span class="sxs-lookup"><span data-stu-id="e1338-116">BinaryVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#binaryversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1338-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-119">CRLcheck</span><span class="sxs-lookup"><span data-stu-id="e1338-119">CRLcheck</span></span>](/windows/client-management/mdm/firewall-csp#crlcheck)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-122">CurrentProfiles</span><span class="sxs-lookup"><span data-stu-id="e1338-122">CurrentProfiles</span></span>](/windows/client-management/mdm/firewall-csp#currentprofiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-125">DisableStatefulFtp</span><span class="sxs-lookup"><span data-stu-id="e1338-125">DisableStatefulFtp</span></span>](/windows/client-management/mdm/firewall-csp#disablestatefulftp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e1338-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-128">EnablePacketQueue</span><span class="sxs-lookup"><span data-stu-id="e1338-128">EnablePacketQueue</span></span>](/windows/client-management/mdm/firewall-csp#enablepacketqueue)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1338-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1338-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1338-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1338-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1338-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1338-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-135">IPsecExempt</span><span class="sxs-lookup"><span data-stu-id="e1338-135">IPsecExempt</span></span>](/windows/client-management/mdm/firewall-csp#ipsecexempt)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-136">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-138">OpportunisticallyMatchAuthSetPerKM</span><span class="sxs-lookup"><span data-stu-id="e1338-138">OpportunisticallyMatchAuthSetPerKM</span></span>](/windows/client-management/mdm/firewall-csp#opportunisticallymatchauthsetperkm)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e1338-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1338-141">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e1338-141">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1338-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1338-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1338-144">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1338-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-145">PolicyVersion</span><span class="sxs-lookup"><span data-stu-id="e1338-145">PolicyVersion</span></span>](/windows/client-management/mdm/firewall-csp#policyversion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1338-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-148">PolicyVersionSupported</span><span class="sxs-lookup"><span data-stu-id="e1338-148">PolicyVersionSupported</span></span>](/windows/client-management/mdm/firewall-csp#policyversionsupported)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-149">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-149">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-151">PresharedKeyEncoding</span><span class="sxs-lookup"><span data-stu-id="e1338-151">PresharedKeyEncoding</span></span>](/windows/client-management/mdm/firewall-csp#presharedkeyencoding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-152">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-152">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e1338-154">SaIdleTime</span><span class="sxs-lookup"><span data-stu-id="e1338-154">SaIdleTime</span></span>](/windows/client-management/mdm/firewall-csp#saidletime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1338-155">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e1338-155">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e1338-156">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1338-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1338-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1338-157">Requirements</span></span>



| <span data-ttu-id="e1338-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1338-158">Requirement</span></span> | <span data-ttu-id="e1338-159">Value</span><span class="sxs-lookup"><span data-stu-id="e1338-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1338-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1338-160">Minimum supported client</span></span><br/> | <span data-ttu-id="e1338-161">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1338-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e1338-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1338-162">Minimum supported server</span></span><br/> | <span data-ttu-id="e1338-163">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e1338-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e1338-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1338-164">Namespace</span></span><br/>                | <span data-ttu-id="e1338-165">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e1338-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="e1338-166">MOF</span><span class="sxs-lookup"><span data-stu-id="e1338-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1338-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1338-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1338-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1338-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1338-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1338-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

