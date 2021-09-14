---
description: Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea IContextNode::GetType).
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propiedades de sugerencias de análisis (Iaguid.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_AHP_ALLOWPARTIALDICTIONARYTERMS
- GUID_AHP_ANALYSISHINTNAME
- GUID_AHP_COERCETOFACTOID
- GUID_AHP_ENABLEDUNICODECHARACTERRANGES
- GUID_AHP_FACTOID
- GUID_AHP_GUIDE
- GUID_AHP_PREFIXTEXT
- GUID_AHP_SUFFIXTEXT
- GUID_AHP_TOPINKBREAKSONLY
- GUID_AHP_WORDLIST
- GUID_AHP_WORDMODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 8a7a25cfa94bb7f2354418ded2b35e3137364901
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247869"
---
# <a name="analysis-hint-properties"></a>Propiedades de la sugerencia de análisis

Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea [**IContextNode::GetType**](icontextnode-gettype.md)).

En la tabla siguiente se describe la información a la que hace referencia cada constante.



| Constante                                                                                                                                                                                                                                  | Descripción                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt> </dl>       | Si se permiten términos de diccionario parciales en una sugerencia de análisis.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt> </dl>                                        | Nombre de una sugerencia de análisis.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt> </dl>                                           | Si el analizador de entrada de lápiz limita su análisis de la entrada de lápiz dentro del área de la sugerencia para ajustarse al factoid.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt> </dl> | La sugerencia contiene una matriz de caracteres que representan el conjunto restringido de caracteres Unicode admitidos admitidos por este InkRecognizer.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID \_ AHP \_ FACTOID**</dt> </dl>                                                                   | El factoid en una sugerencia de análisis.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**GUID \_ AHP \_ GUIDE**</dt> </dl>                                                                         | Estructura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) que representa la guía de una sugerencia de análisis.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PREFIXTEXT**</dt> </dl>                                                          | Texto de prefijo de una sugerencia de análisis.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt> </dl>                                                          | Texto del sufijo en una sugerencia de análisis.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt> </dl>                                        | Si las segmentaciones múltiples en los resultados del reconocimiento de entrada de lápiz están deshabilitadas.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**LISTA \_ DE PALABRAS DE GUID AHP \_**</dt> </dl>                                                                | Matriz de cadenas que representa la lista de palabras para una sugerencia de análisis.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ AHP \_ WORDMODE**</dt> </dl>                                                                | Si el analizador de entrada de lápiz da prioridad a los resultados de una sola palabra en lugar de a los resultados de varias palabras para una sugerencia de análisis.<br/>                                      |



## <a name="remarks"></a>Observaciones

Estos GUID se usan para identificar las propiedades que [**IInkAnalyzer**](iinkanalyzer.md) puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode::GetType).**](icontextnode-gettype.md)

Para obtener o establecer las propiedades de [**un IContextNode**](icontextnode.md) en general, vea [Propiedades del nodo de contexto.](context-node-properties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Iaguid.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades del nodo de contexto](context-node-properties.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHintsByName (Método)**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




