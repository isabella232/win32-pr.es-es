---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método no usa ningún parámetro.
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: 'Constructor FOURCCMap:: FOURCCMap (FourCC. h): no hay parámetros'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678863"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="7f1a3-104">Constructor FOURCCMap:: FOURCCMap (FourCC. h): no hay parámetros</span><span class="sxs-lookup"><span data-stu-id="7f1a3-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="7f1a3-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="7f1a3-105">Constructor method.</span></span> <span data-ttu-id="7f1a3-106">Constructor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y los subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="7f1a3-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f1a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7f1a3-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="7f1a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7f1a3-108">Parameters</span></span>

<span data-ttu-id="7f1a3-109">Este constructor no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7f1a3-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f1a3-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7f1a3-110">Remarks</span></span>

<span data-ttu-id="7f1a3-111">Si este objeto se construye con el código **FourCC** , se crea un **GUID** para que coincida.</span><span class="sxs-lookup"><span data-stu-id="7f1a3-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="7f1a3-112">Si este objeto se crea con un **GUID** existente, el valor de **FourCC** del objeto se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="7f1a3-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="7f1a3-113">Después, el valor de **FourCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7f1a3-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f1a3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f1a3-114">Requirements</span></span>


| <span data-ttu-id="7f1a3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f1a3-115">Requirement</span></span> | <span data-ttu-id="7f1a3-116">Value</span><span class="sxs-lookup"><span data-stu-id="7f1a3-116">Value</span></span> |
|-|-|
| <span data-ttu-id="7f1a3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7f1a3-117">Header</span></span>  | <span data-ttu-id="7f1a3-118">FourCC. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="7f1a3-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="7f1a3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f1a3-119">Library</span></span> | <span data-ttu-id="7f1a3-120">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="7f1a3-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="7f1a3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="7f1a3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f1a3-122">**Clase FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="7f1a3-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




