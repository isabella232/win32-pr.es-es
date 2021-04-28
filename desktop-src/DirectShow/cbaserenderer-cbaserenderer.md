---
description: 'Constructor CBaseRenderer.CBaseRenderer: método constructor.'
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Constructor CBaseRenderer.CBaseRenderer (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 68ebc6255456f0fcbb4bf732a91dce981d0f78ce
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119913"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="85a6f-103">Constructor CBaseRenderer.CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="85a6f-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="85a6f-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="85a6f-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="85a6f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85a6f-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="85a6f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85a6f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85a6f-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="85a6f-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="85a6f-108">Identificador de clase del representador.</span><span class="sxs-lookup"><span data-stu-id="85a6f-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="85a6f-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="85a6f-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="85a6f-110">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="85a6f-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="85a6f-111">*Punk*</span><span class="sxs-lookup"><span data-stu-id="85a6f-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="85a6f-112">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="85a6f-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="85a6f-113">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="85a6f-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="85a6f-114">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="85a6f-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="85a6f-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="85a6f-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="85a6f-116">Recibe un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="85a6f-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="85a6f-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="85a6f-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="85a6f-118">Resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="85a6f-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="85a6f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85a6f-119">Requirements</span></span>



| <span data-ttu-id="85a6f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="85a6f-120">Requirement</span></span> | <span data-ttu-id="85a6f-121">Value</span><span class="sxs-lookup"><span data-stu-id="85a6f-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85a6f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85a6f-122">Header</span></span><br/>  | <dl> <span data-ttu-id="85a6f-123"><dt>Renbase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="85a6f-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="85a6f-124">Library</span></span><br/> | <dl> <span data-ttu-id="85a6f-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="85a6f-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85a6f-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="85a6f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85a6f-127">**CBaseRenderer (clase)**</span><span class="sxs-lookup"><span data-stu-id="85a6f-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




