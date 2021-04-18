---
title: MDM_Firewall_PublicProfile02 (clase)
description: La \_ clase PublicProfile02 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.
ms.assetid: 5524b931-10fa-43dc-8901-238312ecb6a8
keywords:
- MDM_Firewall_PublicProfile02 (clase)
- MDM_Firewall_PublicProfile02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Firewall_PublicProfile02
- MDM_Firewall_PublicProfile02.InstanceID
- MDM_Firewall_PublicProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530bac28c33b9ed3937f962a7f040e82b2ee1919
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489935"
---
# <a name="mdm_firewall_publicprofile02-class"></a><span data-ttu-id="31487-105">\_Clase PublicProfile02 de Firewall de MDM \_</span><span class="sxs-lookup"><span data-stu-id="31487-105">MDM\_Firewall\_PublicProfile02 class</span></span>

<span data-ttu-id="31487-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="31487-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="31487-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="31487-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="31487-108">La \_ clase PublicProfile02 de Firewall de MDM \_ se usa para configurar las opciones del firewall de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="31487-108">The MDM\_Firewall\_PublicProfile02 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="31487-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="31487-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="31487-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="31487-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_PublicProfile02
{
  string InstanceID;
  string ParentID;
  sint32 EnableFirewall;
  sint32 DisableStealthMode;
  sint32 Shielded;
  sint32 DisableUnicastResponsesToMulticastBroadcast;
  sint32 DisableInboundNotifications;
  sint32 AuthAppsAllowUserPrefMerge;
  sint32 GlobalPortsAllowUserPrefMerge;
  sint32 AllowLocalPolicyMerge;
  sint32 AllowLocalIpsecPolicyMerge;
  sint32 DefaultOutboundAction;
  sint32 DefaultInboundAction;
  sint32 DisableStealthModeIpsecSecuredPacketExemption;
};
```

## <a name="members"></a><span data-ttu-id="31487-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="31487-111">Members</span></span>

<span data-ttu-id="31487-112">La **clase \_ \_ PublicProfile02 de Firewall de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="31487-112">The **MDM\_Firewall\_PublicProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="31487-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31487-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="31487-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="31487-114">Properties</span></span>

<span data-ttu-id="31487-115">La **clase \_ \_ PublicProfile02 de Firewall de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="31487-115">The **MDM\_Firewall\_PublicProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="31487-116">AllowLocalIpsecPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="31487-116">AllowLocalIpsecPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalipsecpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-119">AllowLocalPolicyMerge</span><span class="sxs-lookup"><span data-stu-id="31487-119">AllowLocalPolicyMerge</span></span>](/windows/client-management/mdm/firewall-csp#allowlocalpolicymerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-122">AuthAppsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="31487-122">AuthAppsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#authappsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-125">DefaultInboundAction</span><span class="sxs-lookup"><span data-stu-id="31487-125">DefaultInboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultinboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-128">DefaultOutboundAction</span><span class="sxs-lookup"><span data-stu-id="31487-128">DefaultOutboundAction</span></span>](/windows/client-management/mdm/firewall-csp#defaultoutboundaction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-131">DisableInboundNotifications</span><span class="sxs-lookup"><span data-stu-id="31487-131">DisableInboundNotifications</span></span>](/windows/client-management/mdm/firewall-csp#disableinboundnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-134">DisableStealthMode</span><span class="sxs-lookup"><span data-stu-id="31487-134">DisableStealthMode</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-137">DisableStealthModeIpsecSecuredPacketExemption</span><span class="sxs-lookup"><span data-stu-id="31487-137">DisableStealthModeIpsecSecuredPacketExemption</span></span>](/windows/client-management/mdm/firewall-csp#disablestealthmodeipsecsecuredpacketexemption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-140">DisableUnicastResponsesToMulticastBroadcast</span><span class="sxs-lookup"><span data-stu-id="31487-140">DisableUnicastResponsesToMulticastBroadcast</span></span>](/windows/client-management/mdm/firewall-csp#disableunicastresponsestomulticastbroadcast)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-143">EnableFirewall</span><span class="sxs-lookup"><span data-stu-id="31487-143">EnableFirewall</span></span>](/windows/client-management/mdm/firewall-csp#enablefirewall)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-146">GlobalPortsAllowUserPrefMerge</span><span class="sxs-lookup"><span data-stu-id="31487-146">GlobalPortsAllowUserPrefMerge</span></span>](/windows/client-management/mdm/firewall-csp#globalportsallowuserprefmerge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31487-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="31487-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="31487-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31487-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31487-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31487-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31487-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="31487-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="31487-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="31487-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="31487-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="31487-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="31487-156">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="31487-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="31487-157">Blindada</span><span class="sxs-lookup"><span data-stu-id="31487-157">Shielded</span></span>](/windows/client-management/mdm/firewall-csp#shielded)
</dt> <dd> <dl> <dt>

<span data-ttu-id="31487-158">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="31487-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="31487-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="31487-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31487-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31487-160">Requirements</span></span>



| <span data-ttu-id="31487-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="31487-161">Requirement</span></span> | <span data-ttu-id="31487-162">Value</span><span class="sxs-lookup"><span data-stu-id="31487-162">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31487-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31487-163">Minimum supported client</span></span><br/> | <span data-ttu-id="31487-164">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="31487-164">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="31487-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="31487-165">Minimum supported server</span></span><br/> | <span data-ttu-id="31487-166">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="31487-166">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="31487-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31487-167">Namespace</span></span><br/>                | <span data-ttu-id="31487-168">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="31487-168">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="31487-169">MOF</span><span class="sxs-lookup"><span data-stu-id="31487-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31487-170"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31487-170"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="31487-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="31487-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31487-172"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31487-172"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

