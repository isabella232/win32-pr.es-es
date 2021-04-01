---
title: MDM_Policy_Config01_Cellular02 (clase)
description: La \_ clase Config01 de Cellular02 de directivas MDM \_ \_ configura las directivas de telefonía móvil.
ms.assetid: e5926a21-a375-4d1c-8b37-7fe7f7532c50
keywords:
- MDM_Policy_Config01_Cellular02 (clase)
- MDM_Policy_Config01_Cellular02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cellular02
- MDM_Policy_Config01_Cellular02.InstanceID
- MDM_Policy_Config01_Cellular02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1b6d9163723299b144368d9d2b73a12ccc7a91
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150111"
---
# <a name="mdm_policy_config01_cellular02-class"></a><span data-ttu-id="d116f-105">\_ \_ Clase Cellular02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="d116f-105">MDM\_Policy\_Config01\_Cellular02 class</span></span>

<span data-ttu-id="d116f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d116f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d116f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d116f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d116f-108">La \_ clase Config01 de Cellular02 de directivas MDM \_ \_ configura las directivas de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="d116f-108">The MDM\_Policy\_Config01\_Cellular02 class configures the cellular policies.</span></span>

<span data-ttu-id="d116f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d116f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d116f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d116f-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cellular02
{
  string InstanceID;
  string ParentID;
  string LetAppsAccessCellularData_UserInControlOfTheseApps;
  string LetAppsAccessCellularData_ForceDenyTheseApps;
  string LetAppsAccessCellularData_ForceAllowTheseApps;
  sint32 LetAppsAccessCellularData;
  string ShowAppCellularAccessUI;
};
```

## <a name="members"></a><span data-ttu-id="d116f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d116f-111">Members</span></span>

<span data-ttu-id="d116f-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Cellular02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d116f-112">The **MDM\_Policy\_Config01\_Cellular02** class has these types of members:</span></span>

-   [<span data-ttu-id="d116f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d116f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d116f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d116f-114">Properties</span></span>

<span data-ttu-id="d116f-115">La **clase \_ \_ Config01 de \_ Cellular02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d116f-115">The **MDM\_Policy\_Config01\_Cellular02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d116f-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d116f-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d116f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d116f-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d116f-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d116f-120">LetAppsAccessCellularData</span><span class="sxs-lookup"><span data-stu-id="d116f-120">LetAppsAccessCellularData</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d116f-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d116f-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d116f-123">LetAppsAccessCellularData \_ ForceAllowTheseApps</span><span class="sxs-lookup"><span data-stu-id="d116f-123">LetAppsAccessCellularData\_ForceAllowTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forceallowtheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d116f-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d116f-126">LetAppsAccessCellularData \_ ForceDenyTheseApps</span><span class="sxs-lookup"><span data-stu-id="d116f-126">LetAppsAccessCellularData\_ForceDenyTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-forcedenytheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d116f-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d116f-129">LetAppsAccessCellularData \_ UserInControlOfTheseApps</span><span class="sxs-lookup"><span data-stu-id="d116f-129">LetAppsAccessCellularData\_UserInControlOfTheseApps</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-letappsaccesscellulardata-userincontroloftheseapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d116f-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d116f-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d116f-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d116f-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d116f-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d116f-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d116f-136">ShowAppCellularAccessUI</span><span class="sxs-lookup"><span data-stu-id="d116f-136">ShowAppCellularAccessUI</span></span>](/windows/client-management/mdm/policy-csp-cellular#cellular-showappcellularaccessui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d116f-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d116f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d116f-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d116f-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d116f-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d116f-139">Requirements</span></span>



| <span data-ttu-id="d116f-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d116f-140">Requirement</span></span> | <span data-ttu-id="d116f-141">Value</span><span class="sxs-lookup"><span data-stu-id="d116f-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d116f-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d116f-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d116f-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d116f-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d116f-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d116f-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d116f-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d116f-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d116f-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d116f-146">Namespace</span></span><br/>                | <span data-ttu-id="d116f-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d116f-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d116f-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d116f-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d116f-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d116f-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d116f-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d116f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d116f-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d116f-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

