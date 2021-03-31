---
title: MDM_Policy_Config01_WirelessDisplay02 (clase)
description: La \_ clase Config01 de WirelessDisplay02 de directivas MDM \_ \_ representa las directivas de pantalla inalámbrica disponibles.
ms.assetid: 24b72ed9-cc14-4318-a9d1-597976083242
keywords:
- MDM_Policy_Config01_WirelessDisplay02 (clase)
- MDM_Policy_Config01_WirelessDisplay02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WirelessDisplay02
- MDM_Policy_Config01_WirelessDisplay02.InstanceID
- MDM_Policy_Config01_WirelessDisplay02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b99183f8fdf599df8b5c1b4e82b9b536f47019
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996456"
---
# <a name="mdm_policy_config01_wirelessdisplay02-class"></a><span data-ttu-id="5f0ea-105">\_ \_ Clase WirelessDisplay02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="5f0ea-105">MDM\_Policy\_Config01\_WirelessDisplay02 class</span></span>

<span data-ttu-id="5f0ea-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5f0ea-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5f0ea-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5f0ea-108">La **clase \_ \_ Config01 de \_ WirelessDisplay02 de directivas MDM** representa las directivas de pantalla inalámbrica disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-108">The **MDM\_Policy\_Config01\_WirelessDisplay02** class represents the wireless display policies available.</span></span>

<span data-ttu-id="5f0ea-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0ea-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f0ea-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WirelessDisplay02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMdnsDiscovery;
  sint32 AllowMdnsAdvertisement;
  sint32 AllowProjectionFromPCOverInfrastructure;
  sint32 AllowProjectionFromPC;
  sint32 AllowProjectionToPC;
  sint32 AllowProjectionToPCOverInfrastructure;
  sint32 AllowUserInputFromWirelessDisplayReceiver;
  sint32 RequirePinForPairing;
};
```

## <a name="members"></a><span data-ttu-id="5f0ea-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f0ea-111">Members</span></span>

<span data-ttu-id="5f0ea-112">La clase Config01 de la **\_ Directiva MDM \_ \_ WirelessDisplay02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5f0ea-112">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="5f0ea-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f0ea-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5f0ea-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f0ea-114">Properties</span></span>

<span data-ttu-id="5f0ea-115">La **clase \_ \_ Config01 de \_ WirelessDisplay02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-115">The **MDM\_Policy\_Config01\_WirelessDisplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5f0ea-116">AllowMdnsAdvertisement</span><span class="sxs-lookup"><span data-stu-id="5f0ea-116">AllowMdnsAdvertisement</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsadvertisement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-119">AllowMdnsDiscovery</span><span class="sxs-lookup"><span data-stu-id="5f0ea-119">AllowMdnsDiscovery</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowmdnsdiscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-122">AllowProjectionFromPC</span><span class="sxs-lookup"><span data-stu-id="5f0ea-122">AllowProjectionFromPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-125">AllowProjectionFromPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="5f0ea-125">AllowProjectionFromPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectionfrompcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-128">AllowProjectionToPC</span><span class="sxs-lookup"><span data-stu-id="5f0ea-128">AllowProjectionToPC</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-131">AllowProjectionToPCOverInfrastructure</span><span class="sxs-lookup"><span data-stu-id="5f0ea-131">AllowProjectionToPCOverInfrastructure</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowprojectiontopcoverinfrastructure)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5f0ea-134">AllowUserInputFromWirelessDisplayReceiver</span><span class="sxs-lookup"><span data-stu-id="5f0ea-134">AllowUserInputFromWirelessDisplayReceiver</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-allowuserinputfromwirelessdisplayreceiver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5f0ea-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f0ea-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f0ea-141">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="5f0ea-142">Para esta clase, la cadena es "WirelessDisplay".</span><span class="sxs-lookup"><span data-stu-id="5f0ea-142">For this class, the string is "WirelessDisplay".</span></span>

</dd> <dt>

<span data-ttu-id="5f0ea-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5f0ea-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5f0ea-147">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5f0ea-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="5f0ea-148">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="5f0ea-148">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="5f0ea-149">RequirePinForPairing</span><span class="sxs-lookup"><span data-stu-id="5f0ea-149">RequirePinForPairing</span></span>](/windows/client-management/mdm/policy-csp-wirelessdisplay#wirelessdisplay-requirepinforpairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5f0ea-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5f0ea-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5f0ea-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5f0ea-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f0ea-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f0ea-152">Requirements</span></span>



| <span data-ttu-id="5f0ea-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0ea-153">Requirement</span></span> | <span data-ttu-id="5f0ea-154">Value</span><span class="sxs-lookup"><span data-stu-id="5f0ea-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0ea-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f0ea-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5f0ea-156">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5f0ea-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5f0ea-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5f0ea-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5f0ea-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5f0ea-158">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="5f0ea-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5f0ea-159">Namespace</span></span><br/>                | <span data-ttu-id="5f0ea-160">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="5f0ea-160">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="5f0ea-161">MOF</span><span class="sxs-lookup"><span data-stu-id="5f0ea-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f0ea-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ea-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="5f0ea-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5f0ea-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f0ea-164"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="5f0ea-164"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

