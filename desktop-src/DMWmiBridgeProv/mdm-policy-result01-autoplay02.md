---
title: MDM_Policy_Result01_Autoplay02 (clase)
description: La \_ clase Result01 de Autoplay02 de directivas MDM \_ \_ representa las directivas de reproducción automática disponibles.
ms.assetid: f116015d-f10e-4d17-9c0b-7253894e6c0f
keywords:
- MDM_Policy_Result01_Autoplay02 (clase)
- MDM_Policy_Result01_Autoplay02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Autoplay02
- MDM_Policy_Result01_Autoplay02.InstanceID
- MDM_Policy_Result01_Autoplay02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9abf48754cff1513d6d373c9addb34b8ec9acc26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151102"
---
# <a name="mdm_policy_result01_autoplay02-class"></a><span data-ttu-id="3aac6-105">\_ \_ Clase Autoplay02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="3aac6-105">MDM\_Policy\_Result01\_Autoplay02 class</span></span>

<span data-ttu-id="3aac6-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3aac6-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3aac6-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3aac6-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3aac6-108">La \_ clase Result01 de Autoplay02 de directivas MDM \_ \_ representa las directivas de reproducción automática disponibles.</span><span class="sxs-lookup"><span data-stu-id="3aac6-108">The MDM\_Policy\_Result01\_Autoplay02 class represents the available autoplay policies.</span></span>

<span data-ttu-id="3aac6-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3aac6-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aac6-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3aac6-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Autoplay02
{
  string InstanceID;
  string ParentID;
  string DisallowAutoplayForNonVolumeDevices;
  string SetDefaultAutoRunBehavior;
  string TurnOffAutoPlay;
};
```

## <a name="members"></a><span data-ttu-id="3aac6-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3aac6-111">Members</span></span>

<span data-ttu-id="3aac6-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Autoplay02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3aac6-112">The **MDM\_Policy\_Result01\_Autoplay02** class has these types of members:</span></span>

-   [<span data-ttu-id="3aac6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3aac6-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3aac6-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3aac6-114">Properties</span></span>

<span data-ttu-id="3aac6-115">La **clase \_ \_ Result01 de \_ Autoplay02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3aac6-115">The **MDM\_Policy\_Result01\_Autoplay02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3aac6-116">DisallowAutoplayForNonVolumeDevices</span><span class="sxs-lookup"><span data-stu-id="3aac6-116">DisallowAutoplayForNonVolumeDevices</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-disallowautoplayfornonvolumedevices)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aac6-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3aac6-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3aac6-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3aac6-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3aac6-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aac6-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3aac6-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3aac6-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3aac6-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3aac6-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3aac6-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aac6-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3aac6-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3aac6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3aac6-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3aac6-127">SetDefaultAutoRunBehavior</span><span class="sxs-lookup"><span data-stu-id="3aac6-127">SetDefaultAutoRunBehavior</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-setdefaultautorunbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aac6-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3aac6-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3aac6-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3aac6-130">TurnOffAutoPlay</span><span class="sxs-lookup"><span data-stu-id="3aac6-130">TurnOffAutoPlay</span></span>](/windows/client-management/mdm/policy-csp-autoplay#autoplay-turnoffautoplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3aac6-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3aac6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3aac6-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3aac6-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3aac6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3aac6-133">Requirements</span></span>



| <span data-ttu-id="3aac6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3aac6-134">Requirement</span></span> | <span data-ttu-id="3aac6-135">Value</span><span class="sxs-lookup"><span data-stu-id="3aac6-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aac6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aac6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3aac6-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3aac6-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3aac6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3aac6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3aac6-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3aac6-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3aac6-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3aac6-140">Namespace</span></span><br/>                | <span data-ttu-id="3aac6-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="3aac6-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3aac6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="3aac6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3aac6-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3aac6-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3aac6-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3aac6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aac6-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aac6-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

