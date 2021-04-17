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
# <a name="analysiswarningcode-enumeration"></a>Enumeración AnalysisWarningCode

Especifica el conjunto de advertencias disponibles que se pueden producir durante el análisis de tinta.

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AnalysisWarningCode_Aborted"></span><span id="analysiswarningcode_aborted"></span><span id="ANALYSISWARNINGCODE_ABORTED"></span>**AnalysisWarningCode \_ anulado**
</dt> <dd>

Se anuló la operación de análisis.

Solo se devuelve cuando se llama a la operación de análisis sincrónica. La anulación de una operación asincrónica no generará un evento [**\_ IAnalysisEvents:: Results**](-ianalysisevents-results.md) .

</dd> <dt>

<span id="AnalysisWarningCode_NoMatchingInkAnalysisRecognizerFound"></span><span id="analysiswarningcode_nomatchinginkanalysisrecognizerfound"></span><span id="ANALYSISWARNINGCODE_NOMATCHINGINKANALYSISRECOGNIZERFOUND"></span>**AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**
</dt> <dd>

El [**IInkAnalyzer**](iinkanalyzer.md) no puede encontrar un reconocedor de tinta que cumpla los requisitos de idioma o de funcionalidad necesarios para realizar la operación de análisis.

</dd> <dt>

<span id="AnalysisWarningCode_FactoidNotSupported"></span><span id="analysiswarningcode_factoidnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidNotSupported**
</dt> <dd>

El reconocedor de tinta no pudo respetar el valor de Factoid especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).

</dd> <dt>

<span id="AnalysisWarningCode_FactoidCoercionNotSupported"></span><span id="analysiswarningcode_factoidcoercionnotsupported"></span><span id="ANALYSISWARNINGCODE_FACTOIDCOERCIONNOTSUPPORTED"></span>**AnalysisWarningCode \_ FactoidCoercionNotSupported**
</dt> <dd>

El reconocedor de tinta no pudo forzar los resultados en el conjunto de Factoid especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).

</dd> <dt>

<span id="AnalysisWarningCode_GuideNotSupported"></span><span id="analysiswarningcode_guidenotsupported"></span><span id="ANALYSISWARNINGCODE_GUIDENOTSUPPORTED"></span>**AnalysisWarningCode \_ GuideNotSupported**
</dt> <dd>

El reconocedor de tinta no pudo respetar el conjunto de la guía especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).

</dd> <dt>

<span id="AnalysisWarningCode_WordlistNotSupported"></span><span id="analysiswarningcode_wordlistnotsupported"></span><span id="ANALYSISWARNINGCODE_WORDLISTNOTSUPPORTED"></span>**AnalysisWarningCode \_ WordlistNotSupported**
</dt> <dd>

El reconocedor de tinta no pudo respetar el conjunto de lista de palabras especificado en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).

</dd> <dt>

<span id="AnalysisWarningCode_WordModeNotSupported"></span><span id="analysiswarningcode_wordmodenotsupported"></span><span id="ANALYSISWARNINGCODE_WORDMODENOTSUPPORTED"></span>**AnalysisWarningCode \_ WordModeNotSupported**
</dt> <dd>

El reconocedor de tinta no pudo respetar el modo de Word especificado establecido en el nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [propiedades de sugerencia de análisis](analysis-hint-properties.md)).

</dd> <dt>

<span id="AnalysisWarningCode_PartialDictionaryTermsNotSupported"></span><span id="analysiswarningcode_partialdictionarytermsnotsupported"></span><span id="ANALYSISWARNINGCODE_PARTIALDICTIONARYTERMSNOTSUPPORTED"></span>**AnalysisWarningCode \_ PartialDictionaryTermsNotSupported**
</dt> <dd>

Indica que no se pudieron devolver términos de diccionario parciales desde [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_TextRecognitionProcessFailed"></span><span id="analysiswarningcode_textrecognitionprocessfailed"></span><span id="ANALYSISWARNINGCODE_TEXTRECOGNITIONPROCESSFAILED"></span>**AnalysisWarningCode \_ TextRecognitionProcessFailed**
</dt> <dd>

Indica que se ha producido un error en el proceso de reconocimiento de texto.

</dd> <dt>

<span id="AnalysisWarningCode_AddInkToRecognizerFailed"></span><span id="analysiswarningcode_addinktorecognizerfailed"></span><span id="ANALYSISWARNINGCODE_ADDINKTORECOGNIZERFAILED"></span>**AnalysisWarningCode \_ AddInkToRecognizerFailed**
</dt> <dd>

No se pudo agregar la entrada manuscrita a [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md). Por ejemplo, se producirá un error al agregar trazos recopilados desde un mouse en un reconocedor de gestos, ya que el reconocedor de gestos requiere trazos recopilados de un digitalizador.

</dd> <dt>

<span id="AnalysisWarningCode_SetPrefixSuffixFailed"></span><span id="analysiswarningcode_setprefixsuffixfailed"></span><span id="ANALYSISWARNINGCODE_SETPREFIXSUFFIXFAILED"></span>**AnalysisWarningCode \_ SetPrefixSuffixFailed**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no pudo respetar el prefijo o el texto del sufijo especificado de un nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md) y [las propiedades](analysis-hint-properties.md)de la sugerencia de análisis).

