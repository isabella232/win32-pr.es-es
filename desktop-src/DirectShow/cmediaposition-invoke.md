---
description: El método Invoke proporciona acceso a las propiedades y los métodos expuestos por el objeto.
ms.assetid: 3c03751d-239b-4cc5-bfab-8d1aed1074b8
title: Método CMediaPosition. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3955848bf2a87e0983ddd7dc3bef48f157ae6648
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671555"
---
# <a name="cmediapositioninvoke-method"></a><span data-ttu-id="c9506-103">CMediaPosition. Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="c9506-103">CMediaPosition.Invoke method</span></span>

<span data-ttu-id="c9506-104">El `Invoke` método proporciona acceso a las propiedades y los métodos expuestos por el objeto.</span><span class="sxs-lookup"><span data-stu-id="c9506-104">The `Invoke` method provides access to properties and methods exposed by the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9506-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c9506-105">Syntax</span></span>


```C++
HRESULT Invoke(
   DISPID     dispidMember,
   REFIID     riid,
   LCID       lcid,
   WORD       wFlags,
   DISPPARAMS *pdispparams,
   VARIANT    *pvarResult,
   EXCEPINFO  *pexcepinfo,
   UINT       *puArgErr
);
```



## <a name="parameters"></a><span data-ttu-id="c9506-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c9506-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9506-107">*dispidMember*</span><span class="sxs-lookup"><span data-stu-id="c9506-107">*dispidMember*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-108">Identificador del miembro.</span><span class="sxs-lookup"><span data-stu-id="c9506-108">Identifier of the member.</span></span> <span data-ttu-id="c9506-109">Use [**CMediaPosition:: GetIDsOfNames**](cmediaposition-getidsofnames.md) para obtener el identificador de envío.</span><span class="sxs-lookup"><span data-stu-id="c9506-109">Use [**CMediaPosition::GetIDsOfNames**](cmediaposition-getidsofnames.md) to obtain the dispatch identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-110">*riid*</span><span class="sxs-lookup"><span data-stu-id="c9506-110">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-111">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="c9506-111">Reserved for future use.</span></span> <span data-ttu-id="c9506-112">Debe ser un IID \_ null.</span><span class="sxs-lookup"><span data-stu-id="c9506-112">Must be IID\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-113">*lcid*</span><span class="sxs-lookup"><span data-stu-id="c9506-113">*lcid*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-114">Contexto de configuración regional en el que se interpretan los argumentos.</span><span class="sxs-lookup"><span data-stu-id="c9506-114">Locale context in which to interpret arguments.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-115">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="c9506-115">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-116">Marcas que describen el contexto de la llamada.</span><span class="sxs-lookup"><span data-stu-id="c9506-116">Flags describing the context of the call.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-117">*pdispparams*</span><span class="sxs-lookup"><span data-stu-id="c9506-117">*pdispparams*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-118">Puntero a una estructura **DIPPARAMS** que contiene los argumentos.</span><span class="sxs-lookup"><span data-stu-id="c9506-118">Pointer to a **DIPPARAMS** structure that contains the arguments.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-119">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="c9506-119">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-120">Puntero a una **variante** que recibe el resultado, o **null** si el llamador no espera ningún resultado.</span><span class="sxs-lookup"><span data-stu-id="c9506-120">Pointer to a **VARIANT** that receives the result, or **NULL** if the caller expects no result.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-121">*pexcepinfo*</span><span class="sxs-lookup"><span data-stu-id="c9506-121">*pexcepinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-122">Puntero a una estructura que recibe información de excepción.</span><span class="sxs-lookup"><span data-stu-id="c9506-122">Pointer to a structure that receives exception information.</span></span>

</dd> <dt>

<span data-ttu-id="c9506-123">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="c9506-123">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="c9506-124">Puntero a una variable que recibe el índice del primer argumento que produce un error.</span><span class="sxs-lookup"><span data-stu-id="c9506-124">Pointer to a variable that receives the index of the first argument that causes an error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9506-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c9506-125">Return value</span></span>

<span data-ttu-id="c9506-126">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c9506-126">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c9506-127">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="c9506-127">Possible values include the following.</span></span>



| <span data-ttu-id="c9506-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c9506-128">Return code</span></span>                                                                                              | <span data-ttu-id="c9506-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9506-129">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="c9506-130"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-130"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="c9506-131">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c9506-131">Success.</span></span><br/>                              |
| <dl> <span data-ttu-id="c9506-132"><dt>**DISP \_ E \_ UNKNOWNINTERFACE**</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-132"><dt>**DISP\_E\_UNKNOWNINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="c9506-133">El parámetro *riid* no es un IID \_ nulo</span><span class="sxs-lookup"><span data-stu-id="c9506-133">The *riid* parameter is not IID\_NULL</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9506-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9506-134">Requirements</span></span>



| <span data-ttu-id="c9506-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9506-135">Requirement</span></span> | <span data-ttu-id="c9506-136">Value</span><span class="sxs-lookup"><span data-stu-id="c9506-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9506-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c9506-137">Header</span></span><br/>  | <dl> <span data-ttu-id="c9506-138"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-138"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c9506-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c9506-139">Library</span></span><br/> | <dl> <span data-ttu-id="c9506-140"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c9506-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9506-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9506-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9506-142">**Clase CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="c9506-142">**CMediaPosition Class**</span></span>](cmediaposition.md)
</dt> </dl>

 

 




