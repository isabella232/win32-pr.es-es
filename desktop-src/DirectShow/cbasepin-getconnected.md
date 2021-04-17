---
description: El método GetConnected recupera el PIN conectado a este pin.
ms.assetid: 7b47aa8e-55a9-45f8-aa32-902fee037c72
title: Método CBasePin. GetConnected (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetConnected
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e5c583b06a9c25126a611736002c455a2c93ed90
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660699"
---
# <a name="cbasepingetconnected-method"></a><span data-ttu-id="e8507-103">CBasePin. GetConnected, método</span><span class="sxs-lookup"><span data-stu-id="e8507-103">CBasePin.GetConnected method</span></span>

<span data-ttu-id="e8507-104">El `GetConnected` método recupera el PIN conectado a este pin.</span><span class="sxs-lookup"><span data-stu-id="e8507-104">The `GetConnected` method retrieves the pin connected to this pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8507-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8507-105">Syntax</span></span>


```C++
IPin* GetConnected();
```



## <a name="parameters"></a><span data-ttu-id="e8507-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e8507-106">Parameters</span></span>

<span data-ttu-id="e8507-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e8507-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e8507-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e8507-108">Return value</span></span>

<span data-ttu-id="e8507-109">Devuelve un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) de otro PIN.</span><span class="sxs-lookup"><span data-stu-id="e8507-109">Returns a pointer to the other pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8507-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8507-110">Remarks</span></span>

<span data-ttu-id="e8507-111">Si el PIN no está conectado, este método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="e8507-111">If the pin is not connected, this method returns **NULL**.</span></span> <span data-ttu-id="e8507-112">Llame al método [**CBasePin:: IsConnected**](cbasepin-isconnected.md) para determinar si el PIN está conectado.</span><span class="sxs-lookup"><span data-stu-id="e8507-112">Call the [**CBasePin::IsConnected**](cbasepin-isconnected.md) method to determine whether the pin is connected.</span></span>

<span data-ttu-id="e8507-113">El método no llama a **AddRef** en la interfaz **IPin** , por lo que el llamador no debe liberar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="e8507-113">The method does not call **AddRef** on the **IPin** interface, so the caller should not release the interface.</span></span>

## <a name="examples"></a><span data-ttu-id="e8507-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8507-114">Examples</span></span>

<span data-ttu-id="e8507-115">Dado que el recuento de referencias no se incrementa en el puntero devuelto, puede encadenar las llamadas de método juntas:</span><span class="sxs-lookup"><span data-stu-id="e8507-115">Because the reference count is not incremented on the returned pointer, you can chain method calls together:</span></span>


```C++
if (m_MyPin->IsConnected())
{
    m_MyPin->GetConnected()->EndOfStream();
}
```



<span data-ttu-id="e8507-116">Este modelo de codificación es muy práctico. pero como se muestra en el ejemplo, debe tener cuidado de no desreferenciar un puntero **nulo** cuando el PIN esté desconectado.</span><span class="sxs-lookup"><span data-stu-id="e8507-116">This coding pattern is very convenient; but as the example shows, you must be careful not to dereference a **NULL** pointer when the pin is unconnected.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8507-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8507-117">Requirements</span></span>



| <span data-ttu-id="e8507-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8507-118">Requirement</span></span> | <span data-ttu-id="e8507-119">Value</span><span class="sxs-lookup"><span data-stu-id="e8507-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8507-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8507-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e8507-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e8507-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e8507-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e8507-122">Library</span></span><br/> | <dl> <span data-ttu-id="e8507-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e8507-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8507-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8507-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8507-125">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e8507-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




