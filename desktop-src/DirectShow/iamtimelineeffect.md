---
description: La interfaz IAMTimelineEffect proporciona métodos para manipular los efectos de audio y vídeo en los servicios de edición de DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interfaz IAMTimelineEffect (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681256"
---
# <a name="iamtimelineeffect-interface"></a><span data-ttu-id="66a27-103">Interfaz IAMTimelineEffect</span><span class="sxs-lookup"><span data-stu-id="66a27-103">IAMTimelineEffect interface</span></span>

> [!Note]  
> <span data-ttu-id="66a27-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="66a27-104">\[Deprecated.</span></span> <span data-ttu-id="66a27-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="66a27-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="66a27-106">La `IAMTimelineEffect` interfaz proporciona métodos para manipular los efectos de audio y vídeo en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="66a27-106">The `IAMTimelineEffect` interface provides methods for manipulating audio and video effects in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="66a27-107">Se puede Agregar un efecto a cualquier objeto Timeline que exponga la interfaz [**IAMTimelineEffectable**](iamtimelineeffectable.md) .</span><span class="sxs-lookup"><span data-stu-id="66a27-107">An effect can be added to any timeline object that exposes the [**IAMTimelineEffectable**](iamtimelineeffectable.md) interface.</span></span> <span data-ttu-id="66a27-108">Para establecer las propiedades de un efecto, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="66a27-108">To set properties on an effect, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="66a27-109">El objeto de efecto DES es realmente un contenedor para uno de otros dos objetos:</span><span class="sxs-lookup"><span data-stu-id="66a27-109">The DES effect object is actually a wrapper for one of two other objects:</span></span>

-   <span data-ttu-id="66a27-110">Para los efectos de audio, cualquier filtro de efecto de audio de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="66a27-110">For audio effects, any DirectShow audio effect filter.</span></span>
-   <span data-ttu-id="66a27-111">En el caso de efectos de vídeo y 1-entrada de objeto de transformación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="66a27-111">For video effects, and 1-input DirectX Transform object.</span></span>

<span data-ttu-id="66a27-112">Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros.</span><span class="sxs-lookup"><span data-stu-id="66a27-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span>

<span data-ttu-id="66a27-113">Para especificar el filtro o el objeto de transformación de DirectX para un efecto, llame al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="66a27-113">To specify the filter or DirectX Transform object for an effect, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="66a27-114">Para crear un objeto de efecto, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el \_ efecto de tipo principal de la escala de tiempo \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="66a27-114">To create an effect object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_EFFECT.</span></span> <span data-ttu-id="66a27-115">Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineEffect` interfaz.</span><span class="sxs-lookup"><span data-stu-id="66a27-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineEffect` interface.</span></span>

## <a name="members"></a><span data-ttu-id="66a27-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="66a27-116">Members</span></span>

<span data-ttu-id="66a27-117">La interfaz **IAMTimelineEffect** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="66a27-117">The **IAMTimelineEffect** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="66a27-118">**IAMTimelineEffect** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="66a27-118">**IAMTimelineEffect** also has these types of members:</span></span>

-   [<span data-ttu-id="66a27-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="66a27-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66a27-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="66a27-120">Methods</span></span>

<span data-ttu-id="66a27-121">La interfaz **IAMTimelineEffect** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="66a27-121">The **IAMTimelineEffect** interface has these methods.</span></span>



| <span data-ttu-id="66a27-122">Método</span><span class="sxs-lookup"><span data-stu-id="66a27-122">Method</span></span>                                                           | <span data-ttu-id="66a27-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="66a27-123">Description</span></span>                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="66a27-124">**EffectGetPriority**</span><span class="sxs-lookup"><span data-stu-id="66a27-124">**EffectGetPriority**</span></span>](iamtimelineeffect-effectgetpriority.md) | <span data-ttu-id="66a27-125">Recupera el nivel de prioridad del efecto.</span><span class="sxs-lookup"><span data-stu-id="66a27-125">Retrieves the effect's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66a27-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66a27-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="66a27-127">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="66a27-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="66a27-128">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="66a27-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="66a27-129">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="66a27-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="66a27-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a27-130">Requirements</span></span>



| <span data-ttu-id="66a27-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a27-131">Requirement</span></span> | <span data-ttu-id="66a27-132">Value</span><span class="sxs-lookup"><span data-stu-id="66a27-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a27-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66a27-133">Header</span></span><br/>  | <dl> <span data-ttu-id="66a27-134"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a27-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="66a27-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66a27-135">Library</span></span><br/> | <dl> <span data-ttu-id="66a27-136"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66a27-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a27-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="66a27-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a27-138">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="66a27-138">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
