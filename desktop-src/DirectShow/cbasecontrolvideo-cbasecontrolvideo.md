---
description: 'Constructor CBaseControlVideo.CBaseControlVideo: método constructor.'
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructor CBaseControlVideo.CBaseControlVideo (Ctlutil.h)
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
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096353"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="7b3b9-103">Constructor CBaseControlVideo.CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="7b3b9-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="7b3b9-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b3b9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b3b9-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="7b3b9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7b3b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b3b9-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="7b3b9-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3b9-108">Puntero al objeto de filtro multimedia propietario.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="7b3b9-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="7b3b9-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3b9-110">Puntero a la sección crítica que se usará para el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="7b3b9-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="7b3b9-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3b9-112">Puntero a la descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="7b3b9-113">*Punk*</span><span class="sxs-lookup"><span data-stu-id="7b3b9-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3b9-114">Puntero a la **interfaz IUnknown de control,** si el objeto forma parte de un agregado; de lo contrario, debe ser **NULL.**</span><span class="sxs-lookup"><span data-stu-id="7b3b9-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7b3b9-115">*Phr*</span><span class="sxs-lookup"><span data-stu-id="7b3b9-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="7b3b9-116">Puntero a una variable que recibe un valor HRESULT que indica el éxito o error del método constructor.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b3b9-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7b3b9-117">Remarks</span></span>

<span data-ttu-id="7b3b9-118">El objeto implementa la interfaz de control [**IBasicVideo.**](/windows/desktop/api/Control/nn-control-ibasicvideo)</span><span class="sxs-lookup"><span data-stu-id="7b3b9-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="7b3b9-119">Todos los métodos de interfaz [**de IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) que implementa esta clase requieren que el filtro se conecte correctamente.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="7b3b9-120">Por este motivo, a la clase se le pasa un pin con el que debe sincronizarse.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="7b3b9-121">Cada vez que se llama a un método de interfaz, el objeto determina que el pin sigue conectado.</span><span class="sxs-lookup"><span data-stu-id="7b3b9-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b3b9-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b3b9-122">Requirements</span></span>



| <span data-ttu-id="7b3b9-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b3b9-123">Requirement</span></span> | <span data-ttu-id="7b3b9-124">Value</span><span class="sxs-lookup"><span data-stu-id="7b3b9-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b3b9-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b3b9-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7b3b9-126"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3b9-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7b3b9-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7b3b9-127">Library</span></span><br/> | <dl> <span data-ttu-id="7b3b9-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7b3b9-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b3b9-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7b3b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b3b9-130">**CBaseControlVideo (clase)**</span><span class="sxs-lookup"><span data-stu-id="7b3b9-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




