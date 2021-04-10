---
description: Recupera los resultados del análisis del objeto InkDivider.
ms.assetid: 7fc2bb5a-172f-4f4e-84dd-e31925f86982
title: CallDivideResults función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResults
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 11878e6a0ac953b9b7eb27ce21bb67001f9d88d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153597"
---
# <a name="calldivideresults-function"></a><span data-ttu-id="f9398-103">CallDivideResults función)</span><span class="sxs-lookup"><span data-stu-id="f9398-103">CallDivideResults function</span></span>

<span data-ttu-id="f9398-104">Recupera los resultados del análisis del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-104">Retrieves analysis results from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="f9398-105">Esta función no está pensada para ser utilizada por el código de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f9398-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9398-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9398-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResults(
  _In_  INT_PTR   hDivider,
  _Out_ int       aWordStrokeIds[],
  _Out_ int       aLineStrokeIds[],
  _Out_ int       aParagraphStrokeIds[],
  _Out_ int       aDrawingStrokeIds[],
  _Out_ SAFEARRAY **pastrWords,
  _Out_ SAFEARRAY **pastrLines,
  _Out_ SAFEARRAY **pastrParagraphs,
  _Out_ int       *aWordRotationCenterX,
  _Out_ int       *aWordRotationCenterY,
  _Out_ float     *aWordAngle,
  _Out_ int       *aLineRotationCenterX,
  _Out_ int       *aLineRotationCenterY,
  _Out_ float     *aLineAngle
);
```



## <a name="parameters"></a><span data-ttu-id="f9398-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f9398-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9398-108">*hDivider* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="f9398-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-109">Identificador del objeto [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-110">*aWordStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-110">*aWordStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-111">Matriz de identificadores asociados a la palabra que se pasa a la clase [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-111">An array of identifiers associated with the word that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-112">*aLineStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-112">*aLineStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-113">Matriz de propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados a la línea que se pasa a la clase [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-113">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the line that is passed in to the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-114">*aParagraphStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-114">*aParagraphStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-115">Una matriz de las propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados con el párrafo de la clase [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-115">An array of the [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the paragraph from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-116">*aDrawingStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-116">*aDrawingStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-117">Matriz de propiedades de [**identificador**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) para los objetos [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) asociados al dibujo de la clase [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f9398-117">An array of [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects associated with the drawing from the [**InkDivider**](inkdivider-class.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-118">*pastrWords* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-118">*pastrWords* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-119">Matriz de palabras devuelta por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="f9398-119">An array of words returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-120">*pastrLines* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-120">*pastrLines* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-121">Matriz de líneas devuelta por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="f9398-121">An array of lines returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-122">*pastrParagraphs* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-122">*pastrParagraphs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-123">Matriz de párrafos devuelta por el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="f9398-123">An array of paragraphs returned from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-124">*aWordRotationCenterX* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-124">*aWordRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-125">Matriz de los puntos centrales de las palabras a lo largo del eje x del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="f9398-125">An array of the center points of the words along the x-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-126">*aWordRotationCenterY* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-126">*aWordRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-127">Matriz de los puntos centrales de las palabras a lo largo del eje y del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="f9398-127">An array of the center points of the words along the y-axis from ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-128">*aWordAngle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-128">*aWordAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-129">Una matriz que contiene los ángulos por los que se van a girar las palabras para obtener los mejores resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="f9398-129">An array containing the angles by which to rotate the words for best analysis results.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-130">*aLineRotationCenterX* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-130">*aLineRotationCenterX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-131">Una matriz que contiene los puntos centrales de las líneas a lo largo del eje x.</span><span class="sxs-lookup"><span data-stu-id="f9398-131">An array containing the center points of the lines along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-132">*aLineRotationCenterY* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-132">*aLineRotationCenterY* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-133">Una matriz que contiene los puntos centrales de las líneas a lo largo del eje y.</span><span class="sxs-lookup"><span data-stu-id="f9398-133">An array containing the center points of the lines along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="f9398-134">*aLineAngle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f9398-134">*aLineAngle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9398-135">Una matriz que contiene los ángulos por los que se giran las líneas para obtener los mejores resultados del análisis.</span><span class="sxs-lookup"><span data-stu-id="f9398-135">An array containing the angles by which to rotate the lines for best analysis results.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9398-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f9398-136">Return value</span></span>

<span data-ttu-id="f9398-137">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="f9398-137">This function can return one of these values.</span></span>



| <span data-ttu-id="f9398-138">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f9398-138">Return code</span></span>                                                                                   | <span data-ttu-id="f9398-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9398-139">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="f9398-140"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f9398-140"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f9398-141">La función se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="f9398-141">The function succeeded.</span></span><br/>                                |
| <dl> <span data-ttu-id="f9398-142"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f9398-142"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f9398-143">El parámetro *hDivider* no es válido.</span><span class="sxs-lookup"><span data-stu-id="f9398-143">The *hDivider* parameter is invalid.</span></span><br/>                   |
| <dl> <span data-ttu-id="f9398-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f9398-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9398-145">No se pudo asignar suficiente memoria para almacenar los resultados.</span><span class="sxs-lookup"><span data-stu-id="f9398-145">Could not allocate enough memory to store the results.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9398-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9398-146">Remarks</span></span>

<span data-ttu-id="f9398-147">Para evitar pérdidas de memoria, debe liberar los recursos de *pastrWords*, *pastrLines* y *pastrParagraphs*.</span><span class="sxs-lookup"><span data-stu-id="f9398-147">To avoid memory leaks you must release the resources for *pastrWords*, *pastrLines*, and *pastrParagraphs*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9398-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9398-148">Requirements</span></span>



| <span data-ttu-id="f9398-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9398-149">Requirement</span></span> | <span data-ttu-id="f9398-150">Value</span><span class="sxs-lookup"><span data-stu-id="f9398-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9398-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9398-151">Minimum supported client</span></span><br/> | <span data-ttu-id="f9398-152">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f9398-152">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="f9398-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9398-153">Minimum supported server</span></span><br/> | <span data-ttu-id="f9398-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f9398-154">None supported</span></span><br/>                                                             |
| <span data-ttu-id="f9398-155">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f9398-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9398-156"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9398-156"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




