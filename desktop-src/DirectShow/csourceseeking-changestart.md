---
description: Se llama al método cambie las cuando cambia la posición de inicio.
ms.assetid: d0a5497e-43e9-4d1f-9106-1f4cd8fcb372
title: Método CSourceSeeking. cambie las (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.ChangeStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d0a2751cf0ad1ecc6fddeeffd97b97c32b4a31b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661310"
---
# <a name="csourceseekingchangestart-method"></a><span data-ttu-id="6b65a-103">CSourceSeeking. cambie las, método</span><span class="sxs-lookup"><span data-stu-id="6b65a-103">CSourceSeeking.ChangeStart method</span></span>

<span data-ttu-id="6b65a-104">`ChangeStart`Se llama al método cuando cambia la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="6b65a-104">The `ChangeStart` method is called when the start position changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b65a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b65a-105">Syntax</span></span>


```C++
virtual HRESULT ChangeStart() = 0;
```



## <a name="parameters"></a><span data-ttu-id="6b65a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b65a-106">Parameters</span></span>

<span data-ttu-id="6b65a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6b65a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b65a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b65a-108">Return value</span></span>

<span data-ttu-id="6b65a-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6b65a-109">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b65a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b65a-110">Remarks</span></span>

<span data-ttu-id="6b65a-111">El método [**CSourceSeeking:: SetPositions**](csourceseeking-setpositions.md) llama a este método si cambia la posición de inicio.</span><span class="sxs-lookup"><span data-stu-id="6b65a-111">The [**CSourceSeeking::SetPositions**](csourceseeking-setpositions.md) method calls this method if the start position changes.</span></span> <span data-ttu-id="6b65a-112">Este método es virtual puro; la clase derivada debe implementarla.</span><span class="sxs-lookup"><span data-stu-id="6b65a-112">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="6b65a-113">Después de una operación de búsqueda, las marcas de tiempo se deben reiniciar desde cero.</span><span class="sxs-lookup"><span data-stu-id="6b65a-113">After a seek operation, time stamps should restart from zero.</span></span> <span data-ttu-id="6b65a-114">Las horas de los medios deben reflejar la nueva hora de inicio.</span><span class="sxs-lookup"><span data-stu-id="6b65a-114">Media times should reflect the new start time.</span></span> <span data-ttu-id="6b65a-115">En el ejemplo siguiente se muestra una posible implementación:</span><span class="sxs-lookup"><span data-stu-id="6b65a-115">The following example shows a possible implementation:</span></span>


```C++
HRESULT CMyStream::ChangeStart( )
{
    m_rtSampleTime = 0;          // Reset the time stamps.
    m_rtMediaTime = m_rtStart;   // Reset the media times.
    UpdateFromSeek();
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="6b65a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b65a-116">Requirements</span></span>



| <span data-ttu-id="6b65a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b65a-117">Requirement</span></span> | <span data-ttu-id="6b65a-118">Value</span><span class="sxs-lookup"><span data-stu-id="6b65a-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b65a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b65a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6b65a-120"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b65a-120"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6b65a-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6b65a-121">Library</span></span><br/> | <dl> <span data-ttu-id="6b65a-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6b65a-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b65a-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b65a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b65a-124">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="6b65a-124">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




