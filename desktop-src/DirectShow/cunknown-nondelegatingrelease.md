---
description: 'Disminuye el recuento de referencias en el objeto. Este método implementa el método INonDelegatingUnknown:: NonDelegatingRelease.'
ms.assetid: 58610f7d-5524-450f-a0f8-b299944abc78
title: Método CUnknown. NonDelegatingRelease (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingRelease
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec709d4b636eea6a145f9a24a868ad5c495e4477
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680876"
---
# <a name="cunknownnondelegatingrelease-method"></a><span data-ttu-id="5a1de-104">CUnknown. NonDelegatingRelease, método</span><span class="sxs-lookup"><span data-stu-id="5a1de-104">CUnknown.NonDelegatingRelease method</span></span>

<span data-ttu-id="5a1de-105">Disminuye el recuento de referencias en el objeto.</span><span class="sxs-lookup"><span data-stu-id="5a1de-105">Decrements the reference count on the object.</span></span> <span data-ttu-id="5a1de-106">Este método implementa el método **INonDelegatingUnknown:: NonDelegatingRelease** .</span><span class="sxs-lookup"><span data-stu-id="5a1de-106">This method implements the **INonDelegatingUnknown::NonDelegatingRelease** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1de-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a1de-107">Syntax</span></span>


```C++
ULONG NonDelegatingRelease();
```



## <a name="parameters"></a><span data-ttu-id="5a1de-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5a1de-108">Parameters</span></span>

<span data-ttu-id="5a1de-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5a1de-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a1de-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5a1de-110">Return value</span></span>

<span data-ttu-id="5a1de-111">Devuelve el recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="5a1de-111">Returns the reference count.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a1de-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a1de-112">Remarks</span></span>

<span data-ttu-id="5a1de-113">Cuando el recuento de referencias llega a cero, el objeto se elimina a sí mismo.</span><span class="sxs-lookup"><span data-stu-id="5a1de-113">When the reference count reaches zero, the object deletes itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1de-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a1de-114">Requirements</span></span>



| <span data-ttu-id="5a1de-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a1de-115">Requirement</span></span> | <span data-ttu-id="5a1de-116">Value</span><span class="sxs-lookup"><span data-stu-id="5a1de-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1de-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a1de-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5a1de-118"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a1de-118"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5a1de-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a1de-119">Library</span></span><br/> | <dl> <span data-ttu-id="5a1de-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5a1de-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




