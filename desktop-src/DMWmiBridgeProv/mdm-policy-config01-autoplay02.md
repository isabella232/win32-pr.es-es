---
title: MDM_Policy_Config01_Autoplay02 (clase)
description: La \_ clase Config01 de Autoplay02 de directivas MDM \_ \_ configura las directivas de reproducción automática disponibles.
ms.assetid: ef7ccdb6-3f77-4c43-87d9-56acda97be21
keywords:
- MDM_Policy_Config01_Autoplay02 (clase)
- MDM_Policy_Config01_Autoplay02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Autoplay02
- MDM_Policy_Config01_Autoplay02.InstanceID
- MDM_Policy_Config01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e064d0b0eed457bcafdf4da9bf8e72fbb4916e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079182"
---
# <a name="mdm_policy_config01_autoplay02-class"></a><span data-ttu-id="8c49d-105">\_ \_ Clase Autoplay02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="8c49d-105">MDM\_Policy\_Config01\_Autoplay02 class</span></span>

<span data-ttu-id="8c49d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="8c49d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8c49d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="8c49d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8c49d-108">La \_ clase Config01 de Autoplay02 de directivas MDM \_ \_ configura las directivas de reproducción automática disponibles.</span><span class="sxs-lookup"><span data-stu-id="8c49d-108">The MDM\_Policy\_Config01\_Autoplay02 class configures the available autoplay policies.</span></span>

<span data-ttu-id="8c49d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8c49d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c49d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c49d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="8c49d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="8c49d-111">Members</span></span>

<span data-ttu-id="8c49d-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Autoplay02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8c49d-112">The **MDM\_Policy\_Config01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="8c49d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c49d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8c49d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c49d-114">Properties</span></span>

<span data-ttu-id="8c49d-115">La **clase \_ \_ Config01 de \_ Autoplay02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8c49d-115">The **MDM\_Policy\_Config01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="8c49d-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="8c49d-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c49d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c49d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8c49d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c49d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8c49d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c49d-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c49d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c49d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c49d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8c49d-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8c49d-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c49d-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c49d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8c49d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8c49d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c49d-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="8c49d-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c49d-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c49d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8c49d-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8c49d-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="8c49d-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8c49d-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8c49d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8c49d-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8c49d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c49d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c49d-133">Requirements</span></span>



| <span data-ttu-id="8c49d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c49d-134">Requirement</span></span> | <span data-ttu-id="8c49d-135">Value</span><span class="sxs-lookup"><span data-stu-id="8c49d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c49d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c49d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8c49d-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="8c49d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8c49d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8c49d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8c49d-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8c49d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8c49d-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8c49d-140">Namespace</span></span><br/>                | <span data-ttu-id="8c49d-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="8c49d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="8c49d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8c49d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c49d-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8c49d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c49d-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8c49d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c49d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c49d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

