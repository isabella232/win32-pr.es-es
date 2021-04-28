---
description: 'Método CMediaPosition.GetIDsOfNames: el método GetIDsOfNames asigna un conjunto de nombres a un conjunto correspondiente de DISPIDs.'
ms.assetid: 4d3780ff-905f-4166-86d4-32395090b5cb
title: Método CMediaPosition.GetIDsOfNames (Ctlutil.h)
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
ms.openlocfilehash: 26a348e58fa84aa4134ce9f2ea756874b9ce2724
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095533"
---
# <a name="cmediapositiongetidsofnames-method"></a><span data-ttu-id="f14f4-103">Método CMediaPosition.GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="f14f4-103">CMediaPosition.GetIDsOfNames method</span></span>

<span data-ttu-id="f14f4-104">El `GetIDsOfNames` método asigna un conjunto de nombres a un conjunto correspondiente de DISPID.</span><span class="sxs-lookup"><span data-stu-id="f14f4-104">The `GetIDsOfNames` method maps a set of names to a corresponding set of DISPIDs.</span></span>

## <a name="syntax"></a><span data-ttu-id="f14f4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f14f4-105">Syntax</span></span>


```C++
HRESULT GetIDsOfNames(
   REFIID  riid,
   OLECHAR **rgszNames,
   UINT    cNames,
   LCID    lcid,
   DISPID  *rgdispid
);
```



## <a name="parameters"></a><span data-ttu-id="f14f4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f14f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f14f4-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="f14f4-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="f14f4-108">Reservado.</span><span class="sxs-lookup"><span data-stu-id="f14f4-108">Reserved.</span></span> <span data-ttu-id="f14f4-109">Use IID \_ NULL.</span><span class="sxs-lookup"><span data-stu-id="f14f4-109">Use IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="f14f4-110">*rgszNames*</span><span class="sxs-lookup"><span data-stu-id="f14f4-110">*rgszNames*</span></span> 
</dt> <dd>

<span data-ttu-id="f14f4-111">Dirección de una matriz de cadenas de caracteres anchos que contienen los nombres que se asignarán.</span><span class="sxs-lookup"><span data-stu-id="f14f4-111">Address of an array of wide-character strings that contain the names to be mapped.</span></span>

</dd> <dt>

<span data-ttu-id="f14f4-112">*cNames*</span><span class="sxs-lookup"><span data-stu-id="f14f4-112">*cNames*</span></span> 
</dt> <dd>

<span data-ttu-id="f14f4-113">Tamaño de la matriz especificada por el *parámetro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="f14f4-113">Size of the array given by the *rgszNames* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f14f4-114">*lcid*</span><span class="sxs-lookup"><span data-stu-id="f14f4-114">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="f14f4-115">Contexto de configuración regional en el que se interpretarán los nombres.</span><span class="sxs-lookup"><span data-stu-id="f14f4-115">Locale context in which to interpret the names.</span></span> <span data-ttu-id="f14f4-116">Puede ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f14f4-116">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f14f4-117">*rgdispid*</span><span class="sxs-lookup"><span data-stu-id="f14f4-117">*rgdispid*</span></span> 
</dt> <dd>

<span data-ttu-id="f14f4-118">Puntero a una matriz que recibe los DISPID.</span><span class="sxs-lookup"><span data-stu-id="f14f4-118">Pointer to an array that receives the DISPIDs.</span></span> <span data-ttu-id="f14f4-119">Cada elemento de recibe un identificador que corresponde a uno de los nombres pasados en el *parámetro rgszNames.*</span><span class="sxs-lookup"><span data-stu-id="f14f4-119">Each element of receives an identifier that corresponds to one of the names passed in the *rgszNames* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f14f4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f14f4-120">Return value</span></span>

<span data-ttu-id="f14f4-121">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f14f4-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f14f4-122">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="f14f4-122">Possible values include the following.</span></span>



| <span data-ttu-id="f14f4-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f14f4-123">Return code</span></span>                                                                                         | <span data-ttu-id="f14f4-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="f14f4-124">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="f14f4-125"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f14f4-125"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="f14f4-126">Correcto.</span><span class="sxs-lookup"><span data-stu-id="f14f4-126">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="f14f4-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f14f4-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="f14f4-128">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="f14f4-128">Insufficient memory.</span></span><br/>                     |
| <dl> <span data-ttu-id="f14f4-129"><dt>**DISP \_ E \_ UNKNOWNNAME**</dt></span><span class="sxs-lookup"><span data-stu-id="f14f4-129"><dt>**DISP\_E\_UNKNOWNNAME**</dt></span></span> </dl> | <span data-ttu-id="f14f4-130">No se conocían uno o varios de los nombres.</span><span class="sxs-lookup"><span data-stu-id="f14f4-130">One or more of the names were not known.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f14f4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f14f4-131">Requirements</span></span>



| <span data-ttu-id="f14f4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f14f4-132">Requirement</span></span> | <span data-ttu-id="f14f4-133">Value</span><span class="sxs-lookup"><span data-stu-id="f14f4-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f14f4-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f14f4-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f14f4-135"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f14f4-135"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f14f4-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f14f4-136">Library</span></span><br/> | <dl> <span data-ttu-id="f14f4-137"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f14f4-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f14f4-138">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f14f4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f14f4-139">**CMediaPosition (clase)**</span><span class="sxs-lookup"><span data-stu-id="f14f4-139">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




