---
description: 'Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea IContextNode:: GetType).'
ms.assetid: 8300c792-a741-49de-a03b-f4840ea5d647
title: Propiedades de la sugerencia de análisis (Iaguid. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000852"
---
# <a name="analysis-hint-properties"></a>Propiedades de la sugerencia de análisis

Define identificadores únicos globales (GUID) para las propiedades de un nodo de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).

En la tabla siguiente se describe la información a la que hace referencia cada constante.



| Constante                                                                                                                                                                                                                                  | Descripción                                                                                                                                               |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_AHP_ALLOWPARTIALDICTIONARYTERMS"></span><span id="guid_ahp_allowpartialdictionaryterms"></span><dl> <dt>**GUID \_ AHP \_ ALLOWPARTIALDICTIONARYTERMS**</dt> </dl>       | Indica si se permiten términos de diccionario parciales en una sugerencia de análisis.<br/>                                                                              |
| <span id="GUID_AHP_ANALYSISHINTNAME"></span><span id="guid_ahp_analysishintname"></span><dl> <dt>**GUID \_ AHP \_ ANALYSISHINTNAME**</dt> </dl>                                        | Nombre de una sugerencia de análisis.<br/>                                                                                                                  |
| <span id="GUID_AHP_COERCETOFACTOID"></span><span id="guid_ahp_coercetofactoid"></span><dl> <dt>**GUID \_ AHP \_ COERCETOFACTOID**</dt> </dl>                                           | Si el analizador de tintas limita su análisis de tinta dentro del área de la sugerencia para ajustarse al Factoid.<br/>                                          |
| <span id="GUID_AHP_ENABLEDUNICODECHARACTERRANGES"></span><span id="guid_ahp_enabledunicodecharacterranges"></span><dl> <dt>**GUID \_ AHP \_ ENABLEDUNICODECHARACTERRANGES**</dt> </dl> | La sugerencia contiene una matriz de caracteres que representa el conjunto restringido de juegos de caracteres Unicode admitidos que admite este InkRecognizer.<br/> |
| <span id="GUID_AHP_FACTOID"></span><span id="guid_ahp_factoid"></span><dl> <dt>**GUID \_ AHP \_ FACTOID**</dt> </dl>                                                                   | Factoid en una sugerencia de análisis.<br/>                                                                                                               |
| <span id="GUID_AHP_GUIDE"></span><span id="guid_ahp_guide"></span><dl> <dt>**\_Guía de AHP de GUID \_**</dt> </dl>                                                                         | La estructura [**InkAnalysisRecognizerGuide**](inkanalysisrecognizerguide.md) que representa la guía de una sugerencia de análisis.<br/>                 |
| <span id="GUID_AHP_PREFIXTEXT"></span><span id="guid_ahp_prefixtext"></span><dl> <dt>**GUID \_ AHP \_ PREFIXTEXT**</dt> </dl>                                                          | Texto del prefijo en una sugerencia de análisis.<br/>                                                                                                           |
| <span id="GUID_AHP_SUFFIXTEXT"></span><span id="guid_ahp_suffixtext"></span><dl> <dt>**GUID \_ AHP \_ SUFFIXTEXT**</dt> </dl>                                                          | Texto del sufijo en una sugerencia de análisis.<br/>                                                                                                           |
| <span id="GUID_AHP_TOPINKBREAKSONLY"></span><span id="guid_ahp_topinkbreaksonly"></span><dl> <dt>**GUID \_ AHP \_ TOPINKBREAKSONLY**</dt> </dl>                                        | Si se deshabilitan los diversos segmentos de los resultados del reconocimiento de tinta.<br/>                                                                |
| <span id="GUID_AHP_WORDLIST"></span><span id="guid_ahp_wordlist"></span><dl> <dt>**\_AHP de \_ palabras de GUID**</dt> </dl>                                                                | Matriz de cadenas que representa la lista de palabras de una sugerencia de análisis.<br/>                                                                       |
| <span id="GUID_AHP_WORDMODE"></span><span id="guid_ahp_wordmode"></span><dl> <dt>**GUID \_ AHP \_ WORDMODE**</dt> </dl>                                                                | Si el analizador de tinta tiene prioridad sobre los resultados de una sola palabra en los resultados de varias palabras para una sugerencia de análisis.<br/>                                      |



## <a name="remarks"></a>Observaciones

Estos GUID se usan para identificar las propiedades que [**IInkAnalyzer**](iinkanalyzer.md) puede establecer en un nodo de contexto de sugerencia de análisis (vea [**IContextNode:: GetType**](icontextnode-gettype.md)).

Para obtener o establecer las propiedades de un [**IContextNode**](icontextnode.md) en general, consulte [propiedades del nodo de contexto](context-node-properties.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades del nodo de contexto](context-node-properties.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer:: GetAnalysisHintsByName (método)**](iinkanalyzer-getanalysishintsbyname.md)
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

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




