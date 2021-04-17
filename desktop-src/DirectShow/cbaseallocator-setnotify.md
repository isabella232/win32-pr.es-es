---
description: 'El método SetNotify establece o quita una devolución de llamada en el asignador. El asignador llama al método de devolución de llamada cada vez que se llama al método IMemAllocator:: ReleaseBuffer del asignador.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Método CBaseAllocator. SetNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661128"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="b2186-104">CBaseAllocator. SetNotify, método</span><span class="sxs-lookup"><span data-stu-id="b2186-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="b2186-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) puede modificarse o no estar disponible en versiones posteriores.\]</span><span class="sxs-lookup"><span data-stu-id="b2186-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="b2186-106">El `SetNotify` método establece o quita una devolución de llamada en el asignador.</span><span class="sxs-lookup"><span data-stu-id="b2186-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="b2186-107">El asignador llama al método de devolución de llamada cada vez que se llama al método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) del asignador.</span><span class="sxs-lookup"><span data-stu-id="b2186-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2186-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2186-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="b2186-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2186-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2186-110">*pNotify*</span><span class="sxs-lookup"><span data-stu-id="b2186-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="b2186-111">Puntero a la interfaz [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) que se usará para la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b2186-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="b2186-112">El autor de la llamada debe implementar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b2186-112">The caller must implement the interface.</span></span> <span data-ttu-id="b2186-113">Use el valor **null** para quitar la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b2186-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2186-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2186-114">Return value</span></span>

<span data-ttu-id="b2186-115">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="b2186-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2186-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2186-116">Remarks</span></span>

<span data-ttu-id="b2186-117">Este método implementa el método [**IMemAllocatorCallbackTemp:: SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) .</span><span class="sxs-lookup"><span data-stu-id="b2186-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="b2186-118">El asignador no expone la interfaz [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) a menos que la marca *fEnableReleaseCallback* esté establecida en **true** en el constructor [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="b2186-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="b2186-119">Este método establece la variable miembro [**CBaseAllocator:: m \_ pNotify**](cbaseallocator-m-pnotify.md) igual a *pNotify* e incrementa el recuento de referencias en la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b2186-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="b2186-120">Si *m \_ pNotify* no es **null**, el método **ReleaseBuffer** del asignador llama a [**IMemAllocatorNotifyCallbackTemp:: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span><span class="sxs-lookup"><span data-stu-id="b2186-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="b2186-121">Vea la sección Comentarios de ese método para obtener información sobre la implementación de la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b2186-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2186-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2186-122">Requirements</span></span>



| <span data-ttu-id="b2186-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2186-123">Requirement</span></span> | <span data-ttu-id="b2186-124">Value</span><span class="sxs-lookup"><span data-stu-id="b2186-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2186-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2186-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b2186-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2186-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b2186-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2186-127">Library</span></span><br/> | <dl> <span data-ttu-id="b2186-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b2186-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2186-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2186-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2186-130">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="b2186-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




