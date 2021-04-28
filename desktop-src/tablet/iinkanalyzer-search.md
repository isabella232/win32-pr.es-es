---
description: 'Método IInkAnalyzer::Search: proporciona una búsqueda aproximada basada en frases sin mayúsculas y minúsculas para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.'
ms.assetid: 5b5ce4b5-45ef-42ef-866b-2f38c32d8c86
title: Método IInkAnalyzer::Search (IACom.h)
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
ms.openlocfilehash: 94ccdebf8c8a134a845ff3df3017d710d1da93f1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113733"
---
# <a name="iinkanalyzersearch-method"></a><span data-ttu-id="4e02a-103">IInkAnalyzer::Search (método)</span><span class="sxs-lookup"><span data-stu-id="4e02a-103">IInkAnalyzer::Search method</span></span>

<span data-ttu-id="4e02a-104">Proporciona una búsqueda aproximada y sin mayúsculas de minúsculas basada en frases para trazos de escritura analizados y trazos de dibujo analizados que tienen tipos reconocidos.</span><span class="sxs-lookup"><span data-stu-id="4e02a-104">Provides a fuzzy, case-insensitive phrase based search for analyzed writing strokes and analyzed drawing strokes that have recognized types.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e02a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e02a-105">Syntax</span></span>


```C++
HRESULT Search(
  [in]      BSTR  bstrPhraseToMatch,
  [in, out] ULONG *pulSearchResultCount,
  [out]     ULONG **ppulStrokeCountPerResult,
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     ULONG **ppulStrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="4e02a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e02a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e02a-107">*bstrPhraseToMatch* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-107">*bstrPhraseToMatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e02a-108">Frase que se encontrará en las alternativas para los trazos analizados actualmente.</span><span class="sxs-lookup"><span data-stu-id="4e02a-108">The phrase that will be found in the alternates for the currently analyzed strokes.</span></span>

</dd> <dt>

<span data-ttu-id="4e02a-109">*pulSearchResultCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-109">*pulSearchResultCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e02a-110">Número máximo de resultados devueltos por la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4e02a-110">The maximum number of results returned from the search.</span></span>

</dd> <dt>

<span data-ttu-id="4e02a-111">*ppulStrokeCountPerResult* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-111">*ppulStrokeCountPerResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e02a-112">Puntero a una matriz del número de trazos en cada resultado de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4e02a-112">Pointer to an array of the number of strokes in each search result.</span></span>

</dd> <dt>

<span data-ttu-id="4e02a-113">*pulStrokeIdsCount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-113">*pulStrokeIdsCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e02a-114">Número de id. de trazo en *ppulStrokeIds*.</span><span class="sxs-lookup"><span data-stu-id="4e02a-114">The number of stroke IDs in *ppulStrokeIds*.</span></span>

</dd> <dt>

<span data-ttu-id="4e02a-115">*ppulStrokeIds* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-115">*ppulStrokeIds* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e02a-116">Puntero a una matriz de los ID de trazo que representan un conjunto de conjuntos de trazos.</span><span class="sxs-lookup"><span data-stu-id="4e02a-116">Pointer to an array of stroke IDs representing a set of sets of strokes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e02a-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e02a-117">Return value</span></span>

<span data-ttu-id="4e02a-118">Para obtener una descripción de los valores [devueltos, vea Clases e interfaces: análisis de entrada de lápiz.](classes-and-interfaces---ink-analysis.md)</span><span class="sxs-lookup"><span data-stu-id="4e02a-118">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4e02a-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4e02a-119">Remarks</span></span>

<span data-ttu-id="4e02a-120">Esta búsqueda busca subcadenas de varias palabras y palabras únicas.</span><span class="sxs-lookup"><span data-stu-id="4e02a-120">This search finds multi-word and single word substrings.</span></span> <span data-ttu-id="4e02a-121">Se buscan resultados de reconocimiento alternativos y segmentaciones alternativas.</span><span class="sxs-lookup"><span data-stu-id="4e02a-121">Both alternate recognition results and alternate segmentations are searched.</span></span>

<span data-ttu-id="4e02a-122">Todas las cadenas entrantes se convertirán en un solo uso de mayúsculas y minúsculas para la comparación mediante el LCID del subproceso actual para realizar esta conversión con el fin de respetar las convenciones de casos culturales.</span><span class="sxs-lookup"><span data-stu-id="4e02a-122">All incoming strings will be converted to a single casing for comparison utilizing the LCID of the current thread to do this conversion to respect cultural case conventions.</span></span>

<span data-ttu-id="4e02a-123">La cadena pasada se trata como una frase.</span><span class="sxs-lookup"><span data-stu-id="4e02a-123">The string passed is treated as a phrase.</span></span> <span data-ttu-id="4e02a-124">Las palabras y los caracteres deben aparecer en los alteradores de los trazos en el orden especificado.</span><span class="sxs-lookup"><span data-stu-id="4e02a-124">Words and characters must appear in the alterantes for the strokes in the order specified.</span></span> <span data-ttu-id="4e02a-125">La primera y la última palabra de la frase pueden coincidir como subcadenas (la primera palabra que aparece al final de una alternativa y la última palabra aparece al mendigar de una), pero cualquier otra palabra (las que están dentro de la frase) debe aparecer como palabras enteras.</span><span class="sxs-lookup"><span data-stu-id="4e02a-125">The first and last words of the phrase may be matched as substrings (the first word appearing at the end of an alternate and the last word appearing at the begginging of one), but any other words (those inside of the phrase) must appear as whole words.</span></span>

<span data-ttu-id="4e02a-126">Si la cadena pasada no tiene ningún espacio en blanco entre caracteres, la subcadena se puede encontrar en cualquier lugar dentro de una sola palabra en una alternativa.</span><span class="sxs-lookup"><span data-stu-id="4e02a-126">If the string passed in has no whitespace in between characters, the substring may be found anywhere inside of a single word in an alternate.</span></span>

<span data-ttu-id="4e02a-127">Solo la presencia o ausencia de espacios en blanco entre caracteres cambia los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4e02a-127">Only the presence or absence of whitespace between characters changes the results of search.</span></span> <span data-ttu-id="4e02a-128">Se omite el espacio en blanco que no está rodeado por caracteres.</span><span class="sxs-lookup"><span data-stu-id="4e02a-128">Whitespace that is not surrounded by characters is ignored.</span></span> <span data-ttu-id="4e02a-129">El tipo de espacio en blanco se omite (una pestaña o un espacio entre caracteres dará el mismo resultado).</span><span class="sxs-lookup"><span data-stu-id="4e02a-129">The type of the whitespace is ignored (a tab or a space between characters will give the same result).</span></span> <span data-ttu-id="4e02a-130">La cantidad de espacios en blanco no importa: un espacio o dos espacios entre caracteres darán el mismo resultado.</span><span class="sxs-lookup"><span data-stu-id="4e02a-130">The amount of whitespace does not matter - one space or two spaces in between characters will give the same result.</span></span>

<span data-ttu-id="4e02a-131">La búsqueda no genera eventos PopulateContextNode.</span><span class="sxs-lookup"><span data-stu-id="4e02a-131">Search does not generate PopulateContextNode events.</span></span> <span data-ttu-id="4e02a-132">Solo se buscarán los trazos que ya se hayan rellenado.</span><span class="sxs-lookup"><span data-stu-id="4e02a-132">Only the strokes that have already been populated will be searched.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e02a-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e02a-133">Requirements</span></span>



| <span data-ttu-id="4e02a-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e02a-134">Requirement</span></span> | <span data-ttu-id="4e02a-135">Valor</span><span class="sxs-lookup"><span data-stu-id="4e02a-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e02a-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e02a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4e02a-137">Solo aplicaciones de escritorio de Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="4e02a-137">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4e02a-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4e02a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4e02a-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4e02a-139">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="4e02a-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e02a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e02a-141"><dt>IACom.h (también requiere IACom \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="4e02a-141"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="4e02a-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4e02a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e02a-143"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e02a-143"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="4e02a-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4e02a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e02a-145">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="4e02a-145">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




