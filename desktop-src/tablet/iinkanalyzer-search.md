---
description: Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: 'IInkAnalyzer:: Search (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Search
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ea9755c0f2836b363b967a3d6bfdc5d64a1305b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154408"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="67b3f-103">IInkAnalyzer:: Search (método)</span><span class="sxs-lookup"><span data-stu-id="67b3f-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="67b3f-104">Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="67b3f-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="67b3f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67b3f-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="67b3f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67b3f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67b3f-107">*bstrPhraseToMatch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67b3f-108">La frase que se encontrará en las alternativas para los trazos analizados actualmente.</span><span class="sxs-lookup"><span data-stu-id="67b3f-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="67b3f-109">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67b3f-110">Número máximo de resultados que se devuelven de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="67b3f-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="67b3f-111">*ppulStrokeCountPerResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67b3f-112">Puntero a una matriz del número de trazos en cada resultado de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="67b3f-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="67b3f-113">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="67b3f-114">Número de identificadores de trazo en *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="67b3f-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="67b3f-115">*ppulStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67b3f-116">Puntero a una matriz de identificadores de trazo que representa un conjunto de conjuntos de trazos.</span><span class="sxs-lookup"><span data-stu-id="67b3f-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67b3f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67b3f-117">Return value</span></span>

<span data-ttu-id="67b3f-118">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="67b3f-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="67b3f-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67b3f-119">Remarks</span></span>

<span data-ttu-id="67b3f-120">Esta búsqueda busca subcadenas con varias palabras y una sola palabra.</span><span class="sxs-lookup"><span data-stu-id="67b3f-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="67b3f-121">Se busca en los resultados de reconocimiento alternativos y en los segmentaciones alternativos.</span><span class="sxs-lookup"><span data-stu-id="67b3f-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="67b3f-122">Todas las cadenas de entrada se convertirán en un único uso de mayúsculas y minúsculas para la comparación mediante el LCID del subproceso actual para realizar esta conversión para respetar las convenciones culturales de casos.</span><span class="sxs-lookup"><span data-stu-id="67b3f-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="67b3f-123">La cadena que se pasa se trata como una frase.</span><span class="sxs-lookup"><span data-stu-id="67b3f-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="67b3f-124">Las palabras y los caracteres deben aparecer en el alterantes para los trazos en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="67b3f-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="67b3f-125">La primera y la última palabra de la frase pueden coincidir como subcadenas (la primera palabra aparece al final de una alternativa y la última palabra aparece en el begginging de una), pero otras palabras (las que se encuentran dentro de la frase) deben aparecer como palabras completas.</span><span class="sxs-lookup"><span data-stu-id="67b3f-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="67b3f-126">Si la cadena que se pasa no tiene ningún espacio en blanco entre los caracteres, la subcadena se puede encontrar en cualquier parte dentro de una sola palabra en una alternativa.</span><span class="sxs-lookup"><span data-stu-id="67b3f-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="67b3f-127">Solo la presencia o ausencia de espacio en blanco entre los caracteres cambia los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="67b3f-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="67b3f-128">Se omiten los espacios en blanco que no están rodeados por caracteres.</span><span class="sxs-lookup"><span data-stu-id="67b3f-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="67b3f-129">Se omite el tipo de espacio en blanco (una tabulación o un espacio entre los caracteres darán el mismo resultado).</span><span class="sxs-lookup"><span data-stu-id="67b3f-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="67b3f-130">La cantidad de espacio en blanco no importa: un espacio o dos espacios entre caracteres darán el mismo resultado.</span><span class="sxs-lookup"><span data-stu-id="67b3f-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="67b3f-131">La búsqueda no genera eventos PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="67b3f-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="67b3f-132">Solo se buscarán los trazos que ya se han rellenado.</span><span class="sxs-lookup"><span data-stu-id="67b3f-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="67b3f-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67b3f-133">Requirements</span></span>



| <span data-ttu-id="67b3f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="67b3f-134">Requirement</span></span> | <span data-ttu-id="67b3f-135">Value</span><span class="sxs-lookup"><span data-stu-id="67b3f-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b3f-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67b3f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="67b3f-137">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="67b3f-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="67b3f-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67b3f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="67b3f-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="67b3f-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="67b3f-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67b3f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="67b3f-141"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="67b3f-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="67b3f-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67b3f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67b3f-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67b3f-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="67b3f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="67b3f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67b3f-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="67b3f-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




