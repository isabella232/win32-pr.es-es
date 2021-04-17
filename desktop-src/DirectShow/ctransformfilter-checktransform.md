---
description: El método CheckTransform comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: Método CTransformFilter. CheckTransform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660731"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="98d95-103">CTransformFilter. CheckTransform, método</span><span class="sxs-lookup"><span data-stu-id="98d95-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="98d95-104">El `CheckTransform` método comprueba si un tipo de medio de entrada es compatible con un tipo de medio de salida.</span><span class="sxs-lookup"><span data-stu-id="98d95-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="98d95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98d95-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="98d95-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98d95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98d95-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="98d95-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="98d95-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="98d95-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="98d95-109">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="98d95-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="98d95-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de salida.</span><span class="sxs-lookup"><span data-stu-id="98d95-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98d95-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98d95-111">Return value</span></span>

<span data-ttu-id="98d95-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98d95-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="98d95-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="98d95-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="98d95-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98d95-114">Return code</span></span>                                                                                                | <span data-ttu-id="98d95-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="98d95-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="98d95-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="98d95-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="98d95-117">Los tipos de medios son compatibles.</span><span class="sxs-lookup"><span data-stu-id="98d95-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="98d95-118"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="98d95-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="98d95-119">Los tipos de medios no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="98d95-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98d95-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98d95-120">Remarks</span></span>

<span data-ttu-id="98d95-121">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="98d95-121">The derived class must implement this method.</span></span> <span data-ttu-id="98d95-122">Devuelve S \_ OK si el filtro puede aceptar ambos tipos de medios especificados o un código de error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98d95-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="98d95-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98d95-123">Requirements</span></span>



| <span data-ttu-id="98d95-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="98d95-124">Requirement</span></span> | <span data-ttu-id="98d95-125">Value</span><span class="sxs-lookup"><span data-stu-id="98d95-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98d95-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98d95-126">Header</span></span><br/>  | <dl> <span data-ttu-id="98d95-127"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98d95-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98d95-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="98d95-128">Library</span></span><br/> | <dl> <span data-ttu-id="98d95-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="98d95-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




