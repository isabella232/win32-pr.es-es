---
description: La función CreateMediaType asigna una nueva \_ estructura de tipo de medio am \_ , incluido el bloque de formato.
ms.assetid: 841a8c51-6027-49d6-b3d8-b5e21e3d5f13
title: Función CreateMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ea3eaee03ebf98ac22d702bde9a165fda21e51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680861"
---
# <a name="createmediatype-function"></a><span data-ttu-id="22d98-103">CreateMediaType función)</span><span class="sxs-lookup"><span data-stu-id="22d98-103">CreateMediaType function</span></span>

<span data-ttu-id="22d98-104">La función **CreateMediaType** asigna una nueva estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , incluido el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="22d98-104">The **CreateMediaType** function allocates a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d98-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22d98-105">Syntax</span></span>


```C++
AM_MEDIA_TYPE* WINAPI CreateMediaType(
   AM_MEDIA_TYPE const *pSrc
);
```



## <a name="parameters"></a><span data-ttu-id="22d98-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d98-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="22d98-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="22d98-108">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="22d98-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="22d98-109">El método copia esta estructura en la nueva estructura.</span><span class="sxs-lookup"><span data-stu-id="22d98-109">The method copies this structure into the new structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d98-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22d98-110">Return value</span></span>

<span data-ttu-id="22d98-111">Devuelve una nueva estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) , o **null** si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="22d98-111">Returns a new [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, or **NULL** if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="22d98-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="22d98-112">Remarks</span></span>

<span data-ttu-id="22d98-113">Para liberar la memoria asignada por esta función, llame a [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="22d98-113">To free the memory allocated by this function, call [**DeleteMediaType**](deletemediatype.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22d98-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22d98-114">Requirements</span></span>



| <span data-ttu-id="22d98-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d98-115">Requirement</span></span> | <span data-ttu-id="22d98-116">Value</span><span class="sxs-lookup"><span data-stu-id="22d98-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d98-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="22d98-117">Header</span></span><br/>  | <dl> <span data-ttu-id="22d98-118"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="22d98-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="22d98-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="22d98-119">Library</span></span><br/> | <dl> <span data-ttu-id="22d98-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="22d98-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d98-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="22d98-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d98-122">**Funciones de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="22d98-122">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




