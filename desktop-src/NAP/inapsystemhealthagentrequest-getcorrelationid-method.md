---
title: Método INapSystemHealthAgentRequest GetCorrelationId (NapSystemHealthAgent. h)
description: Lo utilizan los agentes de mantenimiento del sistema para correlacionar las respuestas de SoH y SoH.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Método GetCorrelationId NAP
- Método GetCorrelationId NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535602"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="f8748-106">INapSystemHealthAgentRequest:: GetCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="f8748-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="f8748-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f8748-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f8748-108">Los agentes de mantenimiento del sistema usan el método **INapSystemHealthAgentRequest:: GetCorrelationId** para correlacionar las respuestas del SOH y el SOH.</span><span class="sxs-lookup"><span data-stu-id="f8748-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8748-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8748-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="f8748-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8748-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8748-111">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f8748-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8748-112">Un puntero a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) único para el intercambio de SOH.</span><span class="sxs-lookup"><span data-stu-id="f8748-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8748-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f8748-113">Return value</span></span>

<span data-ttu-id="f8748-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="f8748-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f8748-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f8748-115">Return code</span></span>                                                                                     | <span data-ttu-id="f8748-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8748-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8748-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f8748-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="f8748-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f8748-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f8748-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="f8748-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f8748-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f8748-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="f8748-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f8748-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f8748-123">Requirements</span></span>



| <span data-ttu-id="f8748-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8748-124">Requirement</span></span> | <span data-ttu-id="f8748-125">Value</span><span class="sxs-lookup"><span data-stu-id="f8748-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8748-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8748-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f8748-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f8748-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f8748-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f8748-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f8748-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f8748-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f8748-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f8748-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8748-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f8748-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f8748-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8748-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f8748-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f8748-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8748-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8748-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="f8748-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8748-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8748-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="f8748-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





