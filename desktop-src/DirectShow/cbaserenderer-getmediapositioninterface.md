---
description: El método GetMediaPositionInterface recupera los punteros de interfaz IMediaPosition y IMediaSeeking del filtro.
ms.assetid: aeca4484-cecc-4d07-aa77-56221ff75699
title: Método CBaseRenderer. GetMediaPositionInterface (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetMediaPositionInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d41d777b88f0e18ae1510c32b7e89024ea7bdd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670561"
---
# <a name="cbaserenderergetmediapositioninterface-method"></a><span data-ttu-id="94627-103">CBaseRenderer. GetMediaPositionInterface, método</span><span class="sxs-lookup"><span data-stu-id="94627-103">CBaseRenderer.GetMediaPositionInterface method</span></span>

<span data-ttu-id="94627-104">El `GetMediaPositionInterface` método recupera los punteros de interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) y [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) del filtro.</span><span class="sxs-lookup"><span data-stu-id="94627-104">The `GetMediaPositionInterface` method retrieves the filter's [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="94627-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94627-105">Syntax</span></span>


```C++
virtual HRESULT GetMediaPositionInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a><span data-ttu-id="94627-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94627-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94627-107">*riid*</span><span class="sxs-lookup"><span data-stu-id="94627-107">*riid*</span></span> 
</dt> <dd>

<span data-ttu-id="94627-108">Identificador de referencia de la interfaz.</span><span class="sxs-lookup"><span data-stu-id="94627-108">Reference identifier of the interface.</span></span>

</dd> <dt>

<span data-ttu-id="94627-109">*PPV*</span><span class="sxs-lookup"><span data-stu-id="94627-109">*ppv*</span></span> 
</dt> <dd>

<span data-ttu-id="94627-110">Dirección de una variable que recibe el puntero de interfaz.</span><span class="sxs-lookup"><span data-stu-id="94627-110">Address of a variable that receives the interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94627-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94627-111">Return value</span></span>

<span data-ttu-id="94627-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94627-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="94627-113">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="94627-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="94627-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="94627-114">Return code</span></span>                                                                                   | <span data-ttu-id="94627-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="94627-115">Description</span></span>                         |
|-----------------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="94627-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="94627-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="94627-117">Correcto.</span><span class="sxs-lookup"><span data-stu-id="94627-117">Success.</span></span><br/>                 |
| <dl> <span data-ttu-id="94627-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="94627-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="94627-119">Memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="94627-119">Insufficient memory.</span></span><br/>     |
| <dl> <span data-ttu-id="94627-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="94627-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="94627-121">No se admite la interfaz.</span><span class="sxs-lookup"><span data-stu-id="94627-121">Interface not supported.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="94627-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94627-122">Remarks</span></span>

<span data-ttu-id="94627-123">El filtro delega todos los comandos de búsqueda en un objeto [**CRendererPosPassThru**](crendererpospassthru.md) , que los pasa arriba.</span><span class="sxs-lookup"><span data-stu-id="94627-123">The filter delegates all seeking commands to a [**CRendererPosPassThru**](crendererpospassthru.md) object, which passes them upstream.</span></span> <span data-ttu-id="94627-124">Este método crea el objeto **CRendererPosPassThru** , si aún no existe, y lo consulta para la interfaz solicitada.</span><span class="sxs-lookup"><span data-stu-id="94627-124">This method creates the **CRendererPosPassThru** object, if it does not yet exist, and queries it for the requested interface.</span></span>

<span data-ttu-id="94627-125">La variable miembro [**CBaseRenderer:: m \_ pPosition**](cbaserenderer-m-pposition.md) almacena un puntero al objeto **CRendererPosPassThru** .</span><span class="sxs-lookup"><span data-stu-id="94627-125">The [**CBaseRenderer::m\_pPosition**](cbaserenderer-m-pposition.md) member variable stores a pointer to the **CRendererPosPassThru** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="94627-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94627-126">Requirements</span></span>



| <span data-ttu-id="94627-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94627-127">Requirement</span></span> | <span data-ttu-id="94627-128">Value</span><span class="sxs-lookup"><span data-stu-id="94627-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94627-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94627-129">Header</span></span><br/>  | <dl> <span data-ttu-id="94627-130"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94627-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="94627-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94627-131">Library</span></span><br/> | <dl> <span data-ttu-id="94627-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="94627-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94627-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="94627-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94627-134">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="94627-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




