---
title: Método INapSystemHealthValidationRequest GetStringCorrelationId (NapSystemHealthValidator. h)
description: Lo usan los validadores de mantenimiento del sistema (SHV) que deben registrar esta información.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Método GetStringCorrelationId NAP
- Método GetStringCorrelationId NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535524"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="55eb3-106">INapSystemHealthValidationRequest:: GetStringCorrelationId (método)</span><span class="sxs-lookup"><span data-stu-id="55eb3-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="55eb3-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="55eb3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="55eb3-108">Los validadores de mantenimiento del sistema (SHV) que deben registrar esta información usan el método **INapSystemHealthValidationRequest:: GetStringCorrelationId** .</span><span class="sxs-lookup"><span data-stu-id="55eb3-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="55eb3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55eb3-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="55eb3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55eb3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55eb3-111">*CorrelationId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="55eb3-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="55eb3-112">Un puntero a un puntero a un [**StringCorrelationId**](nap-type-constants.md) único para el intercambio de SOH.</span><span class="sxs-lookup"><span data-stu-id="55eb3-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55eb3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55eb3-113">Return value</span></span>

<span data-ttu-id="55eb3-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="55eb3-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="55eb3-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="55eb3-115">Return code</span></span>                                                                                     | <span data-ttu-id="55eb3-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="55eb3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="55eb3-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="55eb3-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="55eb3-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="55eb3-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="55eb3-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="55eb3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="55eb3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="55eb3-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="55eb3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="55eb3-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55eb3-123">Requirements</span></span>



| <span data-ttu-id="55eb3-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="55eb3-124">Requirement</span></span> | <span data-ttu-id="55eb3-125">Value</span><span class="sxs-lookup"><span data-stu-id="55eb3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55eb3-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55eb3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="55eb3-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55eb3-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="55eb3-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55eb3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="55eb3-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="55eb3-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55eb3-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55eb3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="55eb3-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="55eb3-132">IDL</span><span class="sxs-lookup"><span data-stu-id="55eb3-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55eb3-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="55eb3-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55eb3-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55eb3-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55eb3-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="55eb3-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="55eb3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55eb3-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="55eb3-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





