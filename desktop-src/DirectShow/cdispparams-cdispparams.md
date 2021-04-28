---
description: 'Constructor CDispParams.CDispParams: método constructor.'
ms.assetid: da67a5e4-b4a1-4a38-93fe-0965695e93f5
title: Constructor CDispParams.CDispParams (Ctlutil.h)
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
ms.openlocfilehash: 42f55a57a0f9e06d3001c2638d457fe0b82a914d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095793"
---
# <a name="cdispparamscdispparams-constructor"></a><span data-ttu-id="9b4e6-103">Constructor CDispParams.CDispParams</span><span class="sxs-lookup"><span data-stu-id="9b4e6-103">CDispParams.CDispParams constructor</span></span>

<span data-ttu-id="9b4e6-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="9b4e6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b4e6-105">Syntax</span></span>


```C++
CDispParams(
   UINT    nArgs,
   VARIANT *pArgs
);
```



## <a name="parameters"></a><span data-ttu-id="9b4e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b4e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4e6-107">*nArgs*</span><span class="sxs-lookup"><span data-stu-id="9b4e6-107">*nArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4e6-108">Número de argumentos pasados al método o propiedad.</span><span class="sxs-lookup"><span data-stu-id="9b4e6-108">Number of arguments passed to the method or property.</span></span>

</dd> <dt>

<span data-ttu-id="9b4e6-109">*pArgs*</span><span class="sxs-lookup"><span data-stu-id="9b4e6-109">*pArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="9b4e6-110">Puntero a la lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="9b4e6-110">Pointer to the list of arguments.</span></span> <span data-ttu-id="9b4e6-111">En la lista, cada argumento se almacena con su tipo de variante.</span><span class="sxs-lookup"><span data-stu-id="9b4e6-111">In the list, each argument is stored with its variant type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9b4e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b4e6-112">Requirements</span></span>



| <span data-ttu-id="9b4e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b4e6-113">Requirement</span></span> | <span data-ttu-id="9b4e6-114">Value</span><span class="sxs-lookup"><span data-stu-id="9b4e6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4e6-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b4e6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9b4e6-116"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b4e6-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b4e6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b4e6-117">Library</span></span><br/> | <dl> <span data-ttu-id="9b4e6-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9b4e6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4e6-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="9b4e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4e6-120">**CDispParams (clase)**</span><span class="sxs-lookup"><span data-stu-id="9b4e6-120">**CDispParams Class**</span></span>](cdispparams.md)
</dt> </dl>

 

 




