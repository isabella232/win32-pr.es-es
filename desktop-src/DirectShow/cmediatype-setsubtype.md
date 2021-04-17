---
description: El método SetSubtype especifica el subtipo.
ms.assetid: cf52e0dc-d75b-408e-a63c-481d55151d4a
title: Método CMediaType. SetSubtype (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetSubtype
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6474777b1b2e91ce0b676fdc7dbd572d7c622f0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670732"
---
# <a name="cmediatypesetsubtype-method"></a><span data-ttu-id="883b0-103">CMediaType. SetSubtype, método</span><span class="sxs-lookup"><span data-stu-id="883b0-103">CMediaType.SetSubtype method</span></span>

<span data-ttu-id="883b0-104">El `SetSubtype` método especifica el subtipo.</span><span class="sxs-lookup"><span data-stu-id="883b0-104">The `SetSubtype` method specifies the subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="883b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="883b0-105">Syntax</span></span>


```C++
void SetSubtype(
   const GUID *psubtype
);
```



## <a name="parameters"></a><span data-ttu-id="883b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="883b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="883b0-107">*psubtype*</span><span class="sxs-lookup"><span data-stu-id="883b0-107">*psubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="883b0-108">Puntero a un **GUID** que especifica el subtipo.</span><span class="sxs-lookup"><span data-stu-id="883b0-108">Pointer to a **GUID** that specifies the subtype.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="883b0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="883b0-109">Return value</span></span>

<span data-ttu-id="883b0-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="883b0-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="883b0-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="883b0-111">Requirements</span></span>



| <span data-ttu-id="883b0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="883b0-112">Requirement</span></span> | <span data-ttu-id="883b0-113">Value</span><span class="sxs-lookup"><span data-stu-id="883b0-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="883b0-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="883b0-114">Header</span></span><br/>  | <dl> <span data-ttu-id="883b0-115"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="883b0-115"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="883b0-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="883b0-116">Library</span></span><br/> | <dl> <span data-ttu-id="883b0-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="883b0-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883b0-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="883b0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883b0-119">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="883b0-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




