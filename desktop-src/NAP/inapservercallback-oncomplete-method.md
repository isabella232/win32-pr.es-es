---
title: Método INapServerCallback (NapSystemHealthValidator. h)
description: Lo usan los SHV para indicar la finalización de la solicitud asincrónica.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Método alcomplete NAP
- Método alcomplete NAP, interfaz INapServerCallback
- Interfaz INapServerCallback NAP, método alcomplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493235"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="ab620-106">INapServerCallback:: alcomplete (método)</span><span class="sxs-lookup"><span data-stu-id="ab620-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="ab620-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ab620-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ab620-108">Los SHV usan el método **INapServerCallback:: alcomplete** para indicar la finalización de la solicitud asincrónica.</span><span class="sxs-lookup"><span data-stu-id="ab620-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab620-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab620-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="ab620-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab620-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab620-111">*solicitud* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ab620-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab620-112">Un puntero a un objeto [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) que representa una solicitud de validación.</span><span class="sxs-lookup"><span data-stu-id="ab620-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="ab620-113">*ErrorCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab620-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab620-114">Un [**código de error de NAP**](nap-error-constants.md) que indica el motivo por el que no se pudo realizar la validación.</span><span class="sxs-lookup"><span data-stu-id="ab620-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="ab620-115">Normalmente, el valor devuelto del método [**INapSystemHealthValidationRequest:: SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) se pasa a este parámetro.</span><span class="sxs-lookup"><span data-stu-id="ab620-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="ab620-116">Sin embargo, si no se pudo llamar a **SetSoHResponse** debido a un error de reprocesamiento, se pasa el valor devuelto por el comando con errores.</span><span class="sxs-lookup"><span data-stu-id="ab620-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab620-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab620-117">Return value</span></span>

<span data-ttu-id="ab620-118">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="ab620-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ab620-119">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ab620-119">Return code</span></span>                                                                                     | <span data-ttu-id="ab620-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab620-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab620-121"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ab620-122">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab620-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ab620-123"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ab620-124">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="ab620-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ab620-125"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ab620-126">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="ab620-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ab620-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab620-127">Remarks</span></span>

<span data-ttu-id="ab620-128">Los validadores deben devolver los valores \_ correctos si se pudo completar la validación de [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) , independientemente de si el **SoHRequest** ha superado la comprobación de estado.</span><span class="sxs-lookup"><span data-stu-id="ab620-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab620-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab620-129">Requirements</span></span>



| <span data-ttu-id="ab620-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab620-130">Requirement</span></span> | <span data-ttu-id="ab620-131">Value</span><span class="sxs-lookup"><span data-stu-id="ab620-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab620-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab620-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ab620-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="ab620-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="ab620-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab620-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ab620-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab620-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ab620-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab620-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab620-137"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab620-138">IDL</span><span class="sxs-lookup"><span data-stu-id="ab620-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab620-139"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="ab620-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab620-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab620-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab620-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="ab620-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab620-142">See also</span></span>

<dl> <span data-ttu-id="ab620-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ab620-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ab620-144">**INapServerCallback**</span><span class="sxs-lookup"><span data-stu-id="ab620-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="ab620-145">**INapSystemHealthValidationRequest**</span><span class="sxs-lookup"><span data-stu-id="ab620-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





