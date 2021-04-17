---
description: Método de constructor.
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructor CBaseVideoRenderer. CBaseVideoRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.CBaseVideoRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ed49be63d9c2c05e12a2ac92ae33f64705460b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680287"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="a3967-103">Constructor CBaseVideoRenderer. CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="a3967-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="a3967-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="a3967-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3967-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3967-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="a3967-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3967-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="a3967-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="a3967-108">Identificador de clase para este representador.</span><span class="sxs-lookup"><span data-stu-id="a3967-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="a3967-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="a3967-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a3967-110">Puntero a una descripción que se usa para la depuración.</span><span class="sxs-lookup"><span data-stu-id="a3967-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="a3967-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a3967-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a3967-112">Puntero al objeto propietario agregado.</span><span class="sxs-lookup"><span data-stu-id="a3967-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="a3967-113">*phr*</span><span class="sxs-lookup"><span data-stu-id="a3967-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="a3967-114">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a3967-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3967-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3967-115">Requirements</span></span>



| <span data-ttu-id="a3967-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3967-116">Requirement</span></span> | <span data-ttu-id="a3967-117">Value</span><span class="sxs-lookup"><span data-stu-id="a3967-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3967-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3967-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a3967-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3967-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a3967-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3967-120">Library</span></span><br/> | <dl> <span data-ttu-id="a3967-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3967-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3967-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3967-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3967-123">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="a3967-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




