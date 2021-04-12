---
description: Representa los atributos que se aplican a la entrada manuscrita cuando se dibuja.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Clase InkDrawingAttributes (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361180"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="4a7b7-103">Clase InkDrawingAttributes</span><span class="sxs-lookup"><span data-stu-id="4a7b7-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="4a7b7-104">Representa los atributos que se aplican a la entrada manuscrita cuando se dibuja.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="4a7b7-105">**InkDrawingAttributes** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4a7b7-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="4a7b7-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4a7b7-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="4a7b7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a7b7-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="4a7b7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a7b7-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="4a7b7-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4a7b7-109">Interfaces</span></span>

<span data-ttu-id="4a7b7-110">La clase **InkDrawingAttributes** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="4a7b7-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="4a7b7-111">Interface</span></span>                 | <span data-ttu-id="4a7b7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a7b7-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="4a7b7-113">**IInkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="4a7b7-114">Este objeto implementa la interfaz com **IInkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="4a7b7-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a7b7-115">Methods</span></span>

<span data-ttu-id="4a7b7-116">La clase **InkDrawingAttributes** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="4a7b7-117">Método</span><span class="sxs-lookup"><span data-stu-id="4a7b7-117">Method</span></span>                         | <span data-ttu-id="4a7b7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a7b7-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a7b7-119">**Clonar**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="4a7b7-120">Crea un objeto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** o [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicado.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4a7b7-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a7b7-121">Properties</span></span>

<span data-ttu-id="4a7b7-122">La clase **InkDrawingAttributes** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="4a7b7-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a7b7-123">Property</span></span>                                                                           | <span data-ttu-id="4a7b7-124">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="4a7b7-124">Access type</span></span>           | <span data-ttu-id="4a7b7-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a7b7-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a7b7-126">**Sin suavizado**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="4a7b7-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-127">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-128">Obtiene o establece el valor que especifica si se mezclan los colores de primer plano y de fondo a lo largo del borde de la tinta para aumentar la suavidad de un trazo de tinta.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="4a7b7-129">**Color**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="4a7b7-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-130">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-131">Obtiene o establece el color de la tinta dibujada con este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="4a7b7-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="4a7b7-133">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-133">Read-only</span></span><br/>  | <span data-ttu-id="4a7b7-134">Obtiene la colección de datos definidos por la aplicación que se almacena en el objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="4a7b7-135">**FitToCurve**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="4a7b7-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-136">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-137">Obtiene o establece el valor que especifica si la entrada de lápiz se representa como una serie de curvas en lugar de como líneas entre los puntos de ejemplo de lápiz.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="4a7b7-138">**Height**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="4a7b7-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-139">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-140">Obtiene o establece el alto del lápiz al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="4a7b7-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="4a7b7-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-142">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-143">Obtiene o establece el valor que especifica si la tinta dibujada se vuelve más ancha y aumenta la presión de la punta del lápiz en la superficie de la tableta.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="4a7b7-144">**PenTip**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="4a7b7-145">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-145">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-146">Obtiene o establece la punta del lápiz que se va a usar (bola o rectángulo) al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="4a7b7-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="4a7b7-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-148">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-149">Obtiene o establece cómo interactúa el color de la pluma con los colores de fondo existentes en la pantalla cuando se dibuja la tinta.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="4a7b7-150">**Transparencia**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="4a7b7-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-151">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-152">Obtiene o establece el valor de transparencia de la entrada de lápiz dibujada.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="4a7b7-153">Los valores van desde cero (totalmente opaco) hasta 255 (totalmente transparente).</span><span class="sxs-lookup"><span data-stu-id="4a7b7-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="4a7b7-154">**Width**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="4a7b7-155">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4a7b7-155">Read/write</span></span><br/> | <span data-ttu-id="4a7b7-156">Obtiene o establece el ancho del lápiz al dibujar la entrada manuscrita con este objeto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="4a7b7-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4a7b7-157">Remarks</span></span>

<span data-ttu-id="4a7b7-158">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="4a7b7-159">Estos atributos de dibujo se pueden asociar a un trazo o un cursor y especificar opciones de configuración como el color, el ancho y la transparencia.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="4a7b7-160">Para especificar los atributos de dibujo de un trazo, use la propiedad [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del objeto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="4a7b7-161">Para especificar los atributos de dibujo de todos los trazos dentro de una colección de trazos, llame al método [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) de la colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4a7b7-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="4a7b7-162">Cada objeto [**InkCollector**](inkcollector-class.md) , el objeto [**InkOverlay**](inkoverlay-class.md) y el control [InkPicture](inkpicture-control-reference.md) pueden especificar un conjunto diferente de atributos de dibujo para el mismo cursor.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="4a7b7-163">Use la propiedad [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) del objeto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) para obtener o establecer los atributos de dibujo de un cursor.</span><span class="sxs-lookup"><span data-stu-id="4a7b7-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a7b7-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a7b7-164">Requirements</span></span>



| <span data-ttu-id="4a7b7-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a7b7-165">Requirement</span></span> | <span data-ttu-id="4a7b7-166">Value</span><span class="sxs-lookup"><span data-stu-id="4a7b7-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a7b7-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a7b7-167">Minimum supported client</span></span><br/> | <span data-ttu-id="4a7b7-168">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="4a7b7-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4a7b7-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4a7b7-169">Minimum supported server</span></span><br/> | <span data-ttu-id="4a7b7-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4a7b7-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4a7b7-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a7b7-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a7b7-172"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4a7b7-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4a7b7-173">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a7b7-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a7b7-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a7b7-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="4a7b7-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a7b7-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a7b7-176">**DrawingAttributes (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="4a7b7-177">**DrawingAttributes (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="4a7b7-178">**DrawingAttributes (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="4a7b7-179">**Propiedad DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="4a7b7-180">**Propiedad DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="4a7b7-181">**Propiedad DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="4a7b7-182">**Método ModifyDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="4a7b7-183">**Interfaz IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="4a7b7-184">**Clase InkDisp**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="4a7b7-185">**Interfaz IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="4a7b7-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

