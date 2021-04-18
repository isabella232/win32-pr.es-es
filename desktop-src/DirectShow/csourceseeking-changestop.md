---
description: Se llama al método ChangeStop cuando cambia la posición de detención.
ms.assetid: 3d4a73a4-68e6-449c-9637-62cad937c4b4
title: Método CSourceSeeking. ChangeStop (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eefcc64b4692363c8caa8f39a3a0db9beb0d08b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690340"
---
# <a name="csourceseekingchangestop-method"></a><span data-ttu-id="0eec1-103">CSourceSeeking. ChangeStop, método</span><span class="sxs-lookup"><span data-stu-id="0eec1-103">CSourceSeeking.ChangeStop method</span></span>

<span data-ttu-id="0eec1-104">`ChangeStop`Se llama al método cuando cambia la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="0eec1-104">The `ChangeStop` method is called when the stop position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eec1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0eec1-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStop() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0eec1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0eec1-106">Parameters</span></span>

<span data-ttu-id="0eec1-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0eec1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0eec1-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0eec1-108">Return value</span></span>

<span data-ttu-id="0eec1-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0eec1-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0eec1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0eec1-110">Remarks</span></span>

<span data-ttu-id="0eec1-111">El método [**CSourceSeeking:: SetPositions**](csourceseeking-setpositions.md) llama a este método si cambia la posición de detención.</span><span class="sxs-lookup"><span data-stu-id="0eec1-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the stop position changes.</span></span> <span data-ttu-id="0eec1-112">Este método es virtual puro; la clase derivada debe implementarla.</span><span class="sxs-lookup"><span data-stu-id="0eec1-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="0eec1-113">En el ejemplo siguiente se muestra una posible implementación:</span><span class="sxs-lookup"><span data-stu-id="0eec1-113">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStop( )
{
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="0eec1-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0eec1-114">Requirements</span></span>



| <span data-ttu-id="0eec1-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0eec1-115">Requirement</span></span> | <span data-ttu-id="0eec1-116">Value</span><span class="sxs-lookup"><span data-stu-id="0eec1-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0eec1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0eec1-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0eec1-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0eec1-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0eec1-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0eec1-119">Library</span></span><br/> | <dl> <span data-ttu-id="0eec1-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0eec1-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0eec1-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0eec1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0eec1-122">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="0eec1-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




