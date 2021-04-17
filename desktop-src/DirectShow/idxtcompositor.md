---
description: La interfaz IDxtCompositor establece propiedades en la transición del compositor. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición del compositor.
ms.assetid: 519f1e00-4b67-4014-906b-043f2478baa7
title: Interfaz IDxtCompositor (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtCompositor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c2e19f555fe01cbec3763bc1dc76d11aeb5f5ecb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680900"
---
# <a name="idxtcompositor-interface"></a><span data-ttu-id="2488c-103">Interfaz IDxtCompositor</span><span class="sxs-lookup"><span data-stu-id="2488c-103">IDxtCompositor interface</span></span>

> [!Note]  
> <span data-ttu-id="2488c-104">\[En desuso.</span><span class="sxs-lookup"><span data-stu-id="2488c-104">\[Deprecated.</span></span> <span data-ttu-id="2488c-105">Esta API se puede quitar de las versiones futuras de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2488c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2488c-106">La `IDxtCompositor` interfaz establece las propiedades en la transición del [compositor](compositor-transition.md) .</span><span class="sxs-lookup"><span data-stu-id="2488c-106">The `IDxtCompositor` interface sets properties on the [Compositor](compositor-transition.md) transition.</span></span>

<span data-ttu-id="2488c-107">Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición del compositor.</span><span class="sxs-lookup"><span data-stu-id="2488c-107">This interface is used internally by DirectShow Editing Services (DES) when it renders the Compositor transition.</span></span> <span data-ttu-id="2488c-108">Las aplicaciones DES no tienen que usar esta interfaz.</span><span class="sxs-lookup"><span data-stu-id="2488c-108">DES applications do not have to use this interface.</span></span> <span data-ttu-id="2488c-109">Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="2488c-109">To set the properties on a transition in DES, use the [**IPropertySetter**](ipropertysetter.md) interface.</span></span>

<span data-ttu-id="2488c-110">La transición de compositor compone una imagen de primer plano en una imagen de fondo.</span><span class="sxs-lookup"><span data-stu-id="2488c-110">The Compositor transition composites a foreground image onto a background image.</span></span> <span data-ttu-id="2488c-111">El *rectángulo de origen* define la sección de la imagen de primer plano que se compone.</span><span class="sxs-lookup"><span data-stu-id="2488c-111">The *source rectangle* defines the section of the foreground image that is composited.</span></span> <span data-ttu-id="2488c-112">El *rectángulo de destino* define la sección de la imagen de fondo que recibe la imagen de primer plano.</span><span class="sxs-lookup"><span data-stu-id="2488c-112">The *destination rectangle* defines the section of the background image that receives the foreground image.</span></span> <span data-ttu-id="2488c-113">En el siguiente diagrama se ilustran estos rectángulos.</span><span class="sxs-lookup"><span data-stu-id="2488c-113">The following diagram illustrates these rectangles.</span></span>

![propiedades de la transición de compositor](images/compmeasure.png)

## <a name="members"></a><span data-ttu-id="2488c-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="2488c-115">Members</span></span>

<span data-ttu-id="2488c-116">La interfaz **IDxtCompositor** hereda de **IDXEffect**.</span><span class="sxs-lookup"><span data-stu-id="2488c-116">The **IDxtCompositor** interface inherits from **IDXEffect**.</span></span> <span data-ttu-id="2488c-117">**IDxtCompositor** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2488c-117">**IDxtCompositor** also has these types of members:</span></span>

-   [<span data-ttu-id="2488c-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="2488c-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2488c-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="2488c-119">Methods</span></span>

<span data-ttu-id="2488c-120">La interfaz **IDxtCompositor** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2488c-120">The **IDxtCompositor** interface has these methods.</span></span>



| <span data-ttu-id="2488c-121">Método</span><span class="sxs-lookup"><span data-stu-id="2488c-121">Method</span></span>                                                   | <span data-ttu-id="2488c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2488c-122">Description</span></span>                                                         |
|:---------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="2488c-123">**obtener \_ alto**</span><span class="sxs-lookup"><span data-stu-id="2488c-123">**get\_Height**</span></span>](idxtcompositor-get-height.md)         | <span data-ttu-id="2488c-124">Recupera el alto del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-124">Retrieves the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="2488c-125">**obtener \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="2488c-125">**get\_OffsetX**</span></span>](idxtcompositor-get-offsetx.md)       | <span data-ttu-id="2488c-126">Recupera el desplazamiento horizontal del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-126">Retrieves the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="2488c-127">**obtener \_ desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="2488c-127">**get\_OffsetY**</span></span>](idxtcompositor-get-offsety.md)       | <span data-ttu-id="2488c-128">Recupera el desplazamiento vertical del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-128">Retrieves the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="2488c-129">**obtener \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="2488c-129">**get\_SrcHeight**</span></span>](idxtcompositor-get-srcheight.md)   | <span data-ttu-id="2488c-130">Recupera el alto del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-130">Retrieves the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="2488c-131">**obtener \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="2488c-131">**get\_SrcOffsetX**</span></span>](idxtcompositor-get-srcoffsetx.md) | <span data-ttu-id="2488c-132">Recupera el desplazamiento horizontal del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-132">Retrieves the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="2488c-133">**obtener \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="2488c-133">**get\_SrcOffsetY**</span></span>](idxtcompositor-get-srcoffsety.md) | <span data-ttu-id="2488c-134">Recupera el desplazamiento vertical del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-134">Retrieves the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="2488c-135">**obtener \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="2488c-135">**get\_SrcWidth**</span></span>](idxtcompositor-get-srcwidth.md)     | <span data-ttu-id="2488c-136">Recupera el ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-136">Retrieves the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="2488c-137">**obtener \_ ancho**</span><span class="sxs-lookup"><span data-stu-id="2488c-137">**get\_Width**</span></span>](idxtcompositor-get-width.md)           | <span data-ttu-id="2488c-138">Recupera el ancho del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-138">Retrieves the width of the target rectangle.</span></span><br/>             |
| [<span data-ttu-id="2488c-139">**colocar \_ alto**</span><span class="sxs-lookup"><span data-stu-id="2488c-139">**put\_Height**</span></span>](idxtcompositor-put-height.md)         | <span data-ttu-id="2488c-140">Especifica el alto del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-140">Specifies the height of the target rectangle.</span></span><br/>            |
| [<span data-ttu-id="2488c-141">**Put \_ offsetX**</span><span class="sxs-lookup"><span data-stu-id="2488c-141">**put\_OffsetX**</span></span>](idxtcompositor-put-offsetx.md)       | <span data-ttu-id="2488c-142">Especifica el desplazamiento horizontal del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-142">Specifies the horizontal offset of the target rectangle.</span></span><br/> |
| [<span data-ttu-id="2488c-143">**colocar \_ desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="2488c-143">**put\_OffsetY**</span></span>](idxtcompositor-put-offsety.md)       | <span data-ttu-id="2488c-144">Especifica el desplazamiento vertical del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-144">Specifies the vertical offset of the target rectangle.</span></span><br/>   |
| [<span data-ttu-id="2488c-145">**Put \_ SrcHeight**</span><span class="sxs-lookup"><span data-stu-id="2488c-145">**put\_SrcHeight**</span></span>](idxtcompositor-put-srcheight.md)   | <span data-ttu-id="2488c-146">Especifica el alto del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-146">Specifies the height of the source rectangle.</span></span><br/>            |
| [<span data-ttu-id="2488c-147">**Put \_ SrcOffsetX**</span><span class="sxs-lookup"><span data-stu-id="2488c-147">**put\_SrcOffsetX**</span></span>](idxtcompositor-put-srcoffsetx.md) | <span data-ttu-id="2488c-148">Especifica el desplazamiento horizontal del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-148">Specifies the horizontal offset of the source rectangle.</span></span><br/> |
| [<span data-ttu-id="2488c-149">**Put \_ SrcOffsetY**</span><span class="sxs-lookup"><span data-stu-id="2488c-149">**put\_SrcOffsetY**</span></span>](idxtcompositor-put-srcoffsety.md) | <span data-ttu-id="2488c-150">Especifica el desplazamiento vertical del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-150">Specifies the vertical offset of the source rectangle.</span></span><br/>   |
| [<span data-ttu-id="2488c-151">**Put \_ SrcWidth**</span><span class="sxs-lookup"><span data-stu-id="2488c-151">**put\_SrcWidth**</span></span>](idxtcompositor-put-srcwidth.md)     | <span data-ttu-id="2488c-152">Especifica el ancho del rectángulo de origen.</span><span class="sxs-lookup"><span data-stu-id="2488c-152">Specifies the width of the source rectangle.</span></span><br/>             |
| [<span data-ttu-id="2488c-153">**colocar \_ ancho**</span><span class="sxs-lookup"><span data-stu-id="2488c-153">**put\_Width**</span></span>](idxtcompositor-put-width.md)           | <span data-ttu-id="2488c-154">Especifica el ancho del rectángulo de destino.</span><span class="sxs-lookup"><span data-stu-id="2488c-154">Specifies the width of the target rectangle.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="2488c-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2488c-155">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2488c-156">El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.</span><span class="sxs-lookup"><span data-stu-id="2488c-156">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2488c-157">Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="2488c-157">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2488c-158">QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="2488c-158">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2488c-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2488c-159">Requirements</span></span>



| <span data-ttu-id="2488c-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="2488c-160">Requirement</span></span> | <span data-ttu-id="2488c-161">Value</span><span class="sxs-lookup"><span data-stu-id="2488c-161">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2488c-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2488c-162">Header</span></span><br/>  | <dl> <span data-ttu-id="2488c-163"><dt>QEDIT. h</dt></span><span class="sxs-lookup"><span data-stu-id="2488c-163"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2488c-164">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2488c-164">Library</span></span><br/> | <dl> <span data-ttu-id="2488c-165"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2488c-165"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 




