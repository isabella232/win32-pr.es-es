---
description: Representa el área que utiliza el reconocedor en el que se puede dibujar la entrada manuscrita. El área se conoce como la guía de reconocimiento.
ms.assetid: c4990aa5-8c8b-4206-8376-b5c0d0c8e0a7
title: Clase InkRecognizerGuide (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRecognizerGuide
- InkRecognizerGuide.IInkRecognizerGuide
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 55729513f748afc87f184b73eaba976184307bc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279384"
---
# <a name="inkrecognizerguide-class"></a><span data-ttu-id="f02de-104">Clase InkRecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="f02de-104">InkRecognizerGuide class</span></span>

<span data-ttu-id="f02de-105">Representa el área que utiliza el reconocedor en el que se puede dibujar la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="f02de-105">Represents the area that the recognizer uses in which ink can be drawn.</span></span> <span data-ttu-id="f02de-106">El área se conoce como la guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f02de-106">The area is known as the recognition guide.</span></span>

<span data-ttu-id="f02de-107">**InkRecognizerGuide** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f02de-107">**InkRecognizerGuide** has these types of members:</span></span>

-   [<span data-ttu-id="f02de-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f02de-108">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="f02de-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f02de-109">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="f02de-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f02de-110">Interfaces</span></span>

<span data-ttu-id="f02de-111">La clase **InkRecognizerGuide** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f02de-111">The **InkRecognizerGuide** class defines these interfaces.</span></span>



| <span data-ttu-id="f02de-112">Interfaz</span><span class="sxs-lookup"><span data-stu-id="f02de-112">Interface</span></span>               | <span data-ttu-id="f02de-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f02de-113">Description</span></span>                                                                  |
|:------------------------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="f02de-114">**IInkRecognizerGuide**</span><span class="sxs-lookup"><span data-stu-id="f02de-114">**IInkRecognizerGuide**</span></span> | <span data-ttu-id="f02de-115">Este objeto implementa la interfaz com **IInkRecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="f02de-115">This object implements the **IInkRecognizerGuide** COM interface.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f02de-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f02de-116">Properties</span></span>

<span data-ttu-id="f02de-117">La clase **InkRecognizerGuide** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f02de-117">The **InkRecognizerGuide** class has these properties.</span></span>



| <span data-ttu-id="f02de-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f02de-118">Property</span></span>                                                       | <span data-ttu-id="f02de-119">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="f02de-119">Access type</span></span>           | <span data-ttu-id="f02de-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="f02de-120">Description</span></span>                                                                                                                    |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f02de-121">**Columnas**</span><span class="sxs-lookup"><span data-stu-id="f02de-121">**Columns**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_columns)<br/>       | <span data-ttu-id="f02de-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-122">Read/write</span></span><br/> | <span data-ttu-id="f02de-123">Obtiene o establece el número de columnas del cuadro guía.</span><span class="sxs-lookup"><span data-stu-id="f02de-123">Gets or sets the number of columns in the guide box.</span></span><br/>                                                                |
| [<span data-ttu-id="f02de-124">**DrawnBox**</span><span class="sxs-lookup"><span data-stu-id="f02de-124">**DrawnBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox)<br/>     | <span data-ttu-id="f02de-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-125">Read/write</span></span><br/> | <span data-ttu-id="f02de-126">Obtiene o establece el cuadro que se dibuja físicamente en la pantalla de la tableta y en el que tiene lugar la escritura.</span><span class="sxs-lookup"><span data-stu-id="f02de-126">Gets or sets the box that is physically drawn on the tablet's screen and in which writing takes place.</span></span><br/>              |
| [<span data-ttu-id="f02de-127">**GuideData**</span><span class="sxs-lookup"><span data-stu-id="f02de-127">**GuideData**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_guidedata)<br/>   | <span data-ttu-id="f02de-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-128">Read/write</span></span><br/> | <span data-ttu-id="f02de-129">Obtiene o establece los datos de la guía para los desarrolladores de C++.</span><span class="sxs-lookup"><span data-stu-id="f02de-129">Gets or sets guide data for C++ developers.</span></span><br/>                                                                         |
| [<span data-ttu-id="f02de-130">**Elips**</span><span class="sxs-lookup"><span data-stu-id="f02de-130">**Midline**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_midline)<br/>       | <span data-ttu-id="f02de-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-131">Read/write</span></span><br/> | <span data-ttu-id="f02de-132">Obtiene o establece el alto de la media media.</span><span class="sxs-lookup"><span data-stu-id="f02de-132">Gets or sets the midline height.</span></span> <span data-ttu-id="f02de-133">El alto de línea media es la distancia desde la línea base hasta la línea media del cuadro dibujado.</span><span class="sxs-lookup"><span data-stu-id="f02de-133">The midline height is distance from the baseline to the midline, of the drawn box.</span></span><br/> |
| [<span data-ttu-id="f02de-134">**Las**</span><span class="sxs-lookup"><span data-stu-id="f02de-134">**Rows**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_rows)<br/>             | <span data-ttu-id="f02de-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-135">Read/write</span></span><br/> | <span data-ttu-id="f02de-136">Obtiene o establece el número de filas del cuadro guía.</span><span class="sxs-lookup"><span data-stu-id="f02de-136">Gets or sets the number of rows in the guide box.</span></span><br/>                                                                   |
| [<span data-ttu-id="f02de-137">**WritingBox**</span><span class="sxs-lookup"><span data-stu-id="f02de-137">**WritingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox)<br/> | <span data-ttu-id="f02de-138">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f02de-138">Read/write</span></span><br/> | <span data-ttu-id="f02de-139">Obtiene o establece el área de escritura invisible del cuadro de guía en el que se puede producir realmente la escritura.</span><span class="sxs-lookup"><span data-stu-id="f02de-139">Gets or sets the invisible writing area of the guide box in which writing can actually take place.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f02de-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f02de-140">Remarks</span></span>

<span data-ttu-id="f02de-141">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="f02de-141">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method.</span></span>

<span data-ttu-id="f02de-142">De forma predeterminada, no hay ninguna guía de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f02de-142">By default, there is no recognizer guide.</span></span> <span data-ttu-id="f02de-143">Una guía predeterminada tiene todos los valores de propiedad establecidos en 0.</span><span class="sxs-lookup"><span data-stu-id="f02de-143">A default guide has all property values set to 0.</span></span> <span data-ttu-id="f02de-144">Debe utilizar las propiedades de este objeto para establecer la guía.</span><span class="sxs-lookup"><span data-stu-id="f02de-144">You must use the properties of this object to set the guide.</span></span>

<span data-ttu-id="f02de-145">Si la aplicación ha dibujado instrucciones en la pantalla en la que se espera que el usuario escriba, la aplicación debe establecer los valores de las propiedades de la guía del reconocedor para informar al reconocedor.</span><span class="sxs-lookup"><span data-stu-id="f02de-145">If the application has drawn guidelines on the screen on which the user is expected to write, the application should set the values of the properties of the recognizer guide to inform the recognizer.</span></span> <span data-ttu-id="f02de-146">Estas propiedades son solo para el uso del reconocedor.</span><span class="sxs-lookup"><span data-stu-id="f02de-146">These properties are for the recognizer's use only.</span></span> <span data-ttu-id="f02de-147">El establecimiento de ellos no dibuja pistas visuales en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f02de-147">Setting them does not, by itself, draw visual clues on the display.</span></span> <span data-ttu-id="f02de-148">La aplicación o el control dibujan las pistas visuales.</span><span class="sxs-lookup"><span data-stu-id="f02de-148">The application or the control draws the visual clues.</span></span>

<span data-ttu-id="f02de-149">La guía del reconocedor puede constar de filas y columnas, y estas proporcionan al reconocedor un contexto mejor en el que realizar el reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f02de-149">The recognizer guide can consist of rows and columns, and these give the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="f02de-150">Las letras como "t" y "I" se reconocen más fácilmente cuando se usa una guía para dar contexto a la tinta.</span><span class="sxs-lookup"><span data-stu-id="f02de-150">Letters such as "t" and "I" are more easily recognized when a guide is used to give context to the ink.</span></span> <span data-ttu-id="f02de-151">Por ejemplo, puede dibujar líneas horizontales en una pantalla que muestren el lugar en el que debe producirse la escritura (este tipo de guía solo consistiría en filas y no en columnas).</span><span class="sxs-lookup"><span data-stu-id="f02de-151">For example, you can draw horizontal lines on a screen, that show where writing should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="f02de-152">Al escribir en las líneas, en lugar de un espacio arbitrario, mejora la precisión del reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="f02de-152">By writing on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="f02de-153">En la guía se especifican los límites de la tinta en las coordenadas del espacio de tinta.</span><span class="sxs-lookup"><span data-stu-id="f02de-153">The guide specifies the boundaries of the ink in ink space coordinates.</span></span>

<span data-ttu-id="f02de-154">La propiedad [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) puede definir un cuadro que tenga el mismo tamaño que el cuadro definido por la propiedad [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) .</span><span class="sxs-lookup"><span data-stu-id="f02de-154">The [**DrawnBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_drawnbox) property can define a box which is the same size as or smaller than the box defined by the [**WritingBox**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizerguide-get_writingbox) property.</span></span>

<span data-ttu-id="f02de-155">En la siguiente ilustración se muestran los elementos de una guía de reconocimiento con dos filas y ninguna columna.</span><span class="sxs-lookup"><span data-stu-id="f02de-155">The following figure shows the elements of a recognizer guide with two rows and no columns.</span></span>

![Ilustración que muestra los elementos de la guía del reconocedor](images/927cc2f3-549f-4279-aab9-bd5ade070eaf.jpg)

<span data-ttu-id="f02de-157">Además de dibujar líneas en la pantalla que muestren los usuarios en los que escribir, puede dibujar celdas en la pantalla en la que se escriben caracteres o palabras.</span><span class="sxs-lookup"><span data-stu-id="f02de-157">In addition to drawing lines on the screen that show users where to write, you can draw cells on the screen in which characters or words are written.</span></span> <span data-ttu-id="f02de-158">Esto se denomina entrada de conversión boxing y es útil con algunos idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="f02de-158">This is called boxed input and is useful with some Asian languages.</span></span> <span data-ttu-id="f02de-159">Para determinar si el reconocedor es capaz de proporcionar una entrada de conversión boxing, llame a la propiedad [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) del objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) .</span><span class="sxs-lookup"><span data-stu-id="f02de-159">To determine if the recognizer is capable of boxed input, call the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object.</span></span>

