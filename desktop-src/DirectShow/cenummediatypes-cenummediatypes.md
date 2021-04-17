---
description: Método de constructor.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructor CEnumMediaTypes. CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e17357d90c57f1a7d489d07fa56206343f50788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660869"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="f3b5e-103">Constructor CEnumMediaTypes. CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="f3b5e-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="f3b5e-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="f3b5e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3b5e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f3b5e-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="f3b5e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f3b5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b5e-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="f3b5e-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b5e-108">Puntero al pin en el que se va a realizar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="f3b5e-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="f3b5e-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="f3b5e-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="f3b5e-110">Puntero a la interfaz [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de un enumerador que se va a clonar o **null**.</span><span class="sxs-lookup"><span data-stu-id="f3b5e-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3b5e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f3b5e-111">Remarks</span></span>

<span data-ttu-id="f3b5e-112">Si *pEnumMediaTypes* es **null**, este método inicializa el enumerador al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f3b5e-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="f3b5e-113">De lo contrario, duplica el estado interno del enumerador especificado por *pEnumMediaTypes*.</span><span class="sxs-lookup"><span data-stu-id="f3b5e-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b5e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b5e-114">Requirements</span></span>



| <span data-ttu-id="f3b5e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b5e-115">Requirement</span></span> | <span data-ttu-id="f3b5e-116">Value</span><span class="sxs-lookup"><span data-stu-id="f3b5e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b5e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3b5e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f3b5e-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f3b5e-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f3b5e-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f3b5e-119">Library</span></span><br/> | <dl> <span data-ttu-id="f3b5e-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f3b5e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3b5e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f3b5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3b5e-122">**Clase CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="f3b5e-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




