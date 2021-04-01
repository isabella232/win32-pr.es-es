---
description: Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos IContextNode.
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: Interfaz IAnalysisAlternate (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275489"
---
# <a name="ianalysisalternate-interface"></a>Interfaz IAnalysisAlternate

Representa las posibles coincidencias de palabras de reconocimiento de escritura a mano para objetos [**IContextNode**](icontextnode.md) .

## <a name="members"></a>Miembros

La interfaz **IAnalysisAlternate** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternate** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IAnalysisAlternate** tiene estos métodos.



| Método                                                                          | Descripción                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAlternateNodes**](ianalysisalternate-getalternatenodes.md)               | Recupera los objetos [**IContextNode**](icontextnode.md) asociados a esta alternativa.<br/>                                                       |
| [**GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md) | Recupera un valor que indica el nivel de confianza que [**IInkAnalyzer**](iinkanalyzer.md) tiene en la precisión de **IAnalysisAlternate**.<br/> |
| [**GetRecognizedString**](ianalysisalternate-getrecognizedstring.md)           | Recupera el valor de cadena reconocido del objeto **IAnalysisAlternate** .<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | Recupera los identificadores de trazo asociados a este **IAnalysisAlternate**.<br/>                                                                    |



 

## <a name="remarks"></a>Observaciones

Hay muchas variaciones en la escritura a mano de los usuarios. Por ese motivo, los reconocedores de escritura a mano a veces pueden convertir la escritura a mano en texto diferente del previsto por el usuario. Cuando un [**IInkAnalyzer**](iinkanalyzer.md) realiza un análisis en una colección de trazos, el **IInkAnalyzer** busca el conjunto de palabras más probable que representa la escritura a mano. Además, **IInkAnalyzer** también encuentra conjuntos de coincidencias de reconocimiento alternativas, que se almacenan en una colección [**IAnalysisAlternates**](ianalysisalternates.md) . Para que un usuario pueda aprovechar las alternativas de reconocimiento, debe crear una interfaz de usuario que permita al usuario seleccionar el **IAnalysisAlternate** correcto.

Los objetos **IAnalysisAlternate** se obtienen generalmente a través del [**método IInkAnalyzer:: GetAlternates**](iinkanalyzer-getalternates.md). El primer objeto **IAnalysisAlternate** de la colección es lo que el [**IInkAnalyzer**](iinkanalyzer.md) considera como la alternativa más probable.

Esta interfaz es equivalente a [System. Windows. Ink. AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) en el .NET Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                     |
| Encabezado<br/>                   | <dl> <dt>IACom. h (también requiere IACom \_ i. c)</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForContextNodes (método)**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternatesForStrokes (método)**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: GetAlternates (método)**](iinkanalyzer-getalternates.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

