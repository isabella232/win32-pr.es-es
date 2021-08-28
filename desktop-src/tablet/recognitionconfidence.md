---
description: Indica el nivel de confianza que tiene IInkAnalyzer en la precisión del resultado del reconocimiento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumeración RecognitionConfidence (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b5943b303c01a681b1df9d6d919df1822a5f2345c85fb5c52e3ab865ee58dd0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596635"
---
# <a name="recognitionconfidence-enumeration"></a>Enumeración RecognitionConfidence

Indica el nivel de confianza que tiene [**IInkAnalyzer**](iinkanalyzer.md) en la precisión del resultado del reconocimiento.

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ Strong**
</dt> <dd>

Confianza sólida en el resultado o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ Intermediate**
</dt> <dd>

Confianza intermedia en el resultado o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ Poor**
</dt> <dd>

Confianza deficiente en el resultado o alternativa.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ Unknown**
</dt> <dd>

El [**IInkAnalysisRecognizer que**](iinkanalysisrecognizer.md) generó el texto reconocido no admite niveles de confianza.

</dd> </dl>

## <a name="remarks"></a>Comentarios

[**IInkAnalyzer usa**](iinkanalyzer.md) uno o varios [**objetos IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para convertir la escritura a mano en texto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate::GetRecognitionConfidence (Método)**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Propiedades del nodo de contexto](context-node-properties.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