</dd> <dt>

<span id="AnalysisWarningCode_InkAnalysisRecognizerInitializationFailed"></span><span id="analysiswarningcode_inkanalysisrecognizerinitializationfailed"></span><span id="ANALYSISWARNINGCODE_INKANALYSISRECOGNIZERINITIALIZATIONFAILED"></span>**AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) no pudo crear una instancia, clonar o establecer trazos en [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).

</dd> <dt>

<span id="AnalysisWarningCode_ConfirmedWithoutInkRecognition"></span><span id="analysiswarningcode_confirmedwithoutinkrecognition"></span><span id="ANALYSISWARNINGCODE_CONFIRMEDWITHOUTINKRECOGNITION"></span>**AnalysisWarningCode \_ ConfirmedWithoutInkRecognition**
</dt> <dd>

Indica que el usuario ha confirmado un objeto [**IContextNode**](icontextnode.md) sin tener ningún valor de reconocimiento calculado para el nodo.

</dd> <dt>

<span id="AnalysisWarningCode_BackgroundException"></span><span id="analysiswarningcode_backgroundexception"></span><span id="ANALYSISWARNINGCODE_BACKGROUNDEXCEPTION"></span>**AnalysisWarningCode \_ BackgroundException**
</dt> <dd>

La operación en segundo plano no se completó debido a una excepción. Se trata de un error irrecuperable y requiere que se vuelvan a crear instancias de [**IInkAnalyzer**](iinkanalyzer.md) antes de su uso.

</dd> <dt>

<span id="AnalysisWarningCode_ContextNodeLocationNotSet"></span><span id="analysiswarningcode_contextnodelocationnotset"></span><span id="ANALYSISWARNINGCODE_CONTEXTNODELOCATIONNOTSET"></span>**AnalysisWarningCode \_ ContextNodeLocationNotSet**
</dt> <dd>

Indica que un objeto [**IContextNode**](icontextnode.md) no tiene un conjunto de ubicación adecuado (vea [**IContextNode:: SetLocation**](icontextnode-setlocation.md)). El método [**IContextNode:: GetLocation**](icontextnode-getlocation.md) debe devolver un valor que no esté vacío a menos que el objeto **IContextNode** se marque como parcialmente rellenado.

</dd> <dt>

<span id="AnalysisWarningCode_LanguageIdNotRespected"></span><span id="analysiswarningcode_languageidnotrespected"></span><span id="ANALYSISWARNINGCODE_LANGUAGEIDNOTRESPECTED"></span>**AnalysisWarningCode \_ LanguageIdNotRespected**
</dt> <dd>

El identificador de idioma establecido en un trazo asociado a un nodo de reconocedor personalizado (vea [**IContextNode:: GetType**](icontextnode-gettype.md)) no coincidía con el identificador de idioma de la [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) usada. Todavía se reconoció la tinta con el **IInkAnalysisRecognizer** especificado.

</dd> <dt>

<span id="AnalysisWarningCode_EnableUnicodeCharacterRangesNotSupported"></span><span id="analysiswarningcode_enableunicodecharacterrangesnotsupported"></span><span id="ANALYSISWARNINGCODE_ENABLEUNICODECHARACTERRANGESNOTSUPPORTED"></span>**AnalysisWarningCode \_ EnableUnicodeCharacterRangesNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no admite la habilitación de intervalos de caracteres Unicode según lo especificado.

</dd> <dt>

<span id="AnalysisWarningCode_TopInkBreaksOnlyNotSupported"></span><span id="analysiswarningcode_topinkbreaksonlynotsupported"></span><span id="ANALYSISWARNINGCODE_TOPINKBREAKSONLYNOTSUPPORTED"></span>**AnalysisWarningCode \_ TopInkBreaksOnlyNotSupported**
</dt> <dd>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) no admite TopInkBreaks solo aunque las sugerencias contenían la solicitud solo para TopInkBreaks.

</dd> <dt>

<span id="AnalysisWarningCode_AnalysisAlreadyRunning"></span><span id="analysiswarningcode_analysisalreadyrunning"></span><span id="ANALYSISWARNINGCODE_ANALYSISALREADYRUNNING"></span>**AnalysisWarningCode \_ AnalysisAlreadyRunning**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md) ya está realizando el análisis en segundo plano.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**AnalysisWarningCode \_ BackgroundException** es el único valor de código de advertencia que requiere que se vuelva a crear una instancia del objeto [**IInkAnalyzer**](iinkanalyzer.md) antes de su uso.

Otros valores de código de advertencias, como **AnalysisWarningCode \_ InkAnalysisRecognizerInitializationFailed** y **AnalysisWarningCode \_ NoMatchingInkAnalysisRecognizerFound**, pueden requerir que el objeto [**IInkAnalyzer**](iinkanalyzer.md) use otro reconocedor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




