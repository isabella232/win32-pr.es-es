---
description: 'Constructor CEnumMediaTypes.CEnumMediaTypes: método constructor.'
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Constructor CEnumMediaTypes.CEnumMediaTypes (Amfilter.h)
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
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095683"
---
# <a name="cenummediatypescenummediatypes-constructor"></a><span data-ttu-id="60fde-103">Constructor CEnumMediaTypes.CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="60fde-103">CEnumMediaTypes.CEnumMediaTypes constructor</span></span>

<span data-ttu-id="60fde-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="60fde-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="60fde-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60fde-105">Syntax</span></span>


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a><span data-ttu-id="60fde-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60fde-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60fde-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="60fde-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="60fde-108">Puntero al pin en el que se va a realizar la enumeración.</span><span class="sxs-lookup"><span data-stu-id="60fde-108">Pointer to the pin on which the enumeration is to be performed.</span></span>

</dd> <dt>

<span data-ttu-id="60fde-109">*pEnumMediaTypes*</span><span class="sxs-lookup"><span data-stu-id="60fde-109">*pEnumMediaTypes*</span></span> 
</dt> <dd>

<span data-ttu-id="60fde-110">Puntero a la [**interfaz IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) de un enumerador que se clona, o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="60fde-110">Pointer to the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60fde-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="60fde-111">Remarks</span></span>

<span data-ttu-id="60fde-112">Si *pEnumMediaTypes* es **NULL,** este método inicializa el enumerador al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="60fde-112">If *pEnumMediaTypes* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="60fde-113">De lo contrario, duplica el estado interno del enumerador especificado por *pEnumMediaTypes*.</span><span class="sxs-lookup"><span data-stu-id="60fde-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumMediaTypes*.</span></span>

## <a name="requirements"></a><span data-ttu-id="60fde-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60fde-114">Requirements</span></span>



| <span data-ttu-id="60fde-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="60fde-115">Requirement</span></span> | <span data-ttu-id="60fde-116">Value</span><span class="sxs-lookup"><span data-stu-id="60fde-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60fde-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60fde-117">Header</span></span><br/>  | <dl> <span data-ttu-id="60fde-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="60fde-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60fde-119">Library</span></span><br/> | <dl> <span data-ttu-id="60fde-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="60fde-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60fde-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="60fde-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60fde-122">**CEnumMediaTypes (clase)**</span><span class="sxs-lookup"><span data-stu-id="60fde-122">**CEnumMediaTypes Class**</span></span>](cenummediatypes.md)
</dt> </dl>

 

 




