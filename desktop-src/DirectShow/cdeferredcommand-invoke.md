---
description: El método Invoke proporciona acceso a los métodos y propiedades expuestos por un objeto.
ms.assetid: d9539b89-b7c2-4b4d-b6d6-6275cc6d7e7c
title: Método CDeferredCommand. Invoke (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Invoke
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 268cfc3d4665eeacafbd695b974f55445747e151
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680500"
---
# <a name="cdeferredcommandinvoke-method"></a><span data-ttu-id="a7f55-103">CDeferredCommand. Invoke (método)</span><span class="sxs-lookup"><span data-stu-id="a7f55-103">CDeferredCommand.Invoke method</span></span>

<span data-ttu-id="a7f55-104">El `Invoke` método proporciona acceso a los métodos y propiedades expuestos por un objeto.</span><span class="sxs-lookup"><span data-stu-id="a7f55-104">The `Invoke` method provides access to methods and properties exposed by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a7f55-105">Syntax</span></span>


```C++
HRESULT Invoke();
```



## <a name="parameters"></a><span data-ttu-id="a7f55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a7f55-106">Parameters</span></span>

<span data-ttu-id="a7f55-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a7f55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a7f55-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a7f55-108">Return value</span></span>

<span data-ttu-id="a7f55-109">Devuelve VFW \_ E \_ ya \_ cancelado si **m \_ pQueue** es **null**.</span><span class="sxs-lookup"><span data-stu-id="a7f55-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="a7f55-110">De lo contrario, devuelve el **valor HRESULT** resultante de una llamada a **IDispatch:: GetTypeInfo** o **IUnknown:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a7f55-110">Otherwise, returns the **HRESULT** resulting from a call to **IDispatch::GetTypeInfo** or **IUnknown::QueryInterface**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7f55-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7f55-111">Requirements</span></span>



| <span data-ttu-id="a7f55-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7f55-112">Requirement</span></span> | <span data-ttu-id="a7f55-113">Value</span><span class="sxs-lookup"><span data-stu-id="a7f55-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f55-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a7f55-114">Header</span></span><br/>  | <dl> <span data-ttu-id="a7f55-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7f55-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a7f55-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7f55-116">Library</span></span><br/> | <dl> <span data-ttu-id="a7f55-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a7f55-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7f55-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7f55-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7f55-119">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="a7f55-119">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




