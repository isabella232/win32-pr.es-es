---
description: Especifica el conjunto de advertencias disponibles que se pueden producir durante el análisis de tinta.
ms.assetid: 52676f1d-8d67-4bdb-9d4f-3e409ffa8332
title: Enumeración AnalysisWarningCode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisWarningCode
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 651408678daa64788952b2706980968ca315abf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667649"
---
# <a name="analysiswarningcode-enumeration"></a><span data-ttu-id="5e9c9-103">Enumeración AnalysisWarningCode</span><span class="sxs-lookup"><span data-stu-id="5e9c9-103">AnalysisWarningCode enumeration</span></span>

<span data-ttu-id="5e9c9-104">Especifica el conjunto de advertencias disponibles que se pueden producir durante el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-104">Specifies the set of available warnings that can occur during ink analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e9c9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e9c9-105">Syntax</span></span>


```C++
typedef enum AnalysisWarningCode { 
  AnalysisWarningCode_Aborted                                    = 0,
  AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound       = 1,
  AnalysisWarningCode_FactoidNotSupported                        = 2,
  AnalysisWarningCode_FactoidCoercionNotSupported                = 3,
  AnalysisWarningCode_GuideNotSupported                          = 4,
  AnalysisWarningCode_WordlistNotSupported                       = 5,
  AnalysisWarningCode_WordModeNotSupported                       = 6,
  AnalysisWarningCode_PartialDictionaryTermsNotSupported         = 7,
  AnalysisWarningCode_TextRecognitionProcessFailed               = 8,
  AnalysisWarningCode_AddInkToRecognizerFailed                   = 9,
  AnalysisWarningCode_SetPrefixSuffixFailed                      = 10,
  AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed  = 11,
  AnalysisWarningCode_ConfirmedWithoutInkRecognition             = 12,
  AnalysisWarningCode_BackgroundException                        = 13,
  AnalysisWarningCode_ContextNodeLocationNotSet                  = 14,
  AnalysisWarningCode_LanguageIdNotRespected                     = 15,
  AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported   = 16,
  AnalysisWarningCode_TopInkBreaksOnlyNotSupported               = 17,
  AnalysisWarningCode_AnalysisAlreadyRunning                     = 18
} AnalysisWarningCode;
```



## <a name="constants"></a><span data-ttu-id="5e9c9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="5e9c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5e9c9-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-107"><span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode\_Aborted**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-108">Se anuló la operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-108">The analysis operation was aborted.</span></span>

