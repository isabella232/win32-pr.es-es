---
title: MDM_Policy_User_Result01_Education02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Education02 representa las directivas de educación.
ms.assetid: 34dcc478-5f39-4e1a-908b-46cbbf2ff4fd
keywords:
- MDM_Policy_User_Result01_Education02 (clase)
- MDM_Policy_User_Result01_Education02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Education02
- MDM_Policy_User_Result01_Education02.InstanceID
- MDM_Policy_User_Result01_Education02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce82ae1131287ec04c77e084e822609a0e0ab07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422344"
---
# <a name="mdm_policy_user_result01_education02-class"></a><span data-ttu-id="d2317-105">\_Clase Education02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="d2317-105">MDM\_Policy\_User\_Result01\_Education02 class</span></span>

<span data-ttu-id="d2317-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="d2317-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d2317-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="d2317-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d2317-108">La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Education02 representa las directivas de educación.</span><span class="sxs-lookup"><span data-stu-id="d2317-108">The MDM\_Policy\_User\_Result01\_Education02 class represents the education policies.</span></span>

<span data-ttu-id="d2317-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d2317-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2317-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2317-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Education02
{
  string InstanceID;
  string ParentID;
  string DefaultPrinterName;
  sint32 PreventAddingNewPrinters;
  string PrinterNames;
};
```

## <a name="members"></a><span data-ttu-id="d2317-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="d2317-111">Members</span></span>

<span data-ttu-id="d2317-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Education02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d2317-112">The **MDM\_Policy\_User\_Result01\_Education02** class has these types of members:</span></span>

-   [<span data-ttu-id="d2317-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2317-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d2317-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2317-114">Properties</span></span>

<span data-ttu-id="d2317-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Education02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d2317-115">The **MDM\_Policy\_User\_Result01\_Education02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="d2317-116">DefaultPrinterName</span><span class="sxs-lookup"><span data-stu-id="d2317-116">DefaultPrinterName</span></span>](/windows/client-management/mdm/policy-csp-education#education-defaultprintername)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2317-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2317-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2317-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d2317-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2317-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d2317-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2317-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2317-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2317-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2317-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2317-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2317-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="d2317-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="d2317-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2317-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2317-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2317-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d2317-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d2317-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d2317-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2317-127">PreventAddingNewPrinters</span><span class="sxs-lookup"><span data-stu-id="d2317-127">PreventAddingNewPrinters</span></span>](/windows/client-management/mdm/policy-csp-education#education-preventaddingnewprinters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2317-128">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="d2317-128">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="d2317-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d2317-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="d2317-130">PrinterNames</span><span class="sxs-lookup"><span data-stu-id="d2317-130">PrinterNames</span></span>](/windows/client-management/mdm/policy-csp-education#education-printernames)
</dt> <dd> <dl> <dt>

<span data-ttu-id="d2317-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d2317-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d2317-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d2317-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d2317-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2317-133">Requirements</span></span>



| <span data-ttu-id="d2317-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2317-134">Requirement</span></span> | <span data-ttu-id="d2317-135">Value</span><span class="sxs-lookup"><span data-stu-id="d2317-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2317-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2317-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d2317-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d2317-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2317-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2317-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d2317-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="d2317-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d2317-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2317-140">Namespace</span></span><br/>                | <span data-ttu-id="d2317-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="d2317-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d2317-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d2317-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2317-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2317-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2317-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2317-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2317-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2317-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

