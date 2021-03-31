---
title: MDM_Policy_Config01_Connectivity02 (clase)
description: La \_ clase Config01 de Connectivity02 de directivas MDM \_ \_ representa las directivas de conexión disponibles.
ms.assetid: 670e48c2-1af1-45e9-81c6-cdf3a310240f
keywords:
- MDM_Policy_Config01_Connectivity02 (clase)
- MDM_Policy_Config01_Connectivity02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Connectivity02
- MDM_Policy_Config01_Connectivity02.InstanceID
- MDM_Policy_Config01_Connectivity02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b39b897998bf47c5f5411456ccae7fcb6927aef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801874"
---
# <a name="mdm_policy_config01_connectivity02-class"></a><span data-ttu-id="bceca-105">\_ \_ Clase Connectivity02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="bceca-105">MDM\_Policy\_Config01\_Connectivity02 class</span></span>

<span data-ttu-id="bceca-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="bceca-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bceca-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="bceca-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bceca-108">La **clase \_ \_ Config01 de \_ Connectivity02 de directivas MDM** representa las directivas de conexión disponibles.</span><span class="sxs-lookup"><span data-stu-id="bceca-108">The **MDM\_Policy\_Config01\_Connectivity02** class represents the connection policies available.</span></span>

<span data-ttu-id="bceca-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bceca-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bceca-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bceca-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Connectivity02
{
  string InstanceID;
  string ParentID;
  sint32 AllowBluetooth;
  sint32 AllowCellularData;
  sint32 AllowCellularDataRoaming;
  sint32 AllowVPNOverCellular;
  sint32 AllowVPNRoamingOverCellular;
  string DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards;
  string DisableDownloadingOfPrintDriversOverHTTP;
  string DiablePrintingOverHTTP;
  string HardenedUNCPaths;
  string ProhibitInstallationAndConfigurationOfNetworkBridge;
  sint32 DisallowNetworkConnectivityActiveTests;
  sint32 AllowConnectedDevices;
};
```

## <a name="members"></a><span data-ttu-id="bceca-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="bceca-111">Members</span></span>

<span data-ttu-id="bceca-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Connectivity02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bceca-112">The **MDM\_Policy\_Config01\_Connectivity02** class has these types of members:</span></span>

-   [<span data-ttu-id="bceca-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bceca-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bceca-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bceca-114">Properties</span></span>

<span data-ttu-id="bceca-115">La **clase \_ \_ Config01 de \_ Connectivity02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bceca-115">The **MDM\_Policy\_Config01\_Connectivity02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="bceca-116">AllowBluetooth</span><span class="sxs-lookup"><span data-stu-id="bceca-116">AllowBluetooth</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowbluetooth)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-119">AllowCellularData</span><span class="sxs-lookup"><span data-stu-id="bceca-119">AllowCellularData</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-122">AllowCellularDataRoaming</span><span class="sxs-lookup"><span data-stu-id="bceca-122">AllowCellularDataRoaming</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowcellulardataroaming)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-125">AllowConnectedDevices</span><span class="sxs-lookup"><span data-stu-id="bceca-125">AllowConnectedDevices</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowconnecteddevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-128">AllowVPNOverCellular</span><span class="sxs-lookup"><span data-stu-id="bceca-128">AllowVPNOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-131">AllowVPNRoamingOverCellular</span><span class="sxs-lookup"><span data-stu-id="bceca-131">AllowVPNRoamingOverCellular</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-allowvpnroamingovercellular)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-134">DiablePrintingOverHTTP</span><span class="sxs-lookup"><span data-stu-id="bceca-134">DiablePrintingOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-diableprintingoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-137">DisableDownloadingOfPrintDriversOverHTTP</span><span class="sxs-lookup"><span data-stu-id="bceca-137">DisableDownloadingOfPrintDriversOverHTTP</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disabledownloadingofprintdriversoverhttp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span><span class="sxs-lookup"><span data-stu-id="bceca-140">DisableInternetDownloadForWebPublishingAndOnlineOrderingWizards</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disableinternetdownloadforwebpublishingandonlineorderingwizards)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-143">DisallowNetworkConnectivityActiveTests</span><span class="sxs-lookup"><span data-stu-id="bceca-143">DisallowNetworkConnectivityActiveTests</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-disallownetworkconnectivityactivetests)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bceca-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bceca-146">HardenedUNCPaths</span><span class="sxs-lookup"><span data-stu-id="bceca-146">HardenedUNCPaths</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-hardeneduncpaths)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bceca-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bceca-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bceca-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bceca-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bceca-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bceca-153">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="bceca-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="bceca-154">Para esta clase, la cadena es "Connectivity".</span><span class="sxs-lookup"><span data-stu-id="bceca-154">For this class, the string is "Connectivity".</span></span>

</dd> <dt>

<span data-ttu-id="bceca-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bceca-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bceca-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bceca-158">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bceca-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bceca-159">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="bceca-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="bceca-160">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="bceca-160">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="bceca-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span><span class="sxs-lookup"><span data-stu-id="bceca-161">ProhibitInstallationAndConfigurationOfNetworkBridge</span></span>](/windows/client-management/mdm/policy-csp-connectivity#connectivity-prohibitinstallationandconfigurationofnetworkbridge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bceca-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bceca-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bceca-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bceca-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bceca-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bceca-164">Requirements</span></span>



| <span data-ttu-id="bceca-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="bceca-165">Requirement</span></span> | <span data-ttu-id="bceca-166">Value</span><span class="sxs-lookup"><span data-stu-id="bceca-166">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bceca-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bceca-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bceca-168">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="bceca-168">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bceca-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bceca-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bceca-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bceca-170">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bceca-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bceca-171">Namespace</span></span><br/>                | <span data-ttu-id="bceca-172">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="bceca-172">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="bceca-173">MOF</span><span class="sxs-lookup"><span data-stu-id="bceca-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bceca-174"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bceca-174"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bceca-175">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bceca-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bceca-176"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bceca-176"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bceca-177">Vea también</span><span class="sxs-lookup"><span data-stu-id="bceca-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bceca-178">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="bceca-178">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

