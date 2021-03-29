---
title: IWMPEvents4 SyncEstimationComplete, método
description: El evento SyncEstimationComplete se produce cuando se completa una estimación de tamaño, iniciada anteriormente por IWMPSyncDevice3 estimateSyncSize.
ms.assetid: 2fb45a13-d82b-48b6-b9bb-46409f33a33f
keywords:
- Método SyncEstimationComplete de Windows Media Player
- Método SyncEstimationComplete Windows Media Player, interfaz IWMPEvents4
- Interfaz IWMPEvents4 Windows Media Player, método SyncEstimationComplete
topic_type:
- apiref
api_name:
- IWMPEvents4.SyncEstimationComplete
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 209ed2f2bd0f075dbaa8d442a276c994d50ce2e5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788679"
---
# <a name="iwmpevents4syncestimationcomplete-method"></a><span data-ttu-id="7f4e9-106">IWMPEvents4:: SyncEstimationComplete (método)</span><span class="sxs-lookup"><span data-stu-id="7f4e9-106">IWMPEvents4::SyncEstimationComplete method</span></span>

<span data-ttu-id="7f4e9-107">El evento **SyncEstimationComplete** se produce cuando se completa una estimación de tamaño, iniciada anteriormente por [**IWMPSyncDevice3:: estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize).</span><span class="sxs-lookup"><span data-stu-id="7f4e9-107">The **SyncEstimationComplete** event occurs when a size estimation, previously initiated by [**IWMPSyncDevice3::estimateSyncSize**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize), is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f4e9-108">Syntax</span></span>


```C++
void SyncEstimationComplete(
  [in] IWMPSyncDevice *pDevice,
  [in] long           hrResult,
  [in] long           lEstimatedUsedSpace,
  [in] long           lEstimatedSize
);
```



## <a name="parameters"></a><span data-ttu-id="7f4e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f4e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f4e9-110">*pDevice* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f4e9-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f4e9-111">Puntero a la interfaz [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) que representa el dispositivo para el que se inició la estimación del tamaño.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-111">Pointer to the [**IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice) interface that represents the device for which the size estimation was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="7f4e9-112">*hrResult* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f4e9-112">*hrResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f4e9-113">Valor que indica si la estimación se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-113">A value that indicates the success or failure of the estimation.</span></span>



| <span data-ttu-id="7f4e9-114">Value</span><span class="sxs-lookup"><span data-stu-id="7f4e9-114">Value</span></span>                                                                                                                                       | <span data-ttu-id="7f4e9-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7f4e9-115">Meaning</span></span>                                |
|---------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <span data-ttu-id="7f4e9-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4e9-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7f4e9-117">La estimación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-117">The estimation succeeded.</span></span><br/>   |
| <span id="E_ABORT"></span><span id="e_abort"></span><dl> <span data-ttu-id="7f4e9-118"><dt>**E \_ anular**</dt></span><span class="sxs-lookup"><span data-stu-id="7f4e9-118"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="7f4e9-119">Se anuló la estimación.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-119">The estimation was aborted.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7f4e9-120">*lEstimatedUsedSpace* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f4e9-120">*lEstimatedUsedSpace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f4e9-121">Espacio Estimado (en bytes) que se utilizaría en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-121">The estimated space (in bytes) that would be used on the device.</span></span>

</dd> <dt>

<span data-ttu-id="7f4e9-122">*lEstimatedSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7f4e9-122">*lEstimatedSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f4e9-123">Tamaño estimado (en bytes) de los datos que se van a sincronizar.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-123">The estimated size (in bytes) of the data to be synchronized.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f4e9-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7f4e9-124">Return value</span></span>

<span data-ttu-id="7f4e9-125">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="7f4e9-125">This method does not return a value.</span></span>

## <a name="see-also"></a><span data-ttu-id="7f4e9-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f4e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f4e9-127">**Interfaz IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="7f4e9-127">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
</dt> <dt>

[<span data-ttu-id="7f4e9-128">**IWMPSyncDevice3::estimateSyncSize**</span><span class="sxs-lookup"><span data-stu-id="7f4e9-128">**IWMPSyncDevice3::estimateSyncSize**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice3-estimatesyncsize)
</dt> </dl>

 

 





