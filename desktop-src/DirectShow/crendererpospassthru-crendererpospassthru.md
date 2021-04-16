---
description: Método de constructor.
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Constructor CRendererPosPassThru. CRendererPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 97b21ba3ad9438189f97c3e0bb9f011b210a0195
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671309"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="c01a7-103">Constructor CRendererPosPassThru. CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="c01a7-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="c01a7-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="c01a7-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c01a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c01a7-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="c01a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c01a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c01a7-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="c01a7-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="c01a7-108">Puntero al nombre del objeto, para la depuración.</span><span class="sxs-lookup"><span data-stu-id="c01a7-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="c01a7-109">Asigne este parámetro en la memoria estática.</span><span class="sxs-lookup"><span data-stu-id="c01a7-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="c01a7-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="c01a7-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="c01a7-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="c01a7-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="c01a7-112">Si se agrega el objeto, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="c01a7-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="c01a7-113">De lo contrario, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="c01a7-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c01a7-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="c01a7-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="c01a7-115">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c01a7-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="c01a7-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="c01a7-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c01a7-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="c01a7-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="c01a7-118">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="c01a7-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c01a7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c01a7-119">Requirements</span></span>



| <span data-ttu-id="c01a7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c01a7-120">Requirement</span></span> | <span data-ttu-id="c01a7-121">Value</span><span class="sxs-lookup"><span data-stu-id="c01a7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c01a7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c01a7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c01a7-123"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c01a7-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c01a7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c01a7-124">Library</span></span><br/> | <dl> <span data-ttu-id="c01a7-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c01a7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




