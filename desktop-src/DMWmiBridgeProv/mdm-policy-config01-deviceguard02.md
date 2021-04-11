---
title: MDM_Policy_Config01_DeviceGuard02 (clase)
description: La \_ Directiva MDM \_ Config01 \_ DeviceGuard02 configura las directivas de Device Guard.
ms.assetid: b8edf906-2486-4d8d-9410-d216bacf1728
keywords:
- MDM_Policy_Config01_DeviceGuard02 (clase)
- MDM_Policy_Config01_DeviceGuard02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceGuard02
- MDM_Policy_Config01_DeviceGuard02.InstanceID
- MDM_Policy_Config01_DeviceGuard02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebcc8f3d929708cdff3ada8fe440f49a1aeb1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078919"
---
# <a name="mdm_policy_config01_deviceguard02-class"></a><span data-ttu-id="25090-105">\_ \_ Clase DeviceGuard02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="25090-105">MDM\_Policy\_Config01\_DeviceGuard02 class</span></span>

<span data-ttu-id="25090-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="25090-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="25090-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="25090-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="25090-108">La \_ Directiva MDM \_ Config01 \_ DeviceGuard02 configura las directivas de Device Guard.</span><span class="sxs-lookup"><span data-stu-id="25090-108">The MDM\_Policy\_Config01\_DeviceGuard02 configures the Device Guard policies.</span></span>

<span data-ttu-id="25090-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="25090-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="25090-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25090-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceGuard02
{
  string InstanceID;
  string ParentID;
  sint32 EnableVirtualizationBasedSecurity;
  sint32 LsaCfgFlags;
  sint32 RequirePlatformSecurityFeatures;
};
```

## <a name="members"></a><span data-ttu-id="25090-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="25090-111">Members</span></span>

<span data-ttu-id="25090-112">La clase Config01 de la **\_ Directiva MDM \_ \_ DeviceGuard02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="25090-112">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these types of members:</span></span>

-   [<span data-ttu-id="25090-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25090-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25090-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25090-114">Properties</span></span>

<span data-ttu-id="25090-115">La **clase \_ \_ Config01 de \_ DeviceGuard02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="25090-115">The **MDM\_Policy\_Config01\_DeviceGuard02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="25090-116">EnableVirtualizationBasedSecurity</span><span class="sxs-lookup"><span data-stu-id="25090-116">EnableVirtualizationBasedSecurity</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-enablevirtualizationbasedsecurity)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25090-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="25090-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="25090-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25090-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25090-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="25090-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25090-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25090-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25090-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25090-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25090-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="25090-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25090-123">LsaCfgFlags</span><span class="sxs-lookup"><span data-stu-id="25090-123">LsaCfgFlags</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-lsacfgflags)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25090-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="25090-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="25090-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25090-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="25090-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="25090-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25090-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="25090-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="25090-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="25090-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25090-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="25090-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="25090-130">RequirePlatformSecurityFeatures</span><span class="sxs-lookup"><span data-stu-id="25090-130">RequirePlatformSecurityFeatures</span></span>](/windows/client-management/mdm/policy-csp-deviceguard#deviceguard-requireplatformsecurityfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="25090-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="25090-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="25090-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="25090-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="25090-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25090-133">Requirements</span></span>



| <span data-ttu-id="25090-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="25090-134">Requirement</span></span> | <span data-ttu-id="25090-135">Value</span><span class="sxs-lookup"><span data-stu-id="25090-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25090-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25090-136">Minimum supported client</span></span><br/> | <span data-ttu-id="25090-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="25090-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25090-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25090-138">Minimum supported server</span></span><br/> | <span data-ttu-id="25090-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="25090-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="25090-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="25090-140">Namespace</span></span><br/>                | <span data-ttu-id="25090-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="25090-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="25090-142">MOF</span><span class="sxs-lookup"><span data-stu-id="25090-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25090-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25090-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="25090-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25090-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25090-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25090-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

