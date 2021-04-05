---
title: MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 (clase)
description: La \_ \_ \_ clase EnterpriseDataProtection01 StoreApps03 de AppLocker de MDM captura la lista de aplicaciones de Windows a las que se les permite administrar datos empresariales. Debe utilizarse junto con la configuración de./Vendor/MSFT/Policy/ConfigSource/DataProtection.
ms.assetid: f37fe52d-dbe1-45b7-acd5-5047c46d9bd0
keywords:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 (clase)
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.InstanceID
- MDM_AppLocker_EnterpriseDataProtection01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240f641e542bbbe0c71fd686e2d9df3908b9bab3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997069"
---
# <a name="mdm_applocker_enterprisedataprotection01_storeapps03-class"></a><span data-ttu-id="03c87-106">MDM \_ AppLocker \_ EnterpriseDataProtection01 \_ clase StoreApps03</span><span class="sxs-lookup"><span data-stu-id="03c87-106">MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03 class</span></span>

<span data-ttu-id="03c87-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="03c87-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="03c87-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="03c87-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="03c87-109">La **clase \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de AppLocker de MDM** captura la lista de aplicaciones de Windows a las que se les permite administrar datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="03c87-109">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class captures the list of Windows apps that are allowed to handle enterprise data.</span></span> <span data-ttu-id="03c87-110">Debe utilizarse junto con la configuración de./Vendor/MSFT/Policy/ConfigSource/DataProtection.</span><span class="sxs-lookup"><span data-stu-id="03c87-110">Should be used in conjunction with the settings in ./Vendor/MSFT/Policy/ConfigSource/DataProtection .</span></span>

<span data-ttu-id="03c87-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="03c87-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c87-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03c87-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_EnterpriseDataProtection01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
};
```

## <a name="members"></a><span data-ttu-id="03c87-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="03c87-113">Members</span></span>

<span data-ttu-id="03c87-114">La **clase \_ \_ EnterpriseDataProtection01 de \_ StoreApps03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03c87-114">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="03c87-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03c87-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03c87-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03c87-116">Properties</span></span>

<span data-ttu-id="03c87-117">La **clase \_ \_ EnterpriseDataProtection01 \_ StoreApps03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03c87-117">The **MDM\_AppLocker\_EnterpriseDataProtection01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03c87-118">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03c87-118">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c87-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03c87-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03c87-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03c87-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03c87-121">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03c87-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03c87-122">Define las restricciones para ejecutar aplicaciones de la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="03c87-122">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="03c87-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="03c87-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c87-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03c87-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03c87-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03c87-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03c87-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="03c87-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="03c87-127">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="03c87-127">Describes the full path to the parent node.</span></span> <span data-ttu-id="03c87-128">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*".</span><span class="sxs-lookup"><span data-stu-id="03c87-128">For this class, the string is "./Vendor/MSFT/AppLocker/EnterpriseDataProtection/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="03c87-129">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="03c87-129">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c87-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03c87-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03c87-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03c87-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03c87-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c87-132">Requirements</span></span>



| <span data-ttu-id="03c87-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c87-133">Requirement</span></span> | <span data-ttu-id="03c87-134">Value</span><span class="sxs-lookup"><span data-stu-id="03c87-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c87-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c87-135">Minimum supported client</span></span><br/> | <span data-ttu-id="03c87-136">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="03c87-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03c87-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03c87-137">Minimum supported server</span></span><br/> | <span data-ttu-id="03c87-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="03c87-138">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="03c87-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03c87-139">Namespace</span></span><br/>                | <span data-ttu-id="03c87-140">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="03c87-140">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="03c87-141">MOF</span><span class="sxs-lookup"><span data-stu-id="03c87-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03c87-142"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03c87-142"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="03c87-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03c87-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03c87-144"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c87-144"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c87-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="03c87-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c87-146">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="03c87-146">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

