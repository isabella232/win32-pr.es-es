---
title: MDM_Policy_Result01_ActiveXControls02 (clase)
description: La \_ clase Result01 de ActiveXControls02 de directivas MDM \_ \_ representa las directivas de controles ActiveX disponibles.
ms.assetid: 46778743-59d7-4d37-836c-3f263bb8a083
keywords:
- MDM_Policy_Result01_ActiveXControls02 (clase)
- MDM_Policy_Result01_ActiveXControls02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ActiveXControls02
- MDM_Policy_Result01_ActiveXControls02.InstanceID
- MDM_Policy_Result01_ActiveXControls02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36ee572cfbbd823ce9e819688d9399b22f5d564c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079422"
---
# <a name="mdm_policy_result01_activexcontrols02-class"></a><span data-ttu-id="b1e92-105">\_ \_ Clase ActiveXControls02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="b1e92-105">MDM\_Policy\_Result01\_ActiveXControls02 class</span></span>

<span data-ttu-id="b1e92-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b1e92-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b1e92-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b1e92-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b1e92-108">La \_ clase Result01 de ActiveXControls02 de directivas MDM \_ \_ representa las directivas de controles ActiveX disponibles.</span><span class="sxs-lookup"><span data-stu-id="b1e92-108">The MDM\_Policy\_Result01\_ActiveXControls02 class represents the available ActiveX Controls policies.</span></span>

<span data-ttu-id="b1e92-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b1e92-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1e92-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1e92-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ActiveXControls02
{
  string InstanceID;
  string ParentID;
  string ApprovedInstallationSites;
};
```

## <a name="members"></a><span data-ttu-id="b1e92-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b1e92-111">Members</span></span>

<span data-ttu-id="b1e92-112">La clase Result01 de la **\_ Directiva MDM \_ \_ ActiveXControls02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b1e92-112">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these types of members:</span></span>

-   [<span data-ttu-id="b1e92-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1e92-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1e92-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b1e92-114">Properties</span></span>

<span data-ttu-id="b1e92-115">La **clase \_ \_ Result01 de \_ ActiveXControls02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b1e92-115">The **MDM\_Policy\_Result01\_ActiveXControls02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b1e92-116">ApprovedInstallationSites</span><span class="sxs-lookup"><span data-stu-id="b1e92-116">ApprovedInstallationSites</span></span>](/windows/client-management/mdm/policy-csp-activexcontrols#activexcontrols-approvedinstallationsites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e92-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1e92-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1e92-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b1e92-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1e92-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b1e92-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e92-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1e92-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1e92-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1e92-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e92-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1e92-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b1e92-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b1e92-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1e92-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b1e92-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1e92-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b1e92-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1e92-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b1e92-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1e92-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1e92-127">Requirements</span></span>



| <span data-ttu-id="b1e92-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1e92-128">Requirement</span></span> | <span data-ttu-id="b1e92-129">Value</span><span class="sxs-lookup"><span data-stu-id="b1e92-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1e92-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e92-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b1e92-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b1e92-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1e92-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1e92-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b1e92-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b1e92-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b1e92-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b1e92-134">Namespace</span></span><br/>                | <span data-ttu-id="b1e92-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b1e92-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b1e92-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b1e92-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1e92-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1e92-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1e92-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1e92-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1e92-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1e92-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

