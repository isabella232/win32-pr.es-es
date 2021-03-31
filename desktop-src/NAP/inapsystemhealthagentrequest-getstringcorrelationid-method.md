---
title: Método INapSystemHealthAgentRequest GetStringCorrelationId (NapSystemHealthAgent. h)
description: Lo utilizan los agentes de mantenimiento del sistema para registrar el identificador de correlación.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interfaz INapSystemHealthAgentRequest
- Interfaz INapSystemHealthAgentRequest NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801831"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="8ec6f-106">INapSystemHealthAgentRequest:: GetStringCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="8ec6f-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="8ec6f-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8ec6f-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8ec6f-108">Los agentes de mantenimiento del sistema usan el método **INapSystemHealthAgentRequest:: GetStringCorrelationId** para registrar el identificador de correlación.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec6f-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ec6f-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="8ec6f-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ec6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec6f-111">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="8ec6f-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec6f-112">Un puntero a un puntero a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) único para este intercambio de SOH.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec6f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec6f-113">Return value</span></span>

<span data-ttu-id="8ec6f-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8ec6f-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ec6f-115">Return code</span></span>                                                                                     | <span data-ttu-id="8ec6f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ec6f-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ec6f-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8ec6f-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8ec6f-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8ec6f-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8ec6f-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8ec6f-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="8ec6f-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ec6f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ec6f-123">Requirements</span></span>



| <span data-ttu-id="8ec6f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ec6f-124">Requirement</span></span> | <span data-ttu-id="8ec6f-125">Value</span><span class="sxs-lookup"><span data-stu-id="8ec6f-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec6f-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec6f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec6f-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8ec6f-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8ec6f-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ec6f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec6f-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ec6f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8ec6f-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ec6f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec6f-131"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ec6f-132">IDL</span><span class="sxs-lookup"><span data-stu-id="8ec6f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ec6f-133"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ec6f-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ec6f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ec6f-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ec6f-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="8ec6f-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ec6f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec6f-137">**INapSystemHealthAgentRequest**</span><span class="sxs-lookup"><span data-stu-id="8ec6f-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





