---
description: Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.
ms.assetid: dfd481f9-38fd-433f-b1fc-697c735c13da
title: 'IInkAnalyzer:: SearchWithLanguageId (método) (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SearchWithLanguageId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 829878a6fd326abb8a685b644cfc222ba6921385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809997"
---
# <a name="iinkanalyzersearchwithlanguageid-method"></a><span data-ttu-id="bc420-103">IInkAnalyzer:: SearchWithLanguageId (método)</span><span class="sxs-lookup"><span data-stu-id="bc420-103">IInkAnalyzer::SearchWithLanguageId method</span></span>

<span data-ttu-id="bc420-104">Proporciona una búsqueda aproximada de mayúsculas y minúsculas basada en frases para los trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="bc420-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc420-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc420-105">Syntax</span></span>


```C++
HRESULT SearchWithLanguageId(
  [in]      BSTR  bstrPhraseToMatch,
  [in]      LONG  lSearchStringLanguageId,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="bc420-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bc420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc420-107">*bstrPhraseToMatch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc420-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-108">La frase que se encontrará en las alternativas para los trazos analizados actualmente.</span><span class="sxs-lookup"><span data-stu-id="bc420-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="bc420-109">*lSearchStringLanguageId* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bc420-109">*lSearchStringLanguageId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-110">LCID asociado a la cadena que se pasa.</span><span class="sxs-lookup"><span data-stu-id="bc420-110">The LCID associated with the string that is passed.</span></span> <span data-ttu-id="bc420-111">Se utiliza para convertir el caso internamente para admitir comparaciones que no distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bc420-111">Used to convert the case internally to support case insensitive comparisons.</span></span>

</dd> <dt>

<span data-ttu-id="bc420-112">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc420-112">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-113">Número máximo de resultados que se devuelven de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bc420-113">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="bc420-114">*ppulStrokeCountPerResult* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc420-114">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-115">Puntero a una matriz del número de trazos en cada resultado de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bc420-115">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="bc420-116">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bc420-116">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-117">Número de identificadores de trazo en *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="bc420-117">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="bc420-118">*ppulStrokeIds* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bc420-118">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc420-119">Puntero a una matriz de identificadores de trazo que representa un conjunto de conjuntos de trazos.</span><span class="sxs-lookup"><span data-stu-id="bc420-119">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc420-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bc420-120">Return value</span></span>

<span data-ttu-id="bc420-121">Para obtener una descripción de los valores devueltos, vea [clases e interfaces-análisis de tinta](classes-and-interfaces---ink-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="bc420-121">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc420-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bc420-122">Remarks</span></span>

<span data-ttu-id="bc420-123">Esta búsqueda busca subcadenas con varias palabras y una sola palabra.</span><span class="sxs-lookup"><span data-stu-id="bc420-123">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="bc420-124">Se busca en los resultados de reconocimiento alternativos y en los segmentaciones alternativos.</span><span class="sxs-lookup"><span data-stu-id="bc420-124">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="bc420-125">Todas las cadenas de entrada se convertirán en un único uso de mayúsculas y minúsculas para la comparación mediante el LCID del subproceso actual para realizar esta conversión para respetar las convenciones culturales de casos.</span><span class="sxs-lookup"><span data-stu-id="bc420-125">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="bc420-126">La cadena que se pasa se trata como una frase.</span><span class="sxs-lookup"><span data-stu-id="bc420-126">The string passed is treated as a phrase.</span></span> <span data-ttu-id="bc420-127">Las palabras y los caracteres deben aparecer en el alterantes para los trazos en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="bc420-127">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="bc420-128">La primera y la última palabra de la frase pueden coincidir como subcadenas (la primera palabra aparece al final de una alternativa y la última palabra aparece en el begginging de una), pero otras palabras (las que se encuentran dentro de la frase) deben aparecer como palabras completas.</span><span class="sxs-lookup"><span data-stu-id="bc420-128">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="bc420-129">Si la cadena que se pasa no tiene ningún espacio en blanco entre los caracteres, la subcadena se puede encontrar en cualquier parte dentro de una sola palabra en una alternativa.</span><span class="sxs-lookup"><span data-stu-id="bc420-129">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="bc420-130">Solo la presencia o ausencia de espacio en blanco entre los caracteres cambia los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="bc420-130">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="bc420-131">Se omiten los espacios en blanco que no están rodeados por caracteres.</span><span class="sxs-lookup"><span data-stu-id="bc420-131">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="bc420-132">Se omite el tipo de espacio en blanco (una tabulación o un espacio entre los caracteres darán el mismo resultado).</span><span class="sxs-lookup"><span data-stu-id="bc420-132">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="bc420-133">La cantidad de espacio en blanco no importa: un espacio o dos espacios entre caracteres darán el mismo resultado.</span><span class="sxs-lookup"><span data-stu-id="bc420-133">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="bc420-134">La búsqueda no genera eventos PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="bc420-134">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="bc420-135">Solo se buscarán los trazos que ya se han rellenado.</span><span class="sxs-lookup"><span data-stu-id="bc420-135">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc420-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc420-136">Requirements</span></span>



| <span data-ttu-id="bc420-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc420-137">Requirement</span></span> | <span data-ttu-id="bc420-138">Value</span><span class="sxs-lookup"><span data-stu-id="bc420-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc420-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc420-139">Minimum supported client</span></span><br/> | <span data-ttu-id="bc420-140">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bc420-140">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="bc420-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc420-141">Minimum supported server</span></span><br/> | <span data-ttu-id="bc420-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="bc420-142">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="bc420-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc420-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc420-144"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bc420-144"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bc420-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc420-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc420-146"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc420-146"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="bc420-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc420-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc420-148">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="bc420-148">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




