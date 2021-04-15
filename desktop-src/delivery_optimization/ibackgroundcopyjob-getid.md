---
title: Método GetId IBackgroundCopyJob (Deliveryoptimization. h)
description: Recupera el identificador usado para identificar el trabajo en la cola.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (método)
- Método GetId, interfaz IBackgroundCopyJob
- Interfaz IBackgroundCopyJob, método GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695934"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="63bdb-106">IBackgroundCopyJob:: GetId (método)</span><span class="sxs-lookup"><span data-stu-id="63bdb-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="63bdb-107">Recupera el identificador usado para identificar el trabajo en la cola.</span><span class="sxs-lookup"><span data-stu-id="63bdb-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="63bdb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63bdb-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="63bdb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63bdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63bdb-110">*pJobID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="63bdb-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63bdb-111">GUID que identifica el trabajo en la cola de tareas.</span><span class="sxs-lookup"><span data-stu-id="63bdb-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63bdb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63bdb-112">Return value</span></span>

<span data-ttu-id="63bdb-113">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de **HRESULT** de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="63bdb-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="63bdb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63bdb-114">Remarks</span></span>

<span data-ttu-id="63bdb-115">El servicio genera el identificador al [crear](ibackgroundcopymanager-createjob.md) el trabajo.</span><span class="sxs-lookup"><span data-stu-id="63bdb-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="63bdb-116">Para usar el identificador con el fin de recuperar un puntero de la interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) para el trabajo, llame al método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .</span><span class="sxs-lookup"><span data-stu-id="63bdb-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="63bdb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63bdb-117">Requirements</span></span>



| <span data-ttu-id="63bdb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="63bdb-118">Requirement</span></span> | <span data-ttu-id="63bdb-119">Value</span><span class="sxs-lookup"><span data-stu-id="63bdb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63bdb-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63bdb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="63bdb-121">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="63bdb-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="63bdb-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63bdb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="63bdb-123">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="63bdb-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="63bdb-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63bdb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="63bdb-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="63bdb-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="63bdb-126">IDL</span><span class="sxs-lookup"><span data-stu-id="63bdb-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63bdb-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63bdb-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="63bdb-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63bdb-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="63bdb-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63bdb-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="63bdb-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63bdb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63bdb-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63bdb-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="63bdb-132">IID</span><span class="sxs-lookup"><span data-stu-id="63bdb-132">IID</span></span><br/>                      | <span data-ttu-id="63bdb-133">IID_IBackgroundCopyJob se define como 37668D37-507E-4160-9316-26306D150B12</span><span class="sxs-lookup"><span data-stu-id="63bdb-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="63bdb-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="63bdb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63bdb-135">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="63bdb-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="63bdb-136">**IBackgroundCopyManager:: CreateJob**</span><span class="sxs-lookup"><span data-stu-id="63bdb-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="63bdb-137">**IBackgroundCopyManager::GetJob**</span><span class="sxs-lookup"><span data-stu-id="63bdb-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





