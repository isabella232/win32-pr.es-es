---
title: MDM_Policy_Config01_DataProtection02 (clase)
description: La \_ clase MDM Policy \_ Config01 \_ DataProtection02 representa las directivas de protección de datos disponibles.
ms.assetid: 54750bae-ee5d-4db9-896f-28d9550c4d5d
keywords:
- MDM_Policy_Config01_DataProtection02 (clase)
- MDM_Policy_Config01_DataProtection02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DataProtection02
- MDM_Policy_Config01_DataProtection02.InstanceID
- MDM_Policy_Config01_DataProtection02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692dfd675c07ddc7eebbfcd75e09cb521126c746
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996959"
---
# <a name="mdm_policy_config01_dataprotection02-class"></a><span data-ttu-id="6ec67-105">\_ \_ Clase DataProtection02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="6ec67-105">MDM\_Policy\_Config01\_DataProtection02 class</span></span>

<span data-ttu-id="6ec67-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6ec67-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6ec67-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6ec67-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6ec67-108">La clase **MDM \_ Policy \_ Config01 \_ DataProtection02** representa las directivas de protección de datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="6ec67-108">The **MDM\_Policy\_Config01\_DataProtection02** class represents the data protection policies available.</span></span>

<span data-ttu-id="6ec67-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6ec67-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ec67-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ec67-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DataProtection02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDirectMemoryAccess;
  string LegacySelectiveWipeID;
};
```

## <a name="members"></a><span data-ttu-id="6ec67-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ec67-111">Members</span></span>

<span data-ttu-id="6ec67-112">La clase Config01 de la **\_ Directiva MDM \_ \_ DataProtection02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ec67-112">The **MDM\_Policy\_Config01\_DataProtection02** class has these types of members:</span></span>

-   [<span data-ttu-id="6ec67-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ec67-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ec67-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ec67-114">Properties</span></span>

<span data-ttu-id="6ec67-115">La **clase \_ \_ Config01 de \_ DataProtection02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ec67-115">The **MDM\_Policy\_Config01\_DataProtection02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6ec67-116">AllowDirectMemoryAccess</span><span class="sxs-lookup"><span data-stu-id="6ec67-116">AllowDirectMemoryAccess</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-allowdirectmemoryaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec67-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6ec67-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ec67-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ec67-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6ec67-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec67-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ec67-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ec67-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ec67-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ec67-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6ec67-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="6ec67-124">Para esta clase, la cadena es "desproteccion".</span><span class="sxs-lookup"><span data-stu-id="6ec67-124">For this class, the string is "DataProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="6ec67-125">LegacySelectiveWipeID</span><span class="sxs-lookup"><span data-stu-id="6ec67-125">LegacySelectiveWipeID</span></span>](/windows/client-management/mdm/policy-csp-dataprotection#dataprotection-legacyselectivewipeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec67-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ec67-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ec67-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ec67-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6ec67-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ec67-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ec67-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ec67-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ec67-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ec67-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6ec67-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6ec67-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="6ec67-133">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="6ec67-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ec67-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ec67-134">Requirements</span></span>



| <span data-ttu-id="6ec67-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ec67-135">Requirement</span></span> | <span data-ttu-id="6ec67-136">Value</span><span class="sxs-lookup"><span data-stu-id="6ec67-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ec67-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec67-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6ec67-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ec67-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ec67-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ec67-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6ec67-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ec67-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6ec67-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ec67-141">Namespace</span></span><br/>                | <span data-ttu-id="6ec67-142">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="6ec67-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="6ec67-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6ec67-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ec67-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ec67-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ec67-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ec67-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ec67-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ec67-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ec67-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ec67-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ec67-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="6ec67-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

