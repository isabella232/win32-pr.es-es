---
title: MDM_Policy_Config01_RemoteAssistance02 (clase)
description: La \_ clase Config01 de RemoteAssistance02 de directivas MDM \_ \_ configura las directivas de asistencia remota.
ms.assetid: bcc6c570-66d9-4dcd-b7f2-2d03733c0bcb
keywords:
- MDM_Policy_Config01_RemoteAssistance02 (clase)
- MDM_Policy_Config01_RemoteAssistance02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteAssistance02
- MDM_Policy_Config01_RemoteAssistance02.InstanceID
- MDM_Policy_Config01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aceadb2eb784e72e4e332cdd34df44d779c99e97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905228"
---
# <a name="mdm_policy_config01_remoteassistance02-class"></a><span data-ttu-id="75170-105">\_ \_ Clase RemoteAssistance02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="75170-105">MDM\_Policy\_Config01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="75170-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="75170-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="75170-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="75170-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="75170-108">La \_ clase Config01 de RemoteAssistance02 de directivas MDM \_ \_ configura las directivas de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="75170-108">The MDM\_Policy\_Config01\_RemoteAssistance02 class configures the remote assistance policies.</span></span>

<span data-ttu-id="75170-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="75170-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75170-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75170-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="75170-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="75170-111">Members</span></span>

<span data-ttu-id="75170-112">La clase Config01 de la **\_ Directiva MDM \_ \_ RemoteAssistance02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="75170-112">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="75170-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75170-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75170-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="75170-114">Properties</span></span>

<span data-ttu-id="75170-115">La **clase \_ \_ Config01 de \_ RemoteAssistance02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="75170-115">The **MDM\_Policy\_Config01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="75170-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="75170-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75170-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="75170-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="75170-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75170-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75170-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75170-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="75170-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="75170-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="75170-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75170-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="75170-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75170-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="75170-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75170-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75170-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="75170-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75170-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="75170-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="75170-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="75170-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="75170-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75170-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="75170-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75170-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75170-136">Requirements</span></span>



| <span data-ttu-id="75170-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="75170-137">Requirement</span></span> | <span data-ttu-id="75170-138">Value</span><span class="sxs-lookup"><span data-stu-id="75170-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75170-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75170-139">Minimum supported client</span></span><br/> | <span data-ttu-id="75170-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="75170-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75170-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75170-141">Minimum supported server</span></span><br/> | <span data-ttu-id="75170-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="75170-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="75170-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75170-143">Namespace</span></span><br/>                | <span data-ttu-id="75170-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="75170-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="75170-145">MOF</span><span class="sxs-lookup"><span data-stu-id="75170-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75170-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75170-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="75170-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75170-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75170-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75170-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