<span data-ttu-id="f02de-160">En la ilustración siguiente se muestra una guía de reconocedor con cuatro columnas.</span><span class="sxs-lookup"><span data-stu-id="f02de-160">The following figure shows a recognizer guide with four columns.</span></span>

![Ilustración en la que se muestra la guía del reconocedor con cuatro columnas](images/de44c07e-4b55-42d0-8e8b-997e2da79e52.jpg)

## <a name="requirements"></a><span data-ttu-id="f02de-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02de-162">Requirements</span></span>



| <span data-ttu-id="f02de-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="f02de-163">Requirement</span></span> | <span data-ttu-id="f02de-164">Value</span><span class="sxs-lookup"><span data-stu-id="f02de-164">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f02de-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02de-165">Minimum supported client</span></span><br/> | <span data-ttu-id="f02de-166">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f02de-166">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f02de-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02de-167">Minimum supported server</span></span><br/> | <span data-ttu-id="f02de-168">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f02de-168">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f02de-169">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f02de-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="f02de-170"><dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f02de-170"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f02de-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f02de-171">Library</span></span><br/>                  | <dl> <span data-ttu-id="f02de-172"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f02de-172"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f02de-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="f02de-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02de-174">**Interfaz IInkRecognizer**</span><span class="sxs-lookup"><span data-stu-id="f02de-174">**IInkRecognizer Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer)
</dt> <dt>

[<span data-ttu-id="f02de-175">**Clase InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="f02de-175">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

