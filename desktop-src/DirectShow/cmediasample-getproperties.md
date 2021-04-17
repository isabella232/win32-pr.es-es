---
description: 'El método GetProperties recupera las propiedades del ejemplo. Este método implementa el método IMediaSample2:: GetProperties.'
ms.assetid: c2a6d611-9c17-41fb-bb6d-f5b17f1c9966
title: Método CMediaSample. GetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.GetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06ee1022f298e2f5167d348777b33fc2f1703eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670478"
---
# <a name="cmediasamplegetproperties-method"></a><span data-ttu-id="330ae-104">CMediaSample. GetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="330ae-104">CMediaSample.GetProperties method</span></span>

<span data-ttu-id="330ae-105">El `GetProperties` método recupera las propiedades del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="330ae-105">The `GetProperties` method retrieves the properties of the sample.</span></span> <span data-ttu-id="330ae-106">Este método implementa el método [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) .</span><span class="sxs-lookup"><span data-stu-id="330ae-106">This method implements the [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="330ae-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="330ae-107">Syntax</span></span>


```C++
HRESULT GetProperties(
   DWORD cbProperties,
   BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="330ae-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="330ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="330ae-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="330ae-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="330ae-110">Longitud de los datos de propiedad que se van a recuperar, en bytes.</span><span class="sxs-lookup"><span data-stu-id="330ae-110">Length of property data to retrieve, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="330ae-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="330ae-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="330ae-112">Puntero a un búfer de tamaño *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="330ae-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="330ae-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="330ae-113">Return value</span></span>

<span data-ttu-id="330ae-114">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="330ae-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="330ae-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="330ae-115">Return code</span></span>                                                                               | <span data-ttu-id="330ae-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="330ae-116">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="330ae-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="330ae-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="330ae-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="330ae-118">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="330ae-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="330ae-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="330ae-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="330ae-120">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="330ae-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="330ae-121">Requirements</span></span>



| <span data-ttu-id="330ae-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="330ae-122">Requirement</span></span> | <span data-ttu-id="330ae-123">Value</span><span class="sxs-lookup"><span data-stu-id="330ae-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330ae-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="330ae-124">Header</span></span><br/>  | <dl> <span data-ttu-id="330ae-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="330ae-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="330ae-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="330ae-126">Library</span></span><br/> | <dl> <span data-ttu-id="330ae-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="330ae-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="330ae-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="330ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330ae-129">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="330ae-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




