---
description: La interfaz IAMTimelineTrans proporciona métodos para manipular las transiciones en los servicios de edición de DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interfaz IAMTimelineTrans (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690998"
---
# <a name="iamtimelinetrans-interface"></a><span data-ttu-id="aeb22-103">Interfaz IAMTimelineTrans</span><span class="sxs-lookup"><span data-stu-id="aeb22-103">IAMTimelineTrans interface</span></span>

> [!Note]  
> <span data-ttu-id="aeb22-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="aeb22-104">\[Deprecated.</span></span> <span data-ttu-id="aeb22-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="aeb22-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="aeb22-106">La `IAMTimelineTrans` interfaz proporciona métodos para manipular las transiciones en los [servicios de edición de DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="aeb22-106">The `IAMTimelineTrans` interface provides methods for manipulating transitions in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="aeb22-107">Una transición es una progresión entre una capa de vídeo y la composición representada de todas las capas de vídeo con una prioridad más baja.</span><span class="sxs-lookup"><span data-stu-id="aeb22-107">A transition is a progression between one video layer and the rendered composite of all video layers with a lower priority.</span></span> <span data-ttu-id="aeb22-108">Se puede Agregar una transición a cualquier objeto Timeline que exponga la interfaz [**IAMTimelineTransable**](iamtimelinetransable.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-108">A transition can be added to any timeline object that exposes the [**IAMTimelineTransable**](iamtimelinetransable.md) interface.</span></span> <span data-ttu-id="aeb22-109">Para establecer las propiedades de una transición, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-109">To set properties on a transition, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="aeb22-110">El objeto de transición DES es realmente un contenedor para un objeto de transformación de DirectX.</span><span class="sxs-lookup"><span data-stu-id="aeb22-110">The DES transition object is actually a wrapper for a DirectX Transform object.</span></span> <span data-ttu-id="aeb22-111">Se puede usar cualquier objeto de transformación de DirectX de entrada 2 para implementar el efecto visual de la transición.</span><span class="sxs-lookup"><span data-stu-id="aeb22-111">Any 2-input DirectX Transform object can be used to implement the visual effect for the transition.</span></span> <span data-ttu-id="aeb22-112">Microsoft ya no admite el desarrollo de objetos de transformación de DirectX de terceros.</span><span class="sxs-lookup"><span data-stu-id="aeb22-112">Microsoft no longer supports the development of third-party DirectX Transform objects.</span></span> <span data-ttu-id="aeb22-113">Para especificar el objeto de transformación de DirectX para una transición, llame al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-113">To specify the DirectX Transform object for a transition, call the [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) method.</span></span>

<span data-ttu-id="aeb22-114">Para crear un objeto de transición, llame a [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) con el valor de transición de tipo principal de la escala de tiempo \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aeb22-114">To create a transition object, call [**IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) with the value TIMELINE\_MAJOR\_TYPE\_TRANSITION.</span></span> <span data-ttu-id="aeb22-115">Puede consultar el puntero [**IAMTimelineObj**](iamtimelineobj.md) devuelto para la `IAMTimelineTrans` interfaz.</span><span class="sxs-lookup"><span data-stu-id="aeb22-115">You can query the returned [**IAMTimelineObj**](iamtimelineobj.md) pointer for the `IAMTimelineTrans` interface.</span></span>

## <a name="members"></a><span data-ttu-id="aeb22-116">Miembros</span><span class="sxs-lookup"><span data-stu-id="aeb22-116">Members</span></span>

<span data-ttu-id="aeb22-117">La interfaz **IAMTimelineTrans** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-117">The **IAMTimelineTrans** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="aeb22-118">**IAMTimelineTrans** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="aeb22-118">**IAMTimelineTrans** also has these types of members:</span></span>

-   [<span data-ttu-id="aeb22-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="aeb22-119">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="aeb22-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="aeb22-120">Methods</span></span>

<span data-ttu-id="aeb22-121">La interfaz **IAMTimelineTrans** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="aeb22-121">The **IAMTimelineTrans** interface has these methods.</span></span>



| <span data-ttu-id="aeb22-122">Método</span><span class="sxs-lookup"><span data-stu-id="aeb22-122">Method</span></span>                                                  | <span data-ttu-id="aeb22-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeb22-123">Description</span></span>                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="aeb22-124">**GetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="aeb22-124">**GetCutPoint**</span></span>](iamtimelinetrans-getcutpoint.md)     | <span data-ttu-id="aeb22-125">Recupera el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="aeb22-125">Retrieves the cut point.</span></span><br/>                                                    |
| [<span data-ttu-id="aeb22-126">**GetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="aeb22-126">**GetCutPoint2**</span></span>](iamtimelinetrans-getcutpoint2.md)   | <span data-ttu-id="aeb22-127">Recupera el punto de corte, como un valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-127">Retrieves the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>             |
| [<span data-ttu-id="aeb22-128">**GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="aeb22-128">**GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)     | <span data-ttu-id="aeb22-129">Determina si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="aeb22-129">Determines whether the transition is rendered as a cut.</span></span><br/>                     |
| [<span data-ttu-id="aeb22-130">**GetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="aeb22-130">**GetSwapInputs**</span></span>](iamtimelinetrans-getswapinputs.md) | <span data-ttu-id="aeb22-131">Recupera un valor que indica si se intercambian las entradas de la transición.</span><span class="sxs-lookup"><span data-stu-id="aeb22-131">Retrieves a value that indicates whether the transition inputs are swapped.</span></span><br/> |
| [<span data-ttu-id="aeb22-132">**SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="aeb22-132">**SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)     | <span data-ttu-id="aeb22-133">Establece el punto de corte.</span><span class="sxs-lookup"><span data-stu-id="aeb22-133">Sets the cut point.</span></span><br/>                                                         |
| [<span data-ttu-id="aeb22-134">**SetCutPoint2**</span><span class="sxs-lookup"><span data-stu-id="aeb22-134">**SetCutPoint2**</span></span>](iamtimelinetrans-setcutpoint2.md)   | <span data-ttu-id="aeb22-135">Establece el punto de corte, como un valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="aeb22-135">Sets the cut point, as a [**REFTIME**](reftime.md) value.</span></span><br/>                  |
| [<span data-ttu-id="aeb22-136">**SetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="aeb22-136">**SetCutsOnly**</span></span>](iamtimelinetrans-setcutsonly.md)     | <span data-ttu-id="aeb22-137">Especifica si la transición se representa como un corte.</span><span class="sxs-lookup"><span data-stu-id="aeb22-137">Specifies whether the transition is rendered as a cut.</span></span><br/>                      |
| [<span data-ttu-id="aeb22-138">**SetSwapInputs**</span><span class="sxs-lookup"><span data-stu-id="aeb22-138">**SetSwapInputs**</span></span>](iamtimelinetrans-setswapinputs.md) | <span data-ttu-id="aeb22-139">Especifica si se intercambian las entradas de la transición.</span><span class="sxs-lookup"><span data-stu-id="aeb22-139">Specifies whether the transition inputs are swapped.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="aeb22-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aeb22-140">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="aeb22-141">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="aeb22-141">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="aeb22-142">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="aeb22-142">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="aeb22-143">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="aeb22-143">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="aeb22-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeb22-144">Requirements</span></span>



| <span data-ttu-id="aeb22-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeb22-145">Requirement</span></span> | <span data-ttu-id="aeb22-146">Value</span><span class="sxs-lookup"><span data-stu-id="aeb22-146">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb22-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aeb22-147">Header</span></span><br/>  | <dl> <span data-ttu-id="aeb22-148"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="aeb22-148"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="aeb22-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aeb22-149">Library</span></span><br/> | <dl> <span data-ttu-id="aeb22-150"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aeb22-150"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeb22-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="aeb22-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeb22-152">Trabajar con efectos y transiciones</span><span class="sxs-lookup"><span data-stu-id="aeb22-152">Working with Effects and Transitions</span></span>](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
