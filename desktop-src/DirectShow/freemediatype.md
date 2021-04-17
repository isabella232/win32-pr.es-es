---
description: La función FreeMediaType elimina el bloque de formato en una \_ estructura de tipo de medio am \_ .
ms.assetid: b7ec335e-518d-4aa6-8cde-8cb92184d0b0
title: Función FreeMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f332ccc9a60473a9d814481b759221dc6468d5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680873"
---
# <a name="freemediatype-function"></a><span data-ttu-id="f0799-103">FreeMediaType función)</span><span class="sxs-lookup"><span data-stu-id="f0799-103">FreeMediaType function</span></span>

<span data-ttu-id="f0799-104">La función **FreeMediaType** elimina el bloque de formato en una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="f0799-104">The **FreeMediaType** function deletes the format block in an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0799-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0799-105">Syntax</span></span>


```C++
void FreeMediaType(
   AM_MEDIA_TYPE &mt
);
```



## <a name="parameters"></a><span data-ttu-id="f0799-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f0799-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0799-107">*MT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="f0799-107">*mt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="f0799-108">Referencia a una estructura [**de \_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="f0799-108">A reference to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0799-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f0799-109">Return value</span></span>

<span data-ttu-id="f0799-110">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f0799-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0799-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f0799-111">Remarks</span></span>

<span data-ttu-id="f0799-112">El bloque de formato se asigna en el montón.</span><span class="sxs-lookup"><span data-stu-id="f0799-112">The format block is allocated on the heap.</span></span> <span data-ttu-id="f0799-113">El miembro **pbFormat** del [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) apunta al bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="f0799-113">The **pbFormat** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) points to the format block.</span></span> <span data-ttu-id="f0799-114">Use esta función para liberar solo el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="f0799-114">Use this function to free just the format block.</span></span> <span data-ttu-id="f0799-115">Para eliminar una estructura **de \_ \_ tipo de medio am** asignada, llame a [**DeleteMediaType**](deletemediatype.md).</span><span class="sxs-lookup"><span data-stu-id="f0799-115">To delete an allocated **AM\_MEDIA\_TYPE** structure, call [**DeleteMediaType**](deletemediatype.md).</span></span>

<span data-ttu-id="f0799-116">Esta función se define en la biblioteca de [clases base de DirectShow](directshow-base-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="f0799-116">This function is defined in the [DirectShow Base Classes](directshow-base-classes.md) library.</span></span> <span data-ttu-id="f0799-117">Si prefiere no vincular a la biblioteca de clases base, puede usar el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="f0799-117">If you prefer not to link to the base class library, you can use the following code:</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="f0799-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0799-118">Requirements</span></span>



| <span data-ttu-id="f0799-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0799-119">Requirement</span></span> | <span data-ttu-id="f0799-120">Value</span><span class="sxs-lookup"><span data-stu-id="f0799-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0799-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f0799-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f0799-122"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f0799-122"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="f0799-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0799-123">Library</span></span><br/> | <dl> <span data-ttu-id="f0799-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f0799-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0799-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0799-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0799-126">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="f0799-126">**DeleteMediaType**</span></span>](deletemediatype.md)
</dt> <dt>

[<span data-ttu-id="f0799-127">**Funciones de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="f0799-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




