---
title: MDM_VPNv2_PluginProfile02 (clase)
description: La \_ clase PlugInProfile02 de VPNv2 de MDM \_ describe la información necesaria al usar un complemento de VPN basado en la tienda Windows.
ms.assetid: 522c32e5-74f9-46b2-b590-ca6ade241e97
keywords:
- MDM_VPNv2_PluginProfile02 (clase)
- MDM_VPNv2_PluginProfile02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_PluginProfile02
- MDM_VPNv2_PluginProfile02.InstanceID
- MDM_VPNv2_PluginProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 008d60b28ec1d2cec9431cc63ac4d0c406d18060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996403"
---
# <a name="mdm_vpnv2_pluginprofile02-class"></a><span data-ttu-id="debb5-105">\_Clase PluginProfile02 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="debb5-105">MDM\_VPNv2\_PluginProfile02 class</span></span>

<span data-ttu-id="debb5-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="debb5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="debb5-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="debb5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="debb5-108">La **clase \_ \_ PlugInProfile02 de VPNv2 de MDM** describe la información necesaria al usar un complemento de VPN basado en la tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="debb5-108">The **MDM\_VPNv2\_PlugInProfile02** class describes the information needed when using a Windows Store based VPN plugin.</span></span>

<span data-ttu-id="debb5-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="debb5-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="debb5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="debb5-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_PluginProfile02
{
  string InstanceID;
  string ParentID;
  string ServerUrlList;
  string CustomConfiguration;
  string PluginPackageFamilyName;
  string CustomStoreUrl;
};
```

## <a name="members"></a><span data-ttu-id="debb5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="debb5-111">Members</span></span>

<span data-ttu-id="debb5-112">La **clase \_ \_ PluginProfile02 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="debb5-112">The **MDM\_VPNv2\_PluginProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="debb5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="debb5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="debb5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="debb5-114">Properties</span></span>

<span data-ttu-id="debb5-115">La **clase \_ \_ PluginProfile02 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="debb5-115">The **MDM\_VPNv2\_PluginProfile02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="debb5-116">CustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="debb5-116">CustomConfiguration</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="debb5-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="debb5-119">CustomStoreUrl</span><span class="sxs-lookup"><span data-stu-id="debb5-119">CustomStoreUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-customstoreurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="debb5-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="debb5-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="debb5-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="debb5-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="debb5-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="debb5-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="debb5-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="debb5-126">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="debb5-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="debb5-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="debb5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="debb5-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="debb5-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="debb5-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="debb5-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="debb5-132">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="debb5-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="debb5-133">PluginPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="debb5-133">PluginPackageFamilyName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-pluginpackagefamilyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="debb5-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="debb5-136">ServerUrlList</span><span class="sxs-lookup"><span data-stu-id="debb5-136">ServerUrlList</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-pluginprofile-serverurllist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="debb5-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="debb5-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="debb5-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="debb5-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="debb5-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="debb5-139">Requirements</span></span>



| <span data-ttu-id="debb5-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="debb5-140">Requirement</span></span> | <span data-ttu-id="debb5-141">Value</span><span class="sxs-lookup"><span data-stu-id="debb5-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="debb5-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="debb5-142">Minimum supported client</span></span><br/> | <span data-ttu-id="debb5-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="debb5-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="debb5-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="debb5-144">Minimum supported server</span></span><br/> | <span data-ttu-id="debb5-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="debb5-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="debb5-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="debb5-146">Namespace</span></span><br/>                | <span data-ttu-id="debb5-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="debb5-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="debb5-148">MOF</span><span class="sxs-lookup"><span data-stu-id="debb5-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="debb5-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="debb5-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="debb5-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="debb5-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="debb5-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="debb5-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="debb5-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="debb5-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="debb5-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="debb5-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