<span data-ttu-id="5e9c9-109">Solo se devuelve cuando se llama a la operación de análisis sincrónica.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-109">Returned only when the synchronous analysis operation is called.</span></span> <span data-ttu-id="5e9c9-110">La anulación de una operación asincrónica no generará un evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .</span><span class="sxs-lookup"><span data-stu-id="5e9c9-110">Aborting an asynchronous operation will not raise an [**\_IAnalysisEvents::Results**](-ianalysisevents-results.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-111"><span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-112">El [**IInkAnalyzer**](iinkanalyzer.md) no puede encontrar un reconocedor de tinta que cumpla los requisitos de idioma o de funcionalidad necesarios para realizar la operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-112">The [**IInkAnalyzer**](iinkanalyzer.md) cannot find an ink recognizer that meets language or capability requirements needed to perform the analysis operation.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-113"><span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-114">El reconocedor de tinta no pudo respetar el valor de Factoid especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-114">The ink recognizer was unable to respect the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-115"><span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode\_FactoidCoercionNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-116">El reconocedor de tinta no pudo forzar los resultados en el conjunto de Factoid especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-116">The ink recognizer was unable to coerce its results to the specified factoid set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-117"><span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode\_GuideNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-118">El reconocedor de tinta no pudo respetar el conjunto de la guía especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-118">The ink recognizer was unable to respect the specified guide set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-119"><span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode\_WordlistNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-120">El reconocedor de tinta no pudo respetar el conjunto de lista de palabras especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-120">The ink recognizer was unable to respect the specified word list set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-121"><span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode\_WordModeNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-122">El reconocedor de tinta no pudo respetar el modo de Word especificado establecido en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [propiedades de sugerencia de análisis](analysis-hint-properties.md)).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-122">The ink recognizer was unable to respect the specified word mode set on the analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-123"><span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode\_PartialDictionaryTermsNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-124">Indica que no se pudieron devolver términos de diccionario parciales desde [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-124">Indicates that partial dictionary terms could not be returned from the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-125"><span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode\_TextRecognitionProcessFailed**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-126">Indica que se ha producido un error en el proceso de reconocimiento de texto.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-126">Indicates the text recognition process failed.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-127"><span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode\_AddInkToRecognizerFailed**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-128">No se pudo agregar la entrada manuscrita a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-128">The ink could not be added to the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span> <span data-ttu-id="5e9c9-129">Por ejemplo, se producirá un error al agregar trazos recopilados desde un mouse en un reconocedor de gestos, ya que el reconocedor de gestos requiere trazos recopilados de un digitalizador.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-129">For example, adding strokes collected from a mouse on a gesture recognizer will fail, as the gesture recognizer requires strokes collected from a digitizer.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-130"><span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode\_SetPrefixSuffixFailed**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-131">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no pudo respetar el prefijo o el texto del sufijo especificado de un nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-131">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) was unable to respect the specified prefix or suffix text of an analysis hint node (see [**IContextNode::GetType**](icontextnode-gettype.md) and [Analysis Hint Properties](analysis-hint-properties.md)).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-132"><span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-133">[**IInkAnalyzer**](iinkanalyzer.md) no pudo crear una instancia, clonar o establecer trazos en [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-133">The [**IInkAnalyzer**](iinkanalyzer.md) was not able to instantiate, clone, or set strokes on the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-134"><span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode\_ConfirmedWithoutInkRecognition**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-135">Indica que el usuario ha confirmado un objeto [**IContextNode**](icontextnode.md) sin tener ningún valor de reconocimiento calculado para el nodo.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-135">Indicates that an [**IContextNode**](icontextnode.md) object has been confirmed by the user without having any recognition values computed for the node.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-136"><span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode\_BackgroundException**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-137">La operación en segundo plano no se completó debido a una excepción.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-137">The background operation did not complete due to an exception.</span></span> <span data-ttu-id="5e9c9-138">Se trata de un error irrecuperable y requiere que se vuelvan a crear instancias de [**IInkAnalyzer**](iinkanalyzer.md) antes de su uso.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-138">This is a fatal error and requires that the [**IInkAnalyzer**](iinkanalyzer.md) is re-instantiated before further use.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-139"><span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode\_ContextNodeLocationNotSet**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-140">Indica que un objeto [**IContextNode**](icontextnode.md) no tiene un conjunto de ubicación adecuado (vea [**IContextNode:: SetLocation**](icontextnode-setlocation.md)).</span><span class="sxs-lookup"><span data-stu-id="5e9c9-140">Indicates that an [**IContextNode**](icontextnode.md) object does not have a proper location set (see [**IContextNode::SetLocation**](icontextnode-setlocation.md)).</span></span> <span data-ttu-id="5e9c9-141">El método [**IContextNode:: GetLocation**](icontextnode-getlocation.md) debe devolver un valor que no esté vacío a menos que el objeto **IContextNode** se marque como parcialmente rellenado.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-141">The [**IContextNode::GetLocation**](icontextnode-getlocation.md) method must return a non-empty value unless the **IContextNode** object is marked as partially populated.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-142"><span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode\_LanguageIdNotRespected**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-143">El identificador de idioma establecido en un trazo asociado a un nodo de reconocedor personalizado (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) no coincidía con el identificador de idioma de la [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usada.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-143">The language identifier set on a stroke associated with a custom recognizer node (see [**IContextNode::GetType**](icontextnode-gettype.md)) did not match the language identifier of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) used.</span></span> <span data-ttu-id="5e9c9-144">Todavía se reconoció la tinta con el **IInkAnalysisRecognizer** especificado.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-144">The ink was still recognized with the specified **IInkAnalysisRecognizer**.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-145"><span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode\_EnableUnicodeCharacterRangesNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-146">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no admite la habilitación de intervalos de caracteres Unicode según lo especificado.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-146">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support enabling Unicode character ranges as specified.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-147"><span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode\_TopInkBreaksOnlyNotSupported**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-148">[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no admite TopInkBreaks solo aunque las sugerencias contenían la solicitud solo para TopInkBreaks.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-148">The [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) does not support TopInkBreaks only even though the hints contained the request for TopInkBreaks only.</span></span>

</dd> <dt>

<span data-ttu-id="5e9c9-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-149"><span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode\_AnalysisAlreadyRunning**</span></span>
</dt> <dd>

<span data-ttu-id="5e9c9-150">[**IInkAnalyzer**](iinkanalyzer.md) ya está realizando el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-150">The [**IInkAnalyzer**](iinkanalyzer.md) is already performing background analysis.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e9c9-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e9c9-151">Remarks</span></span>

<span data-ttu-id="5e9c9-152">**AnalysisWarningCode \_ BackgroundException** es el único valor de código de advertencia que requiere que se vuelva a crear una instancia del objeto [**IInkAnalyzer**](iinkanalyzer.md) antes de su uso.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-152">**AnalysisWarningCode\_BackgroundException** is the only warning code value that requires that the [**IInkAnalyzer**](iinkanalyzer.md) object is re-instantiated before further use.</span></span>

<span data-ttu-id="5e9c9-153">Otros valores de código de advertencias, como **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** y **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, pueden requerir que el objeto [**IInkAnalyzer**](iinkanalyzer.md) use otro reconocedor.</span><span class="sxs-lookup"><span data-stu-id="5e9c9-153">Other warnings code values, such as **AnalysisWarningCode\_InkAnalysisRecognizerInitializationFailed** and **AnalysisWarningCode\_NoMatchingInkAnalysisRecognizerFound**, might require that the [**IInkAnalyzer**](iinkanalyzer.md) object use a different recognizer.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e9c9-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e9c9-154">Requirements</span></span>



| <span data-ttu-id="5e9c9-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e9c9-155">Requirement</span></span> | <span data-ttu-id="5e9c9-156">Value</span><span class="sxs-lookup"><span data-stu-id="5e9c9-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e9c9-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9c9-157">Minimum supported client</span></span><br/> | <span data-ttu-id="5e9c9-158">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5e9c9-158">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5e9c9-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e9c9-159">Minimum supported server</span></span><br/> | <span data-ttu-id="5e9c9-160">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5e9c9-160">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5e9c9-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e9c9-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e9c9-162"><dt>IACom. h (también requiere IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5e9c9-162"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e9c9-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e9c9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e9c9-164">**IAnalysisWarning::GetWarningCode**</span><span class="sxs-lookup"><span data-stu-id="5e9c9-164">**IAnalysisWarning::GetWarningCode**</span></span>](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[<span data-ttu-id="5e9c9-165">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="5e9c9-165">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




