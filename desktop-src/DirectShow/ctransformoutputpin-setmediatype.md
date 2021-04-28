---
description: 'Método CTransformOutputPin.SetMediaType: el método SetMediaType establece el tipo de medio para la conexión.'
ms.assetid: 1d6569c1-e27b-4e96-af5a-64a78b762afd
title: Método CTransformOutputPin.SetMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5aa8dcfbf573f6ca5b047c9f84567a84985732c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084803"
---
# <a name="ctransformoutputpinsetmediatype-method"></a><span data-ttu-id="cd39d-103">CTransformOutputPin.SetMediaType (método)</span><span class="sxs-lookup"><span data-stu-id="cd39d-103">CTransformOutputPin.SetMediaType method</span></span>

<span data-ttu-id="cd39d-104">El `SetMediaType` método establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="cd39d-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd39d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd39d-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="cd39d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd39d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd39d-107">*Mt*</span><span class="sxs-lookup"><span data-stu-id="cd39d-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="cd39d-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="cd39d-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd39d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd39d-109">Return value</span></span>

<span data-ttu-id="cd39d-110">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd39d-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd39d-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd39d-111">Remarks</span></span>

<span data-ttu-id="cd39d-112">Este método invalida el [**método CBasePin::SetMediaType.**](cbasepin-setmediatype.md)</span><span class="sxs-lookup"><span data-stu-id="cd39d-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="cd39d-113">Llama al método [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) del filtro para informar al filtro.</span><span class="sxs-lookup"><span data-stu-id="cd39d-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="cd39d-114">El pin debe comprobar que el tipo de medio es aceptable antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="cd39d-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd39d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd39d-115">Requirements</span></span>



| <span data-ttu-id="cd39d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd39d-116">Requirement</span></span> | <span data-ttu-id="cd39d-117">Value</span><span class="sxs-lookup"><span data-stu-id="cd39d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd39d-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd39d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="cd39d-119"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd39d-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cd39d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cd39d-120">Library</span></span><br/> | <dl> <span data-ttu-id="cd39d-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cd39d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




