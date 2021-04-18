---
description: Recupera el valor de FOURCC&\# 160; DWORD del objeto FOURCCMap.
ms.assetid: bb382a57-8499-44c0-b287-2d31f5f5d1d0
title: 'FOURCCMap:: GetFOURCC (método) (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.GetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c76493ff172f7a5611367fd50aa3b7957cf5441b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653443"
---
# <a name="fourccmapgetfourcc-method"></a><span data-ttu-id="81be7-103">FOURCCMap:: GetFOURCC (método)</span><span class="sxs-lookup"><span data-stu-id="81be7-103">FOURCCMap::GetFOURCC method</span></span>

<span data-ttu-id="81be7-104">Recupera el **valor DWORD** de **FourCC** del objeto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="81be7-104">Retrieves the **FOURCC** **DWORD** from the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="81be7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81be7-105">Syntax</span></span>


```C++
DWORD GetFOURCC();
```



## <a name="parameters"></a><span data-ttu-id="81be7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="81be7-106">Parameters</span></span>

<span data-ttu-id="81be7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="81be7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="81be7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="81be7-108">Return value</span></span>

<span data-ttu-id="81be7-109">Devuelve el valor **DWORD** de **FourCC** .</span><span class="sxs-lookup"><span data-stu-id="81be7-109">Returns the **FOURCC** **DWORD** value.</span></span> <span data-ttu-id="81be7-110">Tenga en cuenta que si crea un **GUID** que no se derivó originalmente de un **FourCC**, el valor devuelto será esencialmente aleatorio.</span><span class="sxs-lookup"><span data-stu-id="81be7-110">Note that if you construct a **GUID** that was not originally derived from a **FOURCC**, the return value will be essentially random.</span></span>

## <a name="requirements"></a><span data-ttu-id="81be7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81be7-111">Requirements</span></span>



| <span data-ttu-id="81be7-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="81be7-112">Requirement</span></span> | <span data-ttu-id="81be7-113">Value</span><span class="sxs-lookup"><span data-stu-id="81be7-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81be7-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="81be7-114">Header</span></span><br/>  | <dl> <span data-ttu-id="81be7-115"><dt>FourCC. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="81be7-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="81be7-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="81be7-116">Library</span></span><br/> | <dl> <span data-ttu-id="81be7-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="81be7-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81be7-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="81be7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81be7-119">**Clase FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="81be7-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




