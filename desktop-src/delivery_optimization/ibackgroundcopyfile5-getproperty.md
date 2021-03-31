---
title: Método IBackgroundCopyFile5 GetProperty (Deliveryoptimization. h)
description: Obtiene una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Método GetProperty
- Método GetProperty, interfaz IBackgroundCopyFile5
- Interfaz IBackgroundCopyFile5, método GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150207"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="70853-106">IBackgroundCopyFile5:: GetProperty (método)</span><span class="sxs-lookup"><span data-stu-id="70853-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="70853-107">Obtiene una propiedad genérica de la transferencia de archivos de optimización de entrega (DO).</span><span class="sxs-lookup"><span data-stu-id="70853-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="70853-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70853-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="70853-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70853-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70853-110">*PropertyId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="70853-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="70853-111">Especifica la propiedad de archivo cuyo valor se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="70853-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="70853-112">*PropertyValue* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="70853-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70853-113">Valor de la propiedad, que se devuelve como un puntero a una Unión de BITS_FILE_PROPERTY_VALUE.</span><span class="sxs-lookup"><span data-stu-id="70853-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="70853-114">Use el campo de Unión apropiado para el valor de identificador de propiedad que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="70853-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70853-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70853-115">Return value</span></span>

<span data-ttu-id="70853-116">Si este método se ejecuta correctamente, devuelve **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="70853-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="70853-117">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="70853-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="70853-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70853-118">Requirements</span></span>



| <span data-ttu-id="70853-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="70853-119">Requirement</span></span> | <span data-ttu-id="70853-120">Value</span><span class="sxs-lookup"><span data-stu-id="70853-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70853-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70853-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70853-122">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="70853-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="70853-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70853-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70853-124">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="70853-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="70853-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70853-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="70853-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="70853-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="70853-127">IDL</span><span class="sxs-lookup"><span data-stu-id="70853-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70853-128"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70853-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="70853-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="70853-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="70853-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="70853-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="70853-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70853-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70853-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70853-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="70853-133">IID</span><span class="sxs-lookup"><span data-stu-id="70853-133">IID</span></span><br/>                      | <span data-ttu-id="70853-134">IID_IBackgroundCopyFile5 se define como 85C1657F-DAFC-40E8-8834-DF18EA25717E</span><span class="sxs-lookup"><span data-stu-id="70853-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="70853-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="70853-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70853-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="70853-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="70853-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="70853-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





