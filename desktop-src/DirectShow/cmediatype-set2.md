---
description: El método Set establece el tipo de medio desde otro tipo de medio.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: Método CMediaType. set (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: afe99c3f5ee10e6aacd3dadf69af320b110688af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670557"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="42d2d-103">Método CMediaType. set (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="42d2d-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="42d2d-104">El `Set` método establece el tipo de medio desde otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="42d2d-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="42d2d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42d2d-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="42d2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42d2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42d2d-107">*mtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="42d2d-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="42d2d-108">Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="42d2d-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42d2d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42d2d-109">Return value</span></span>

<span data-ttu-id="42d2d-110">Devuelve S \_ OK o E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="42d2d-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="42d2d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42d2d-111">Remarks</span></span>

<span data-ttu-id="42d2d-112">Este método copia el tipo de medio completo de *mtype*.</span><span class="sxs-lookup"><span data-stu-id="42d2d-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="42d2d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42d2d-113">Requirements</span></span>



| <span data-ttu-id="42d2d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="42d2d-114">Requirement</span></span> | <span data-ttu-id="42d2d-115">Value</span><span class="sxs-lookup"><span data-stu-id="42d2d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42d2d-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42d2d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="42d2d-117"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42d2d-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="42d2d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42d2d-118">Library</span></span><br/> | <dl> <span data-ttu-id="42d2d-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="42d2d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42d2d-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="42d2d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42d2d-121">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="42d2d-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




