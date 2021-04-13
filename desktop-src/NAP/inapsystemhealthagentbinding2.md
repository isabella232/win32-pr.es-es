---
title: Interfaz INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
description: Los Sha usan para comunicarse con el NapAgent. | Interfaz INapSystemHealthAgentBinding2 (NapSystemHealthAgent. h)
ms.assetid: 2b087d79-a738-42d6-a8f2-4698ab844446
keywords:
- Interfaz INapSystemHealthAgentBinding2 NAP
- Interfaz INapSystemHealthAgentBinding2 NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9a7491a2e78d66399f9ca246bcee9182e4f95d0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362158"
---
# <a name="inapsystemhealthagentbinding2-interface"></a><span data-ttu-id="efaf4-106">Interfaz INapSystemHealthAgentBinding2</span><span class="sxs-lookup"><span data-stu-id="efaf4-106">INapSystemHealthAgentBinding2 interface</span></span>

> [!Note]  
> <span data-ttu-id="efaf4-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="efaf4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="efaf4-108">**INapSystemHealthAgentBinding2** proporciona métodos que los Sha usan para comunicarse con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="efaf4-108">The **INapSystemHealthAgentBinding2** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="efaf4-109">Esta interfaz hereda todos los métodos de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) y se debe usar en su lugar.</span><span class="sxs-lookup"><span data-stu-id="efaf4-109">This interface inherits all the methods of [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="efaf4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="efaf4-110">Members</span></span>

<span data-ttu-id="efaf4-111">La interfaz **INapSystemHealthAgentBinding2** hereda de [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span><span class="sxs-lookup"><span data-stu-id="efaf4-111">The **INapSystemHealthAgentBinding2** interface inherits from [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md).</span></span> <span data-ttu-id="efaf4-112">**INapSystemHealthAgentBinding2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="efaf4-112">**INapSystemHealthAgentBinding2** also has these types of members:</span></span>

-   [<span data-ttu-id="efaf4-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="efaf4-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="efaf4-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="efaf4-114">Methods</span></span>

<span data-ttu-id="efaf4-115">La interfaz **INapSystemHealthAgentBinding2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="efaf4-115">The **INapSystemHealthAgentBinding2** interface has these methods.</span></span>



| <span data-ttu-id="efaf4-116">Método</span><span class="sxs-lookup"><span data-stu-id="efaf4-116">Method</span></span>                                                                                                                    | <span data-ttu-id="efaf4-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="efaf4-117">Description</span></span>                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efaf4-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span><span class="sxs-lookup"><span data-stu-id="efaf4-118">**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**</span></span>](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) | <span data-ttu-id="efaf4-119">Lo llaman los Sha para determinar el estado de aislamiento del sistema y el estado de aislamiento extendido.</span><span class="sxs-lookup"><span data-stu-id="efaf4-119">Called by SHAs to determine the system isolation state and extended isolation state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efaf4-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="efaf4-120">Remarks</span></span>

<span data-ttu-id="efaf4-121">Todas las API de esta interfaz devolverán **RPC \_ E \_ desconectadas** si NapAgent está detenido.</span><span class="sxs-lookup"><span data-stu-id="efaf4-121">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="efaf4-122">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="efaf4-122">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="efaf4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efaf4-123">Requirements</span></span>



| <span data-ttu-id="efaf4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="efaf4-124">Requirement</span></span> | <span data-ttu-id="efaf4-125">Value</span><span class="sxs-lookup"><span data-stu-id="efaf4-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efaf4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efaf4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="efaf4-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="efaf4-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="efaf4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efaf4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="efaf4-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="efaf4-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="efaf4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="efaf4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="efaf4-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="efaf4-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="efaf4-132">IDL</span><span class="sxs-lookup"><span data-stu-id="efaf4-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="efaf4-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="efaf4-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="efaf4-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efaf4-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efaf4-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="efaf4-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="efaf4-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="efaf4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efaf4-137">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="efaf4-137">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> <dt>

[<span data-ttu-id="efaf4-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="efaf4-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="efaf4-139">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="efaf4-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





