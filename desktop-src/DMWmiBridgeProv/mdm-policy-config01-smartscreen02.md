---
title: MDM_Policy_Config01_SmartScreen02 (clase)
description: La \_ clase Config01 de SmartScreen02 de directivas MDM \_ \_ configura las directivas de pantalla inteligente.
ms.assetid: e5ad04a1-afa9-4887-a4c1-c92c574a5398
keywords:
- MDM_Policy_Config01_SmartScreen02 (clase)
- MDM_Policy_Config01_SmartScreen02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_SmartScreen02
- MDM_Policy_Config01_SmartScreen02.InstanceID
- MDM_Policy_Config01_SmartScreen02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e0b8ca0c1e53005ab2a2ab80cce3f18dec40b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079424"
---
# <a name="mdm_policy_config01_smartscreen02-class"></a><span data-ttu-id="9c037-105">\_ \_ Clase SmartScreen02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="9c037-105">MDM\_Policy\_Config01\_SmartScreen02 class</span></span>

<span data-ttu-id="9c037-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9c037-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9c037-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9c037-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9c037-108">La \_ clase Config01 de SmartScreen02 de directivas MDM \_ \_ configura las directivas de pantalla inteligente.</span><span class="sxs-lookup"><span data-stu-id="9c037-108">The MDM\_Policy\_Config01\_SmartScreen02 class configures the smart screen policies.</span></span>

<span data-ttu-id="9c037-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9c037-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c037-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c037-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_SmartScreen02
{
  string InstanceID;
  string ParentID;
  sint32 EnableAppInstallControl;
  sint32 EnableSmartScreenInShell;
  sint32 PreventOverrideForFilesInShell;
};
```

## <a name="members"></a><span data-ttu-id="9c037-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c037-111">Members</span></span>

<span data-ttu-id="9c037-112">La clase Config01 de la **\_ Directiva MDM \_ \_ SmartScreen02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c037-112">The **MDM\_Policy\_Config01\_SmartScreen02** class has these types of members:</span></span>

-   [<span data-ttu-id="9c037-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c037-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c037-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c037-114">Properties</span></span>

<span data-ttu-id="9c037-115">La **clase \_ \_ Config01 de \_ SmartScreen02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c037-115">The **MDM\_Policy\_Config01\_SmartScreen02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9c037-116">EnableAppInstallControl</span><span class="sxs-lookup"><span data-stu-id="9c037-116">EnableAppInstallControl</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enableappinstallcontrol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c037-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9c037-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c037-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9c037-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9c037-119">EnableSmartScreenInShell</span><span class="sxs-lookup"><span data-stu-id="9c037-119">EnableSmartScreenInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-enablesmartscreeninshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c037-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9c037-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c037-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9c037-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c037-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9c037-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c037-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c037-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c037-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c037-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c037-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c037-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9c037-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9c037-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c037-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9c037-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9c037-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c037-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9c037-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9c037-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9c037-130">PreventOverrideForFilesInShell</span><span class="sxs-lookup"><span data-stu-id="9c037-130">PreventOverrideForFilesInShell</span></span>](/windows/client-management/mdm/policy-csp-smartscreen#smartscreen-preventoverrideforfilesinshell)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c037-131">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="9c037-131">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="9c037-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9c037-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9c037-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c037-133">Requirements</span></span>



| <span data-ttu-id="9c037-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c037-134">Requirement</span></span> | <span data-ttu-id="9c037-135">Value</span><span class="sxs-lookup"><span data-stu-id="9c037-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c037-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c037-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c037-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c037-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c037-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c037-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c037-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9c037-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9c037-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c037-140">Namespace</span></span><br/>                | <span data-ttu-id="9c037-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9c037-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9c037-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9c037-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c037-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c037-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c037-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c037-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c037-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c037-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

