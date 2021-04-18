---
description: Indica si el objeto ha cambiado desde que se guardó por última vez en su flujo actual.
ms.assetid: 69840be6-062e-4505-8381-ea04e822c660
title: Método CPersistStream. IsDirty (pStream. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.IsDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3bc57998b63ece5ca32543fc00d1d3b5b4389b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670999"
---
# <a name="cpersiststreamisdirty-method"></a><span data-ttu-id="dec9f-103">CPersistStream. IsDirty (método)</span><span class="sxs-lookup"><span data-stu-id="dec9f-103">CPersistStream.IsDirty method</span></span>

<span data-ttu-id="dec9f-104">Indica si el objeto ha cambiado desde que se guardó por última vez en su flujo actual.</span><span class="sxs-lookup"><span data-stu-id="dec9f-104">Indicates whether the object has changed since it was last saved to its current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dec9f-105">Syntax</span></span>


```C++
HRESULT IsDirty();
```



## <a name="parameters"></a><span data-ttu-id="dec9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dec9f-106">Parameters</span></span>

<span data-ttu-id="dec9f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="dec9f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dec9f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dec9f-108">Return value</span></span>

<span data-ttu-id="dec9f-109">Devuelve S \_ OK si es necesario guardar el filtro y s \_ false si no es necesario guardarlo.</span><span class="sxs-lookup"><span data-stu-id="dec9f-109">Returns S\_OK if the filter needs saving and S\_FALSE if it does not need saving.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec9f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dec9f-110">Remarks</span></span>

<span data-ttu-id="dec9f-111">Esta función miembro implementa el método **IPersistStream:: IsDirty** .</span><span class="sxs-lookup"><span data-stu-id="dec9f-111">This member function implements the **IPersistStream::IsDirty** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dec9f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dec9f-112">Requirements</span></span>



| <span data-ttu-id="dec9f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="dec9f-113">Requirement</span></span> | <span data-ttu-id="dec9f-114">Value</span><span class="sxs-lookup"><span data-stu-id="dec9f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dec9f-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dec9f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="dec9f-116"><dt>PStream. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dec9f-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dec9f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dec9f-117">Library</span></span><br/> | <dl> <span data-ttu-id="dec9f-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dec9f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dec9f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dec9f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dec9f-120">**Clase CPersistStream**</span><span class="sxs-lookup"><span data-stu-id="dec9f-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




