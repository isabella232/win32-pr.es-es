---
description: Obtenga información sobre el método CMediaType. CMediaType constructor (mtype. h). Este método usa el parámetro ' majortype '.
ms.assetid: 89356578-0509-46c1-abd4-421688017f1d
title: 'Constructor CMediaType. CMediaType (mtype. h): parámetro majortype'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a99717e41424a99b3c1e79674426fb14c5b57b9d
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678864"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---majortype-parameter"></a><span data-ttu-id="6290e-104">Constructor CMediaType. CMediaType (mtype. h): parámetro majortype</span><span class="sxs-lookup"><span data-stu-id="6290e-104">CMediaType.CMediaType constructor (Mtype.h) - majortype parameter</span></span>

<span data-ttu-id="6290e-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="6290e-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6290e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6290e-106">Syntax</span></span>


```C++
CMediaType(
   const GUID *majortype
);
```



## <a name="parameters"></a><span data-ttu-id="6290e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6290e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6290e-108">*majortype*</span><span class="sxs-lookup"><span data-stu-id="6290e-108">*majortype*</span></span> 
</dt> <dd>

<span data-ttu-id="6290e-109">Puntero a un **GUID** de tipo principal.</span><span class="sxs-lookup"><span data-stu-id="6290e-109">Pointer to a major type **GUID**.</span></span> <span data-ttu-id="6290e-110">El constructor inicializa el GUID de tipo principal en este valor.</span><span class="sxs-lookup"><span data-stu-id="6290e-110">The constructor initializes the major type GUID to this value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6290e-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6290e-111">Remarks</span></span>

<span data-ttu-id="6290e-112">El constructor llama al método [**CMediaType:: InitMediaType**](cmediatype-initmediatype.md) para inicializar el tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="6290e-112">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="6290e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6290e-113">Requirements</span></span>

| <span data-ttu-id="6290e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6290e-114">Requirement</span></span>                   | <span data-ttu-id="6290e-115">Value</span><span class="sxs-lookup"><span data-stu-id="6290e-115">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6290e-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6290e-116">Header</span></span>  | <span data-ttu-id="6290e-117">Mtype. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="6290e-117">Mtype.h (include Streams.h)</span></span>                                                                                     |
| <span data-ttu-id="6290e-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6290e-118">Library</span></span> | <span data-ttu-id="6290e-119">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="6290e-119">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="6290e-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6290e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6290e-121">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="6290e-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




