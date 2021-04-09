---
title: MDM_Policy_Result01_ApplicationDefaults02 (clase)
description: La \_ clase Result01 de ApplicationDefaults02 de directivas MDM \_ \_ representa las directivas de valores predeterminados de aplicación disponibles.
ms.assetid: bf7df9a1-7af1-49a6-9456-3e6ec48234e2
keywords:
- MDM_Policy_Result01_ApplicationDefaults02 (clase)
- MDM_Policy_Result01_ApplicationDefaults02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_ApplicationDefaults02
- MDM_Policy_Result01_ApplicationDefaults02.InstanceID
- MDM_Policy_Result01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10592ceb4e4f401ce9f64c24ef207a4e2e033e9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150354"
---
# <a name="mdm_policy_result01_applicationdefaults02-class"></a><span data-ttu-id="2a3c4-105">\_ \_ Clase ApplicationDefaults02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="2a3c4-105">MDM\_Policy\_Result01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="2a3c4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2a3c4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2a3c4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2a3c4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2a3c4-108">La \_ clase Result01 de ApplicationDefaults02 de directivas MDM \_ \_ representa las directivas de valores predeterminados de aplicación disponibles.</span><span class="sxs-lookup"><span data-stu-id="2a3c4-108">The MDM\_Policy\_Result01\_ApplicationDefaults02 class represents the available application defaults policies.</span></span>

<span data-ttu-id="2a3c4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2a3c4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3c4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a3c4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="2a3c4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2a3c4-111">Members</span></span>

<span data-ttu-id="2a3c4-112">La clase Result01 de la **\_ Directiva MDM \_ \_ ApplicationDefaults02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2a3c4-112">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="2a3c4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a3c4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2a3c4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a3c4-114">Properties</span></span>

<span data-ttu-id="2a3c4-115">La **clase \_ \_ Result01 de \_ ApplicationDefaults02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2a3c4-115">The **MDM\_Policy\_Result01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2a3c4-116">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="2a3c4-116">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a3c4-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2a3c4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a3c4-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2a3c4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a3c4-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2a3c4-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a3c4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2a3c4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a3c4-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a3c4-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a3c4-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a3c4-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2a3c4-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2a3c4-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2a3c4-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2a3c4-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2a3c4-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2a3c4-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2a3c4-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2a3c4-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a3c4-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3c4-127">Requirements</span></span>



| <span data-ttu-id="2a3c4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3c4-128">Requirement</span></span> | <span data-ttu-id="2a3c4-129">Value</span><span class="sxs-lookup"><span data-stu-id="2a3c4-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3c4-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a3c4-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3c4-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a3c4-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a3c4-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a3c4-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3c4-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2a3c4-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2a3c4-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2a3c4-134">Namespace</span></span><br/>                | <span data-ttu-id="2a3c4-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2a3c4-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2a3c4-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2a3c4-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a3c4-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c4-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a3c4-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2a3c4-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a3c4-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c4-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

