---
description: El método AllocFormatBuffer asigna memoria para el bloque de formato.
ms.assetid: 5ff716c7-f9cf-4b1c-9d3a-62ab955c1392
title: Método CMediaType. AllocFormatBuffer (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.AllocFormatBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6a9314fd06734adcc367b7be34dc8d6d1b9d996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670321"
---
# <a name="cmediatypeallocformatbuffer-method"></a><span data-ttu-id="ed8ba-103">CMediaType. AllocFormatBuffer, método</span><span class="sxs-lookup"><span data-stu-id="ed8ba-103">CMediaType.AllocFormatBuffer method</span></span>

<span data-ttu-id="ed8ba-104">El `AllocFormatBuffer` método asigna memoria para el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-104">The `AllocFormatBuffer` method allocates memory for the format block.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8ba-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed8ba-105">Syntax</span></span>


```C++
BYTE* AllocFormatBuffer(
   ULONG length
);
```



## <a name="parameters"></a><span data-ttu-id="ed8ba-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed8ba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8ba-107">*length*</span><span class="sxs-lookup"><span data-stu-id="ed8ba-107">*length*</span></span> 
</dt> <dd>

<span data-ttu-id="ed8ba-108">Tamaño necesario para el bloque de formato, en bytes.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-108">Size required for the format block, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed8ba-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed8ba-109">Return value</span></span>

<span data-ttu-id="ed8ba-110">Devuelve un puntero al nuevo bloque si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-110">Returns a pointer to the new block if successful.</span></span> <span data-ttu-id="ed8ba-111">De lo contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-111">Otherwise, returns **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed8ba-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ed8ba-112">Remarks</span></span>

<span data-ttu-id="ed8ba-113">Si el método asigna correctamente un nuevo bloque de formato, libera el bloque de formato existente.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-113">If the method successfully allocates a new format block, it frees the existing format block.</span></span> <span data-ttu-id="ed8ba-114">Si se produce un error en la asignación, el método deja el bloque de formato existente.</span><span class="sxs-lookup"><span data-stu-id="ed8ba-114">If the allocation fails, the method leaves the existing format block.</span></span>

<span data-ttu-id="ed8ba-115">El método actualiza los miembros **cbFormat** y **pbFormat** de la estructura de **\_ \_ tipo de medio am** .</span><span class="sxs-lookup"><span data-stu-id="ed8ba-115">The method updates the **cbFormat** and **pbFormat** members of the **AM\_MEDIA\_TYPE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed8ba-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed8ba-116">Requirements</span></span>



| <span data-ttu-id="ed8ba-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed8ba-117">Requirement</span></span> | <span data-ttu-id="ed8ba-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed8ba-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8ba-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed8ba-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ed8ba-120"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ba-120"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ed8ba-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed8ba-121">Library</span></span><br/> | <dl> <span data-ttu-id="ed8ba-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ed8ba-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8ba-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed8ba-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8ba-124">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="ed8ba-124">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




