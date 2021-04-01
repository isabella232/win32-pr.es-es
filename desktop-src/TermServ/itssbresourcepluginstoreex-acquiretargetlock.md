---
title: ITsSbResourcePluginStoreEx AcquireTargetLock, método
description: Bloquea un destino.
ms.assetid: 76707f1d-1f13-4d81-8954-2acf05cda2cd
ms.tgt_platform: multiple
keywords:
- Método AcquireTargetLock Servicios de Escritorio remoto
- Método AcquireTargetLock Servicios de Escritorio remoto, interfaz ITsSbResourcePluginStoreEx
- Interfaz ITsSbResourcePluginStoreEx Servicios de Escritorio remoto, método AcquireTargetLock
topic_type:
- apiref
api_name:
- ITsSbResourcePluginStoreEx.AcquireTargetLock
api_location:
- SbTsV.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c18be0a544ebcea2d2cecb40dcea3a08e4bd35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150031"
---
# <a name="itssbresourcepluginstoreexacquiretargetlock-method"></a><span data-ttu-id="0965d-106">ITsSbResourcePluginStoreEx:: AcquireTargetLock (método)</span><span class="sxs-lookup"><span data-stu-id="0965d-106">ITsSbResourcePluginStoreEx::AcquireTargetLock method</span></span>

<span data-ttu-id="0965d-107">Bloquea un destino.</span><span class="sxs-lookup"><span data-stu-id="0965d-107">Locks a target.</span></span>

## <a name="syntax"></a><span data-ttu-id="0965d-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0965d-108">Syntax</span></span>


```C++
HRESULT AcquireTargetLock(
  [in]  BSTR     targetName,
  [in]  DWORD    dwTimeout,
  [out] IUnknown **ppContext
);
```



## <a name="parameters"></a><span data-ttu-id="0965d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0965d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0965d-110">*targetName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0965d-110">*targetName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0965d-111">Nombre del destino que se va a bloquear.</span><span class="sxs-lookup"><span data-stu-id="0965d-111">The name of the target to lock.</span></span>

</dd> <dt>

<span data-ttu-id="0965d-112">*dwTimeout* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0965d-112">*dwTimeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0965d-113">Tiempo de espera de la operación, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0965d-113">The timeout for the operation, in milliseconds.</span></span>

</dd> <dt>

<span data-ttu-id="0965d-114">*ppContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0965d-114">*ppContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0965d-115">Devuelve un puntero al contexto del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="0965d-115">Returns a pointer to the context of the lock.</span></span> <span data-ttu-id="0965d-116">Para liberar el bloqueo, suministre este puntero al método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) .</span><span class="sxs-lookup"><span data-stu-id="0965d-116">To release the lock, supply this pointer to the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0965d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0965d-117">Return value</span></span>

<span data-ttu-id="0965d-118">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="0965d-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0965d-119">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0965d-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0965d-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0965d-120">Remarks</span></span>

<span data-ttu-id="0965d-121">Una vez adquirido el bloqueo, se supone que el subproceso que realiza la llamada tiene acceso exclusivo al objeto de destino y, por tanto, ningún otro subproceso (dentro del mismo equipo) puede actualizarlo.</span><span class="sxs-lookup"><span data-stu-id="0965d-121">After the lock is acquired, the calling thread is assumed to have exclusive access to the target object and therefore no other thread (within the same machine) can update it.</span></span> <span data-ttu-id="0965d-122">Por lo tanto, el subproceso que realiza la llamada debe llamar al método [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) en cuanto haya realizado las actualizaciones necesarias en el objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="0965d-122">Therefore the calling thread must call the [**ReleaseTargetLock**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock) method as soon as it has made the necessary updates to the target object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0965d-123">Este bloqueo no impide que los objetos de destino se modifiquen externamente si existe más de un agente de conexión en la implementación.</span><span class="sxs-lookup"><span data-stu-id="0965d-123">this lock does not completely prevent target objects from being modified externally if more than one Connection Broker exists in the deployment.</span></span> <span data-ttu-id="0965d-124">El subproceso de llamada debe estar preparado para controlar un error correctamente y reintentar la actualización del destino.</span><span class="sxs-lookup"><span data-stu-id="0965d-124">The calling thread must be prepared to handle a failure gracefully and retry the target update.</span></span>

 

<span data-ttu-id="0965d-125">Este método está disponible en Windows Server 2012 R2 con [KB3091411](https://support.microsoft.com/kb/3091411) instalado en la interfaz [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) .</span><span class="sxs-lookup"><span data-stu-id="0965d-125">This method is available on Windows Server 2012 R2 with [KB3091411](https://support.microsoft.com/kb/3091411) installed in the [**ITsSbResourcePluginStoreEx**](itssbresourcepluginstoreex.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0965d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0965d-126">Requirements</span></span>



| <span data-ttu-id="0965d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0965d-127">Requirement</span></span> | <span data-ttu-id="0965d-128">Value</span><span class="sxs-lookup"><span data-stu-id="0965d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0965d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0965d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0965d-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0965d-130">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0965d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0965d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0965d-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0965d-132">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="0965d-133">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="0965d-133">End of server support</span></span><br/>    | <span data-ttu-id="0965d-134">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0965d-134">Windows Server 2012 R2</span></span><br/>                                                             |
| <span data-ttu-id="0965d-135">IDL</span><span class="sxs-lookup"><span data-stu-id="0965d-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0965d-136"><dt>SbTsV. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0965d-136"><dt>SbTsV.idl</dt></span></span> </dl>          |
| <span data-ttu-id="0965d-137">IID</span><span class="sxs-lookup"><span data-stu-id="0965d-137">IID</span></span><br/>                      | <span data-ttu-id="0965d-138">IID \_ ITsSbResourcePluginStoreEx se define como 80b83ffd-625d-11e5-bea1-a0481c7e9064</span><span class="sxs-lookup"><span data-stu-id="0965d-138">IID\_ITsSbResourcePluginStoreEx is defined as 80b83ffd-625d-11e5-bea1-a0481c7e9064</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0965d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0965d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0965d-140">**ITsSbResourcePluginStoreEx**</span><span class="sxs-lookup"><span data-stu-id="0965d-140">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> </dl>

 

 





