---
description: 'Constructor CBaseVideoRenderer.CBaseVideoRenderer: método constructor.'
ms.assetid: 9b69632b-7932-4a9b-bd68-69b06dd8a5ec
title: Constructor CBaseVideoRenderer.CBaseVideoRenderer (Renbase.h)
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
ms.openlocfilehash: c0ae558238b94402150e5cb15373d202065e485e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095843"
---
# <a name="cbasevideorenderercbasevideorenderer-constructor"></a><span data-ttu-id="c06ac-103">Constructor CBaseVideoRenderer.CBaseVideoRenderer</span><span class="sxs-lookup"><span data-stu-id="c06ac-103">CBaseVideoRenderer.CBaseVideoRenderer constructor</span></span>

<span data-ttu-id="c06ac-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="c06ac-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c06ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c06ac-105">Syntax</span></span>


```C++
CBaseVideoRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="c06ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c06ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c06ac-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="c06ac-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ac-108">Identificador de clase para este representador.</span><span class="sxs-lookup"><span data-stu-id="c06ac-108">Class identifier for this renderer.</span></span>

</dd> <dt>

<span data-ttu-id="c06ac-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="c06ac-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ac-110">Puntero a una descripción utilizada con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="c06ac-110">Pointer to a description used for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="c06ac-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="c06ac-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ac-112">Puntero al objeto propietario agregado.</span><span class="sxs-lookup"><span data-stu-id="c06ac-112">Pointer to the aggregated owner object.</span></span>

</dd> <dt>

<span data-ttu-id="c06ac-113">*Phr*</span><span class="sxs-lookup"><span data-stu-id="c06ac-113">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c06ac-114">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c06ac-114">Pointer to an **HRESULT** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c06ac-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c06ac-115">Requirements</span></span>



| <span data-ttu-id="c06ac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c06ac-116">Requirement</span></span> | <span data-ttu-id="c06ac-117">Value</span><span class="sxs-lookup"><span data-stu-id="c06ac-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c06ac-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c06ac-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c06ac-119"><dt>Renbase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c06ac-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c06ac-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c06ac-120">Library</span></span><br/> | <dl> <span data-ttu-id="c06ac-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c06ac-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c06ac-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c06ac-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c06ac-123">**CBaseVideoRenderer (clase)**</span><span class="sxs-lookup"><span data-stu-id="c06ac-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




