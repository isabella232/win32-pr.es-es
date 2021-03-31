---
title: MDM_Policy_Result01_WiFi02 (clase)
description: La \_ clase Result01 de WiFi02 de directivas MDM \_ \_ representa las directivas de Wi-Fi disponibles.
ms.assetid: 074C4428-401D-4564-B7AC-45C2221EEC3A
keywords:
- MDM_Policy_Result01_WiFi02 (clase)
- MDM_Policy_Result01_WiFi02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WiFi02
- MDM_Policy_Result01_WiFi02.InstanceID
- MDM_Policy_Result01_WiFi02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff9e0349f7a18da3320fab333d5b5fd36715999
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995965"
---
# <a name="mdm_policy_result01_wifi02-class"></a><span data-ttu-id="24aaa-105">\_ \_ Clase WiFi02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="24aaa-105">MDM\_Policy\_Result01\_WiFi02 class</span></span>

<span data-ttu-id="24aaa-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="24aaa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="24aaa-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="24aaa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="24aaa-108">La **clase \_ \_ Result01 de \_ WiFi02 de directivas MDM** representa las directivas de Wi-Fi disponibles.</span><span class="sxs-lookup"><span data-stu-id="24aaa-108">The **MDM\_Policy\_Result01\_WiFi02** class represents the Wi-Fi policies available.</span></span> <span data-ttu-id="24aaa-109">Estas directivas determinan Wi-Fi configuraciones permitidas.</span><span class="sxs-lookup"><span data-stu-id="24aaa-109">These policies determine Wi-Fi configurations that are allowed.</span></span>

<span data-ttu-id="24aaa-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="24aaa-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="24aaa-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24aaa-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WiFi02
{
  string InstanceID;
  string ParentID;
  sint32 AllowInternetSharing;
  sint32 AllowWiFi;
  sint32 AllowWiFiDirect;
  sint32 AllowManualWiFiConfiguration;
  sint32 AllowAutoConnectToWiFiSenseHotspots;
  sint32 WLANScanMode;
};
```

## <a name="members"></a><span data-ttu-id="24aaa-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="24aaa-112">Members</span></span>

<span data-ttu-id="24aaa-113">La clase Result01 de la **\_ Directiva MDM \_ \_ WiFi02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="24aaa-113">The **MDM\_Policy\_Result01\_WiFi02** class has these types of members:</span></span>

-   [<span data-ttu-id="24aaa-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24aaa-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="24aaa-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24aaa-115">Properties</span></span>

<span data-ttu-id="24aaa-116">La **clase \_ \_ Result01 de \_ WiFi02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="24aaa-116">The **MDM\_Policy\_Result01\_WiFi02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="24aaa-117">AllowAutoConnectToWiFiSenseHotspots</span><span class="sxs-lookup"><span data-stu-id="24aaa-117">AllowAutoConnectToWiFiSenseHotspots</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowautoconnecttowifisensehotspots)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="24aaa-120">AllowInternetSharing</span><span class="sxs-lookup"><span data-stu-id="24aaa-120">AllowInternetSharing</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowinternetsharing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="24aaa-123">AllowManualWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="24aaa-123">AllowManualWiFiConfiguration</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowmanualwificonfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="24aaa-126">AllowWiFi</span><span class="sxs-lookup"><span data-stu-id="24aaa-126">AllowWiFi</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifi)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-127">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="24aaa-129">AllowWiFiDirect</span><span class="sxs-lookup"><span data-stu-id="24aaa-129">AllowWiFiDirect</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-allowwifidirect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="24aaa-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="24aaa-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="24aaa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="24aaa-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24aaa-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24aaa-136">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="24aaa-136">Identifies the name of the parent node.</span></span> <span data-ttu-id="24aaa-137">Para esta clase, la cadena es "WiFi".</span><span class="sxs-lookup"><span data-stu-id="24aaa-137">For this class, the string is "WiFi".</span></span>

</dd> <dt>

<span data-ttu-id="24aaa-138">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="24aaa-138">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="24aaa-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="24aaa-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-141">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="24aaa-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="24aaa-142">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="24aaa-142">Describes the full path to the parent node.</span></span> <span data-ttu-id="24aaa-143">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="24aaa-143">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="24aaa-144">WLANScanMode</span><span class="sxs-lookup"><span data-stu-id="24aaa-144">WLANScanMode</span></span>](/windows/client-management/mdm/policy-csp-wifi#wifi-wlanscanmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="24aaa-145">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="24aaa-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="24aaa-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="24aaa-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="24aaa-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24aaa-147">Requirements</span></span>



| <span data-ttu-id="24aaa-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="24aaa-148">Requirement</span></span> | <span data-ttu-id="24aaa-149">Value</span><span class="sxs-lookup"><span data-stu-id="24aaa-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24aaa-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24aaa-150">Minimum supported client</span></span><br/> | <span data-ttu-id="24aaa-151">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="24aaa-151">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="24aaa-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24aaa-152">Minimum supported server</span></span><br/> | <span data-ttu-id="24aaa-153">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="24aaa-153">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="24aaa-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24aaa-154">Namespace</span></span><br/>                | <span data-ttu-id="24aaa-155">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="24aaa-155">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="24aaa-156">MOF</span><span class="sxs-lookup"><span data-stu-id="24aaa-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24aaa-157"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="24aaa-157"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="24aaa-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24aaa-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24aaa-159"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24aaa-159"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24aaa-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="24aaa-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24aaa-161">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="24aaa-161">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

