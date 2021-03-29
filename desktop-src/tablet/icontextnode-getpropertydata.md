---
description: Recupera datos específicos de la aplicación u otros datos de propiedad para el identificador especificado.
ms.assetid: eaf95ff8-7b31-4c05-aa49-0c3bb9e996c0
title: 'IContextNode:: GetPropertyData (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 381d137dd73056a2a6f4c2e9cd3746f9f16c5b2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810034"
---
# <a name="icontextnodegetpropertydata-method"></a><span data-ttu-id="cfb24-103">IContextNode:: GetPropertyData (método)</span><span class="sxs-lookup"><span data-stu-id="cfb24-103">IContextNode::GetPropertyData method</span></span>

<span data-ttu-id="cfb24-104">Recupera datos específicos de la aplicación u otros datos de propiedad para el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="cfb24-104">Retrieves application-specific data or other property data for the specified identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb24-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cfb24-105">Syntax</span></span>


```C++
HRESULT GetPropertyData(
  [in]      const GUID  *pPropertyDataId,
  [in, out]       ULONG *pulPropertyDataSize,
  [out]           BYTE  **ppbPropertyData
);
```



## <a name="parameters"></a><span data-ttu-id="cfb24-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfb24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb24-107">*pPropertyDataId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cfb24-107">*pPropertyDataId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb24-108">El identificador de los datos.</span><span class="sxs-lookup"><span data-stu-id="cfb24-108">The identifier for the data.</span></span>

</dd> <dt>

<span data-ttu-id="cfb24-109">*pulPropertyDataSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cfb24-109">*pulPropertyDataSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb24-110">Tamaño de los datos en bytes.</span><span class="sxs-lookup"><span data-stu-id="cfb24-110">The size of the data in bytes.</span></span> <span data-ttu-id="cfb24-111">No se utiliza el valor que se pasa.</span><span class="sxs-lookup"><span data-stu-id="cfb24-111">The value that is passed in is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cfb24-112">*ppbPropertyData* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cfb24-112">*ppbPropertyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb24-113">Puntero a una matriz de enteros de 8 bits sin signo que contiene los datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="cfb24-113">A pointer to an 8-bit unsigned integer array that contains the property data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb24-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cfb24-114">Return value</span></span>

<span data-ttu-id="cfb24-115">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cfb24-115">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfb24-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfb24-116">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="cfb24-117">Para evitar una pérdida de memoria, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar la memoria de \* *ppbPropertyData* cuando ya no necesite la información.</span><span class="sxs-lookup"><span data-stu-id="cfb24-117">To avoid a memory leak, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) to release the memory from \**ppbPropertyData* when you no longer need the information.</span></span>

 

