---
title: MDM_Policy_Config01_EventLogService02 (clase)
description: La \_ clase Config01 de EventLogService02 de directivas MDM \_ \_ configura el comportamiento del registro de eventos.
ms.assetid: 206934c4-6671-4f13-be79-22ff1fb7ce7e
keywords:
- MDM_Policy_Config01_EventLogService02 (clase)
- MDM_Policy_Config01_EventLogService02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_EventLogService02
- MDM_Policy_Config01_EventLogService02.InstanceID
- MDM_Policy_Config01_EventLogService02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e39d3e78e686886e689ab2333b073108207446a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996195"
---
# <a name="mdm_policy_config01_eventlogservice02-class"></a><span data-ttu-id="2de70-105">\_ \_ Clase EventLogService02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="2de70-105">MDM\_Policy\_Config01\_EventLogService02 class</span></span>

<span data-ttu-id="2de70-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2de70-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2de70-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2de70-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2de70-108">La \_ clase Config01 de EventLogService02 de directivas MDM \_ \_ configura el comportamiento del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="2de70-108">The MDM\_Policy\_Config01\_EventLogService02 class configures the event log behavior.</span></span>

<span data-ttu-id="2de70-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2de70-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2de70-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2de70-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_EventLogService02
{
  string InstanceID;
  string ParentID;
  string ControlEventLogBehavior;
  string SpecifyMaximumFileSizeApplicationLog;
  string SpecifyMaximumFileSizeSecurityLog;
  string SpecifyMaximumFileSizeSystemLog;
};
```

## <a name="members"></a><span data-ttu-id="2de70-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2de70-111">Members</span></span>

<span data-ttu-id="2de70-112">La clase Config01 de la **\_ Directiva MDM \_ \_ EventLogService02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2de70-112">The **MDM\_Policy\_Config01\_EventLogService02** class has these types of members:</span></span>

-   [<span data-ttu-id="2de70-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2de70-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2de70-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2de70-114">Properties</span></span>

<span data-ttu-id="2de70-115">La **clase \_ \_ Config01 de \_ EventLogService02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2de70-115">The **MDM\_Policy\_Config01\_EventLogService02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2de70-116">ControlEventLogBehavior</span><span class="sxs-lookup"><span data-stu-id="2de70-116">ControlEventLogBehavior</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-controleventlogbehavior)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2de70-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2de70-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2de70-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2de70-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2de70-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2de70-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2de70-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2de70-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2de70-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2de70-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2de70-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2de70-127">SpecifyMaximumFileSizeApplicationLog</span><span class="sxs-lookup"><span data-stu-id="2de70-127">SpecifyMaximumFileSizeApplicationLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizeapplicationlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2de70-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2de70-130">SpecifyMaximumFileSizeSecurityLog</span><span class="sxs-lookup"><span data-stu-id="2de70-130">SpecifyMaximumFileSizeSecurityLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesecuritylog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2de70-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2de70-133">SpecifyMaximumFileSizeSystemLog</span><span class="sxs-lookup"><span data-stu-id="2de70-133">SpecifyMaximumFileSizeSystemLog</span></span>](/windows/client-management/mdm/policy-csp-eventlogservice#eventlogservice-specifymaximumfilesizesystemlog)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2de70-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2de70-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2de70-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2de70-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2de70-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2de70-136">Requirements</span></span>



| <span data-ttu-id="2de70-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="2de70-137">Requirement</span></span> | <span data-ttu-id="2de70-138">Value</span><span class="sxs-lookup"><span data-stu-id="2de70-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2de70-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2de70-139">Minimum supported client</span></span><br/> | <span data-ttu-id="2de70-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2de70-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2de70-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2de70-141">Minimum supported server</span></span><br/> | <span data-ttu-id="2de70-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2de70-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2de70-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2de70-143">Namespace</span></span><br/>                | <span data-ttu-id="2de70-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2de70-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2de70-145">MOF</span><span class="sxs-lookup"><span data-stu-id="2de70-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2de70-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2de70-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2de70-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2de70-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2de70-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2de70-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

