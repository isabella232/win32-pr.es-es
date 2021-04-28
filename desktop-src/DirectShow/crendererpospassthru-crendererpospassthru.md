---
description: 'Constructor CRendererPosPassThru.CRendererPosPassThru: método constructor.'
ms.assetid: 9d6f40ee-31bf-4334-bee5-4be834f1f269
title: Constructor CRendererPosPassThru.CRendererPosPassThru (Ctlutil.h)
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
ms.openlocfilehash: 59972f12f0f746ef68c267e3fbd0d071d54193c3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085413"
---
# <a name="crendererpospassthrucrendererpospassthru-constructor"></a><span data-ttu-id="f04d1-103">Constructor CRendererPosPassThru.CRendererPosPassThru</span><span class="sxs-lookup"><span data-stu-id="f04d1-103">CRendererPosPassThru.CRendererPosPassThru constructor</span></span>

<span data-ttu-id="f04d1-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="f04d1-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f04d1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f04d1-105">Syntax</span></span>


```C++
CRendererPosPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         IPin      *pPin
);
```



## <a name="parameters"></a><span data-ttu-id="f04d1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f04d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f04d1-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f04d1-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f04d1-108">Puntero al nombre del objeto para fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="f04d1-108">Pointer to the name of the object, for debugging purposes.</span></span> <span data-ttu-id="f04d1-109">Asigne este parámetro en memoria estática.</span><span class="sxs-lookup"><span data-stu-id="f04d1-109">Allocate this parameter in static memory.</span></span>

</dd> <dt>

<span data-ttu-id="f04d1-110">*Punk*</span><span class="sxs-lookup"><span data-stu-id="f04d1-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f04d1-111">Puntero al propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="f04d1-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="f04d1-112">Si el objeto se agrega, pase un puntero a la interfaz **IUnknown** del objeto de agregación.</span><span class="sxs-lookup"><span data-stu-id="f04d1-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="f04d1-113">De lo contrario, establezca este parámetro en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="f04d1-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f04d1-114">*Phr*</span><span class="sxs-lookup"><span data-stu-id="f04d1-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="f04d1-115">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="f04d1-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="f04d1-116">ignorado.</span><span class="sxs-lookup"><span data-stu-id="f04d1-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="f04d1-117">*pPin*</span><span class="sxs-lookup"><span data-stu-id="f04d1-117">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="f04d1-118">Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="f04d1-118">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the filter's input pin.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f04d1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f04d1-119">Requirements</span></span>



| <span data-ttu-id="f04d1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f04d1-120">Requirement</span></span> | <span data-ttu-id="f04d1-121">Value</span><span class="sxs-lookup"><span data-stu-id="f04d1-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f04d1-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f04d1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="f04d1-123"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="f04d1-123"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f04d1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f04d1-124">Library</span></span><br/> | <dl> <span data-ttu-id="f04d1-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f04d1-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