<span data-ttu-id="cfb24-118">Además de recuperar los datos específicos de la aplicación que se agregaron con [**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md), este método se usa para recuperar propiedades comunes que se describen en las constantes de [las propiedades del nodo de contexto](context-node-properties.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb24-118">In addition to retrieving application-specific data that was added with [**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md), this method is used to retrieve common properties that are described by the [Context Node Properties](context-node-properties.md) constants.</span></span>

<span data-ttu-id="cfb24-119">Las propiedades de tipo cadena incluyen:</span><span class="sxs-lookup"><span data-stu-id="cfb24-119">The string-type properties include:</span></span>

-   <span data-ttu-id="cfb24-120">GUID \_ CNP \_ RECOGNIZEDSTRING</span><span class="sxs-lookup"><span data-stu-id="cfb24-120">GUID\_CNP\_RECOGNIZEDSTRING</span></span>
-   <span data-ttu-id="cfb24-121">GUID \_ CNP \_ nombredeforma</span><span class="sxs-lookup"><span data-stu-id="cfb24-121">GUID\_CNP\_SHAPENAME</span></span>
-   <span data-ttu-id="cfb24-122">GUID \_ AHP \_ ANALYSISHINTNAME</span><span class="sxs-lookup"><span data-stu-id="cfb24-122">GUID\_AHP\_ANALYSISHINTNAME</span></span>
-   <span data-ttu-id="cfb24-123">GUID \_ AHP \_ PREFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="cfb24-123">GUID\_AHP\_PREFIXTEXT</span></span>
-   <span data-ttu-id="cfb24-124">GUID \_ AHP \_ SUFFIXTEXT</span><span class="sxs-lookup"><span data-stu-id="cfb24-124">GUID\_AHP\_SUFFIXTEXT</span></span>
-   <span data-ttu-id="cfb24-125">GUID \_ AHP \_ FACTOID</span><span class="sxs-lookup"><span data-stu-id="cfb24-125">GUID\_AHP\_FACTOID</span></span>

<span data-ttu-id="cfb24-126">El valor devuelto es \*\* \* WCHAR\*_. Si convierte el parámetro \_ *ppbPropertyData* en \**WCHAR \** ,_ la longitud devuelta es `(length of the string + 1) _ sizeof(WCHAR)` .</span><span class="sxs-lookup"><span data-stu-id="cfb24-126">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `(length of the string + 1) _ sizeof(WCHAR)`.</span></span>

<span data-ttu-id="cfb24-127">Las propiedades de tipo booleano incluyen:</span><span class="sxs-lookup"><span data-stu-id="cfb24-127">The Boolean-type properties include:</span></span>

-   <span data-ttu-id="cfb24-128">GUID \_ AHP \_ OVERRIDELANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="cfb24-128">GUID\_AHP\_OVERRIDELANGUAGEID</span></span>
-   <span data-ttu-id="cfb24-129">GUID \_ AHP \_ COERCETOFACTOID</span><span class="sxs-lookup"><span data-stu-id="cfb24-129">GUID\_AHP\_COERCETOFACTOID</span></span>
-   <span data-ttu-id="cfb24-130">GUID \_ AHP \_ WORDMODE</span><span class="sxs-lookup"><span data-stu-id="cfb24-130">GUID\_AHP\_WORDMODE</span></span>

<span data-ttu-id="cfb24-131">El valor devuelto es **Variant \_ bool**.</span><span class="sxs-lookup"><span data-stu-id="cfb24-131">The return value is **VARIANT\_BOOL**.</span></span> <span data-ttu-id="cfb24-132">Si convierte el parámetro \* *ppbPropertyData* en \**Variant \_ bool \** _, la longitud devuelta es `sizeof(VARIANT_BOOL)` .</span><span class="sxs-lookup"><span data-stu-id="cfb24-132">If you cast the \**ppbPropertyData* parameter to \**VARIANT\_BOOL\** _ its returned length is `sizeof(VARIANT_BOOL)`.</span></span>

<span data-ttu-id="cfb24-133">GUID \_ AHP \_ Guide es una propiedad de tipo guía.</span><span class="sxs-lookup"><span data-stu-id="cfb24-133">GUID\_AHP\_GUIDE is a guide-type property.</span></span> <span data-ttu-id="cfb24-134">El valor devuelto _*es \* InkAnalysisRecognitionGuide*_.</span><span class="sxs-lookup"><span data-stu-id="cfb24-134">The return value is _*InkAnalysisRecognitionGuide\**_.</span></span> <span data-ttu-id="cfb24-135">Si convierte el parámetro \_ *ppbPropertyData* en \**InkAnalysisRecognitionGuide \** _, su longitud devuelta es `sizeof(InkAnalysisRecognitionGuide)` .</span><span class="sxs-lookup"><span data-stu-id="cfb24-135">If you cast the \_*ppbPropertyData* parameter to \**InkAnalysisRecognitionGuide\** _ its returned length is `sizeof(InkAnalysisRecognitionGuide)`.</span></span>

<span data-ttu-id="cfb24-136">Las propiedades de tipo entero incluyen:</span><span class="sxs-lookup"><span data-stu-id="cfb24-136">Integer-type properties include:</span></span>

-   <span data-ttu-id="cfb24-137">GUID \_ CNP \_ LINENUMBER</span><span class="sxs-lookup"><span data-stu-id="cfb24-137">GUID\_CNP\_LINENUMBER</span></span>
-   <span data-ttu-id="cfb24-138">GUID \_ CNP \_ POINTSPERINCH</span><span class="sxs-lookup"><span data-stu-id="cfb24-138">GUID\_CNP\_POINTSPERINCH</span></span>
-   <span data-ttu-id="cfb24-139">GUID \_ CNP \_ CONFIDENCELEVEL</span><span class="sxs-lookup"><span data-stu-id="cfb24-139">GUID\_CNP\_CONFIDENCELEVEL</span></span>
-   <span data-ttu-id="cfb24-140">\_confirmación de CNP de GUID \_</span><span class="sxs-lookup"><span data-stu-id="cfb24-140">GUID\_CNP\_CONFIRMATION</span></span>
-   <span data-ttu-id="cfb24-141">GUID \_ CNP \_ MAXIMUMSTROKECOUNT</span><span class="sxs-lookup"><span data-stu-id="cfb24-141">GUID\_CNP\_MAXIMUMSTROKECOUNT</span></span>
-   <span data-ttu-id="cfb24-142">\_segmentación de GUID CNP \_</span><span class="sxs-lookup"><span data-stu-id="cfb24-142">GUID\_CNP\_SEGMENTATION</span></span>
-   <span data-ttu-id="cfb24-143">GUID \_ CNP \_ ALIGNMENTLEVEL</span><span class="sxs-lookup"><span data-stu-id="cfb24-143">GUID\_CNP\_ALIGNMENTLEVEL</span></span>

<span data-ttu-id="cfb24-144">El valor devuelto _*es \* Long*_.</span><span class="sxs-lookup"><span data-stu-id="cfb24-144">The return value is _*LONG\**_.</span></span> <span data-ttu-id="cfb24-145">Si convierte el parámetro \_ *ppbPropertyData* en \**Long \** _ la longitud devuelta es `sizeof(LONG)` .</span><span class="sxs-lookup"><span data-stu-id="cfb24-145">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)`.</span></span>

<span data-ttu-id="cfb24-146">Métricas de línea: las propiedades de tipo incluyen:</span><span class="sxs-lookup"><span data-stu-id="cfb24-146">Line metrics-type properties include:</span></span>

-   <span data-ttu-id="cfb24-147">GUID \_ CNP \_ ascendente</span><span class="sxs-lookup"><span data-stu-id="cfb24-147">GUID\_CNP\_ASCENDERS</span></span>
-   <span data-ttu-id="cfb24-148">GUID \_ CNP \_ descendente</span><span class="sxs-lookup"><span data-stu-id="cfb24-148">GUID\_CNP\_DESCENDERS</span></span>
-   <span data-ttu-id="cfb24-149">\_línea base de CNP de GUID \_</span><span class="sxs-lookup"><span data-stu-id="cfb24-149">GUID\_CNP\_BASELINE</span></span>
-   <span data-ttu-id="cfb24-150">CNP de GUID \_ \_</span><span class="sxs-lookup"><span data-stu-id="cfb24-150">GUID\_CNP\_MIDLINE</span></span>

<span data-ttu-id="cfb24-151">El valor devuelto _*es \* Long*_.</span><span class="sxs-lookup"><span data-stu-id="cfb24-151">The return value is _*LONG\**_.</span></span> <span data-ttu-id="cfb24-152">Si convierte el parámetro \_ *ppbPropertyData* en \**Long \** _ la longitud devuelta es, lo que indica `sizeof(LONG)_4` los valores (x, y) de los puntos de inicio seguidos de los valores (x, y) de los puntos finales.</span><span class="sxs-lookup"><span data-stu-id="cfb24-152">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_4`, signifying the (x, y) values for the starting points followed by the (x, y) values for the ending points.</span></span>

