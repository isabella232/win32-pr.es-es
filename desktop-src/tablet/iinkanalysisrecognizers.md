---
description: Contiene una colección de objetos que implementan la interfaz IInkAnalysisRecognizer y que representan la capacidad de reconocer escritura a mano, objetos o gestos.
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: Interfaz IInkAnalysisRecognizers (IACom. h)
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
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360342"
---
# <a name="iinkanalysisrecognizers-interface"></a>Interfaz IInkAnalysisRecognizers

Contiene una colección de objetos que implementan la interfaz [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) y que representan la capacidad de reconocer escritura a mano, objetos o gestos.

## <a name="members"></a>Miembros

La interfaz **IInkAnalysisRecognizers** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IInkAnalysisRecognizers** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IInkAnalysisRecognizers** tiene estos métodos.



| Método                                                                               | Descripción                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | Recupera el número de objetos [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) de esta colección.<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | Recupera el [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) en el índice especificado.<br/>               |



 

## <a name="remarks"></a>Observaciones

El método [**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority Method**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) de [**IInkAnalyzer**](iinkanalyzer.md) devuelve una colección **IInkAnalysisRecognizers** que contiene los reconocedores de tinta disponibles en el Tablet PC actual.

Para un reconocedor de lenguaje, el método [**IInkAnalysisRecognizer:: GetLanguages**](iinkanalysisrecognizer-getlanguages.md) devuelve una matriz no vacía. Para los reconocedores de gestos y los reconocedores de objetos, el método **IInkAnalysisRecognizer:: GetLanguages** devuelve una matriz vacía.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: GetInkAnalysisRecognizersByPriority (método)**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

