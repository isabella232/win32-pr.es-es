---
description: 'El método ConnectionMediaType recupera el tipo de medio para la conexión de PIN actual, si existe. Este método implementa el método IPin:: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Método CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670413"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="6bb12-104">CBasePin. ConnectionMediaType, método</span><span class="sxs-lookup"><span data-stu-id="6bb12-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="6bb12-105">El método **ConnectionMediaType** recupera el tipo de medio para la conexión de PIN actual, si existe.</span><span class="sxs-lookup"><span data-stu-id="6bb12-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="6bb12-106">Este método implementa el método [**IPin:: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .</span><span class="sxs-lookup"><span data-stu-id="6bb12-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb12-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6bb12-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6bb12-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6bb12-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb12-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="6bb12-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb12-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que recibe el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6bb12-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb12-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bb12-111">Return value</span></span>

<span data-ttu-id="6bb12-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bb12-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6bb12-113">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6bb12-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="6bb12-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6bb12-114">Return code</span></span>                                                                                           | <span data-ttu-id="6bb12-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6bb12-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6bb12-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6bb12-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="6bb12-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6bb12-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="6bb12-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="6bb12-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="6bb12-119">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6bb12-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="6bb12-120"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="6bb12-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="6bb12-121">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="6bb12-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="6bb12-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6bb12-122">Remarks</span></span>

<span data-ttu-id="6bb12-123">Si el PIN está conectado, este método copia el tipo de medio en la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) especificada por *PMT*. El llamador debe liberar el bloque de formato del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6bb12-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="6bb12-124">Puede usar la función [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) o la función auxiliar [**FreeMediaType**](freemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6bb12-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="6bb12-125">Si el PIN no está conectado, este método llena el bloque de memoria especificado por *PMT* y devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="6bb12-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb12-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6bb12-126">Requirements</span></span>



| <span data-ttu-id="6bb12-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb12-127">Requirement</span></span> | <span data-ttu-id="6bb12-128">Value</span><span class="sxs-lookup"><span data-stu-id="6bb12-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb12-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6bb12-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6bb12-130"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb12-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6bb12-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6bb12-131">Library</span></span><br/> | <dl> <span data-ttu-id="6bb12-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6bb12-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb12-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bb12-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb12-134">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6bb12-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

