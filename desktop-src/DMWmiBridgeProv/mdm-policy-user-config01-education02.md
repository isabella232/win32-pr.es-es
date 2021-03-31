---
title: MDM_Policy_User_Config01_Education02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Education02 configura las directivas de educación.
ms.assetid: d9a263c7-ee9c-4857-b9a6-f0efdb373e13
keywords:
- MDM_Policy_User_Config01_Education02 (clase)
- MDM_Policy_User_Config01_Education02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Education02
- MDM_Policy_User_Config01_Education02.InstanceID
- MDM_Policy_User_Config01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae8508668b95edce1d4c4a2d0e99cbba2bc6d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996099"
---
# <a name="mdm_policy_user_config01_education02-class"></a><span data-ttu-id="fba69-105">\_Clase Education02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="fba69-105">MDM\_Policy\_User\_Config01\_Education02 class</span></span>

<span data-ttu-id="fba69-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fba69-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fba69-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fba69-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fba69-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Education02 configura las directivas de educación.</span><span class="sxs-lookup"><span data-stu-id="fba69-108">The MDM\_Policy\_User\_Config01\_Education02 class configures the education policies.</span></span>

<span data-ttu-id="fba69-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fba69-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba69-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fba69-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="fba69-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fba69-111">Members</span></span>

<span data-ttu-id="fba69-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Education02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fba69-112">The **MDM\_Policy\_User\_Config01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="fba69-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fba69-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fba69-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fba69-114">Properties</span></span>

<span data-ttu-id="fba69-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Education02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fba69-115">The **MDM\_Policy\_User\_Config01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fba69-116">DefaultPrinterName</span><span class="sxs-lookup"><span data-stu-id="fba69-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba69-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fba69-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba69-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fba69-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fba69-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fba69-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba69-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fba69-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba69-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fba69-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba69-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fba69-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fba69-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fba69-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba69-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fba69-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba69-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fba69-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fba69-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fba69-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fba69-127">PreventAddingNewPrinters</span><span class="sxs-lookup"><span data-stu-id="fba69-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba69-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fba69-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fba69-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fba69-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fba69-130">PrinterNames</span><span class="sxs-lookup"><span data-stu-id="fba69-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fba69-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fba69-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fba69-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fba69-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fba69-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fba69-133">Requirements</span></span>



| <span data-ttu-id="fba69-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="fba69-134">Requirement</span></span> | <span data-ttu-id="fba69-135">Value</span><span class="sxs-lookup"><span data-stu-id="fba69-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fba69-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba69-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fba69-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fba69-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fba69-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fba69-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fba69-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fba69-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fba69-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fba69-140">Namespace</span></span><br/>                | <span data-ttu-id="fba69-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="fba69-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fba69-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fba69-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fba69-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fba69-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fba69-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fba69-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fba69-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fba69-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

