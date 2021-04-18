---
title: MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 (clase)
description: La \_ \_ \_ clase ApplicationLaunchRestrictions01 StoreApps03 de AppLocker de MDM le permite especificar qué aplicaciones exe se permiten o no para la protección de datos empresariales.
ms.assetid: de5ceaea-589a-4ed7-8dd6-eb9477d68e0e
keywords:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 (clase)
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.InstanceID
- MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54c58610c10e672a6fbc1406b2d022b8ce211871
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656523"
---
# <a name="mdm_applocker_applicationlaunchrestrictions01_storeapps03-class"></a><span data-ttu-id="fe99e-105">MDM \_ AppLocker \_ ApplicationLaunchRestrictions01 \_ clase StoreApps03</span><span class="sxs-lookup"><span data-stu-id="fe99e-105">MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03 class</span></span>

<span data-ttu-id="fe99e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fe99e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fe99e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fe99e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fe99e-108">La **clase \_ \_ ApplicationLaunchRestrictions01 \_ StoreApps03 de AppLocker de MDM** le permite especificar qué aplicaciones exe se permiten o no para la protección de datos empresariales.</span><span class="sxs-lookup"><span data-stu-id="fe99e-108">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class allows you to specify which EXE applications are allowed or disallowed for Enterprise Data Protection.</span></span>

<span data-ttu-id="fe99e-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fe99e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe99e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe99e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_ApplicationLaunchRestrictions01_StoreApps03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="fe99e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fe99e-111">Members</span></span>

<span data-ttu-id="fe99e-112">La **clase \_ \_ ApplicationLaunchRestrictions01 de \_ StoreApps03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fe99e-112">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these types of members:</span></span>

-   [<span data-ttu-id="fe99e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe99e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fe99e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe99e-114">Properties</span></span>

<span data-ttu-id="fe99e-115">La **clase \_ \_ ApplicationLaunchRestrictions01 \_ StoreApps03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fe99e-115">The **MDM\_AppLocker\_ApplicationLaunchRestrictions01\_StoreApps03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fe99e-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="fe99e-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe99e-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe99e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fe99e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fe99e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fe99e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe99e-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe99e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe99e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe99e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe99e-123">Define las restricciones para ejecutar aplicaciones de la Tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="fe99e-123">Defines restrictions for running apps from the Windows Store.</span></span>

</dd> <dt>

<span data-ttu-id="fe99e-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fe99e-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe99e-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe99e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fe99e-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fe99e-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fe99e-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="fe99e-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="fe99e-129">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*".</span><span class="sxs-lookup"><span data-stu-id="fe99e-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions/*Grouping*"</span></span>

</dd> <dt>

[<span data-ttu-id="fe99e-130">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="fe99e-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fe99e-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fe99e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fe99e-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fe99e-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fe99e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe99e-133">Requirements</span></span>



| <span data-ttu-id="fe99e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe99e-134">Requirement</span></span> | <span data-ttu-id="fe99e-135">Value</span><span class="sxs-lookup"><span data-stu-id="fe99e-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe99e-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe99e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fe99e-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe99e-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fe99e-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe99e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fe99e-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fe99e-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fe99e-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fe99e-140">Namespace</span></span><br/>                | <span data-ttu-id="fe99e-141">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="fe99e-141">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fe99e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fe99e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fe99e-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fe99e-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fe99e-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fe99e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe99e-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe99e-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe99e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe99e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe99e-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="fe99e-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

