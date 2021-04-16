---
title: Método ExecuteKCC de la clase MSAD_DomainController
description: Llama a la función DsReplicaConsistencyCheck, que invoca el comprobador de coherencia de la información (KCC) para comprobar la topología de replicación.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Método ExecuteKCC Active Directory
- Método ExecuteKCC Active Directory, clase MSAD_DomainController
- MSAD_DomainController de clase Active Directory, método ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658241"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a><span data-ttu-id="e0fbe-106">Método ExecuteKCC de la \_ clase MSAD DomainController</span><span class="sxs-lookup"><span data-stu-id="e0fbe-106">ExecuteKCC method of the MSAD\_DomainController class</span></span>

<span data-ttu-id="e0fbe-107">Llama a la función [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , que invoca el comprobador de coherencia de la información (KCC) para comprobar la topología de replicación.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-107">Calls the [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) function, which invokes the Knowledge Consistency Checker (KCC) to verify the replication topology.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fbe-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e0fbe-108">Syntax</span></span>


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e0fbe-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0fbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0fbe-110">*TaskID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0fbe-110">*TaskID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbe-111">Tarea que el KCC debe ejecutar.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-111">The task that the KCC should execute.</span></span> <span data-ttu-id="e0fbe-112">**DS \_ La \_ \_ \_ topología de actualización de TASKID de KCC** es el único valor que se admite actualmente.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-112">**DS\_KCC\_TASKID\_UPDATE\_TOPOLOGY** is the only value that is currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="e0fbe-113">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e0fbe-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0fbe-114">Un conjunto de marcas que modifican el comportamiento del método **ExecuteKCC** .</span><span class="sxs-lookup"><span data-stu-id="e0fbe-114">A set of flags that modify the behavior of the **ExecuteKCC** method.</span></span> <span data-ttu-id="e0fbe-115">Este parámetro puede ser cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-115">This parameter can be zero or a combination of one or more of the following values.</span></span>

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span data-ttu-id="e0fbe-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**marca de KCC de DS \_ \_ \_ \_ OP asincrónica**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-116"><span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS\_KCC\_FLAG\_ASYNC\_OP**</span></span>


</dt> <dd>

<span data-ttu-id="e0fbe-117">La tarea se pone en cola y, a continuación, la función devuelve sin esperar a que se complete la tarea.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-117">The task is queued and then the function returns without waiting for the task to complete.</span></span>

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span data-ttu-id="e0fbe-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**marca de KCC de DS \_ \_ \_ atenuada**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-118"><span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**DS\_KCC\_FLAG\_DAMPED**</span></span>


</dt> <dd>

<span data-ttu-id="e0fbe-119">La tarea no se agregará a la cola si otra tarea en cola se ejecutará pronto.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-119">The task will not be added to the queue if another queued task will run soon.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0fbe-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0fbe-120">Return value</span></span>

<span data-ttu-id="e0fbe-121">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e0fbe-121">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fbe-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0fbe-122">Requirements</span></span>



| <span data-ttu-id="e0fbe-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fbe-123">Requirement</span></span> | <span data-ttu-id="e0fbe-124">Value</span><span class="sxs-lookup"><span data-stu-id="e0fbe-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fbe-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0fbe-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fbe-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e0fbe-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e0fbe-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0fbe-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fbe-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0fbe-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0fbe-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e0fbe-129">Namespace</span></span><br/>                | <span data-ttu-id="e0fbe-130">\\MicrosoftActiveDirectory raíz</span><span class="sxs-lookup"><span data-stu-id="e0fbe-130">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="e0fbe-131">MOF</span><span class="sxs-lookup"><span data-stu-id="e0fbe-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0fbe-132"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0fbe-132"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0fbe-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e0fbe-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0fbe-134"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fbe-134"><dt>Replprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fbe-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0fbe-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fbe-136">**MSAD \_ DomainController**</span><span class="sxs-lookup"><span data-stu-id="e0fbe-136">**MSAD\_DomainController**</span></span>](msad-domaincontroller.md)
</dt> </dl>

 

 





