---
title: Método GetStatus de IWMDRMIndividualizationStatus (wmdrmsdk. h)
description: El método GetStatus recupera información detallada sobre el progreso de la individualización.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Método GetStatus formato de Windows Media
- Método GetStatus formato de Windows Media, interfaz IWMDRMIndividualizationStatus
- Interfaz IWMDRMIndividualizationStatus formato de Windows Media, método GetStatus
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708897"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="991c6-106">IWMDRMIndividualizationStatus:: GetStatus (método)</span><span class="sxs-lookup"><span data-stu-id="991c6-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="991c6-107">El método **getStatus** recupera información detallada sobre el progreso de la individualización.</span><span class="sxs-lookup"><span data-stu-id="991c6-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="991c6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="991c6-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="991c6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="991c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991c6-110">*pStatus* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="991c6-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="991c6-111">Recibe una estructura de [**\_ \_ Estado de usuario de WM**](drmwm-individualize-status.md) que contiene información detallada sobre el estado del intento de individualización.</span><span class="sxs-lookup"><span data-stu-id="991c6-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991c6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="991c6-112">Return value</span></span>

<span data-ttu-id="991c6-113">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="991c6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="991c6-114">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="991c6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="991c6-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="991c6-115">Return code</span></span>                                                                          | <span data-ttu-id="991c6-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="991c6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="991c6-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="991c6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="991c6-118">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="991c6-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="991c6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="991c6-119">Remarks</span></span>

<span data-ttu-id="991c6-120">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="991c6-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="991c6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="991c6-121">Requirements</span></span>



| <span data-ttu-id="991c6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="991c6-122">Requirement</span></span> | <span data-ttu-id="991c6-123">Value</span><span class="sxs-lookup"><span data-stu-id="991c6-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="991c6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="991c6-124">Header</span></span><br/> | <dl> <span data-ttu-id="991c6-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="991c6-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991c6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="991c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991c6-127">**Interfaz IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="991c6-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





