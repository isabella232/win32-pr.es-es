---
description: El método Set establece el tipo de medio desde otro tipo de medio.
ms.assetid: b3cf65c2-48db-4ee0-9a74-c1652f017eed
title: 'Método CMediaType. set (mtype. h): parámetro mtype [Ref]'
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
ms.openlocfilehash: e8fd9145ee33dbe4b589b34833836466efa62ada
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389090"
---
# <a name="cmediatypeset-method-mtypeh"></a><span data-ttu-id="11ce7-103">Método CMediaType. set (mtype. h)</span><span class="sxs-lookup"><span data-stu-id="11ce7-103">CMediaType.Set method (Mtype.h)</span></span>

<span data-ttu-id="11ce7-104">El `Set` método establece el tipo de medio desde otro tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="11ce7-104">The `Set` method sets the media type from another media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="11ce7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11ce7-105">Syntax</span></span>


```C++
HRESULT Set(
  [ref] const AM_MEDIA_TYPE &mtype
);
```



## <a name="parameters"></a><span data-ttu-id="11ce7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11ce7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11ce7-107">*mtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="11ce7-107">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="11ce7-108">Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="11ce7-108">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11ce7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11ce7-109">Return value</span></span>

<span data-ttu-id="11ce7-110">Devuelve S \_ OK o E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="11ce7-110">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="11ce7-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11ce7-111">Remarks</span></span>

<span data-ttu-id="11ce7-112">Este método copia el tipo de medio completo de *mtype*.</span><span class="sxs-lookup"><span data-stu-id="11ce7-112">This method copies the entire media type from *mtype*.</span></span>

## <a name="requirements"></a><span data-ttu-id="11ce7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11ce7-113">Requirements</span></span>



| <span data-ttu-id="11ce7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="11ce7-114">Requirement</span></span> | <span data-ttu-id="11ce7-115">Value</span><span class="sxs-lookup"><span data-stu-id="11ce7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11ce7-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11ce7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="11ce7-117"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11ce7-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="11ce7-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="11ce7-118">Library</span></span><br/> | <dl> <span data-ttu-id="11ce7-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="11ce7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11ce7-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="11ce7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11ce7-121">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="11ce7-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




