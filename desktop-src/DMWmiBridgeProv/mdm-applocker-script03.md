---
title: MDM_AppLocker_Script03 (clase)
description: La \_ \_ clase Script03 de APPLOCKER de MDM define las restricciones de directiva para procesar archivos dll.
ms.assetid: 61fada02-7245-4825-945c-b41e9eff8e74
keywords:
- MDM_AppLocker_Script03 (clase)
- MDM_AppLocker_Script03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_AppLocker_Script03
- MDM_AppLocker_Script03.InstanceID
- MDM_AppLocker_Script03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402efedb1e15a0ea0df3dea654328de4ba0ddd86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079742"
---
# <a name="mdm_applocker_script03-class"></a><span data-ttu-id="8a975-105">\_Clase Script03 de AppLocker de MDM \_</span><span class="sxs-lookup"><span data-stu-id="8a975-105">MDM\_AppLocker\_Script03 class</span></span>

<span data-ttu-id="8a975-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="8a975-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8a975-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="8a975-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8a975-108">La **clase \_ \_ Script03 de AppLocker de MDM** define las restricciones de directiva para procesar archivos dll.</span><span class="sxs-lookup"><span data-stu-id="8a975-108">The **MDM\_AppLocker\_Script03** class defines the policy restrictions for processing DLL files.</span></span>

<span data-ttu-id="8a975-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8a975-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a975-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a975-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AppLocker_Script03
{
  string InstanceID;
  string ParentID;
  string Policy;
  string EnforcementMode;
};
```

## <a name="members"></a><span data-ttu-id="8a975-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a975-111">Members</span></span>

<span data-ttu-id="8a975-112">La **clase \_ \_ Script03 de AppLocker de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8a975-112">The **MDM\_AppLocker\_Script03** class has these types of members:</span></span>

-   [<span data-ttu-id="8a975-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a975-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a975-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a975-114">Properties</span></span>

<span data-ttu-id="8a975-115">La **clase \_ \_ Script03 de AppLocker de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8a975-115">The **MDM\_AppLocker\_Script03** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8a975-116">**EnforcementMode**</span><span class="sxs-lookup"><span data-stu-id="8a975-116">**EnforcementMode**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a975-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a975-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a975-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8a975-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a975-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a975-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a975-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a975-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a975-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a975-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a975-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a975-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8a975-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8a975-123">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="8a975-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8a975-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a975-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a975-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a975-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a975-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a975-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a975-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8a975-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="8a975-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="8a975-129">Para esta clase, la cadena es "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions".</span><span class="sxs-lookup"><span data-stu-id="8a975-129">For this class, the string is "./Vendor/MSFT/AppLocker/ApplicationLaunchRestrictions"</span></span>

</dd> <dt>

[<span data-ttu-id="8a975-130">**Directiva**</span><span class="sxs-lookup"><span data-stu-id="8a975-130">**Policy**</span></span>](/windows/client-management/mdm/applocker-csp)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a975-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a975-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a975-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8a975-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a975-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a975-133">Requirements</span></span>



| <span data-ttu-id="8a975-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a975-134">Requirement</span></span> | <span data-ttu-id="8a975-135">Value</span><span class="sxs-lookup"><span data-stu-id="8a975-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a975-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a975-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8a975-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a975-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a975-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a975-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8a975-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8a975-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8a975-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a975-140">Namespace</span></span><br/>                | <span data-ttu-id="8a975-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="8a975-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8a975-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8a975-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a975-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a975-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a975-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a975-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a975-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a975-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a975-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a975-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a975-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="8a975-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

