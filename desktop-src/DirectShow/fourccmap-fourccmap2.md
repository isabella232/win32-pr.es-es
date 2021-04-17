---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método usa el parámetro ' FourCC '.
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: 'Constructor FOURCCMap:: FOURCCMap (FourCC. h): parámetro FourCC'
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105653292"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="eed0f-104">Constructor FOURCCMap:: FOURCCMap (FourCC. h): parámetro FourCC</span><span class="sxs-lookup"><span data-stu-id="eed0f-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="eed0f-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="eed0f-105">Constructor method.</span></span> <span data-ttu-id="eed0f-106">Constructor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y los subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="eed0f-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="eed0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eed0f-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="eed0f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eed0f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eed0f-109">*FourCC*</span><span class="sxs-lookup"><span data-stu-id="eed0f-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="eed0f-110">**DWORD** que especifica el FourCC.</span><span class="sxs-lookup"><span data-stu-id="eed0f-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eed0f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eed0f-111">Remarks</span></span>

<span data-ttu-id="eed0f-112">Si este objeto se construye con el código **FourCC** , se crea un **GUID** para que coincida.</span><span class="sxs-lookup"><span data-stu-id="eed0f-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="eed0f-113">Si este objeto se crea con un **GUID** existente, el valor de **FourCC** del objeto se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="eed0f-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="eed0f-114">Después, el valor de **FourCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="eed0f-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="eed0f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eed0f-115">Requirements</span></span>

| <span data-ttu-id="eed0f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eed0f-116">Requirement</span></span> | <span data-ttu-id="eed0f-117">Value</span><span class="sxs-lookup"><span data-stu-id="eed0f-117">Value</span></span> |
|-|-|
| <span data-ttu-id="eed0f-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eed0f-118">Header</span></span>  | <span data-ttu-id="eed0f-119">FourCC. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="eed0f-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="eed0f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eed0f-120">Library</span></span> | <span data-ttu-id="eed0f-121">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="eed0f-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="eed0f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="eed0f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eed0f-123">**Clase FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="eed0f-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




