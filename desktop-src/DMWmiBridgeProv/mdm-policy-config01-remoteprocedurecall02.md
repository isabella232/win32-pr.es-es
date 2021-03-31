---
title: MDM_Policy_Config01_RemoteProcedureCall02 (clase)
description: La \_ clase Config01 de RemoteProcedureCall02 de directivas MDM \_ \_ configura las directivas de llamada a procedimiento remoto.
ms.assetid: d844c59d-c71e-4a8f-ad1e-955a918a36b8
keywords:
- MDM_Policy_Config01_RemoteProcedureCall02 (clase)
- MDM_Policy_Config01_RemoteProcedureCall02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteProcedureCall02
- MDM_Policy_Config01_RemoteProcedureCall02.InstanceID
- MDM_Policy_Config01_RemoteProcedureCall02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1c1a188afd3694273080c6c369a8dc37abb22a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490498"
---
# <a name="mdm_policy_config01_remoteprocedurecall02-class"></a><span data-ttu-id="a0ead-105">\_ \_ Clase RemoteProcedureCall02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="a0ead-105">MDM\_Policy\_Config01\_RemoteProcedureCall02 class</span></span>

<span data-ttu-id="a0ead-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a0ead-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a0ead-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a0ead-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a0ead-108">La \_ clase Config01 de RemoteProcedureCall02 de directivas MDM \_ \_ configura las directivas de llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="a0ead-108">The MDM\_Policy\_Config01\_RemoteProcedureCall02 class configures the remote procedure call policies.</span></span>

<span data-ttu-id="a0ead-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a0ead-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0ead-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0ead-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteProcedureCall02
{
  string InstanceID;
  string ParentID;
  string RestrictUnauthenticatedRPCClients;
  string RPCEndpointMapperClientAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="a0ead-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a0ead-111">Members</span></span>

<span data-ttu-id="a0ead-112">La clase Config01 de la **\_ Directiva MDM \_ \_ RemoteProcedureCall02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a0ead-112">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these types of members:</span></span>

-   [<span data-ttu-id="a0ead-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0ead-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a0ead-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0ead-114">Properties</span></span>

<span data-ttu-id="a0ead-115">La **clase \_ \_ Config01 de \_ RemoteProcedureCall02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a0ead-115">The **MDM\_Policy\_Config01\_RemoteProcedureCall02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a0ead-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a0ead-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ead-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0ead-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0ead-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0ead-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a0ead-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a0ead-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ead-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0ead-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a0ead-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a0ead-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0ead-124">RestrictUnauthenticatedRPCClients</span><span class="sxs-lookup"><span data-stu-id="a0ead-124">RestrictUnauthenticatedRPCClients</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-restrictunauthenticatedrpcclients)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ead-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0ead-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0ead-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a0ead-127">RPCEndpointMapperClientAuthentication</span><span class="sxs-lookup"><span data-stu-id="a0ead-127">RPCEndpointMapperClientAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remoteprocedurecall#remoteprocedurecall-rpcendpointmapperclientauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a0ead-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a0ead-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a0ead-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a0ead-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a0ead-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0ead-130">Requirements</span></span>



| <span data-ttu-id="a0ead-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0ead-131">Requirement</span></span> | <span data-ttu-id="a0ead-132">Value</span><span class="sxs-lookup"><span data-stu-id="a0ead-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0ead-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0ead-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a0ead-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0ead-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0ead-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0ead-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a0ead-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a0ead-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a0ead-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0ead-137">Namespace</span></span><br/>                | <span data-ttu-id="a0ead-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a0ead-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a0ead-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a0ead-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0ead-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0ead-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0ead-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0ead-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0ead-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0ead-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

