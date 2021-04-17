---
description: 'El método NonDelegatingAddRef incrementa el recuento de referencias en el objeto. Este método implementa el método INonDelegatingUnknown:: NonDelegatingAddRef.'
ms.assetid: abb6ee51-8fb8-4307-b127-b3667260e35a
title: Método CUnknown. NonDelegatingAddRef (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingAddRef
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f97260c03f0931e94e8ce6de8b7816789b2fe66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661057"
---
# <a name="cunknownnondelegatingaddref-method"></a><span data-ttu-id="802bf-104">CUnknown. NonDelegatingAddRef, método</span><span class="sxs-lookup"><span data-stu-id="802bf-104">CUnknown.NonDelegatingAddRef method</span></span>

<span data-ttu-id="802bf-105">El `NonDelegatingAddRef` método incrementa el recuento de referencias en el objeto.</span><span class="sxs-lookup"><span data-stu-id="802bf-105">The `NonDelegatingAddRef` method increments the reference count on the object.</span></span> <span data-ttu-id="802bf-106">Este método implementa el método **INonDelegatingUnknown:: NonDelegatingAddRef** .</span><span class="sxs-lookup"><span data-stu-id="802bf-106">This method implements the **INonDelegatingUnknown::NonDelegatingAddRef** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="802bf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="802bf-107">Syntax</span></span>


```C++
ULONG NonDelegatingAddRef();
```



## <a name="parameters"></a><span data-ttu-id="802bf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="802bf-108">Parameters</span></span>

<span data-ttu-id="802bf-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="802bf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="802bf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="802bf-110">Return value</span></span>

<span data-ttu-id="802bf-111">Devuelve el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="802bf-111">Returns the reference count.</span></span>

## <a name="requirements"></a><span data-ttu-id="802bf-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="802bf-112">Requirements</span></span>



| <span data-ttu-id="802bf-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="802bf-113">Requirement</span></span> | <span data-ttu-id="802bf-114">Value</span><span class="sxs-lookup"><span data-stu-id="802bf-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="802bf-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="802bf-115">Header</span></span><br/>  | <dl> <span data-ttu-id="802bf-116"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="802bf-116"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="802bf-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="802bf-117">Library</span></span><br/> | <dl> <span data-ttu-id="802bf-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="802bf-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




