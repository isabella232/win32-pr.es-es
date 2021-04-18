---
description: El método Transform transforma un ejemplo en su lugar.
ms.assetid: 2268041b-70d4-48a9-9bb8-4ab921cce649
title: Método CTransInPlaceFilter. Transform (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5b84f326807f730745268a217b6066dacb9aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681272"
---
# <a name="ctransinplacefiltertransform-method"></a><span data-ttu-id="027a6-103">CTransInPlaceFilter. Transform (método)</span><span class="sxs-lookup"><span data-stu-id="027a6-103">CTransInPlaceFilter.Transform method</span></span>

<span data-ttu-id="027a6-104">El `Transform` método transforma un ejemplo en contexto.</span><span class="sxs-lookup"><span data-stu-id="027a6-104">The `Transform` method transforms a sample in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="027a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="027a6-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="027a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="027a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027a6-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="027a6-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="027a6-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="027a6-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="027a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="027a6-109">Return value</span></span>

<span data-ttu-id="027a6-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="027a6-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="027a6-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="027a6-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="027a6-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="027a6-112">Return code</span></span>                                                                             | <span data-ttu-id="027a6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="027a6-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="027a6-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="027a6-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="027a6-115">No entregue este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="027a6-115">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="027a6-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="027a6-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="027a6-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="027a6-117">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="027a6-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="027a6-118">Remarks</span></span>

<span data-ttu-id="027a6-119">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="027a6-119">The derived class must implement this method.</span></span> <span data-ttu-id="027a6-120">Transforme los datos de ejemplo en su lugar.</span><span class="sxs-lookup"><span data-stu-id="027a6-120">Transform the sample data in place.</span></span> <span data-ttu-id="027a6-121">Si el filtro usa dos asignadores, copia los datos del ejemplo de entrada a un nuevo ejemplo y pasa la copia a este método.</span><span class="sxs-lookup"><span data-stu-id="027a6-121">If the filter is using two allocators, it copies the data from the input sample to a new sample, and passes the copy to this method.</span></span>

<span data-ttu-id="027a6-122">Si el filtro no debe proporcionar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="027a6-122">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="027a6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="027a6-123">Requirements</span></span>



| <span data-ttu-id="027a6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="027a6-124">Requirement</span></span> | <span data-ttu-id="027a6-125">Value</span><span class="sxs-lookup"><span data-stu-id="027a6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="027a6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="027a6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="027a6-127"><dt>TRANSip. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="027a6-127"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="027a6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="027a6-128">Library</span></span><br/> | <dl> <span data-ttu-id="027a6-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="027a6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027a6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="027a6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027a6-131">**Clase CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="027a6-131">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




