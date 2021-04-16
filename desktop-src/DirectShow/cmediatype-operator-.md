---
description: 'El método CMediaType. CMediaType:: Operator = (mtype. h) sobrecarga el operador de asignación para copiar un tipo de medio.'
ms.assetid: 28115548-97a5-426d-97cd-c5e759d8e39e
title: 'CMediaType. CMediaType:: Operator = Method (mtype. h)-cmtype parámetro'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56eb16c99d867e3cad3be9018c279e3e69f4f122
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678871"
---
# <a name="cmediatypecmediatypeoperator-method-mtypeh---cmtype-parameter"></a><span data-ttu-id="c5e51-103">CMediaType. CMediaType:: Operator = Method (mtype. h)-cmtype parámetro</span><span class="sxs-lookup"><span data-stu-id="c5e51-103">CMediaType.CMediaType::operator= method (Mtype.h) - cmtype parameter</span></span>

<span data-ttu-id="c5e51-104">Este operador sobrecarga el operador de asignación para copiar un tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="c5e51-104">This operator overloads the assignment operator to copy a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5e51-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5e51-105">Syntax</span></span>


```C++
CMediaType& CMediaType::operator=(
  [ref] const CMediaType &cmtype
);
```



## <a name="parameters"></a><span data-ttu-id="c5e51-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5e51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e51-107">*cmtype* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="c5e51-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="c5e51-108">Referencia a un objeto **CMediaType** .</span><span class="sxs-lookup"><span data-stu-id="c5e51-108">Reference to a **CMediaType** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e51-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5e51-109">Return value</span></span>

<span data-ttu-id="c5e51-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="c5e51-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e51-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5e51-111">Requirements</span></span>

| <span data-ttu-id="c5e51-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5e51-112">Requirement</span></span>                   | <span data-ttu-id="c5e51-113">Value</span><span class="sxs-lookup"><span data-stu-id="c5e51-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e51-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5e51-114">Header</span></span>  | <span data-ttu-id="c5e51-115">Mtype. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="c5e51-115">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="c5e51-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5e51-116">Library</span></span> | <span data-ttu-id="c5e51-117">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="c5e51-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="c5e51-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5e51-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e51-119">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="c5e51-119">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




