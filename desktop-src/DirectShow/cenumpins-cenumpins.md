---
description: 'Constructor CEnumPins.CEnumPins: método constructor.'
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Constructor CEnumPins.CEnumPins (Amfilter.h)
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099233"
---
# <a name="cenumpinscenumpins-constructor"></a><span data-ttu-id="f1e3f-103">Constructor CEnumPins.CEnumPins</span><span class="sxs-lookup"><span data-stu-id="f1e3f-103">CEnumPins.CEnumPins constructor</span></span>

<span data-ttu-id="f1e3f-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1e3f-105">Syntax</span></span>


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a><span data-ttu-id="f1e3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1e3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1e3f-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="f1e3f-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="f1e3f-108">Puntero al filtro en el que se enumeran los pines.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-108">Pointer to the filter on which to enumerate the pins.</span></span>

</dd> <dt>

<span data-ttu-id="f1e3f-109">*pEnumPins*</span><span class="sxs-lookup"><span data-stu-id="f1e3f-109">*pEnumPins*</span></span> 
</dt> <dd>

<span data-ttu-id="f1e3f-110">Puntero a la [**interfaz IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) de un enumerador que se clona, o **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f1e3f-110">Pointer to the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface of an enumerator to clone, or **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1e3f-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f1e3f-111">Remarks</span></span>

<span data-ttu-id="f1e3f-112">Si *pEnumPins* es **NULL,** este método inicializa el enumerador al principio de la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-112">If *pEnumPins* is **NULL**, this method initializes the enumerator to the beginning of the enumeration sequence.</span></span> <span data-ttu-id="f1e3f-113">De lo contrario, duplica el estado interno del enumerador especificado por *pEnumPins*.</span><span class="sxs-lookup"><span data-stu-id="f1e3f-113">Otherwise, it duplicates the internal state of the enumerator specified by *pEnumPins*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e3f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1e3f-114">Requirements</span></span>



| <span data-ttu-id="f1e3f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e3f-115">Requirement</span></span> | <span data-ttu-id="f1e3f-116">Value</span><span class="sxs-lookup"><span data-stu-id="f1e3f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e3f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1e3f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f1e3f-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1e3f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1e3f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1e3f-119">Library</span></span><br/> | <dl> <span data-ttu-id="f1e3f-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f1e3f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e3f-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f1e3f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e3f-122">**CEnumPins (clase)**</span><span class="sxs-lookup"><span data-stu-id="f1e3f-122">**CEnumPins Class**</span></span>](cenumpins.md)
</dt> </dl>

 

 




