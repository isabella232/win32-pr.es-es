---
title: INapEnforcementClientBinding método UnInitialize (NapEnforcementClient. h)
description: Concluye el servicio NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Anular la inicialización del método NAP
- Método uninitial NAP, interfaz INapEnforcementClientBinding
- Interfaz INapEnforcementClientBinding NAP, método UnInitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4132ff1a498a598483758623a588fa26e8b75021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666085"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a><span data-ttu-id="c47dc-106">INapEnforcementClientBinding:: UnInitialize (método)</span><span class="sxs-lookup"><span data-stu-id="c47dc-106">INapEnforcementClientBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="c47dc-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c47dc-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c47dc-108">El método **INapEnforcementClientBinding:: UnInitialize** termina el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="c47dc-108">The **INapEnforcementClientBinding::Uninitialize** method concludes the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="c47dc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c47dc-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="c47dc-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c47dc-110">Parameters</span></span>

<span data-ttu-id="c47dc-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c47dc-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c47dc-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c47dc-112">Return value</span></span>

<span data-ttu-id="c47dc-113">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="c47dc-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c47dc-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c47dc-114">Return code</span></span>                                                                                     | <span data-ttu-id="c47dc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c47dc-115">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c47dc-116"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-116"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c47dc-117">La operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c47dc-117">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c47dc-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c47dc-119">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c47dc-119">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c47dc-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c47dc-121">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="c47dc-121">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c47dc-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c47dc-122">Remarks</span></span>

<span data-ttu-id="c47dc-123">El NapAgent bloquea el procesamiento hasta que se completen todas las llamadas existentes en las interfaces [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) y [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="c47dc-123">The NapAgent blocks further processing until all existing calls on the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) and [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interfaces complete.</span></span> <span data-ttu-id="c47dc-124">Al final de esta llamada, NapAgent libera todas sus referencias en punteros COM del cliente de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="c47dc-124">At the end of this call, the NapAgent releases all its references on enforcement client COM pointers.</span></span>

<span data-ttu-id="c47dc-125">Antes de llamar a esta función, el exigidor debe llamar a [**INapEnforcementClientBinding:: NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) en todas las conexiones activas, por lo que se puede notificar a los Sha si alguno de sus SoH-Requests fuera huérfano.</span><span class="sxs-lookup"><span data-stu-id="c47dc-125">Before this function is called, the enforcer must call [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) on all its active connections, so the SHAs can be notified if any of their SoH-Requests were orphaned.</span></span>

<span data-ttu-id="c47dc-126">El cliente de cumplimiento debe llamar al método [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) antes de llamar a este o a cualquier otro método de la interfaz [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="c47dc-126">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="c47dc-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c47dc-127">Requirements</span></span>



| <span data-ttu-id="c47dc-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c47dc-128">Requirement</span></span> | <span data-ttu-id="c47dc-129">Value</span><span class="sxs-lookup"><span data-stu-id="c47dc-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c47dc-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c47dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c47dc-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c47dc-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c47dc-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c47dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c47dc-133">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c47dc-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c47dc-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c47dc-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c47dc-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c47dc-136">IDL</span><span class="sxs-lookup"><span data-stu-id="c47dc-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c47dc-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="c47dc-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c47dc-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c47dc-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c47dc-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c47dc-140">See also</span></span>

<dl> <span data-ttu-id="c47dc-141"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c47dc-141"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c47dc-142">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="c47dc-142">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="c47dc-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span><span class="sxs-lookup"><span data-stu-id="c47dc-143">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[<span data-ttu-id="c47dc-144">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="c47dc-144">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





