---
description: Contiene una colección de objetos que implementan la interfaz IInkAnalysisRecognizer y que representan la capacidad de reconocer escritura a mano, objetos o gestos.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interfaz IInkAnalysisRecognizers (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ac39338e2701011165bd3da476b9e664332e3abb134bdbf4eca64106effb3840
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596765"
---
# <a name="iinkanalysisrecognizers-interface"></a>IInkAnalysisRecognizers (interfaz)

Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.

## <a name="members"></a>Miembros

La **interfaz IInkAnalysisRecognizers** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IInkAnalysisRecognizers** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IInkAnalysisRecognizers** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Recupera el número de [**objetos IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de esta colección.<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Recupera [**IInkAnalysisRecognizer en**](iinkanalysisrecognizer.md) el índice especificado.<br/>               |



 

## <a name="remarks"></a>Comentarios

El método [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority de**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) [**IInkAnalyzer**](iinkanalyzer.md) devuelve una colección **IInkAnalysisRecognizers** que contiene los reconocedores de lápiz disponibles en el tablet PC actual.

Para un reconocedor de lenguaje, el método [**IInkAnalysisRecognizer::GetLanguages**](iinkanalysisrecognizer-getlanguages.md) devuelve una matriz no vacía. Tanto para los reconocedores de gestos como para los reconocedores de objetos, el método **IInkAnalysisRecognizer::GetLanguages** devuelve una matriz vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (también requiere IACom \_ i.c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::GetInkAnalysisRecognizersByPriority (Método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

