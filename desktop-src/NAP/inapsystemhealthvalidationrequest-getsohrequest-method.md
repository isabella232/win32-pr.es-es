---
title: Método INapSystemHealthValidationRequest GetSoHRequest (NapSystemHealthValidator. h)
description: Permite que los validadores de mantenimiento del sistema (SHV) recuperen y validen la información SoHRequest enviada por sus homólogos del agente de mantenimiento del sistema (SHA) en el cliente.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Método GetSoHRequest NAP
- Método GetSoHRequest NAP, interfaz INapSystemHealthValidationRequest
- Interfaz INapSystemHealthValidationRequest NAP, método GetSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151198"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="4fb37-106">INapSystemHealthValidationRequest:: GetSoHRequest (método)</span><span class="sxs-lookup"><span data-stu-id="4fb37-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="4fb37-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="4fb37-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4fb37-108">El método **INapSystemHealthValidationRequest:: GetSoHRequest** permite que los validadores de mantenimiento del sistema (SHV) recuperen y validen la información de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) enviada por sus homólogos del agente de mantenimiento del sistema (SHA) en el cliente.</span><span class="sxs-lookup"><span data-stu-id="4fb37-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb37-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fb37-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="4fb37-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fb37-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fb37-111">*sohRequest* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fb37-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb37-112">Un puntero a un puntero a una estructura [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="4fb37-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fb37-113">*napSystemGenerated* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fb37-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fb37-114">Valor **booleano** que es **true** si el SOH lo creó NAPAGENT en nombre de Sha y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="4fb37-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="4fb37-115">Se utiliza principalmente para indicar un error SHA en el SHV.</span><span class="sxs-lookup"><span data-stu-id="4fb37-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fb37-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fb37-116">Return value</span></span>

<span data-ttu-id="4fb37-117">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="4fb37-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4fb37-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4fb37-118">Return code</span></span>                                                                                     | <span data-ttu-id="4fb37-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fb37-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fb37-120"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4fb37-121">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="4fb37-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4fb37-122"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4fb37-123">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="4fb37-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4fb37-124"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4fb37-125">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="4fb37-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4fb37-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fb37-126">Remarks</span></span>

<span data-ttu-id="4fb37-127">El parámetro *sohRequest* puede devolver **null** si el cliente no envió un [**sohRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) al SHV.</span><span class="sxs-lookup"><span data-stu-id="4fb37-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="4fb37-128">En ese escenario, el SHV puede rellenar un **SoHResponse** con el código de error del [**\_ \_ \_ SOH que falta de NAP E**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="4fb37-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="4fb37-129">Si el parámetro *napSystemGenerated* es **true**, el formato de *SoHRequest* es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="4fb37-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="4fb37-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="4fb37-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="4fb37-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md) =  [ **failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="4fb37-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="4fb37-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md)  =  [ **<Sha-error-código>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="4fb37-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="4fb37-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fb37-133">Requirements</span></span>



| <span data-ttu-id="4fb37-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fb37-134">Requirement</span></span> | <span data-ttu-id="4fb37-135">Value</span><span class="sxs-lookup"><span data-stu-id="4fb37-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fb37-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb37-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4fb37-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4fb37-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="4fb37-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fb37-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4fb37-139">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fb37-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fb37-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4fb37-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fb37-141"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fb37-142">IDL</span><span class="sxs-lookup"><span data-stu-id="4fb37-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fb37-143"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="4fb37-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fb37-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fb37-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fb37-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="4fb37-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fb37-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fb37-147">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="4fb37-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





