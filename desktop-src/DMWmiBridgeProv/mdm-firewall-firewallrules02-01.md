---
title: MDM_Firewall_FirewallRules02_01 (clase)
description: La \_ clase FirewallRules02 01 del firewall de MDM \_ \_ se usa para configurar las opciones del firewall de Windows Defender.
ms.assetid: b09cbd98-152e-486c-acb5-4e1d83e5f8e2
keywords:
- MDM_Firewall_FirewallRules02_01 (clase)
- MDM_Firewall_FirewallRules02_01 clase, descrita
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_Firewall_FirewallRules02_01
- MDM_Firewall_FirewallRules02_01.InstanceID
- MDM_Firewall_FirewallRules02_01.ParentID
- MDM_Firewall_FirewallRules02_01.IcmpTypesAndCodes
- MDM_Firewall_FirewallRules02_01.FriendlyName
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: 494be18ece91e7a1776780542f988b80cb822e42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150120"
---
# <a name="mdm_firewall_firewallrules02_01-class"></a><span data-ttu-id="08765-105">\_ \_ Clase FirewallRules02 01 del Firewall \_ MDM</span><span class="sxs-lookup"><span data-stu-id="08765-105">MDM\_Firewall\_FirewallRules02\_01 class</span></span>

<span data-ttu-id="08765-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="08765-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="08765-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="08765-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="08765-108">La \_ clase FirewallRules02 01 del firewall de MDM \_ \_ se usa para configurar las opciones del firewall de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="08765-108">The MDM\_Firewall\_FirewallRules02\_01 class is used to configure the Windows Defender Firewall settings.</span></span>

<span data-ttu-id="08765-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="08765-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="08765-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08765-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Firewall_FirewallRules02_01
{
  string  InstanceID;
  string  ParentID;
  sint32  Protocol;
  string  LocalPortRanges;
  string  RemotePortRanges;
  string  LocalAddressRanges;
  string  RemoteAddressRanges;
  string  Description;
  boolean Enabled;
  sint32  Profiles;
  string  Direction;
  string  InterfaceTypes;
  string  IcmpTypesAndCodes;
  boolean EdgeTraversal;
  string  LocalUserAuthorizedList;
  string  Status;
  string  FriendlyName;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="08765-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="08765-111">Members</span></span>

<span data-ttu-id="08765-112">La **clase \_ \_ FirewallRules02 \_ 01 del firewall de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="08765-112">The **MDM\_Firewall\_FirewallRules02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="08765-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08765-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="08765-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="08765-114">Properties</span></span>

<span data-ttu-id="08765-115">La **clase \_ \_ FirewallRules02 \_ 01 del firewall de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="08765-115">The **MDM\_Firewall\_FirewallRules02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="08765-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="08765-116">Description</span></span>](/windows/client-management/mdm/firewall-csp#description)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-119">Dirección</span><span class="sxs-lookup"><span data-stu-id="08765-119">Direction</span></span>](/windows/client-management/mdm/firewall-csp#direction)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-122">EdgeTraversal</span><span class="sxs-lookup"><span data-stu-id="08765-122">EdgeTraversal</span></span>](/windows/client-management/mdm/firewall-csp#edgetraversal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-123">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08765-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08765-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-125">Enabled</span><span class="sxs-lookup"><span data-stu-id="08765-125">Enabled</span></span>](/windows/client-management/mdm/firewall-csp#enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="08765-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="08765-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08765-128">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="08765-128">**FriendlyName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08765-131">TBD</span><span class="sxs-lookup"><span data-stu-id="08765-131">TBD</span></span>

</dd> <dt>

<span data-ttu-id="08765-132">**IcmpTypesAndCodes**</span><span class="sxs-lookup"><span data-stu-id="08765-132">**IcmpTypesAndCodes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="08765-135">TBD</span><span class="sxs-lookup"><span data-stu-id="08765-135">TBD</span></span>

</dd> <dt>

<span data-ttu-id="08765-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="08765-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08765-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08765-139">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08765-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-140">InterfaceTypes</span><span class="sxs-lookup"><span data-stu-id="08765-140">InterfaceTypes</span></span>](/windows/client-management/mdm/firewall-csp#interfacetypes)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-143">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="08765-143">LocalAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-146">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="08765-146">LocalPortRanges</span></span>](/windows/client-management/mdm/firewall-csp#localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-149">LocalUserAuthorizedList</span><span class="sxs-lookup"><span data-stu-id="08765-149">LocalUserAuthorizedList</span></span>](/windows/client-management/mdm/firewall-csp#localuserauthorizedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="08765-152">Name</span></span>](/windows/client-management/mdm/firewall-csp#name)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="08765-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="08765-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="08765-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="08765-158">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="08765-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-159">Perfiles</span><span class="sxs-lookup"><span data-stu-id="08765-159">Profiles</span></span>](/windows/client-management/mdm/firewall-csp#profiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-160">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08765-160">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08765-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-161">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-162">Protocolo</span><span class="sxs-lookup"><span data-stu-id="08765-162">Protocol</span></span>](/windows/client-management/mdm/firewall-csp#protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-163">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="08765-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="08765-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-165">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="08765-165">RemoteAddressRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-167">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-167">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-168">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="08765-168">RemotePortRanges</span></span>](/windows/client-management/mdm/firewall-csp#remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-170">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="08765-171">Estado</span><span class="sxs-lookup"><span data-stu-id="08765-171">Status</span></span>](/windows/client-management/mdm/firewall-csp#status)
</dt> <dd> <dl> <dt>

<span data-ttu-id="08765-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="08765-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="08765-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="08765-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="08765-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08765-174">Requirements</span></span>



| <span data-ttu-id="08765-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="08765-175">Requirement</span></span> | <span data-ttu-id="08765-176">Value</span><span class="sxs-lookup"><span data-stu-id="08765-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08765-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08765-177">Minimum supported client</span></span><br/> | <span data-ttu-id="08765-178">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="08765-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="08765-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="08765-179">Minimum supported server</span></span><br/> | <span data-ttu-id="08765-180">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="08765-180">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="08765-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="08765-181">Namespace</span></span><br/>                | <span data-ttu-id="08765-182">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="08765-182">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="08765-183">MOF</span><span class="sxs-lookup"><span data-stu-id="08765-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08765-184"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08765-184"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="08765-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="08765-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08765-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08765-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

