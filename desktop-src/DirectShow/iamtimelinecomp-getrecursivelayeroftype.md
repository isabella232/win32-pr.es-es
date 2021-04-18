---
description: El método GetRecursiveLayerOfType realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la pista virtual n de esa ordenación.
ms.assetid: 409914fd-3faf-418f-bca1-8adf2948f422
title: 'IAMTimelineComp:: GetRecursiveLayerOfType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 28dfe8862561108588e57091e92ab2d424c79c26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680972"
---
# <a name="iamtimelinecompgetrecursivelayeroftype-method"></a><span data-ttu-id="733c8-103">IAMTimelineComp:: GetRecursiveLayerOfType (método)</span><span class="sxs-lookup"><span data-stu-id="733c8-103">IAMTimelineComp::GetRecursiveLayerOfType method</span></span>

> [!Note]  
> <span data-ttu-id="733c8-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="733c8-104">\[Deprecated.</span></span> <span data-ttu-id="733c8-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="733c8-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="733c8-106">El `GetRecursiveLayerOfType` método realiza una ordenación con prioridad a la profundidad de las pistas virtuales contenidas en esta composición y recupera la *n*-ésima pista virtual de esa ordenación.</span><span class="sxs-lookup"><span data-stu-id="733c8-106">The `GetRecursiveLayerOfType` method performs a depth-first ordering of the virtual tracks contained in this composition, and retrieves the *n* th virtual track from that ordering.</span></span>

## <a name="syntax"></a><span data-ttu-id="733c8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="733c8-107">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfType(
  [out] IAMTimelineObj      **ppVirtualTrack,
        long                WhichLayer,
        TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="733c8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="733c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="733c8-109">*ppVirtualTrack* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="733c8-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="733c8-110">Recibe un puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la pista virtual.</span><span class="sxs-lookup"><span data-stu-id="733c8-110">Receives a pointer to the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="733c8-111">*WhichLayer*</span><span class="sxs-lookup"><span data-stu-id="733c8-111">*WhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="733c8-112">Especifica la pista virtual que se va a recuperar, indizada desde cero.</span><span class="sxs-lookup"><span data-stu-id="733c8-112">Specifies which virtual track to retrieve, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="733c8-113">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="733c8-113">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="733c8-114">Miembro del tipo enumerado de [**\_ \_ tipo principal**](timeline-major-type.md) de la escala de tiempo que especifica si se deben incluir pistas en la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="733c8-114">Member of the [**TIMELINE\_MAJOR\_TYPE**](timeline-major-type.md) enumerated type that specifies whether to include tracks in the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="733c8-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="733c8-115">Return value</span></span>

<span data-ttu-id="733c8-116">Devuelve uno de los siguientes valores **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="733c8-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="733c8-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="733c8-117">Return code</span></span>                                                                                  | <span data-ttu-id="733c8-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="733c8-118">Description</span></span>                                 |
|----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="733c8-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="733c8-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="733c8-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="733c8-120">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="733c8-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="733c8-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="733c8-122">No hay ningún objeto del tipo especificado.</span><span class="sxs-lookup"><span data-stu-id="733c8-122">No object of the specified type.</span></span><br/> |
| <dl> <span data-ttu-id="733c8-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="733c8-123"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="733c8-124">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="733c8-124">**NULL** pointer argument.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="733c8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="733c8-125">Remarks</span></span>

<span data-ttu-id="733c8-126">Normalmente, una aplicación no necesita llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="733c8-126">Typically, an application will not need to call this method.</span></span>

<span data-ttu-id="733c8-127">Si el parámetro de *tipo* es la \_ pista de tipo principal de la escala de tiempo \_ \_ , la ordenación con prioridad a la profundidad incluye pistas.</span><span class="sxs-lookup"><span data-stu-id="733c8-127">If the *Type* parameter is TIMELINE\_MAJOR\_TYPE\_TRACK, the depth-first ordering includes tracks.</span></span> <span data-ttu-id="733c8-128">En caso contrario, solo incluye composiciones y grupos.</span><span class="sxs-lookup"><span data-stu-id="733c8-128">If not, it includes only compositions and groups.</span></span> <span data-ttu-id="733c8-129">El propio objeto se incluye en el orden.</span><span class="sxs-lookup"><span data-stu-id="733c8-129">The object itself is included in the ordering.</span></span>

<span data-ttu-id="733c8-130">Por ejemplo, en la siguiente disposición, a partir de la composición A, el orden sería B, C, F, D, E, A.</span><span class="sxs-lookup"><span data-stu-id="733c8-130">For example, in the following arrangement, starting from Composition A, the ordering would be B, C, F, D, E, A.</span></span>

![getrecursivelayeroftype](images/composition.png)

<span data-ttu-id="733c8-132">Si el método se ejecuta correctamente, la interfaz **IAMTimelineObj** que devuelve tiene un recuento de referencias pendiente.</span><span class="sxs-lookup"><span data-stu-id="733c8-132">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="733c8-133">Asegúrese de liberar la interfaz cuando termine de usarla.</span><span class="sxs-lookup"><span data-stu-id="733c8-133">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="733c8-134">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="733c8-134">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="733c8-135">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="733c8-135">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="733c8-136">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="733c8-136">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="733c8-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="733c8-137">Requirements</span></span>



| <span data-ttu-id="733c8-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="733c8-138">Requirement</span></span> | <span data-ttu-id="733c8-139">Value</span><span class="sxs-lookup"><span data-stu-id="733c8-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="733c8-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="733c8-140">Header</span></span><br/>  | <dl> <span data-ttu-id="733c8-141"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="733c8-141"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="733c8-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="733c8-142">Library</span></span><br/> | <dl> <span data-ttu-id="733c8-143"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="733c8-143"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733c8-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="733c8-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733c8-145">**Interfaz IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="733c8-145">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="733c8-146">Códigos de error y de éxito</span><span class="sxs-lookup"><span data-stu-id="733c8-146">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




