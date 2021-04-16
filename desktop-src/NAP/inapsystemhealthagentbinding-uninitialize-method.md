---
title: INapSystemHealthAgentBinding método UnInitialize (NapSystemHealthAgent. h)
description: Hace que el NapAgent libere todas sus referencias a punteros COM del agente de mantenimiento del sistema.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Anular la inicialización del método NAP
- Método uninitial NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método UnInitialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676791"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="6d444-106">INapSystemHealthAgentBinding:: UnInitialize (método)</span><span class="sxs-lookup"><span data-stu-id="6d444-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="6d444-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6d444-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6d444-108">El método **INapSystemHealthAgentBinding:: UnInitialize** hace que NapAgent libere todas sus referencias a punteros com del agente de mantenimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="6d444-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d444-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6d444-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="6d444-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6d444-110">Parameters</span></span>

<span data-ttu-id="6d444-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6d444-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d444-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6d444-112">Return value</span></span>

<span data-ttu-id="6d444-113">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="6d444-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6d444-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6d444-114">Return code</span></span>                                                                                             | <span data-ttu-id="6d444-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6d444-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d444-116"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="6d444-117">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="6d444-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6d444-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="6d444-119">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="6d444-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="6d444-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="6d444-121">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="6d444-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="6d444-122"><dt>**NAP \_ E \_ no \_ inicializado**</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="6d444-123">SHA no se ha inicializado previamente.</span><span class="sxs-lookup"><span data-stu-id="6d444-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="6d444-124"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="6d444-125">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="6d444-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="6d444-126">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="6d444-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6d444-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d444-127">Remarks</span></span>

<span data-ttu-id="6d444-128">La NapAgent bloquea la ejecución de esta llamada al método hasta que se completen todas las llamadas existentes en las interfaces de enlace y devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="6d444-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="6d444-129">SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="6d444-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d444-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d444-130">Requirements</span></span>



| <span data-ttu-id="6d444-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d444-131">Requirement</span></span> | <span data-ttu-id="6d444-132">Value</span><span class="sxs-lookup"><span data-stu-id="6d444-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d444-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d444-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6d444-134">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="6d444-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d444-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d444-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6d444-136">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d444-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6d444-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6d444-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d444-138"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="6d444-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6d444-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d444-140"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="6d444-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6d444-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d444-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d444-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6d444-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d444-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d444-144">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="6d444-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





