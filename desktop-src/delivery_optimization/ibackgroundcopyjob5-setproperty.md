---
title: Método SetProperty de IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Método genérico para configurar las propiedades del trabajo de optimización de entrega (DO).
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803295"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="0f630-106">IBackgroundCopyJob5:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="0f630-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="0f630-107">Método genérico para configurar las propiedades del trabajo de optimización de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="0f630-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f630-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0f630-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="0f630-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0f630-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f630-110">*PropertyId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f630-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f630-111">IDENTIFICADOR de la propiedad que se establece como un valor de enumeración de [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="0f630-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="0f630-112">*PropertyValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0f630-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f630-113">Valor de la propiedad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="0f630-113">The value of the property that is being set.</span></span> <span data-ttu-id="0f630-114">Para contener un valor cuyo tipo sea adecuado para la propiedad, este valor se especifica a través de la Unión [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) que se compone de todos los tipos de propiedad conocidos.</span><span class="sxs-lookup"><span data-stu-id="0f630-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f630-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0f630-115">Return value</span></span>

<span data-ttu-id="0f630-116">El método devuelve los siguientes valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="0f630-116">The method returns the following return values.</span></span>



| <span data-ttu-id="0f630-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0f630-117">Return code</span></span>                                                                          | <span data-ttu-id="0f630-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f630-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="0f630-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f630-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="0f630-120">Correcto</span><span class="sxs-lookup"><span data-stu-id="0f630-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f630-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f630-121">Requirements</span></span>



| <span data-ttu-id="0f630-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f630-122">Requirement</span></span> | <span data-ttu-id="0f630-123">Value</span><span class="sxs-lookup"><span data-stu-id="0f630-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f630-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f630-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0f630-125">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0f630-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0f630-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0f630-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0f630-127">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0f630-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f630-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f630-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f630-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f630-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f630-130">IDL</span><span class="sxs-lookup"><span data-stu-id="0f630-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f630-131"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f630-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f630-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f630-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="0f630-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f630-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0f630-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0f630-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f630-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f630-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0f630-136">IID</span><span class="sxs-lookup"><span data-stu-id="0f630-136">IID</span></span><br/>                      | <span data-ttu-id="0f630-137">IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="0f630-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="0f630-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0f630-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f630-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="0f630-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="0f630-140">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="0f630-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





