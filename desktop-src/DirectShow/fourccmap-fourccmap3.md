---
description: Método de constructor que proporciona la asignación entre los tipos DWORD de formato multimedia de estilo antiguo y los subtipos GUID. Este método usa el parámetro ' pguid '.
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: 'FOURCCMap:: FOURCCMap constructor (FourCC. h): parámetro pguid'
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678868"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="d5575-104">FOURCCMap:: FOURCCMap constructor (FourCC. h): parámetro pguid</span><span class="sxs-lookup"><span data-stu-id="d5575-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="d5575-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="d5575-105">Constructor method.</span></span> <span data-ttu-id="d5575-106">Constructor proporciona la asignación entre los tipos **DWORD** de formato multimedia de estilo antiguo y los subtipos de **GUID** .</span><span class="sxs-lookup"><span data-stu-id="d5575-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5575-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5575-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="d5575-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5575-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5575-109">*pguid*</span><span class="sxs-lookup"><span data-stu-id="d5575-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="d5575-110">Puntero al identificador único global (**GUID**).</span><span class="sxs-lookup"><span data-stu-id="d5575-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d5575-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d5575-111">Remarks</span></span>

<span data-ttu-id="d5575-112">Si este objeto se construye con el código **FourCC** , se crea un **GUID** para que coincida.</span><span class="sxs-lookup"><span data-stu-id="d5575-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="d5575-113">Si este objeto se crea con un **GUID** existente, el valor de **FourCC** del objeto se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="d5575-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="d5575-114">Después, el valor de **FourCC** se puede establecer o recuperar mediante las funciones miembro [**SetFOURCC**](fourccmap-setfourcc.md) y [**GetFOURCC**](fourccmap-getfourcc.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d5575-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5575-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5575-115">Requirements</span></span>

| <span data-ttu-id="d5575-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5575-116">Requirement</span></span> | <span data-ttu-id="d5575-117">Value</span><span class="sxs-lookup"><span data-stu-id="d5575-117">Value</span></span> |
|-|-|
| <span data-ttu-id="d5575-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d5575-118">Header</span></span>  | <span data-ttu-id="d5575-119">FourCC. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="d5575-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="d5575-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d5575-120">Library</span></span> | <span data-ttu-id="d5575-121">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="d5575-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="d5575-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5575-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5575-123">**Clase FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="d5575-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




