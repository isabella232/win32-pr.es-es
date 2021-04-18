---
description: Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: Clase InkDivider (Msinkaut15. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688301"
---
# <a name="inkdivider-class"></a><span data-ttu-id="bdf2f-103">Clase InkDivider</span><span class="sxs-lookup"><span data-stu-id="bdf2f-103">InkDivider class</span></span>

<span data-ttu-id="bdf2f-104">Representa la capacidad de analizar el diseño de una colección de trazos y dividirlos en texto y gráficos.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-104">Represents the ability to analyze the layout of a collection of strokes and divide them into text and graphics.</span></span>

<span data-ttu-id="bdf2f-105">**InkDivider** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bdf2f-105">**InkDivider** has these types of members:</span></span>

-   [<span data-ttu-id="bdf2f-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="bdf2f-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="bdf2f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="bdf2f-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="bdf2f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bdf2f-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="bdf2f-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="bdf2f-109">Interfaces</span></span>

<span data-ttu-id="bdf2f-110">La clase **InkDivider** define estas interfaces.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-110">The **InkDivider** class defines these interfaces.</span></span>



| <span data-ttu-id="bdf2f-111">Interfaz</span><span class="sxs-lookup"><span data-stu-id="bdf2f-111">Interface</span></span>       | <span data-ttu-id="bdf2f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdf2f-112">Description</span></span>                                                          |
|:----------------|:---------------------------------------------------------------------|
| <span data-ttu-id="bdf2f-113">**IInkDivider**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-113">**IInkDivider**</span></span> | <span data-ttu-id="bdf2f-114">Este objeto implementa la interfaz com **IInkDivider** .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-114">This object implements the **IInkDivider** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="bdf2f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="bdf2f-115">Methods</span></span>

<span data-ttu-id="bdf2f-116">La clase **InkDivider** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-116">The **InkDivider** class has these methods.</span></span>



| <span data-ttu-id="bdf2f-117">Método</span><span class="sxs-lookup"><span data-stu-id="bdf2f-117">Method</span></span>                              | <span data-ttu-id="bdf2f-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdf2f-118">Description</span></span>                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdf2f-119">**Dividir**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-119">**Divide**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | <span data-ttu-id="bdf2f-120">Devuelve un objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) que contiene información estructural sobre los trazos en el objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-120">Returns an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object that contains structural information about the strokes in the **InkDivider** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bdf2f-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bdf2f-121">Properties</span></span>

<span data-ttu-id="bdf2f-122">La clase **InkDivider** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-122">The **InkDivider** class has these properties.</span></span>



| <span data-ttu-id="bdf2f-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bdf2f-123">Property</span></span>                                                             | <span data-ttu-id="bdf2f-124">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="bdf2f-124">Access type</span></span>           | <span data-ttu-id="bdf2f-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdf2f-125">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bdf2f-126">**LineHeight**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-126">**LineHeight**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | <span data-ttu-id="bdf2f-127">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bdf2f-127">Read/write</span></span><br/> | <span data-ttu-id="bdf2f-128">Obtiene o establece el alto de escritura a mano esperado en unidades HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-128">Gets or sets the expected handwriting height in HIMETRIC units.</span></span><br/>                                                      |
| [<span data-ttu-id="bdf2f-129">**Estableció**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-129">**RecognizerContext**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | <span data-ttu-id="bdf2f-130">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bdf2f-130">Read/write</span></span><br/> | <span data-ttu-id="bdf2f-131">Obtiene o establece el objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) que se usa para el reconocimiento de escritura a mano.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-131">Gets or sets the [**InkRecognizerContext**](inkrecognizercontext-class.md) object used for handwriting recognition.</span></span><br/> |
| [<span data-ttu-id="bdf2f-132">**Trazos**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-132">**Strokes**</span></span>](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | <span data-ttu-id="bdf2f-133">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bdf2f-133">Read/write</span></span><br/> | <span data-ttu-id="bdf2f-134">Obtiene o establece la colección [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que contiene el objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-134">Gets or sets the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained by the **InkDivider** object.</span></span> <br/>     |



 

## <a name="remarks"></a><span data-ttu-id="bdf2f-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bdf2f-135">Remarks</span></span>

<span data-ttu-id="bdf2f-136">Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-136">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="bdf2f-137">El objeto **InkDivider** utiliza el diseño de los trazos, el orden en que se agregan los trazos, la dirección en la que se dibujan los trazos y otros factores para realizar el análisis de la tinta.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-137">The **InkDivider** object uses the layout of the strokes, the order in which the strokes are added, the direction in which the strokes are drawn, and other factors to perform the analysis of the ink.</span></span> <span data-ttu-id="bdf2f-138">La colección [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) que analiza el objeto **InkDivider** se encuentra en la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) del objeto **InkDivider** .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-138">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that the **InkDivider** object analyzes is contained in the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property of the **InkDivider** object.</span></span> <span data-ttu-id="bdf2f-139">El objeto **InkDivider** analiza dinámicamente la colección InkStrokes a medida que se agrega o se elimina de la colección, pero no realiza ninguna modificación de los trazos.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-139">The **InkDivider** object dynamically analyzes the InkStrokes collection as you add to or delete from the collection, but it performs no modification of the strokes.</span></span>

<span data-ttu-id="bdf2f-140">Los resultados del análisis se devuelven en un objeto [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-140">The analysis results are returned in an [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

<span data-ttu-id="bdf2f-141">El objeto **InkDivider** usa un objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) para dividir con más precisión los trazos y asignar una cadena de reconocimiento a los resultados.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-141">The **InkDivider** object uses an [**InkRecognizerContext**](inkrecognizercontext-class.md) object to more accurately divide the strokes and to assign a recognition string to the results.</span></span>

> [!Note]  
> <span data-ttu-id="bdf2f-142">El objeto **InkDivider** usa los valores de propiedad predeterminados del objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-142">The **InkDivider** object uses the default property settings of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="bdf2f-143">Si no asigna un contexto de reconocedor al objeto **InkDivider** , el objeto **InkDivider** sigue analizando la tinta, pero divide los trazos con menos precisión y no asocia el texto con los resultados de la división.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-143">If you do not assign a recognizer context to the **InkDivider** object, the **InkDivider** object still analyzes the ink, but it divides the strokes less accurately and does not associate text with the division results.</span></span>

> [!Note]  
> <span data-ttu-id="bdf2f-144">La propiedad [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) debe establecerse antes de agregar trazos a la propiedad [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-144">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property should be set before adding strokes to the [**Strokes**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes) property.</span></span> <span data-ttu-id="bdf2f-145">Una vez agregados los trazos al objeto **InkDivider** , no se puede cambiar la propiedad **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="bdf2f-145">After strokes have been added to the **InkDivider** object, the **RecognizerContext** property cannot be changed.</span></span>

 

<span data-ttu-id="bdf2f-146">El **InkDivider** no admite actualmente idiomas verticales.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-146">The **InkDivider** does not currently support vertical languages.</span></span> <span data-ttu-id="bdf2f-147">Para que el objeto **InkDivider** reconozca estos idiomas correctamente, el objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para el lenguaje debe admitir la capacidad de entrada libre y los caracteres deben escribirse de izquierda a derecha.</span><span class="sxs-lookup"><span data-stu-id="bdf2f-147">For the **InkDivider** object to recognize these languages properly the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object for the language must support the free input capability and the characters must be written from left to right.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf2f-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf2f-148">Requirements</span></span>



| <span data-ttu-id="bdf2f-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf2f-149">Requirement</span></span> | <span data-ttu-id="bdf2f-150">Value</span><span class="sxs-lookup"><span data-stu-id="bdf2f-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf2f-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdf2f-151">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf2f-152">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bdf2f-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bdf2f-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bdf2f-153">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf2f-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bdf2f-154">None supported</span></span><br/>                                                                                               |
| <span data-ttu-id="bdf2f-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdf2f-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf2f-156"><dt>Msinkaut15. h (también requiere Msinkaut15 \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bdf2f-156"><dt>Msinkaut15.h (also requires Msinkaut15\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bdf2f-157">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdf2f-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdf2f-158"><dt>Inkdiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdf2f-158"><dt>Inkdiv.dll</dt></span></span> </dl>                                   |



## <a name="see-also"></a><span data-ttu-id="bdf2f-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="bdf2f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf2f-160">**Interfaz IInkDivisionResult**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-160">**IInkDivisionResult Interface**</span></span>](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[<span data-ttu-id="bdf2f-161">**Clase InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="bdf2f-161">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

<span data-ttu-id="bdf2f-162">[Colección InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bdf2f-162">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

