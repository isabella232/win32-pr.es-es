---
title: MDM_Policy_Config01_ApplicationDefaults02 (clase)
description: La \_ clase Config01 de ApplicationDefaults02 de directivas MDM \_ \_ permite a un administrador establecer asociaciones de protocolo y tipo de archivo predeterminadas. Cuando se establece, las asociaciones predeterminadas se aplicarán al inicio de sesión en el equipo.
ms.assetid: 01a45151-bce3-47a7-bffe-1a3f5a1348ff
keywords:
- MDM_Policy_Config01_ApplicationDefaults02 (clase)
- MDM_Policy_Config01_ApplicationDefaults02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationDefaults02
- MDM_Policy_Config01_ApplicationDefaults02.InstanceID
- MDM_Policy_Config01_ApplicationDefaults02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 246278b1e4185337ebb63d9d23f74e2ff8753615
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489928"
---
# <a name="mdm_policy_config01_applicationdefaults02-class"></a><span data-ttu-id="2bb65-106">\_ \_ Clase ApplicationDefaults02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="2bb65-106">MDM\_Policy\_Config01\_ApplicationDefaults02 class</span></span>

<span data-ttu-id="2bb65-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2bb65-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2bb65-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2bb65-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2bb65-109">La \_ clase Config01 de ApplicationDefaults02 de directivas MDM \_ \_ permite a un administrador establecer asociaciones de protocolo y tipo de archivo predeterminadas.</span><span class="sxs-lookup"><span data-stu-id="2bb65-109">The MDM\_Policy\_Config01\_ApplicationDefaults02 class allows an administrator to set default file type and protocol associations.</span></span> <span data-ttu-id="2bb65-110">Cuando se establece, las asociaciones predeterminadas se aplicarán al inicio de sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="2bb65-110">When set, default associations will be applied on sign-in to the PC.</span></span>

<span data-ttu-id="2bb65-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2bb65-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bb65-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2bb65-112">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationDefaults02
{
  string InstanceID;
  string ParentID;
  string DefaultAssociationsConfiguration;
};
```

## <a name="members"></a><span data-ttu-id="2bb65-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="2bb65-113">Members</span></span>

<span data-ttu-id="2bb65-114">La clase Config01 de la **\_ Directiva MDM \_ \_ ApplicationDefaults02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2bb65-114">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these types of members:</span></span>

-   [<span data-ttu-id="2bb65-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2bb65-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2bb65-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2bb65-116">Properties</span></span>

<span data-ttu-id="2bb65-117">La **clase \_ \_ Config01 de \_ ApplicationDefaults02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2bb65-117">The **MDM\_Policy\_Config01\_ApplicationDefaults02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2bb65-118">DefaultAssociationsConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bb65-118">DefaultAssociationsConfiguration</span></span>](/windows/client-management/mdm/policy-csp-applicationdefaults#applicationdefaults-defaultassociationsconfiguration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb65-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2bb65-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb65-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2bb65-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb65-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2bb65-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb65-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2bb65-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb65-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2bb65-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb65-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bb65-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2bb65-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2bb65-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2bb65-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2bb65-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2bb65-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2bb65-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2bb65-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2bb65-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2bb65-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bb65-129">Requirements</span></span>



| <span data-ttu-id="2bb65-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bb65-130">Requirement</span></span> | <span data-ttu-id="2bb65-131">Value</span><span class="sxs-lookup"><span data-stu-id="2bb65-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bb65-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb65-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2bb65-133">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bb65-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2bb65-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bb65-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2bb65-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2bb65-135">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2bb65-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2bb65-136">Namespace</span></span><br/>                | <span data-ttu-id="2bb65-137">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2bb65-137">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2bb65-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2bb65-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2bb65-139"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2bb65-139"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2bb65-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2bb65-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bb65-141"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bb65-141"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

