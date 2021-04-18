---
description: Indica el nivel de confianza que IInkAnalyzer tiene en la precisión del resultado del reconocimiento.
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: Enumeración RecognitionConfidence (IACom. h)
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
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707297"
---
# <a name="recognitionconfidence-enumeration"></a>Enumeración RecognitionConfidence

Indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión del resultado del reconocimiento.

## <a name="syntax"></a>Sintaxis


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

Confianza fuerte en el resultado o alternativo.

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ intermedio**
</dt> <dd>

Confianza intermedia en el resultado o alternativo.

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ pobre**
</dt> <dd>

Mala confianza en el resultado o alternativo.

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ desconocido**
</dt> <dd>

El [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) que generó el texto reconocido no es compatible con los niveles de confianza.

</dd> </dl>

## <a name="remarks"></a>Observaciones

[**IInkAnalyzer**](iinkanalyzer.md) usa uno o varios objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) para convertir la escritura a mano en texto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternate:: GetRecognitionConfidence (método)**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Propiedades del nodo de contexto](context-node-properties.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




