---
description: La función CopyMediaType copia una \_ estructura de tipo de medio am \_ en otra estructura, incluido el bloque de formato
ms.assetid: 5b47e197-abb5-4b2c-ad65-a506c5e239be
title: Función CopyMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CopyMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e37f277244ae9b82c395d7901917e1fc1e78b35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680586"
---
# <a name="copymediatype-function"></a><span data-ttu-id="7311a-103">CopyMediaType función)</span><span class="sxs-lookup"><span data-stu-id="7311a-103">CopyMediaType function</span></span>

<span data-ttu-id="7311a-104">La función **CopyMediaType** copia una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) en otra estructura, incluido el bloque de formato</span><span class="sxs-lookup"><span data-stu-id="7311a-104">The **CopyMediaType** function copies an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure into another structure, including the format block</span></span>

## <a name="syntax"></a><span data-ttu-id="7311a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7311a-105">Syntax</span></span>


```C++
HRESULT WINAPI CopyMediaType(
         AM_MEDIA_TYPE *pmtTarget,
   const AM_MEDIA_TYPE *pmtSource
);
```



## <a name="parameters"></a><span data-ttu-id="7311a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7311a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7311a-107">*pmtTarget*</span><span class="sxs-lookup"><span data-stu-id="7311a-107">*pmtTarget*</span></span> 
</dt> <dd>

<span data-ttu-id="7311a-108">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="7311a-108">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="7311a-109">El método copia el tipo de archivo multimedia en esta estructura.</span><span class="sxs-lookup"><span data-stu-id="7311a-109">The method copies the media type into this structure.</span></span>

</dd> <dt>

<span data-ttu-id="7311a-110">*pmtSource*</span><span class="sxs-lookup"><span data-stu-id="7311a-110">*pmtSource*</span></span> 
</dt> <dd>

<span data-ttu-id="7311a-111">Puntero a la estructura [**de \_ \_ tipo de medio**](/windows/win32/api/strmif/ns-strmif-am_media_type) de origen AM que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="7311a-111">Pointer to a source [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to copy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7311a-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7311a-112">Return value</span></span>

<span data-ttu-id="7311a-113">Devuelve S \_ OK o E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="7311a-113">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="7311a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7311a-114">Remarks</span></span>

<span data-ttu-id="7311a-115">Esta función asigna la memoria para el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="7311a-115">This function allocates the memory for the format block.</span></span> <span data-ttu-id="7311a-116">Si el parámetro *pmtTarget* ya contiene un bloque de formato asignado, se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="7311a-116">If the *pmtTarget* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="7311a-117">Para evitar una pérdida de memoria, llame a [**FreeMediaType**](freemediatype.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="7311a-117">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span>

<span data-ttu-id="7311a-118">Después de que el método vuelva, llame a [**FreeMediaType**](freemediatype.md) en *pmtTarget* para liberar el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="7311a-118">After the method returns, call [**FreeMediaType**](freemediatype.md) on *pmtTarget* to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="7311a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7311a-119">Requirements</span></span>



| <span data-ttu-id="7311a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7311a-120">Requirement</span></span> | <span data-ttu-id="7311a-121">Value</span><span class="sxs-lookup"><span data-stu-id="7311a-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7311a-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7311a-122">Header</span></span><br/>  | <dl> <span data-ttu-id="7311a-123"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7311a-123"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="7311a-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7311a-124">Library</span></span><br/> | <dl> <span data-ttu-id="7311a-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7311a-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7311a-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7311a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7311a-127">**Funciones de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="7311a-127">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

 




