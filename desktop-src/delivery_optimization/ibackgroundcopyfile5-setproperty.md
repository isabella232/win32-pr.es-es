---
title: Método SetProperty de IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Establece una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty (método)
- Método SetProperty, interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, método SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996299"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="50883-106">IBackgroundCopyFile5:: SetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="50883-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="50883-107">Establece una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="50883-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="50883-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="50883-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="50883-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="50883-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50883-110">*PropertyId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="50883-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50883-111">Especifica la propiedad que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="50883-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="50883-112">*ProertyValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="50883-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50883-113">Puntero a una Unión que especifica el valor que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="50883-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="50883-114">Se utiliza el miembro de Unión adecuado para el ID. de propiedad.</span><span class="sxs-lookup"><span data-stu-id="50883-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50883-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="50883-115">Return value</span></span>

<span data-ttu-id="50883-116">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="50883-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="50883-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="50883-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="50883-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50883-118">Requirements</span></span>



| <span data-ttu-id="50883-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="50883-119">Requirement</span></span> | <span data-ttu-id="50883-120">Value</span><span class="sxs-lookup"><span data-stu-id="50883-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50883-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50883-121">Minimum supported client</span></span><br/> | <span data-ttu-id="50883-122">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="50883-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="50883-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="50883-123">Minimum supported server</span></span><br/> | <span data-ttu-id="50883-124">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="50883-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="50883-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="50883-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="50883-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="50883-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="50883-127">IDL</span><span class="sxs-lookup"><span data-stu-id="50883-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="50883-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="50883-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="50883-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="50883-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="50883-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50883-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="50883-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="50883-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50883-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50883-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="50883-133">IID</span><span class="sxs-lookup"><span data-stu-id="50883-133">IID</span></span><br/>                      | <span data-ttu-id="50883-134">IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="50883-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="50883-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="50883-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50883-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="50883-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="50883-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="50883-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





