---
title: Interfaz INapSystemHealthAgentRequest (NapSystemHealthAgent. h)
description: Los Sha usan para comunicarse y coordinar el procesamiento con el sistema NAP.
ms.assetid: 424e0fb7-cce7-4b75-b474-fda0e053284e
keywords:
- Interfaz INapSystemHealthAgentRequest NAP
- Interfaz INapSystemHealthAgentRequest NAP, descripción
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a4e79e2a6347ebffec37595d4ca86b100830047
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534090"
---
# <a name="inapsystemhealthagentrequest-interface"></a><span data-ttu-id="a9c85-105">Interfaz INapSystemHealthAgentRequest</span><span class="sxs-lookup"><span data-stu-id="a9c85-105">INapSystemHealthAgentRequest interface</span></span>

> [!Note]  
> <span data-ttu-id="a9c85-106">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a9c85-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a9c85-107">La interfaz **INapSystemHealthAgentRequest** proporciona métodos que los Sha usan para comunicarse y coordinar el procesamiento con el sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="a9c85-107">The **INapSystemHealthAgentRequest** interface provides methods that SHAs use to communicate and coordinate processing with the NAP system.</span></span>

## <a name="members"></a><span data-ttu-id="a9c85-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a9c85-108">Members</span></span>

<span data-ttu-id="a9c85-109">La interfaz **INapSystemHealthAgentRequest** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a9c85-109">The **INapSystemHealthAgentRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a9c85-110">**INapSystemHealthAgentRequest** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a9c85-110">**INapSystemHealthAgentRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="a9c85-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9c85-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a9c85-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a9c85-112">Methods</span></span>

<span data-ttu-id="a9c85-113">La interfaz **INapSystemHealthAgentRequest** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="a9c85-113">The **INapSystemHealthAgentRequest** interface has these methods.</span></span>



| <span data-ttu-id="a9c85-114">Método</span><span class="sxs-lookup"><span data-stu-id="a9c85-114">Method</span></span>                                                                                                                     | <span data-ttu-id="a9c85-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c85-115">Description</span></span>                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9c85-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span><span class="sxs-lookup"><span data-stu-id="a9c85-116">**INapSystemHealthAgentRequest::GetCacheSoHFlag**</span></span>](inapsystemhealthagentrequest-getcachesohflag-method.md)               | <span data-ttu-id="a9c85-117">Solo lo usa el NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a9c85-117">Used only by the NapAgent.</span></span><br/>                                                            |
| [<span data-ttu-id="a9c85-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="a9c85-118">**INapSystemHealthAgentRequest::GetCorrelationId**</span></span>](inapsystemhealthagentrequest-getcorrelationid-method.md)             | <span data-ttu-id="a9c85-119">Lo usan los agentes de mantenimiento del sistema para correlacionar SOH y [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a9c85-119">Used by system health agents to correlate SoHs and [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/> |
| [<span data-ttu-id="a9c85-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="a9c85-120">**INapSystemHealthAgentRequest::GetSoHRequest**</span></span>](inapsystemhealthagentrequest-getsohrequest-method.md)                   | <span data-ttu-id="a9c85-121">Lo usan los Sha para obtener SOH previamente almacenados en caché por NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a9c85-121">Used by SHAs to get SoHs previously cached by the NapAgent.</span></span><br/>                           |
| [<span data-ttu-id="a9c85-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span><span class="sxs-lookup"><span data-stu-id="a9c85-122">**INapSystemHealthAgentRequest::GetSoHResponse**</span></span>](inapsystemhealthagentrequest-getsohresponse-method.md)                 | <span data-ttu-id="a9c85-123">Lo usa el agente de mantenimiento para recuperar sus [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="a9c85-123">Used by the health agent to retrieve their [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span><br/>         |
| [<span data-ttu-id="a9c85-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span><span class="sxs-lookup"><span data-stu-id="a9c85-124">**INapSystemHealthAgentRequest::GetStringCorrelationId**</span></span>](inapsystemhealthagentrequest-getstringcorrelationid-method.md) | <span data-ttu-id="a9c85-125">Lo utilizan los agentes de mantenimiento del sistema para registrar el identificador de correlación.</span><span class="sxs-lookup"><span data-stu-id="a9c85-125">Used by system health agents to log the correlation ID.</span></span><br/>                               |
| [<span data-ttu-id="a9c85-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span><span class="sxs-lookup"><span data-stu-id="a9c85-126">**INapSystemHealthAgentRequest::SetSoHRequest**</span></span>](inapsystemhealthagentrequest-setsohrequest-method.md)                   | <span data-ttu-id="a9c85-127">Lo usan los agentes de mantenimiento para escribir su solicitud de SoH.</span><span class="sxs-lookup"><span data-stu-id="a9c85-127">Used by health agents to write their SoH request.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a9c85-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9c85-128">Requirements</span></span>



| <span data-ttu-id="a9c85-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c85-129">Requirement</span></span> | <span data-ttu-id="a9c85-130">Value</span><span class="sxs-lookup"><span data-stu-id="a9c85-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c85-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c85-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a9c85-132">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a9c85-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a9c85-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a9c85-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a9c85-134">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a9c85-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a9c85-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a9c85-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9c85-136"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c85-136"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9c85-137">IDL</span><span class="sxs-lookup"><span data-stu-id="a9c85-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a9c85-138"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a9c85-138"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="a9c85-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a9c85-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9c85-140"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9c85-140"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="a9c85-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9c85-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c85-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="a9c85-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a9c85-143">Referencia de NAP</span><span class="sxs-lookup"><span data-stu-id="a9c85-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

