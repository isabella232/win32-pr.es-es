---
title: MDM_Policy_Config01_RemoteShell02 (clase)
description: La \_ clase Config01 de RemoteShell02 de directivas MDM \_ \_ configura las directivas de shell remoto.
ms.assetid: 7026fadb-ec6a-4696-a24c-1b1e071b94b0
keywords:
- MDM_Policy_Config01_RemoteShell02 (clase)
- MDM_Policy_Config01_RemoteShell02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteShell02
- MDM_Policy_Config01_RemoteShell02.InstanceID
- MDM_Policy_Config01_RemoteShell02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c318b0c6f23e92d90091495fdc25993d6958ca56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490828"
---
# <a name="mdm_policy_config01_remoteshell02-class"></a><span data-ttu-id="e08b2-105">\_ \_ Clase RemoteShell02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="e08b2-105">MDM\_Policy\_Config01\_RemoteShell02 class</span></span>

<span data-ttu-id="e08b2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e08b2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e08b2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e08b2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e08b2-108">La \_ clase Config01 de RemoteShell02 de directivas MDM \_ \_ configura las directivas de shell remoto.</span><span class="sxs-lookup"><span data-stu-id="e08b2-108">The MDM\_Policy\_Config01\_RemoteShell02 class configures the remote shell policies.</span></span>

<span data-ttu-id="e08b2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e08b2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08b2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e08b2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteShell02
{
  string InstanceID;
  string ParentID;
  string AllowRemoteShellAccess;
  string MaxConcurrentUsers;
  string SpecifyIdleTimeout;
  string SpecifyMaxMemory;
  string SpecifyMaxProcesses;
  string SpecifyMaxRemoteShells;
  string SpecifyShellTimeout;
};
```

## <a name="members"></a><span data-ttu-id="e08b2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e08b2-111">Members</span></span>

<span data-ttu-id="e08b2-112">La clase Config01 de la **\_ Directiva MDM \_ \_ RemoteShell02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e08b2-112">The **MDM\_Policy\_Config01\_RemoteShell02** class has these types of members:</span></span>

-   [<span data-ttu-id="e08b2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e08b2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e08b2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e08b2-114">Properties</span></span>

<span data-ttu-id="e08b2-115">La **clase \_ \_ Config01 de \_ RemoteShell02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e08b2-115">The **MDM\_Policy\_Config01\_RemoteShell02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e08b2-116">AllowRemoteShellAccess</span><span class="sxs-lookup"><span data-stu-id="e08b2-116">AllowRemoteShellAccess</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-allowremoteshellaccess)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e08b2-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e08b2-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e08b2-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e08b2-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-123">MaxConcurrentUsers</span><span class="sxs-lookup"><span data-stu-id="e08b2-123">MaxConcurrentUsers</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-maxconcurrentusers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e08b2-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e08b2-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e08b2-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e08b2-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-130">SpecifyIdleTimeout</span><span class="sxs-lookup"><span data-stu-id="e08b2-130">SpecifyIdleTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyidletimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-133">SpecifyMaxMemory</span><span class="sxs-lookup"><span data-stu-id="e08b2-133">SpecifyMaxMemory</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxmemory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-136">SpecifyMaxProcesses</span><span class="sxs-lookup"><span data-stu-id="e08b2-136">SpecifyMaxProcesses</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxprocesses)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-139">SpecifyMaxRemoteShells</span><span class="sxs-lookup"><span data-stu-id="e08b2-139">SpecifyMaxRemoteShells</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifymaxremoteshells)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e08b2-142">SpecifyShellTimeout</span><span class="sxs-lookup"><span data-stu-id="e08b2-142">SpecifyShellTimeout</span></span>](/windows/client-management/mdm/policy-csp-remoteshell#remoteshell-specifyshelltimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e08b2-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e08b2-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e08b2-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e08b2-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e08b2-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08b2-145">Requirements</span></span>



| <span data-ttu-id="e08b2-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08b2-146">Requirement</span></span> | <span data-ttu-id="e08b2-147">Value</span><span class="sxs-lookup"><span data-stu-id="e08b2-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08b2-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08b2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e08b2-149">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e08b2-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e08b2-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08b2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e08b2-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e08b2-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e08b2-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e08b2-152">Namespace</span></span><br/>                | <span data-ttu-id="e08b2-153">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e08b2-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e08b2-154">MOF</span><span class="sxs-lookup"><span data-stu-id="e08b2-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e08b2-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e08b2-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e08b2-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e08b2-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08b2-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08b2-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

