---
description: Establece la parte FOURCC del objeto FOURCCMap.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'FOURCCMap:: SetFOURCC (método) (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690579"
---
# <a name="fourccmapsetfourcc-method"></a><span data-ttu-id="04e2a-103">FOURCCMap:: SetFOURCC (método)</span><span class="sxs-lookup"><span data-stu-id="04e2a-103">FOURCCMap::SetFOURCC method</span></span>

<span data-ttu-id="04e2a-104">Establece la parte **FourCC** del objeto [**FOURCCMap**](fourccmap.md) .</span><span class="sxs-lookup"><span data-stu-id="04e2a-104">Sets the **FOURCC** portion of the [**FOURCCMap**](fourccmap.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="04e2a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="04e2a-105">Syntax</span></span>


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="04e2a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="04e2a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04e2a-107">*pguid*</span><span class="sxs-lookup"><span data-stu-id="04e2a-107">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="04e2a-108">Puntero a la parte del identificador único global (**GUID**) devuelta del objeto **FOURCCMap** .</span><span class="sxs-lookup"><span data-stu-id="04e2a-108">Pointer to the returned globally unique identifier (**GUID**) part of the **FOURCCMap** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04e2a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="04e2a-109">Return value</span></span>

<span data-ttu-id="04e2a-110">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="04e2a-110">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04e2a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04e2a-111">Requirements</span></span>



| <span data-ttu-id="04e2a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="04e2a-112">Requirement</span></span> | <span data-ttu-id="04e2a-113">Value</span><span class="sxs-lookup"><span data-stu-id="04e2a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04e2a-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="04e2a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="04e2a-115"><dt>FourCC. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="04e2a-115"><dt>Fourcc.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="04e2a-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04e2a-116">Library</span></span><br/> | <dl> <span data-ttu-id="04e2a-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="04e2a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04e2a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="04e2a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04e2a-119">**Clase FOURCCMap**</span><span class="sxs-lookup"><span data-stu-id="04e2a-119">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




