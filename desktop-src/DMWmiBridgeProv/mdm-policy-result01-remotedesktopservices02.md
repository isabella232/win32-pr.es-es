---
title: MDM_Policy_Result01_RemoteDesktopServices02 (clase)
description: La \_ clase Result01 de la Directiva MDM \_ \_ RemoteDesktopServices02 representa las directivas de servicios de escritorio remoto.
ms.assetid: 015fe30d-2b76-4df5-a81f-65e488db3526
keywords:
- MDM_Policy_Result01_RemoteDesktopServices02 (clase)
- MDM_Policy_Result01_RemoteDesktopServices02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteDesktopServices02
- MDM_Policy_Result01_RemoteDesktopServices02.InstanceID
- MDM_Policy_Result01_RemoteDesktopServices02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0488308a557f1b872de299bda12487287e1081c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995967"
---
# <a name="mdm_policy_result01_remotedesktopservices02-class"></a><span data-ttu-id="47f58-105">\_ \_ Clase RemoteDesktopServices02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="47f58-105">MDM\_Policy\_Result01\_RemoteDesktopServices02 class</span></span>

<span data-ttu-id="47f58-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="47f58-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="47f58-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="47f58-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="47f58-108">La \_ clase Result01 de la Directiva MDM \_ \_ RemoteDesktopServices02 representa las directivas de servicios de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="47f58-108">The MDM\_Policy\_Result01\_RemoteDesktopServices02 class represents the remote desktop services policies.</span></span>

<span data-ttu-id="47f58-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="47f58-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f58-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47f58-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteDesktopServices02
{
  string InstanceID;
  string ParentID;
  string AllowUsersToConnectRemotely;
  string ClientConnectionEncryptionLevel;
  string DoNotAllowDriveRedirection;
  string DoNotAllowPasswordSaving;
  string PromptForPasswordUponConnection;
  string RequireSecureRPCCommunication;
};
```

## <a name="members"></a><span data-ttu-id="47f58-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="47f58-111">Members</span></span>

<span data-ttu-id="47f58-112">La clase Result01 de la **\_ Directiva MDM \_ \_ RemoteDesktopServices02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="47f58-112">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these types of members:</span></span>

-   [<span data-ttu-id="47f58-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47f58-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="47f58-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="47f58-114">Properties</span></span>

<span data-ttu-id="47f58-115">La **clase \_ \_ Result01 de \_ RemoteDesktopServices02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="47f58-115">The **MDM\_Policy\_Result01\_RemoteDesktopServices02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="47f58-116">AllowUsersToConnectRemotely</span><span class="sxs-lookup"><span data-stu-id="47f58-116">AllowUsersToConnectRemotely</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-allowuserstoconnectremotely)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47f58-119">ClientConnectionEncryptionLevel</span><span class="sxs-lookup"><span data-stu-id="47f58-119">ClientConnectionEncryptionLevel</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-clientconnectionencryptionlevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47f58-122">DoNotAllowDriveRedirection</span><span class="sxs-lookup"><span data-stu-id="47f58-122">DoNotAllowDriveRedirection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowdriveredirection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47f58-125">DoNotAllowPasswordSaving</span><span class="sxs-lookup"><span data-stu-id="47f58-125">DoNotAllowPasswordSaving</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-donotallowpasswordsaving)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47f58-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="47f58-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47f58-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f58-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47f58-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="47f58-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="47f58-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="47f58-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="47f58-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="47f58-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47f58-136">PromptForPasswordUponConnection</span><span class="sxs-lookup"><span data-stu-id="47f58-136">PromptForPasswordUponConnection</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-promptforpassworduponconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="47f58-139">RequireSecureRPCCommunication</span><span class="sxs-lookup"><span data-stu-id="47f58-139">RequireSecureRPCCommunication</span></span>](/windows/client-management/mdm/policy-csp-remotedesktopservices#remotedesktopservices-requiresecurerpccommunication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="47f58-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="47f58-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="47f58-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="47f58-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="47f58-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47f58-142">Requirements</span></span>



| <span data-ttu-id="47f58-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="47f58-143">Requirement</span></span> | <span data-ttu-id="47f58-144">Value</span><span class="sxs-lookup"><span data-stu-id="47f58-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47f58-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47f58-145">Minimum supported client</span></span><br/> | <span data-ttu-id="47f58-146">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="47f58-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="47f58-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47f58-147">Minimum supported server</span></span><br/> | <span data-ttu-id="47f58-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="47f58-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="47f58-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="47f58-149">Namespace</span></span><br/>                | <span data-ttu-id="47f58-150">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="47f58-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="47f58-151">MOF</span><span class="sxs-lookup"><span data-stu-id="47f58-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="47f58-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="47f58-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="47f58-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47f58-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47f58-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f58-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

