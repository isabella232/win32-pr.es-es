---
title: Interfaz INapSystemHealthAgentCallback (NapSystemHealthAgent. h)
description: Los declara el sistema e implementan el sistema de escritura SHA para que el NapAgent pueda comunicarse con el SHA.
ms.assetid: f299e796-c81d-4a22-b9c8-f80990098044
keywords:
- Interfaz INapSystemHealthAgentCallback NAP
- Interfaz INapSystemHealthAgentCallback NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11d08dd9cf77d36ca33902c63831135a0cc2fe5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676885"
---
# <a name="inapsystemhealthagentcallback-interface"></a><span data-ttu-id="da18e-105">Interfaz INapSystemHealthAgentCallback</span><span class="sxs-lookup"><span data-stu-id="da18e-105">INapSystemHealthAgentCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="da18e-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="da18e-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="da18e-107">La interfaz **INapSystemHealthAgentCallback** proporciona métodos de devolución de llamada declarados por el sistema e implementados por el escritor Sha para que NapAgent pueda comunicarse con el Sha.</span><span class="sxs-lookup"><span data-stu-id="da18e-107">The **INapSystemHealthAgentCallback** interface provides callback methods that are declared by the system and implemented by the SHA writer so the NapAgent can communicate with the SHA.</span></span>

## <a name="members"></a><span data-ttu-id="da18e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="da18e-108">Members</span></span>

<span data-ttu-id="da18e-109">La interfaz **INapSystemHealthAgentCallback** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="da18e-109">The **INapSystemHealthAgentCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="da18e-110">**INapSystemHealthAgentCallback** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="da18e-110">**INapSystemHealthAgentCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="da18e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="da18e-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="da18e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="da18e-112">Methods</span></span>

<span data-ttu-id="da18e-113">La interfaz **INapSystemHealthAgentCallback** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="da18e-113">The **INapSystemHealthAgentCallback** interface has these methods.</span></span>



| <span data-ttu-id="da18e-114">Método</span><span class="sxs-lookup"><span data-stu-id="da18e-114">Method</span></span>                                                                                                                                           | <span data-ttu-id="da18e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="da18e-115">Description</span></span>                                                                                                          |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da18e-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span><span class="sxs-lookup"><span data-stu-id="da18e-116">**INapSystemHealthAgentCallback::CompareSoHRequests**</span></span>](inapsystemhealthagentcallback-comparesohrequests-method.md)                             | <span data-ttu-id="da18e-117">Utilizado por SHA para comparar el SOH.</span><span class="sxs-lookup"><span data-stu-id="da18e-117">Used by the SHA to compare the SoHs.</span></span><br/>                                                                      |
| [<span data-ttu-id="da18e-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span><span class="sxs-lookup"><span data-stu-id="da18e-118">**INapSystemHealthAgentCallback::GetFixupInfo**</span></span>](inapsystemhealthagentcallback-getfixupinfo-method.md)                                         | <span data-ttu-id="da18e-119">Lo llama NapAgent para determinar el estado del SHA.</span><span class="sxs-lookup"><span data-stu-id="da18e-119">Called by the NapAgent to determine the state of the SHA.</span></span><br/>                                                 |
| [<span data-ttu-id="da18e-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="da18e-120">**INapSystemHealthAgentCallback::GetSoHRequest**</span></span>](inapsystemhealthagentcallback-getsohrequest-method.md)                                       | <span data-ttu-id="da18e-121">Llamado por el NapAgent para consultar la solicitud de SoH de SHA.</span><span class="sxs-lookup"><span data-stu-id="da18e-121">Called by the NapAgent to query the SHA's SoH request.</span></span><br/>                                                    |
| [<span data-ttu-id="da18e-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="da18e-122">**INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest**</span></span>](inapsystemhealthagentcallback-notifyorphanedsohrequest-method.md)                 | <span data-ttu-id="da18e-123">Se llama si se ha consultado una solicitud de SoH desde SHA, pero la respuesta nunca llegó.</span><span class="sxs-lookup"><span data-stu-id="da18e-123">Called if an SoH request was queried from the SHA, but the response never came back.</span></span><br/>                      |
| [<span data-ttu-id="da18e-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span><span class="sxs-lookup"><span data-stu-id="da18e-124">**INapSystemHealthAgentCallback::NotifySystemIsolationStateChange**</span></span>](inapsystemhealthagentcallback-notifysystemisolationstatechange-method.md) | <span data-ttu-id="da18e-125">Lo llama NapAgent para indicar que ha cambiado el estado de aislamiento del sistema o el tiempo de finalización del período de prueba.</span><span class="sxs-lookup"><span data-stu-id="da18e-125">Called by the NapAgent to indicate that the system isolation state or the probation end-time has changed.</span></span><br/> |
| [<span data-ttu-id="da18e-126">**INapSystemHealthAgentCallback::P rocessSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="da18e-126">**INapSystemHealthAgentCallback::ProcessSoHResponse**</span></span>](inapsystemhealthagentcallback-processsohresponse-method.md)                             | <span data-ttu-id="da18e-127">Se llama cuando NapAgent recibe una respuesta de SoH destinada a este agente de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="da18e-127">Called when the NapAgent receives an SoH response destined for this health agent.</span></span><br/>                         |



 

## <a name="requirements"></a><span data-ttu-id="da18e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="da18e-128">Requirements</span></span>



| <span data-ttu-id="da18e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="da18e-129">Requirement</span></span> | <span data-ttu-id="da18e-130">Value</span><span class="sxs-lookup"><span data-stu-id="da18e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da18e-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da18e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="da18e-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="da18e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da18e-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="da18e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="da18e-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="da18e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="da18e-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da18e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="da18e-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="da18e-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="da18e-137">IDL</span><span class="sxs-lookup"><span data-stu-id="da18e-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="da18e-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="da18e-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da18e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="da18e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da18e-140">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="da18e-140">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="da18e-141">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="da18e-141">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

