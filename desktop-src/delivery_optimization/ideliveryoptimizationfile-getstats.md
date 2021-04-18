---
title: Método IDeliveryOptimizationFile Getstats ((Deliveryoptimization. h)
description: Devuelve las estadísticas de descarga y carga de un archivo específico.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (método)
- Método Getstats (, interfaz IDeliveryOptimizationFile
- Interfaz IDeliveryOptimizationFile, método Getstats (
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422528"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a><span data-ttu-id="36d6b-106">IDeliveryOptimizationFile:: Getstats ((método)</span><span class="sxs-lookup"><span data-stu-id="36d6b-106">IDeliveryOptimizationFile::GetStats method</span></span>

<span data-ttu-id="36d6b-107">Devuelve las estadísticas de descarga y carga de un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="36d6b-107">Returns download and upload stats for a specific file.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d6b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="36d6b-108">Syntax</span></span>


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a><span data-ttu-id="36d6b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="36d6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d6b-110">*swarmStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="36d6b-110">*swarmStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36d6b-111">Devuelve las estadísticas de descarga y carga de un archivo específico.</span><span class="sxs-lookup"><span data-stu-id="36d6b-111">Returns download and upload stats for a specific file.</span></span> <span data-ttu-id="36d6b-112">Para obtener más información, vea la estructura [**DOSwarmStats**](doswarmstats.md) .</span><span class="sxs-lookup"><span data-stu-id="36d6b-112">See the [**DOSwarmStats**](doswarmstats.md) structure for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d6b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="36d6b-113">Return value</span></span>

<span data-ttu-id="36d6b-114">Este método debe devolver **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="36d6b-114">This method should return **S_OK**.</span></span>

## <a name="requirements"></a><span data-ttu-id="36d6b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36d6b-115">Requirements</span></span>



| <span data-ttu-id="36d6b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="36d6b-116">Requirement</span></span> | <span data-ttu-id="36d6b-117">Value</span><span class="sxs-lookup"><span data-stu-id="36d6b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d6b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36d6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="36d6b-119">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="36d6b-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="36d6b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="36d6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="36d6b-121">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="36d6b-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="36d6b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="36d6b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="36d6b-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d6b-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="36d6b-124">IDL</span><span class="sxs-lookup"><span data-stu-id="36d6b-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36d6b-125"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36d6b-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="36d6b-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36d6b-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="36d6b-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36d6b-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="36d6b-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="36d6b-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d6b-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d6b-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="36d6b-130">IID</span><span class="sxs-lookup"><span data-stu-id="36d6b-130">IID</span></span><br/>                      | <span data-ttu-id="36d6b-131">IID_IDeliveryOptimizationFile se define como B76B9699-E99E-4101-803F-A20E325D93E2</span><span class="sxs-lookup"><span data-stu-id="36d6b-131">IID_IDeliveryOptimizationFile is defined as B76B9699-E99E-4101-803F-A20E325D93E2</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="36d6b-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="36d6b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d6b-133">**IDeliveryOptimizationFile**</span><span class="sxs-lookup"><span data-stu-id="36d6b-133">**IDeliveryOptimizationFile**</span></span>](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





