---
description: Método de constructor.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructor CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dea0548079f8eb703f0c17557cab6a5e634cf242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690352"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="d0070-103">Constructor CBaseControlVideo. CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="d0070-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="d0070-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="d0070-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0070-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0070-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="d0070-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0070-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="d0070-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="d0070-108">Puntero al objeto de filtro multimedia propietario.</span><span class="sxs-lookup"><span data-stu-id="d0070-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="d0070-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="d0070-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="d0070-110">Puntero a la sección crítica que se va a usar para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d0070-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="d0070-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="d0070-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d0070-112">Puntero a la descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d0070-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="d0070-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d0070-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d0070-114">Puntero a la interfaz **IUnknown** de control, si el objeto forma parte de un agregado; de lo contrario, debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="d0070-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d0070-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="d0070-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="d0070-116">Puntero a una variable que recibe un valor HRESULT que indica si el método de constructor se ha ejecutado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="d0070-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d0070-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0070-117">Remarks</span></span>

<span data-ttu-id="d0070-118">El objeto implementa la interfaz de control [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="d0070-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="d0070-119">Todos los métodos de interfaz de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que esta clase implementa requieren que el filtro se conecte correctamente.</span><span class="sxs-lookup"><span data-stu-id="d0070-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="d0070-120">Por esta razón, se pasa a la clase un código PIN con el que se debe sincronizar.</span><span class="sxs-lookup"><span data-stu-id="d0070-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="d0070-121">Siempre que se llama a un método de interfaz, el objeto determina que el PIN sigue conectado.</span><span class="sxs-lookup"><span data-stu-id="d0070-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0070-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0070-122">Requirements</span></span>



| <span data-ttu-id="d0070-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0070-123">Requirement</span></span> | <span data-ttu-id="d0070-124">Value</span><span class="sxs-lookup"><span data-stu-id="d0070-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0070-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0070-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d0070-126"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d0070-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d0070-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d0070-127">Library</span></span><br/> | <dl> <span data-ttu-id="d0070-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d0070-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0070-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0070-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0070-130">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="d0070-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