<span data-ttu-id="cfb24-153">GUID \_ CNP \_ TEXTRECOGNIZERID es una propiedad **GUID** .</span><span class="sxs-lookup"><span data-stu-id="cfb24-153">GUID\_CNP\_TEXTRECOGNIZERID is a **GUID** property.</span></span> <span data-ttu-id="cfb24-154">El valor devuelto es \*\* \* GUID\*_. Si convierte el parámetro \_ *ppbPropertyData* en \**GUID \** ,_ la longitud devuelta es `sizeof(GUID)` .</span><span class="sxs-lookup"><span data-stu-id="cfb24-154">The return value is \**GUID\**_. If you cast the \_*ppbPropertyData* parameter to \**GUID\**_ its returned length is `sizeof(GUID)`.</span></span>

<span data-ttu-id="cfb24-155">GUID \_ CNP \_ ROTATEDBOUNDINGBOX es una propiedad de rectángulo de selección rotado.</span><span class="sxs-lookup"><span data-stu-id="cfb24-155">GUID\_CNP\_ROTATEDBOUNDINGBOX is a rotated bounding box property.</span></span> <span data-ttu-id="cfb24-156">El valor devuelto _*es \* Long*_.</span><span class="sxs-lookup"><span data-stu-id="cfb24-156">The return value is _*LONG\**_.</span></span> <span data-ttu-id="cfb24-157">Si convierte el parámetro \_ *ppbPropertyData* en \**\* Long* _ la longitud devuelta es, lo que significa que los `sizeof(LONG)_8` valores (x, y) de las cuatro esquinas del cuadro.</span><span class="sxs-lookup"><span data-stu-id="cfb24-157">If you cast the \_*ppbPropertyData* parameter to \**LONG\** _ its returned length is `sizeof(LONG)_8`, signifying the (x, y) values for the four corners of the box.</span></span>

