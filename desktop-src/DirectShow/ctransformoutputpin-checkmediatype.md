---
description: 'Método CTransformOutputPin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 9e31480b-129c-4741-846a-854c70c65606
title: Método CTransformOutputPin.CheckMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7dc0edc642687518979eab1d47c69af039bc3173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084913"
---
# <a name="ctransformoutputpincheckmediatype-method"></a><span data-ttu-id="71659-103">CTransformOutputPin.CheckMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="71659-103">CTransformOutputPin.CheckMediaType method</span></span>

<span data-ttu-id="71659-104">El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="71659-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="71659-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71659-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *mtIn
);
```



## <a name="parameters"></a><span data-ttu-id="71659-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71659-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71659-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="71659-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="71659-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="71659-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71659-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71659-109">Return value</span></span>

<span data-ttu-id="71659-110">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="71659-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="71659-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="71659-111">Possible values include the following.</span></span>



| <span data-ttu-id="71659-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="71659-112">Return code</span></span>                                                                                  | <span data-ttu-id="71659-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="71659-113">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="71659-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71659-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="71659-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="71659-115">Success.</span></span><br/>                                 |
| <dl> <span data-ttu-id="71659-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="71659-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="71659-117">El pin de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="71659-117">The filter's input pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="71659-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71659-118">Remarks</span></span>

<span data-ttu-id="71659-119">Este método implementa el método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro.</span><span class="sxs-lookup"><span data-stu-id="71659-119">This method implements the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="71659-120">Se produce un error en el método si el pin de entrada del filtro no está conectado.</span><span class="sxs-lookup"><span data-stu-id="71659-120">The method fails if the filter's input pin is not connected.</span></span> <span data-ttu-id="71659-121">De lo contrario, llama al método [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) del filtro, que también es virtual puro.</span><span class="sxs-lookup"><span data-stu-id="71659-121">Otherwise, it calls the filter's [**CTransformFilter::CheckTransform**](ctransformfilter-checktransform.md) method, which is also pure virtual.</span></span> <span data-ttu-id="71659-122">La clase derivada del filtro debe implementar **CheckTransform**, que determina si el tipo de medio de salida propuesto es compatible con el tipo de medio de entrada.</span><span class="sxs-lookup"><span data-stu-id="71659-122">The filter's derived class must implement **CheckTransform**, which determines if the proposed output media type is compatible with the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="71659-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71659-123">Requirements</span></span>



| <span data-ttu-id="71659-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="71659-124">Requirement</span></span> | <span data-ttu-id="71659-125">Value</span><span class="sxs-lookup"><span data-stu-id="71659-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71659-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71659-126">Header</span></span><br/>  | <dl> <span data-ttu-id="71659-127"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="71659-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="71659-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="71659-128">Library</span></span><br/> | <dl> <span data-ttu-id="71659-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="71659-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




