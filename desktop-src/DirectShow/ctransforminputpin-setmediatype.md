---
description: El método SetMediaType establece el tipo de medio para la conexión.
ms.assetid: 8e83380f-ba38-4fb8-ac32-40d68a4efea6
title: Método CTransformInputPin. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b42531a003fbad1a2a08864390a512296c440e64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681173"
---
# <a name="ctransforminputpinsetmediatype-method"></a><span data-ttu-id="451a1-103">CTransformInputPin. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="451a1-103">CTransformInputPin.SetMediaType method</span></span>

<span data-ttu-id="451a1-104">El `SetMediaType` método establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="451a1-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="451a1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="451a1-105">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *mt
);
```



## <a name="parameters"></a><span data-ttu-id="451a1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="451a1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="451a1-107">*módulo*</span><span class="sxs-lookup"><span data-stu-id="451a1-107">*mt*</span></span> 
</dt> <dd>

<span data-ttu-id="451a1-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="451a1-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="451a1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="451a1-109">Return value</span></span>

<span data-ttu-id="451a1-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="451a1-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="451a1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="451a1-111">Remarks</span></span>

<span data-ttu-id="451a1-112">Este método invalida el método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="451a1-112">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span> <span data-ttu-id="451a1-113">Llama al método [**CTransformFilter:: SetMediaType**](ctransformfilter-setmediatype.md) del filtro para informar al filtro.</span><span class="sxs-lookup"><span data-stu-id="451a1-113">It calls the filter's [**CTransformFilter::SetMediaType**](ctransformfilter-setmediatype.md) method to inform the filter.</span></span>

<span data-ttu-id="451a1-114">El código PIN debe comprobar que el tipo de medio es aceptable antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="451a1-114">The pin must verify that the media type is acceptable before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="451a1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="451a1-115">Requirements</span></span>



| <span data-ttu-id="451a1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="451a1-116">Requirement</span></span> | <span data-ttu-id="451a1-117">Value</span><span class="sxs-lookup"><span data-stu-id="451a1-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="451a1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="451a1-118">Header</span></span><br/>  | <dl> <span data-ttu-id="451a1-119"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="451a1-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="451a1-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="451a1-120">Library</span></span><br/> | <dl> <span data-ttu-id="451a1-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="451a1-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




