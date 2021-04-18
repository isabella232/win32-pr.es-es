---
description: Método de constructor.
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructor CDispParams. CDispParams (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDispParams.CDispParams
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3beeb0a6e3a18c3fac6606385d9206938bbc1cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680499"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="134b9-103">Constructor CDispParams. CDispParams</span><span class="sxs-lookup"><span data-stu-id="134b9-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="134b9-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="134b9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="134b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="134b9-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="134b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="134b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="134b9-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="134b9-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="134b9-108">Número de argumentos pasados al método o a la propiedad.</span><span class="sxs-lookup"><span data-stu-id="134b9-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="134b9-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="134b9-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="134b9-110">Puntero a la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="134b9-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="134b9-111">En la lista, cada argumento se almacena con su tipo variante.</span><span class="sxs-lookup"><span data-stu-id="134b9-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="134b9-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="134b9-112">Requirements</span></span>



| <span data-ttu-id="134b9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="134b9-113">Requirement</span></span> | <span data-ttu-id="134b9-114">Value</span><span class="sxs-lookup"><span data-stu-id="134b9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="134b9-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="134b9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="134b9-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="134b9-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="134b9-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="134b9-117">Library</span></span><br/> | <dl> <span data-ttu-id="134b9-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="134b9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="134b9-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="134b9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="134b9-120">**Clase CDispParams**</span><span class="sxs-lookup"><span data-stu-id="134b9-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




