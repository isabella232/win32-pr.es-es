---
description: El método SetType especifica el tipo principal.
ms.assetid: 3fd93d5e-73ea-453e-8f08-652d5a81239f
title: Método CMediaType. SetType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfcf6ca634bce92701eb89f26dcfb6bdfb51f698
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671521"
---
# <a name="cmediatypesettype-method"></a><span data-ttu-id="0230c-103">CMediaType. SetType, método</span><span class="sxs-lookup"><span data-stu-id="0230c-103">CMediaType.SetType method</span></span>

<span data-ttu-id="0230c-104">El `SetType` método especifica el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="0230c-104">The `SetType` method specifies the major type.</span></span>

## <a name="syntax"></a><span data-ttu-id="0230c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0230c-105">Syntax</span></span>


```C++
void SetType(
   const GUID *ptype
);
```



## <a name="parameters"></a><span data-ttu-id="0230c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0230c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0230c-107">*ptype*</span><span class="sxs-lookup"><span data-stu-id="0230c-107">*ptype*</span></span> 
</dt> <dd>

<span data-ttu-id="0230c-108">Puntero a un **GUID** que especifica el tipo principal.</span><span class="sxs-lookup"><span data-stu-id="0230c-108">Pointer to a **GUID** that specifies the major type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0230c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0230c-109">Return value</span></span>

<span data-ttu-id="0230c-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="0230c-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0230c-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0230c-111">Requirements</span></span>



| <span data-ttu-id="0230c-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0230c-112">Requirement</span></span> | <span data-ttu-id="0230c-113">Value</span><span class="sxs-lookup"><span data-stu-id="0230c-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0230c-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0230c-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0230c-115"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0230c-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0230c-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0230c-116">Library</span></span><br/> | <dl> <span data-ttu-id="0230c-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0230c-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0230c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0230c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0230c-119">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="0230c-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




