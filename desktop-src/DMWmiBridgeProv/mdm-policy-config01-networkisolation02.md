---
title: MDM_Policy_Config01_NetworkIsolation02 (clase)
description: La \_ clase Config01 de NetworkIsolation02 de directivas MDM \_ \_ representa las directivas de explorador disponibles.
ms.assetid: f25ecbef-d232-4731-bac8-38a7d597db00
keywords:
- MDM_Policy_Config01_NetworkIsolation02 (clase)
- MDM_Policy_Config01_NetworkIsolation02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_NetworkIsolation02
- MDM_Policy_Config01_NetworkIsolation02.InstanceID
- MDM_Policy_Config01_NetworkIsolation02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9062d150de07860fd9d5b2510269ddcc3d2f8a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079348"
---
# <a name="mdm_policy_config01_networkisolation02-class"></a><span data-ttu-id="1bf85-105">\_ \_ Clase NetworkIsolation02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="1bf85-105">MDM\_Policy\_Config01\_NetworkIsolation02 class</span></span>

<span data-ttu-id="1bf85-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1bf85-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1bf85-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1bf85-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1bf85-108">La **clase \_ \_ Config01 de \_ NetworkIsolation02 de directivas MDM** representa las directivas de explorador disponibles.</span><span class="sxs-lookup"><span data-stu-id="1bf85-108">The **MDM\_Policy\_Config01\_NetworkIsolation02** class represents the browser policies available.</span></span>

<span data-ttu-id="1bf85-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1bf85-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf85-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1bf85-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_NetworkIsolation02
{
  string InstanceID;
  string ParentID;
  string EnterpriseIPRange;
  sint32 EnterpriseIPRangesAreAuthoritative;
  string EnterpriseNetworkDomainNames;
  string EnterpriseProxyServers;
  sint32 EnterpriseProxyServersAreAuthoritative;
  string NeutralResources;
  string EnterpriseCloudResources;
  string EnterpriseInternalProxyServers;
};
```

## <a name="members"></a><span data-ttu-id="1bf85-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1bf85-111">Members</span></span>

<span data-ttu-id="1bf85-112">La clase Config01 de la **\_ Directiva MDM \_ \_ NetworkIsolation02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1bf85-112">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these types of members:</span></span>

-   [<span data-ttu-id="1bf85-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bf85-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1bf85-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bf85-114">Properties</span></span>

<span data-ttu-id="1bf85-115">La **clase \_ \_ Config01 de \_ NetworkIsolation02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1bf85-115">The **MDM\_Policy\_Config01\_NetworkIsolation02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1bf85-116">EnterpriseCloudResources</span><span class="sxs-lookup"><span data-stu-id="1bf85-116">EnterpriseCloudResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisecloudresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-119">EnterpriseInternalProxyServers</span><span class="sxs-lookup"><span data-stu-id="1bf85-119">EnterpriseInternalProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseinternalproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-122">EnterpriseIPRange</span><span class="sxs-lookup"><span data-stu-id="1bf85-122">EnterpriseIPRange</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprange)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-125">EnterpriseIPRangesAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="1bf85-125">EnterpriseIPRangesAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseiprangesareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1bf85-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-128">EnterpriseNetworkDomainNames</span><span class="sxs-lookup"><span data-stu-id="1bf85-128">EnterpriseNetworkDomainNames</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterprisenetworkdomainnames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-131">EnterpriseProxyServers</span><span class="sxs-lookup"><span data-stu-id="1bf85-131">EnterpriseProxyServers</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyservers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1bf85-134">EnterpriseProxyServersAreAuthoritative</span><span class="sxs-lookup"><span data-stu-id="1bf85-134">EnterpriseProxyServersAreAuthoritative</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-enterpriseproxyserversareauthoritative)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1bf85-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bf85-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1bf85-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bf85-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1bf85-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1bf85-141">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1bf85-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="1bf85-142">Para esta clase, la cadena es "NetworkIsolation".</span><span class="sxs-lookup"><span data-stu-id="1bf85-142">For this class, the string is "NetworkIsolation".</span></span>

</dd> <dt>

[<span data-ttu-id="1bf85-143">NeutralResources</span><span class="sxs-lookup"><span data-stu-id="1bf85-143">NeutralResources</span></span>](/windows/client-management/mdm/policy-csp-networkisolation#networkisolation-neutralresources)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1bf85-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1bf85-146">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1bf85-146">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1bf85-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1bf85-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1bf85-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1bf85-149">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1bf85-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1bf85-150">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1bf85-150">Describes the full path to the parent node.</span></span> <span data-ttu-id="1bf85-151">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="1bf85-151">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bf85-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1bf85-152">Requirements</span></span>



| <span data-ttu-id="1bf85-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="1bf85-153">Requirement</span></span> | <span data-ttu-id="1bf85-154">Value</span><span class="sxs-lookup"><span data-stu-id="1bf85-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf85-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bf85-155">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf85-156">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1bf85-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1bf85-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1bf85-157">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf85-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1bf85-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1bf85-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1bf85-159">Namespace</span></span><br/>                | <span data-ttu-id="1bf85-160">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1bf85-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1bf85-161">MOF</span><span class="sxs-lookup"><span data-stu-id="1bf85-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1bf85-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1bf85-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1bf85-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1bf85-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1bf85-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bf85-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

