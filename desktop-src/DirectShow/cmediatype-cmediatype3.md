---
description: Obtenga información sobre el método CMediaType. CMediaType constructor (mtype. h). Este método usa los parámetros ' mtype ' y ' PHR '.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: 'Constructor CMediaType. CMediaType (mtype. h): parámetros mtype y PHR'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105670279"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a><span data-ttu-id="c83bd-104">Constructor CMediaType. CMediaType (mtype. h): parámetros mtype y PHR</span><span class="sxs-lookup"><span data-stu-id="c83bd-104">CMediaType.CMediaType constructor (Mtype.h) - mtype and phr parameters</span></span>

<span data-ttu-id="c83bd-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="c83bd-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c83bd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c83bd-106">Syntax</span></span>


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="c83bd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c83bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c83bd-108">*mtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="c83bd-108">*mtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c83bd-109">Referencia a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="c83bd-109">Reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="c83bd-110">El constructor copia el tipo de archivo multimedia en el nuevo objeto, incluido el bloque de formato, si existe.</span><span class="sxs-lookup"><span data-stu-id="c83bd-110">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="c83bd-111">*phr*</span><span class="sxs-lookup"><span data-stu-id="c83bd-111">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c83bd-112">Puntero a una variable que recibe un valor HRESULT.</span><span class="sxs-lookup"><span data-stu-id="c83bd-112">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="c83bd-113">Este parámetro puede ser un puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="c83bd-113">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="c83bd-114">De lo contrario, el autor de la llamada debe establecer el valor en es \_ correcto antes de llamar al constructor.</span><span class="sxs-lookup"><span data-stu-id="c83bd-114">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="c83bd-115">Si se produce un error en el constructor, establece el valor en un código de error.</span><span class="sxs-lookup"><span data-stu-id="c83bd-115">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c83bd-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c83bd-116">Remarks</span></span>

<span data-ttu-id="c83bd-117">El constructor llama al método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="c83bd-117">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="c83bd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c83bd-118">Requirements</span></span>

| <span data-ttu-id="c83bd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c83bd-119">Requirement</span></span>                   | <span data-ttu-id="c83bd-120">Value</span><span class="sxs-lookup"><span data-stu-id="c83bd-120">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c83bd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c83bd-121">Header</span></span>  | <span data-ttu-id="c83bd-122">Mtype. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="c83bd-122">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c83bd-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c83bd-123">Library</span></span> | <span data-ttu-id="c83bd-124">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="c83bd-124">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c83bd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="c83bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c83bd-126">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c83bd-126">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




