---
description: Método de constructor.
ms.assetid: df5efbb3-6bce-4e30-b1b1-d69bf64fa87d
title: Constructor CBaseRenderer. CBaseRenderer (Renbase. h)
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
ms.openlocfilehash: b41f8d7f9681a64f58413aea2fd8717320278f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660762"
---
# <a name="cbaserenderercbaserenderer-constructor"></a><span data-ttu-id="adf7c-103">Constructor CBaseRenderer. CBaseRenderer</span><span class="sxs-lookup"><span data-stu-id="adf7c-103">CBaseRenderer.CBaseRenderer constructor</span></span>

<span data-ttu-id="adf7c-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="adf7c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="adf7c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adf7c-105">Syntax</span></span>


```C++
CBaseRenderer(
   REFCLSID  RenderClass,
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   UINT      TimerResolution = 1
);
```



## <a name="parameters"></a><span data-ttu-id="adf7c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="adf7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="adf7c-107">*RenderClass*</span><span class="sxs-lookup"><span data-stu-id="adf7c-107">*RenderClass*</span></span> 
</dt> <dd>

<span data-ttu-id="adf7c-108">Identificador de clase del representador.</span><span class="sxs-lookup"><span data-stu-id="adf7c-108">Class identifier of the renderer.</span></span>

</dd> <dt>

<span data-ttu-id="adf7c-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="adf7c-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="adf7c-110">Puntero a una cadena que contiene el nombre del filtro, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="adf7c-110">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="adf7c-111">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="adf7c-111">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="adf7c-112">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="adf7c-112">Pointer to the owner of this object.</span></span> <span data-ttu-id="adf7c-113">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="adf7c-113">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="adf7c-114">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="adf7c-114">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="adf7c-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="adf7c-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="adf7c-116">Recibe un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="adf7c-116">Receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="adf7c-117">*TimerResolution*</span><span class="sxs-lookup"><span data-stu-id="adf7c-117">*TimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="adf7c-118">Resolución del temporizador.</span><span class="sxs-lookup"><span data-stu-id="adf7c-118">Timer resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="adf7c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="adf7c-119">Requirements</span></span>



| <span data-ttu-id="adf7c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="adf7c-120">Requirement</span></span> | <span data-ttu-id="adf7c-121">Value</span><span class="sxs-lookup"><span data-stu-id="adf7c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="adf7c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adf7c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="adf7c-123"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="adf7c-123"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="adf7c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="adf7c-124">Library</span></span><br/> | <dl> <span data-ttu-id="adf7c-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="adf7c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="adf7c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="adf7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adf7c-127">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="adf7c-127">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




