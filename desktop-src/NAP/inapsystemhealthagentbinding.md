---
title: Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Los Sha usan para comunicarse con el NapAgent. | Interfaz INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Interfaz INapSystemHealthAgentBinding NAP
- Interfaz INapSystemHealthAgentBinding NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678759"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="947cc-106">Interfaz INapSystemHealthAgentBinding</span><span class="sxs-lookup"><span data-stu-id="947cc-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="947cc-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="947cc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="947cc-108">**INapSystemHealthAgentBinding** proporciona métodos que los Sha usan para comunicarse con NapAgent.</span><span class="sxs-lookup"><span data-stu-id="947cc-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="947cc-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) hereda todos los métodos de esta interfaz y debe usarse en su lugar.</span><span class="sxs-lookup"><span data-stu-id="947cc-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="947cc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="947cc-110">Members</span></span>

<span data-ttu-id="947cc-111">La interfaz **INapSystemHealthAgentBinding** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="947cc-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="947cc-112">**INapSystemHealthAgentBinding** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="947cc-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="947cc-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="947cc-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="947cc-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="947cc-114">Methods</span></span>

<span data-ttu-id="947cc-115">La interfaz **INapSystemHealthAgentBinding** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="947cc-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="947cc-116">Método</span><span class="sxs-lookup"><span data-stu-id="947cc-116">Method</span></span>                                                                                                                     | <span data-ttu-id="947cc-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="947cc-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="947cc-118">**INapSystemHealthAgentBinding::FlushCache**</span><span class="sxs-lookup"><span data-stu-id="947cc-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="947cc-119">Lo llama un SHA para vaciar la memoria caché de SoH.</span><span class="sxs-lookup"><span data-stu-id="947cc-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="947cc-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span><span class="sxs-lookup"><span data-stu-id="947cc-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="947cc-121">Lo llaman los Sha para determinar el estado de aislamiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="947cc-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="947cc-122">**INapSystemHealthAgentBinding:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="947cc-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="947cc-123">Inicializa SHA y enlaza el SHA al servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="947cc-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="947cc-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="947cc-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="947cc-125">Lo llaman los Sha cuando cambia el SoH.</span><span class="sxs-lookup"><span data-stu-id="947cc-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="947cc-126">**INapSystemHealthAgentBinding:: UnInitialize**</span><span class="sxs-lookup"><span data-stu-id="947cc-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="947cc-127">Lo llaman los Sha para hacer que el NapAgent libere todas sus referencias a punteros COM SHA.</span><span class="sxs-lookup"><span data-stu-id="947cc-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="947cc-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="947cc-128">Remarks</span></span>

<span data-ttu-id="947cc-129">Todas las API de esta interfaz devolverán **RPC \_ E \_ desconectadas** si NapAgent está detenido.</span><span class="sxs-lookup"><span data-stu-id="947cc-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="947cc-130">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="947cc-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="947cc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="947cc-131">Requirements</span></span>



| <span data-ttu-id="947cc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="947cc-132">Requirement</span></span> | <span data-ttu-id="947cc-133">Value</span><span class="sxs-lookup"><span data-stu-id="947cc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="947cc-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="947cc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="947cc-135">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="947cc-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="947cc-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="947cc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="947cc-137">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="947cc-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="947cc-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="947cc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="947cc-139"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="947cc-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="947cc-140">IDL</span><span class="sxs-lookup"><span data-stu-id="947cc-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="947cc-141"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="947cc-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="947cc-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="947cc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="947cc-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="947cc-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="947cc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="947cc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="947cc-145">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="947cc-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="947cc-146">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="947cc-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

