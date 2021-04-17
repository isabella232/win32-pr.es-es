---
description: La función DeleteMediaType elimina una estructura de tipo de medio AM asignada \_ \_ , incluido el bloque de formato.
ms.assetid: 970f6b2b-2bf5-418d-b4ae-637561cd6765
title: Función DeleteMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: db0de399ab1be7808370a6d0da57c4c3ca7b8de1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660375"
---
# <a name="deletemediatype-function"></a><span data-ttu-id="d1163-103">DeleteMediaType función)</span><span class="sxs-lookup"><span data-stu-id="d1163-103">DeleteMediaType function</span></span>

<span data-ttu-id="d1163-104">La función **DeleteMediaType** elimina una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada, incluido el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="d1163-104">The **DeleteMediaType** function deletes an allocated [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, including the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1163-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1163-105">Syntax</span></span>


```C++
void WINAPI DeleteMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="d1163-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d1163-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1163-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="d1163-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="d1163-108">Puntero a una estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="d1163-108">A pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1163-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1163-109">Return value</span></span>

<span data-ttu-id="d1163-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d1163-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1163-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1163-111">Remarks</span></span>

<span data-ttu-id="d1163-112">Use esta función para liberar cualquier estructura de tipo de medio que se haya asignado mediante [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) o [**CreateMediaType**](createmediatype.md).</span><span class="sxs-lookup"><span data-stu-id="d1163-112">Use this function to release any media type structure that was allocated using either [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) or [**CreateMediaType**](createmediatype.md).</span></span>

<span data-ttu-id="d1163-113">Esta función se define en la biblioteca de [clases base de DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="d1163-113">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="d1163-114">Si prefiere no vincular a la biblioteca de clases base, puede usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="d1163-114">If you prefer not to link to the base class library, you can use the following code:</span></span>


```C++
// Release the format block for a media type.

void _FreeMediaType(AM_MEDIA_TYPE& mt)
{
    if (mt.cbFormat != 0)
    {
        CoTaskMemFree((PVOID)mt.pbFormat);
        mt.cbFormat = 0;
        mt.pbFormat = NULL;
    }
    if (mt.pUnk != NULL)
    {
        // pUnk should not be used.
        mt.pUnk->Release();
        mt.pUnk = NULL;
    }
}


// Delete a media type structure that was allocated on the heap.
void _DeleteMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt != NULL)
    {
        _FreeMediaType(*pmt); 
        CoTaskMemFree(pmt);
    }
}
```





## <a name="requirements"></a><span data-ttu-id="d1163-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1163-115">Requirements</span></span>



| <span data-ttu-id="d1163-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1163-116">Requirement</span></span> | <span data-ttu-id="d1163-117">Value</span><span class="sxs-lookup"><span data-stu-id="d1163-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1163-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d1163-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d1163-119"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1163-119"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d1163-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d1163-120">Library</span></span><br/> | <dl> <span data-ttu-id="d1163-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d1163-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1163-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1163-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1163-123">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="d1163-123">**FreeMediaType**</span></span>](freemediatype.md)
</dt> <dt>

[<span data-ttu-id="d1163-124">**Funciones de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="d1163-124">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

