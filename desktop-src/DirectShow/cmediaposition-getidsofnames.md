---
description: El método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DispId.
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition. GetIDsOfNames (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.GetIDsOfNames
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc2c7eee4304bb32ac1af2759bc2f094aca1d592
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681014"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="93217-103">CMediaPosition. GetIDsOfNames (método)</span><span class="sxs-lookup"><span data-stu-id="93217-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="93217-104">El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DispId.</span><span class="sxs-lookup"><span data-stu-id="93217-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="93217-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93217-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="93217-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="93217-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93217-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="93217-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="93217-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="93217-108">Reserved.</span></span> <span data-ttu-id="93217-109">Use IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="93217-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="93217-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="93217-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="93217-111">Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se van a asignar.</span><span class="sxs-lookup"><span data-stu-id="93217-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="93217-112">*CNAME*</span><span class="sxs-lookup"><span data-stu-id="93217-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="93217-113">Tamaño de la matriz proporcionado por el parámetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="93217-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="93217-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="93217-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="93217-115">Contexto de configuración regional en el que se van a interpretar los nombres.</span><span class="sxs-lookup"><span data-stu-id="93217-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="93217-116">Puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="93217-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="93217-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="93217-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="93217-118">Puntero a una matriz que recibe los DispId.</span><span class="sxs-lookup"><span data-stu-id="93217-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="93217-119">Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el parámetro *rgszNames* .</span><span class="sxs-lookup"><span data-stu-id="93217-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93217-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="93217-120">Return value</span></span>

<span data-ttu-id="93217-121">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="93217-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="93217-122">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="93217-122">Possible values include the following.</span></span>



| <span data-ttu-id="93217-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="93217-123">Return code</span></span>                                                                                         | <span data-ttu-id="93217-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="93217-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="93217-125"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="93217-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="93217-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="93217-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="93217-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="93217-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="93217-128">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="93217-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="93217-129"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="93217-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="93217-130">No se conocían uno o varios de los nombres.</span><span class="sxs-lookup"><span data-stu-id="93217-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="93217-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93217-131">Requirements</span></span>



| <span data-ttu-id="93217-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="93217-132">Requirement</span></span> | <span data-ttu-id="93217-133">Value</span><span class="sxs-lookup"><span data-stu-id="93217-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93217-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="93217-134">Header</span></span><br/>  | <dl> <span data-ttu-id="93217-135"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="93217-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="93217-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="93217-136">Library</span></span><br/> | <dl> <span data-ttu-id="93217-137"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="93217-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93217-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="93217-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93217-139">**Clase CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="93217-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




