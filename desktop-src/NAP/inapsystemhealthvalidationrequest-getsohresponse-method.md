---
title: Método INapSystemHealthValidationRequest GetSoHResponse (NapSystemHealthValidator. h)
description: Recupera el SoHResponse.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Método GetSoHResponse NAP
- Método GetSoHResponse NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetSoHResponse
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676947"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="23422-106">INapSystemHealthValidationRequest:: GetSoHResponse (método)</span><span class="sxs-lookup"><span data-stu-id="23422-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="23422-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="23422-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="23422-108">El método **INapSystemHealthValidationRequest:: GetSoHResponse** recupera [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="23422-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="23422-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23422-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="23422-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="23422-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23422-111">*sohResponse* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="23422-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23422-112">Un puntero a un puntero al [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh)recibido.</span><span class="sxs-lookup"><span data-stu-id="23422-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23422-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="23422-113">Return value</span></span>

<span data-ttu-id="23422-114">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="23422-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="23422-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="23422-115">Return code</span></span>                                                                                     | <span data-ttu-id="23422-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="23422-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="23422-117"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="23422-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="23422-118">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="23422-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="23422-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="23422-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="23422-120">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="23422-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="23422-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="23422-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="23422-122">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="23422-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="23422-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23422-123">Requirements</span></span>



| <span data-ttu-id="23422-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="23422-124">Requirement</span></span> | <span data-ttu-id="23422-125">Value</span><span class="sxs-lookup"><span data-stu-id="23422-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23422-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23422-126">Minimum supported client</span></span><br/> | <span data-ttu-id="23422-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="23422-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="23422-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23422-128">Minimum supported server</span></span><br/> | <span data-ttu-id="23422-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="23422-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23422-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23422-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="23422-131"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="23422-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="23422-132">IDL</span><span class="sxs-lookup"><span data-stu-id="23422-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23422-133"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23422-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="23422-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="23422-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23422-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23422-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="23422-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="23422-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23422-137">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="23422-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





