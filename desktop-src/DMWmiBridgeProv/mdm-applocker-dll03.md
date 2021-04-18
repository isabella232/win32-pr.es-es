---
title: MDM_AppLocker_DLL03 (clase)
description: La \_ \_ clase DLL03 de APPLOCKER de MDM define las restricciones de directiva para procesar archivos dll.
ms.assetid: 956b2ec0-f8a8-41d1-a571-01e73c4cebf9
keywords:
- MDM_AppLocker_DLL03 (clase)
- MDM_AppLocker_DLL03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_DLL03
- MDM_AppLocker_DLL03.InstanceID
- MDM_AppLocker_DLL03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c332a7d606b21ed9641c3c25f10a011cf7bea6e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658381"
---
# <a name="mdm_applocker_dll03-class"></a><span data-ttu-id="e1939-105">\_Clase DLL03 de AppLocker de MDM \_</span><span class="sxs-lookup"><span data-stu-id="e1939-105">MDM\_AppLocker\_DLL03 class</span></span>

<span data-ttu-id="e1939-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e1939-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e1939-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e1939-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e1939-108">La **clase \_ \_ DLL03 de AppLocker de MDM** define las restricciones de directiva para procesar archivos dll.</span><span class="sxs-lookup"><span data-stu-id="e1939-108">The **MDM\_AppLocker\_DLL03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="e1939-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e1939-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1939-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1939-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_DLL03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
  string NonInteractiveProcessEnforcement;
};
```

## <a name="members"></a><span data-ttu-id="e1939-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e1939-111">Members</span></span>

<span data-ttu-id="e1939-112">La **clase \_ \_ DLL03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e1939-112">The **MDM\_AppLocker\_DLL03** class has these types of members:</span></span>

-   [<span data-ttu-id="e1939-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1939-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1939-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e1939-114">Properties</span></span>

<span data-ttu-id="e1939-115">La **clase \_ \_ DLL03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e1939-115">The **MDM\_AppLocker\_DLL03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e1939-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="e1939-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1939-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1939-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1939-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1939-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1939-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e1939-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1939-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1939-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1939-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1939-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1939-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1939-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e1939-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e1939-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="e1939-124">**NonInteractiveProcessEnforcement**</span><span class="sxs-lookup"><span data-stu-id="e1939-124">**NonInteractiveProcessEnforcement**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1939-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1939-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1939-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1939-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e1939-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e1939-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1939-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1939-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1939-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e1939-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1939-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e1939-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e1939-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e1939-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="e1939-132">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="e1939-132">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="e1939-133">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="e1939-133">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1939-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e1939-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e1939-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e1939-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e1939-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1939-136">Requirements</span></span>



| <span data-ttu-id="e1939-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1939-137">Requirement</span></span> | <span data-ttu-id="e1939-138">Value</span><span class="sxs-lookup"><span data-stu-id="e1939-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1939-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1939-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e1939-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e1939-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e1939-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1939-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e1939-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e1939-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e1939-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e1939-143">Namespace</span></span><br/>                | <span data-ttu-id="e1939-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e1939-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e1939-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e1939-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1939-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1939-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1939-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1939-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1939-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1939-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1939-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1939-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1939-150">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="e1939-150">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

