---
description: El método CheckMediaType determina si un tipo de medio propuesto es compatible con el formato de presentación.
ms.assetid: 567663cf-c79f-4549-9fa9-b16da957d2b1
title: Método CImageDisplay. CheckMediaType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8ebcdbe6bbfe6538a2ea166be0816f31954c7d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660225"
---
# <a name="cimagedisplaycheckmediatype-method"></a><span data-ttu-id="46cec-103">CImageDisplay. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="46cec-103">CImageDisplay.CheckMediaType method</span></span>

<span data-ttu-id="46cec-104">El `CheckMediaType` método determina si un tipo de medio propuesto es compatible con el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="46cec-104">The `CheckMediaType` method determines whether a proposed media type is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="46cec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46cec-105">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmtIn
);
```



## <a name="parameters"></a><span data-ttu-id="46cec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46cec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46cec-107">*pmtIn*</span><span class="sxs-lookup"><span data-stu-id="46cec-107">*pmtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="46cec-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="46cec-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46cec-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46cec-109">Return value</span></span>

<span data-ttu-id="46cec-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="46cec-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="46cec-111">Estos son algunos de los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="46cec-111">Possible values include the following.</span></span>



| <span data-ttu-id="46cec-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="46cec-112">Return code</span></span>                                                                                  | <span data-ttu-id="46cec-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="46cec-113">Description</span></span>                              |
|----------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <span data-ttu-id="46cec-114"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="46cec-114"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="46cec-115">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="46cec-115">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="46cec-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="46cec-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="46cec-117">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="46cec-117">Invalid media type.</span></span><br/>           |
| <dl> <span data-ttu-id="46cec-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="46cec-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="46cec-119">El tipo de medio es compatible.</span><span class="sxs-lookup"><span data-stu-id="46cec-119">The media type is compatible.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="46cec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46cec-120">Requirements</span></span>



| <span data-ttu-id="46cec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="46cec-121">Requirement</span></span> | <span data-ttu-id="46cec-122">Value</span><span class="sxs-lookup"><span data-stu-id="46cec-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46cec-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46cec-123">Header</span></span><br/>  | <dl> <span data-ttu-id="46cec-124"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46cec-124"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46cec-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46cec-125">Library</span></span><br/> | <dl> <span data-ttu-id="46cec-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="46cec-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46cec-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="46cec-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46cec-128">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="46cec-128">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




