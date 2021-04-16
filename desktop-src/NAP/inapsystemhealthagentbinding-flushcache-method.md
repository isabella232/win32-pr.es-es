---
title: Método INapSystemHealthAgentBinding FlushCache (NapSystemHealthAgent. h)
description: Un SHA llama a para vaciar su caché de SoH.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Método FlushCache NAP
- Método FlushCache NAP, interfaz INapSystemHealthAgentBinding
- Interfaz INapSystemHealthAgentBinding NAP, método FlushCache
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676553"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="5e7f8-106">INapSystemHealthAgentBinding:: FlushCache (método)</span><span class="sxs-lookup"><span data-stu-id="5e7f8-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="5e7f8-107">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5e7f8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5e7f8-108">Un SHA llama al método **INapSystemHealthAgentBinding:: FlushCache** para vaciar su caché de SOH.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e7f8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e7f8-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="5e7f8-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e7f8-110">Parameters</span></span>

<span data-ttu-id="5e7f8-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e7f8-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e7f8-112">Return value</span></span>

<span data-ttu-id="5e7f8-113">También se pueden devolver otros códigos de error específicos de COM.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5e7f8-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="5e7f8-114">Return code</span></span>                                                                                         | <span data-ttu-id="5e7f8-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e7f8-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e7f8-116"><dt>**S \_ Aceptar**</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="5e7f8-117">Operación realizada correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="5e7f8-118"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="5e7f8-119">Error de permisos, acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="5e7f8-120"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="5e7f8-121">Límite de recursos del sistema, no se pudo realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5e7f8-122"><dt>**RPC \_ E \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5e7f8-123">NapAgent se ha detenido.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="5e7f8-124">Este objeto se recuperará automáticamente y se volverá a enlazar a NapAgent, una vez que se reinicie.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5e7f8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e7f8-125">Remarks</span></span>

<span data-ttu-id="5e7f8-126">NapAgent mantiene una memoria caché de SOH recientes proporcionadas por diferentes Sha.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="5e7f8-127">Esta caché es útil para optimizar el rendimiento en tiempo de arranque, cuando se puede enlazar Sha o no al sistema.</span><span class="sxs-lookup"><span data-stu-id="5e7f8-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="5e7f8-128">SHA debe llamar a [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) antes de llamar a este método o a cualquier otro método de la interfaz [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .</span><span class="sxs-lookup"><span data-stu-id="5e7f8-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e7f8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e7f8-129">Requirements</span></span>



| <span data-ttu-id="5e7f8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e7f8-130">Requirement</span></span> | <span data-ttu-id="5e7f8-131">Value</span><span class="sxs-lookup"><span data-stu-id="5e7f8-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e7f8-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e7f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5e7f8-133">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5e7f8-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5e7f8-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e7f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5e7f8-135">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e7f8-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5e7f8-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e7f8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e7f8-137"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e7f8-138">IDL</span><span class="sxs-lookup"><span data-stu-id="5e7f8-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e7f8-139"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e7f8-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e7f8-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e7f8-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e7f8-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5e7f8-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e7f8-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e7f8-143">**INapSystemHealthAgentBinding**</span><span class="sxs-lookup"><span data-stu-id="5e7f8-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





