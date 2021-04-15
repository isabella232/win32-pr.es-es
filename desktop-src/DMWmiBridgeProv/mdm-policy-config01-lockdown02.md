---
title: MDM_Policy_Config01_LockDown02 (clase)
description: La \_ clase Config01 de Lockdown02 de directivas MDM \_ \_ representa las directivas de bloqueo disponibles.
ms.assetid: 1d744400-70db-4f6b-97d0-7799fdfda44f
keywords:
- MDM_Policy_Config01_LockDown02 (clase)
- MDM_Policy_Config01_LockDown02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_LockDown02
- MDM_Policy_Config01_LockDown02.InstanceID
- MDM_Policy_Config01_LockDown02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf9914573c1a3f693d88da8b35b2d577e1f21f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490505"
---
# <a name="mdm_policy_config01_lockdown02-class"></a><span data-ttu-id="a5218-105">\_ \_ Clase LockDown02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="a5218-105">MDM\_Policy\_Config01\_LockDown02 class</span></span>

<span data-ttu-id="a5218-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a5218-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a5218-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a5218-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a5218-108">La **clase \_ \_ Config01 de \_ Lockdown02 de directivas MDM** representa las directivas de bloqueo disponibles.</span><span class="sxs-lookup"><span data-stu-id="a5218-108">The **MDM\_Policy\_Config01\_Lockdown02** class represents the lockdown policies available.</span></span>

<span data-ttu-id="a5218-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a5218-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5218-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5218-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_LockDown02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEdgeSwipe;
};
```

## <a name="members"></a><span data-ttu-id="a5218-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a5218-111">Members</span></span>

<span data-ttu-id="a5218-112">La clase Config01 de la **\_ Directiva MDM \_ \_ LockDown02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a5218-112">The **MDM\_Policy\_Config01\_LockDown02** class has these types of members:</span></span>

-   [<span data-ttu-id="a5218-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a5218-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a5218-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a5218-114">Properties</span></span>

<span data-ttu-id="a5218-115">La **clase \_ \_ Config01 de \_ LockDown02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a5218-115">The **MDM\_Policy\_Config01\_LockDown02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a5218-116">AllowEdgeSwipe</span><span class="sxs-lookup"><span data-stu-id="a5218-116">AllowEdgeSwipe</span></span>](/windows/client-management/mdm/policy-csp-lockdown#lockdown-allowedgeswipe)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5218-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a5218-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a5218-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a5218-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a5218-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a5218-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5218-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a5218-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5218-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a5218-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5218-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5218-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a5218-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a5218-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="a5218-124">Para esta clase, la cadena es "bloqueo".</span><span class="sxs-lookup"><span data-stu-id="a5218-124">For this class, the string is "Lockdown".</span></span>

</dd> <dt>

<span data-ttu-id="a5218-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a5218-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a5218-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a5218-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a5218-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a5218-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a5218-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a5218-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a5218-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a5218-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="a5218-130">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="a5218-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5218-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5218-131">Requirements</span></span>



| <span data-ttu-id="a5218-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5218-132">Requirement</span></span> | <span data-ttu-id="a5218-133">Value</span><span class="sxs-lookup"><span data-stu-id="a5218-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5218-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5218-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a5218-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5218-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a5218-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5218-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a5218-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a5218-137">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="a5218-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a5218-138">Namespace</span></span><br/>                | <span data-ttu-id="a5218-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a5218-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="a5218-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a5218-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5218-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a5218-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="a5218-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a5218-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5218-143"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="a5218-143"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