<span data-ttu-id="cfb24-158">GUID \_ CNP \_ Hotpoint es una propiedad de punto de acceso frecuente.</span><span class="sxs-lookup"><span data-stu-id="cfb24-158">GUID\_CNP\_HOTPOINT is a hot point property.</span></span> <span data-ttu-id="cfb24-159">El valor devuelto es \*\* \* Long\*_. Si convierte el parámetro \_ *ppbPropertyData* en \**Long \**_ , la longitud devuelta es, lo que `sizeof(LONG)_2` significa los valores (x, y) para el punto.</span><span class="sxs-lookup"><span data-stu-id="cfb24-159">The return value is \**LONG\**_. If you cast the \_*ppbPropertyData* parameter to \**LONG\**_ its returned length is `sizeof(LONG)_2`, signifying the (x, y) values for the point.</span></span>

<span data-ttu-id="cfb24-160">GUID \_ AHP \_ lista de palabras es una propiedad de lista de palabras.</span><span class="sxs-lookup"><span data-stu-id="cfb24-160">GUID\_AHP\_WORDLIST is a word list property.</span></span> <span data-ttu-id="cfb24-161">El valor devuelto es \*\* \* WCHAR\*_. Si convierte el parámetro \_ *ppbPropertyData* en \**WCHAR \**_ , la longitud devuelta es `n _ sizeof(WCHAR)` , donde `n` es la suma de las longitudes de cadena del número de cadenas de la lista más 1 para cada carácter de terminación **null** para cada cadena.</span><span class="sxs-lookup"><span data-stu-id="cfb24-161">The return value is \**WCHAR\**_. If you cast the \_*ppbPropertyData* parameter to \**WCHAR\**_ its returned length is `n _ sizeof(WCHAR)`, where `n` is the sum of the string lengths of the number of strings in the list plus 1 for each **NULL** termination character for each string.</span></span>

## <a name="examples"></a><span data-ttu-id="cfb24-162">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cfb24-162">Examples</span></span>

<span data-ttu-id="cfb24-163">Este ejemplo muestra un método que tiene acceso a la propiedad del nodo de contexto AlignmentLevel de un tipo de nodo de contexto de párrafo.</span><span class="sxs-lookup"><span data-stu-id="cfb24-163">This example shows a method that accesses the AlignmentLevel context node property of a Paragraph context node type.</span></span>


```C++
// Checks a paragraph context node's alignment level property.
// Only paragraph type context nodes contain the alignment level property.
HRESULT CMyClass::ExploreParagraphNode(
    IContextNode *pParagraphNode)
{
    // Get the AlignmentLevel property data for the paragraph.
    LONG * alignmentLevel = NULL;
    ULONG ulDataLen = 0;

    HRESULT hr = pParagraphNode->GetPropertyData(
        (const GUID*)&GUID_CNP_ALIGNMENTLEVEL,
        &ulDataLen,
        (BYTE**)&alignmentLevel);

    if( FAILED(hr) ||
        ulDataLen != sizeof(LONG) ||
        alignmentLevel == NULL )
    {
        // Insert code that handles an error here.
    }
    else
    {
        // Insert code that uses the alignment level here.
    }

    // Free the memory allocated for the property data.
    ::CoTaskMemFree(alignmentLevel);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="cfb24-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfb24-164">Requirements</span></span>



| <span data-ttu-id="cfb24-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb24-165">Requirement</span></span> | <span data-ttu-id="cfb24-166">Value</span><span class="sxs-lookup"><span data-stu-id="cfb24-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb24-167">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb24-167">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb24-168">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="cfb24-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="cfb24-169">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cfb24-169">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb24-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cfb24-170">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="cfb24-171">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cfb24-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb24-172"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="cfb24-172"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="cfb24-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cfb24-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfb24-174"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb24-174"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="cfb24-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfb24-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb24-176">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="cfb24-176">**IContextNode**</span></span>](icontextnode.md)
</dt> <dt>

[<span data-ttu-id="cfb24-177">**IContextNode::AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="cfb24-177">**IContextNode::AddPropertyData**</span></span>](icontextnode-addpropertydata.md)
</dt> <dt>

[<span data-ttu-id="cfb24-178">**IContextNode::RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="cfb24-178">**IContextNode::RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)
</dt> <dt>

[<span data-ttu-id="cfb24-179">**IContextNode::GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="cfb24-179">**IContextNode::GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)
</dt> <dt>

[<span data-ttu-id="cfb24-180">**IContextNode::ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="cfb24-180">**IContextNode::ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)
</dt> <dt>

[<span data-ttu-id="cfb24-181">**IContextNode::LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="cfb24-181">**IContextNode::LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="cfb24-182">**IContextNode::SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="cfb24-182">**IContextNode::SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)
</dt> <dt>

[<span data-ttu-id="cfb24-183">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="cfb24-183">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

