---
description: El método AlignUp redondea un valor hasta un límite de alineación especificado. Nota quitada en Windows 7. .
ms.assetid: fa2a6567-3eb1-4aa9-b966-2e88b15c67b1
title: Método CPullPin. AlignUp (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.AlignUp
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4f33ae2b7434d90d909315edda4d49e07d8adab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680277"
---
# <a name="cpullpinalignup-method"></a><span data-ttu-id="af246-104">CPullPin. AlignUp, método</span><span class="sxs-lookup"><span data-stu-id="af246-104">CPullPin.AlignUp method</span></span>

<span data-ttu-id="af246-105">El método **AlignUp** redondea un valor hasta un límite de alineación especificado.</span><span class="sxs-lookup"><span data-stu-id="af246-105">The **AlignUp** method rounds a value up to a specified alignment boundary.</span></span>

> [!Note]  
> <span data-ttu-id="af246-106">Se quitó en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="af246-106">Removed in Windows 7.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="af246-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af246-107">Syntax</span></span>


```C++
LONGLONG AlignUp(
   LONGLONG ll,
   LONG     lAlign
);
```



## <a name="parameters"></a><span data-ttu-id="af246-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af246-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af246-109">*ll*</span><span class="sxs-lookup"><span data-stu-id="af246-109">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="af246-110">Especifica el número que se va a alinear.</span><span class="sxs-lookup"><span data-stu-id="af246-110">Specifies the number to align.</span></span>

</dd> <dt>

<span data-ttu-id="af246-111">*lAlign*</span><span class="sxs-lookup"><span data-stu-id="af246-111">*lAlign*</span></span> 
</dt> <dd>

<span data-ttu-id="af246-112">Especifica el límite de alineación.</span><span class="sxs-lookup"><span data-stu-id="af246-112">Specifies the alignment boundary.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af246-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af246-113">Return value</span></span>

<span data-ttu-id="af246-114">Devuelve el resultado alineado.</span><span class="sxs-lookup"><span data-stu-id="af246-114">Returns the aligned result.</span></span>

## <a name="remarks"></a><span data-ttu-id="af246-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af246-115">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="af246-116">Este método puede producir un desbordamiento numérico si se desbordan *ll* + (*lAlign* -1).</span><span class="sxs-lookup"><span data-stu-id="af246-116">This method can cause numeric overflow if *ll* + (*lAlign* - 1) overflows.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="af246-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af246-117">Requirements</span></span>



| <span data-ttu-id="af246-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="af246-118">Requirement</span></span> | <span data-ttu-id="af246-119">Value</span><span class="sxs-lookup"><span data-stu-id="af246-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af246-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af246-120">Header</span></span><br/>  | <dl> <span data-ttu-id="af246-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="af246-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="af246-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="af246-122">Library</span></span><br/> | <dl> <span data-ttu-id="af246-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="af246-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af246-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="af246-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af246-125">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="af246-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




