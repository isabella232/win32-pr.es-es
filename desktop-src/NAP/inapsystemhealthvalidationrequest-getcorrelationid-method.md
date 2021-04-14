---
title: Método INapSystemHealthValidationRequest GetCorrelationId (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) para recuperar el identificador de correlación. A continuación, el SHV debe registrar esta información.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Método GetCorrelationId NAP
- Método GetCorrelationId NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490360"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="38de1-107">INapSystemHealthValidationRequest:: GetCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="38de1-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="38de1-108">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="38de1-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="38de1-109">Los validadores de mantenimiento del sistema (SHV) usan el método **INapSystemHealthValidationRequest:: GetCorrelationId** para recuperar el identificador de correlación.</span><span class="sxs-lookup"><span data-stu-id="38de1-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="38de1-110">A continuación, el SHV debe registrar esta información.</span><span class="sxs-lookup"><span data-stu-id="38de1-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="38de1-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38de1-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="38de1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38de1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38de1-113">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="38de1-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38de1-114">Un puntero a un [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) único para el intercambio de SOH.</span><span class="sxs-lookup"><span data-stu-id="38de1-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38de1-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38de1-115">Return value</span></span>

<span data-ttu-id="38de1-116">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="38de1-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="38de1-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="38de1-117">Return code</span></span>                                                                                     | <span data-ttu-id="38de1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="38de1-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="38de1-119"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="38de1-120">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="38de1-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="38de1-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="38de1-122">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="38de1-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="38de1-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="38de1-124">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="38de1-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="38de1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38de1-125">Requirements</span></span>



| <span data-ttu-id="38de1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="38de1-126">Requirement</span></span> | <span data-ttu-id="38de1-127">Value</span><span class="sxs-lookup"><span data-stu-id="38de1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38de1-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38de1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38de1-129">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="38de1-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="38de1-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38de1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38de1-131">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="38de1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38de1-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38de1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="38de1-133"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="38de1-134">IDL</span><span class="sxs-lookup"><span data-stu-id="38de1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="38de1-135"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="38de1-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38de1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38de1-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38de1-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="38de1-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="38de1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38de1-139">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="38de1-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





