---
title: Método IBackgroundCopyJob5 GetProperty (Deliveryoptimization. h)
description: Método genérico para obtener las propiedades del trabajo de optimización de entrega (DO).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Método GetProperty
- Método GetProperty, interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996481"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="4afb6-106">IBackgroundCopyJob5:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="4afb6-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="4afb6-107">Método genérico para obtener las propiedades del trabajo de optimización de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="4afb6-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4afb6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4afb6-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="4afb6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4afb6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4afb6-110">*PropertyId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4afb6-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4afb6-111">IDENTIFICADOR de la propiedad que se obtiene especificado como un valor de enumeración de [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="4afb6-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="4afb6-112">*pPropertyValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4afb6-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4afb6-113">Valor de propiedad devuelto como BITS_JOB_PROPERTY_VALUE Unión.</span><span class="sxs-lookup"><span data-stu-id="4afb6-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4afb6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4afb6-114">Return value</span></span>

<span data-ttu-id="4afb6-115">El método devuelve los siguientes valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="4afb6-115">The method returns the following return values.</span></span>



| <span data-ttu-id="4afb6-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4afb6-116">Return code</span></span>                                                                          | <span data-ttu-id="4afb6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4afb6-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4afb6-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4afb6-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="4afb6-119">Correcto</span><span class="sxs-lookup"><span data-stu-id="4afb6-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4afb6-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4afb6-120">Requirements</span></span>



| <span data-ttu-id="4afb6-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4afb6-121">Requirement</span></span> | <span data-ttu-id="4afb6-122">Value</span><span class="sxs-lookup"><span data-stu-id="4afb6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4afb6-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4afb6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4afb6-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="4afb6-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4afb6-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4afb6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4afb6-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="4afb6-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4afb6-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4afb6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4afb6-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4afb6-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4afb6-129">IDL</span><span class="sxs-lookup"><span data-stu-id="4afb6-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4afb6-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4afb6-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4afb6-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4afb6-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4afb6-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4afb6-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4afb6-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4afb6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4afb6-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4afb6-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4afb6-135">IID</span><span class="sxs-lookup"><span data-stu-id="4afb6-135">IID</span></span><br/>                      | <span data-ttu-id="4afb6-136">IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="4afb6-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4afb6-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="4afb6-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4afb6-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="4afb6-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="4afb6-139">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="4afb6-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





