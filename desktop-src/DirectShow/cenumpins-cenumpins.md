---
description: Método de constructor.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructor CEnumPins. CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671155"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="128c1-103">Constructor CEnumPins. CEnumPins</span><span class="sxs-lookup"><span data-stu-id="128c1-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="128c1-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="128c1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="128c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="128c1-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="128c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="128c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="128c1-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="128c1-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="128c1-108">Puntero al filtro en el que se enumeran los pin.</span><span class="sxs-lookup"><span data-stu-id="128c1-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="128c1-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="128c1-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="128c1-110">Puntero a la interfaz [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de un enumerador que se va a clonar o **null**.</span><span class="sxs-lookup"><span data-stu-id="128c1-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="128c1-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="128c1-111">Remarks</span></span>

<span data-ttu-id="128c1-112">Si *pEnumPins* es **null**, este método inicializa el enumerador al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="128c1-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="128c1-113">De lo contrario, duplica el estado interno del enumerador especificado por *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="128c1-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="128c1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="128c1-114">Requirements</span></span>



| <span data-ttu-id="128c1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="128c1-115">Requirement</span></span> | <span data-ttu-id="128c1-116">Value</span><span class="sxs-lookup"><span data-stu-id="128c1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="128c1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="128c1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="128c1-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="128c1-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="128c1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="128c1-119">Library</span></span><br/> | <dl> <span data-ttu-id="128c1-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="128c1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="128c1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="128c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="128c1-122">**Clase CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="128c1-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




