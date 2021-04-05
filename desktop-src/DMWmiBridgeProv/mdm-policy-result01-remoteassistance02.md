---
title: MDM_Policy_Result01_RemoteAssistance02 (clase)
description: La \_ clase Result01 de la Directiva MDM \_ \_ RemoteAssistance02 representa las directivas de asistencia remota.
ms.assetid: ddb932ef-b309-4aad-8ab8-9d88739d90be
keywords:
- MDM_Policy_Result01_RemoteAssistance02 (clase)
- MDM_Policy_Result01_RemoteAssistance02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteAssistance02
- MDM_Policy_Result01_RemoteAssistance02.InstanceID
- MDM_Policy_Result01_RemoteAssistance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed928668e4851c981ea7c68d02cd1cdbefbda4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078916"
---
# <a name="mdm_policy_result01_remoteassistance02-class"></a><span data-ttu-id="ac404-105">\_ \_ Clase RemoteAssistance02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="ac404-105">MDM\_Policy\_Result01\_RemoteAssistance02 class</span></span>

<span data-ttu-id="ac404-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="ac404-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ac404-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="ac404-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ac404-108">La \_ clase Result01 de la Directiva MDM \_ \_ RemoteAssistance02 representa las directivas de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="ac404-108">The MDM\_Policy\_Result01\_RemoteAssistance02 class represents the remote assistance policies.</span></span>

<span data-ttu-id="ac404-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ac404-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac404-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac404-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteAssistance02
{
  string InstanceID;
  string ParentID;
  string CustomizeWarningMessages;
  string SessionLogging;
  string SolicitedRemoteAssistance;
  string UnsolicitedRemoteAssistance;
};
```

## <a name="members"></a><span data-ttu-id="ac404-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ac404-111">Members</span></span>

<span data-ttu-id="ac404-112">La clase Result01 de la **\_ Directiva MDM \_ \_ RemoteAssistance02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ac404-112">The **MDM\_Policy\_Result01\_RemoteAssistance02** class has these types of members:</span></span>

-   [<span data-ttu-id="ac404-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac404-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ac404-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac404-114">Properties</span></span>

<span data-ttu-id="ac404-115">La **clase \_ \_ Result01 de \_ RemoteAssistance02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ac404-115">The **MDM\_Policy\_Result01\_RemoteAssistance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="ac404-116">CustomizeWarningMessages</span><span class="sxs-lookup"><span data-stu-id="ac404-116">CustomizeWarningMessages</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-customizewarningmessages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ac404-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac404-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ac404-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac404-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac404-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac404-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ac404-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="ac404-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ac404-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ac404-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ac404-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac404-127">SessionLogging</span><span class="sxs-lookup"><span data-stu-id="ac404-127">SessionLogging</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-sessionlogging)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ac404-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac404-130">SolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="ac404-130">SolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-solicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ac404-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="ac404-133">UnsolicitedRemoteAssistance</span><span class="sxs-lookup"><span data-stu-id="ac404-133">UnsolicitedRemoteAssistance</span></span>](/windows/client-management/mdm/policy-csp-remoteassistance#remoteassistance-unsolicitedremoteassistance)
</dt> <dd> <dl> <dt>

<span data-ttu-id="ac404-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ac404-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ac404-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ac404-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ac404-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac404-136">Requirements</span></span>



| <span data-ttu-id="ac404-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac404-137">Requirement</span></span> | <span data-ttu-id="ac404-138">Value</span><span class="sxs-lookup"><span data-stu-id="ac404-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac404-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac404-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ac404-140">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="ac404-140">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ac404-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ac404-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ac404-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ac404-142">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ac404-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ac404-143">Namespace</span></span><br/>                | <span data-ttu-id="ac404-144">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="ac404-144">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ac404-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ac404-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ac404-146"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ac404-146"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ac404-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ac404-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac404-148"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac404-148"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

