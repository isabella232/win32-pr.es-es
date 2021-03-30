---
title: MDM_Policy_Result01_DeliveryOptimization02 (clase)
description: La \_ clase Result01 de DeliveryOptimization02 de directivas MDM \_ \_ representa las directivas de optimización de entrega disponibles.
ms.assetid: 0f8a6de1-0f6c-4ee2-9235-9b5dc855f8c4
keywords:
- MDM_Policy_Result01_DeliveryOptimization02 (clase)
- MDM_Policy_Result01_DeliveryOptimization02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeliveryOptimization02
- MDM_Policy_Result01_DeliveryOptimization02.InstanceID
- MDM_Policy_Result01_DeliveryOptimization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69408228b2ed67c12de83575ddc524387498e91a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801664"
---
# <a name="mdm_policy_result01_deliveryoptimization02-class"></a><span data-ttu-id="b9209-105">\_ \_ Clase DeliveryOptimization02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="b9209-105">MDM\_Policy\_Result01\_DeliveryOptimization02 class</span></span>

<span data-ttu-id="b9209-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b9209-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b9209-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b9209-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b9209-108">La **clase \_ \_ Result01 de \_ DeliveryOptimization02 de directivas MDM** representa las directivas de optimización de entrega disponibles.</span><span class="sxs-lookup"><span data-stu-id="b9209-108">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class represents the delivery optimization policies available.</span></span>

<span data-ttu-id="b9209-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b9209-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9209-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9209-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeliveryOptimization02
{
  string InstanceID;
  string ParentID;
  sint32 DOAbsoluteMaxCacheSize;
  sint32 DOAllowVPNPeerCaching;
  string DOCacheHost;
  string DOGroupID;
  sint32 DOMaxUploadBandwidth;
  sint32 DOPercentageMaxDownloadBandwidth;
  sint32 DOMonthlyUploadDataCap;
  string DOModifyCacheDrive;
  sint32 DOMinBackgroundQos;
  sint32 DOMinRAMAllowedToPeer;
  sint32 DOMinFileSizeToCache;
  sint32 DOMinDiskSizeAllowedToPeer;
  sint32 DOMinBatteryPercentageAllowedToUpload;
  sint32 DOMaxCacheSize;
  sint32 DOMaxDownloadBandwidth;
  sint32 DOMaxCacheAge;
  sint32 DODownloadMode;
};
```

## <a name="members"></a><span data-ttu-id="b9209-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b9209-111">Members</span></span>

<span data-ttu-id="b9209-112">La clase Result01 de la **\_ Directiva MDM \_ \_ DeliveryOptimization02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b9209-112">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these types of members:</span></span>

-   [<span data-ttu-id="b9209-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9209-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9209-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9209-114">Properties</span></span>

<span data-ttu-id="b9209-115">La **clase \_ \_ Result01 de \_ DeliveryOptimization02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b9209-115">The **MDM\_Policy\_Result01\_DeliveryOptimization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b9209-116">DOAbsoluteMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="b9209-116">DOAbsoluteMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doabsolutemaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-119">DOAllowVPNPeerCaching</span><span class="sxs-lookup"><span data-stu-id="b9209-119">DOAllowVPNPeerCaching</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-doallowvpnpeercaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-122">DOCacheHost</span><span class="sxs-lookup"><span data-stu-id="b9209-122">DOCacheHost</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-docachehost)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9209-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-125">DODownloadMode</span><span class="sxs-lookup"><span data-stu-id="b9209-125">DODownloadMode</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dodownloadmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-128">DOGroupID</span><span class="sxs-lookup"><span data-stu-id="b9209-128">DOGroupID</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dogroupid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9209-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-131">DOMaxCacheAge</span><span class="sxs-lookup"><span data-stu-id="b9209-131">DOMaxCacheAge</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcacheage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-134">DOMaxCacheSize</span><span class="sxs-lookup"><span data-stu-id="b9209-134">DOMaxCacheSize</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxcachesize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-137">DOMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9209-137">DOMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-140">DOMaxUploadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9209-140">DOMaxUploadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domaxuploadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-143">DOMinBackgroundQos</span><span class="sxs-lookup"><span data-stu-id="b9209-143">DOMinBackgroundQos</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbackgroundqos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-146">DOMinBatteryPercentageAllowedToUpload</span><span class="sxs-lookup"><span data-stu-id="b9209-146">DOMinBatteryPercentageAllowedToUpload</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominbatterypercentageallowedtoupload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-149">DOMinDiskSizeAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="b9209-149">DOMinDiskSizeAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domindisksizeallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-152">DOMinFileSizeToCache</span><span class="sxs-lookup"><span data-stu-id="b9209-152">DOMinFileSizeToCache</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominfilesizetocache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-155">DOMinRAMAllowedToPeer</span><span class="sxs-lookup"><span data-stu-id="b9209-155">DOMinRAMAllowedToPeer</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dominramallowedtopeer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-158">DOModifyCacheDrive</span><span class="sxs-lookup"><span data-stu-id="b9209-158">DOModifyCacheDrive</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domodifycachedrive)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9209-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-161">DOMonthlyUploadDataCap</span><span class="sxs-lookup"><span data-stu-id="b9209-161">DOMonthlyUploadDataCap</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-domonthlyuploaddatacap)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b9209-164">DOPercentageMaxDownloadBandwidth</span><span class="sxs-lookup"><span data-stu-id="b9209-164">DOPercentageMaxDownloadBandwidth</span></span>](/windows/client-management/mdm/policy-csp-deliveryoptimization#deliveryoptimization-dopercentagemaxdownloadbandwidth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b9209-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b9209-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b9209-167">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b9209-167">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9209-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9209-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9209-170">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9209-170">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9209-171">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b9209-171">Identifies the name of the parent node.</span></span> <span data-ttu-id="b9209-172">Para esta clase, la cadena es "DeliveryOptimization".</span><span class="sxs-lookup"><span data-stu-id="b9209-172">For this class, the string is "DeliveryOptimization".</span></span>

</dd> <dt>

<span data-ttu-id="b9209-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b9209-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9209-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b9209-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b9209-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b9209-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9209-176">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b9209-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b9209-177">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b9209-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="b9209-178">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="b9209-178">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9209-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9209-179">Requirements</span></span>



| <span data-ttu-id="b9209-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9209-180">Requirement</span></span> | <span data-ttu-id="b9209-181">Value</span><span class="sxs-lookup"><span data-stu-id="b9209-181">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9209-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9209-182">Minimum supported client</span></span><br/> | <span data-ttu-id="b9209-183">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9209-183">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9209-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9209-184">Minimum supported server</span></span><br/> | <span data-ttu-id="b9209-185">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b9209-185">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b9209-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9209-186">Namespace</span></span><br/>                | <span data-ttu-id="b9209-187">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b9209-187">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b9209-188">MOF</span><span class="sxs-lookup"><span data-stu-id="b9209-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9209-189"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9209-189"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9209-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9209-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9209-191"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9209-191"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9209-192">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9209-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9209-193">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="b9209-193">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

