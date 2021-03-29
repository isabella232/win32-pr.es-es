---
description: La función CreatePosPassThru crea un objeto CPosPassThru o un objeto CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: Función CreatePosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680860"
---
# <a name="createpospassthru-function"></a><span data-ttu-id="9c4ce-103">CreatePosPassThru función)</span><span class="sxs-lookup"><span data-stu-id="9c4ce-103">CreatePosPassThru function</span></span>

<span data-ttu-id="9c4ce-104">La `CreatePosPassThru` función crea un objeto [**CPosPassThru**](cpospassthru.md) o un objeto [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="9c4ce-104">The `CreatePosPassThru` function creates a [**CPosPassThru**](cpospassthru.md) object or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c4ce-105">Syntax</span></span>


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a><span data-ttu-id="9c4ce-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9c4ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c4ce-107">*pAgg*</span><span class="sxs-lookup"><span data-stu-id="9c4ce-107">*pAgg*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4ce-108">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-108">Pointer to the owner of this object.</span></span> <span data-ttu-id="9c4ce-109">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-109">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="9c4ce-110">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-110">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9c4ce-111">*bRenderer*</span><span class="sxs-lookup"><span data-stu-id="9c4ce-111">*bRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4ce-112">Valor booleano que especifica si el filtro es un representador.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-112">Boolean value that specifies whether the filter is a renderer.</span></span> <span data-ttu-id="9c4ce-113">Use el valor **true** si el filtro es un representador o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-113">Use the value **TRUE** if the filter is a renderer, or **FALSE** otherwise.</span></span> <span data-ttu-id="9c4ce-114">Si el valor es **true**, este método crea una instancia de la clase [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="9c4ce-114">If the value is **TRUE**, this method creates an instance of the [**CRendererPosPassThru**](crendererpospassthru.md) class.</span></span> <span data-ttu-id="9c4ce-115">Si el valor es **false**, el método crea una instancia de la clase **CPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="9c4ce-115">If the value is **FALSE**, the method creates an instance of the **CPosPassThru** class.</span></span>

</dd> <dt>

<span data-ttu-id="9c4ce-116">*pPin*</span><span class="sxs-lookup"><span data-stu-id="9c4ce-116">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4ce-117">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) en el PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-117">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface on the filter's input pin.</span></span>

</dd> <dt>

<span data-ttu-id="9c4ce-118">*ppPassThru*</span><span class="sxs-lookup"><span data-stu-id="9c4ce-118">*ppPassThru*</span></span> 
</dt> <dd>

<span data-ttu-id="9c4ce-119">Dirección de una variable que recibe un puntero a la interfaz **IUnknown** del objeto.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-119">Address of a variable that receives a pointer to the object's **IUnknown** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c4ce-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9c4ce-120">Return value</span></span>

<span data-ttu-id="9c4ce-121">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-121">Returns S\_OK if successful.</span></span> <span data-ttu-id="9c4ce-122">De lo contrario, devuelve un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-122">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c4ce-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c4ce-123">Remarks</span></span>

<span data-ttu-id="9c4ce-124">Este método usa la interfaz [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-124">This method uses the [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) interface to create the object.</span></span> <span data-ttu-id="9c4ce-125">El objeto se carga dinámicamente desde Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-125">The object is loaded dynamically from Quartz.dll.</span></span>

<span data-ttu-id="9c4ce-126">Si la función se ejecuta correctamente, la interfaz **IUnknown** devuelta tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-126">If the function succeeds, the returned **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="9c4ce-127">El llamador debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="9c4ce-127">The caller must release the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4ce-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c4ce-128">Requirements</span></span>



| <span data-ttu-id="9c4ce-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c4ce-129">Requirement</span></span> | <span data-ttu-id="9c4ce-130">Value</span><span class="sxs-lookup"><span data-stu-id="9c4ce-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4ce-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9c4ce-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9c4ce-132"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9c4ce-132"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9c4ce-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9c4ce-133">Library</span></span><br/> | <dl> <span data-ttu-id="9c4ce-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9c4ce-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c4ce-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c4ce-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c4ce-136">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="9c4ce-136">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




