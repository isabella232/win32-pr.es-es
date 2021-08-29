---
description: Define identificadores únicos globales (GUID) para las propiedades de un IContextNode.
ms.assetid: 14992253-c384-43c1-9465-e015ea2348db
title: Propiedades del nodo de contexto (Iaguid.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNP_ALIGNMENTLEVEL
- GUID_CNP_ASCENDERS
- GUID_CNP_BASELINE
- GUID_CNP_CONFIDENCELEVEL
- GUID_CNP_CUSTOMRECOGNIZERID
- GUID_CNP_DESCENDERS
- GUID_CNP_MIDLINE
- GUID_CNP_NODEDATA
- GUID_CNP_RECOGNIZEDSTRING
- GUID_CNP_ROTATEDBOUNDINGBOX
- GUID_CNP_SEMANTICTYPE
- GUID_CNP_SHAPENAME
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: d8e151103c17a7f19a648b39ba4d6dfdae387886e52af287a80530b5c3cf1b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967734"
---
# <a name="context-node-properties"></a>Propiedades del nodo de contexto

Define identificadores únicos globales (GUID) para las propiedades de [**un IContextNode**](icontextnode.md).

En la tabla siguiente se describe la información a la que hace referencia cada constante.



| Constante                                                                                                                                                                                                 | Descripción                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GUID_CNP_ALIGNMENTLEVEL"></span><span id="guid_cnp_alignmentlevel"></span><dl> <dt>**GUID \_ CNP \_ ALIGNMENTLEVEL**</dt> </dl>             | Nivel de alineación de un párrafo.<br/>                                                                                                               |
| <span id="GUID_CNP_ASCENDERS"></span><span id="guid_cnp_ascenders"></span><dl> <dt>**ASCENDENTES \_ DE CNP \_ GUID**</dt> </dl>                            | Los ascendentes de una palabra de lápiz.<br/>                                                                                                                     |
| <span id="GUID_CNP_BASELINE"></span><span id="guid_cnp_baseline"></span><dl> <dt>**LÍNEA BASE \_ DE CNP \_ GUID**</dt> </dl>                               | Línea base de una palabra de lápiz.<br/>                                                                                                                      |
| <span id="GUID_CNP_CONFIDENCELEVEL"></span><span id="guid_cnp_confidencelevel"></span><dl> <dt>**GUID \_ CNP \_ CONFIDENCELEVEL**</dt> </dl>          | Nivel de confianza en los resultados del reconocimiento.<br/>                                                                                                  |
| <span id="GUID_CNP_CUSTOMRECOGNIZERID"></span><span id="guid_cnp_customrecognizerid"></span><dl> <dt>**GUID \_ CNP \_ CUSTOMRECOGNIZERID**</dt> </dl> | Identificador del reconocedor de lápiz personalizado para un nodo de reconocedor personalizado.<br/>                                                                         |
| <span id="GUID_CNP_DESCENDERS"></span><span id="guid_cnp_descenders"></span><dl> <dt>**DESCENDIENTES \_ DE CNP \_ GUID**</dt> </dl>                         | Descendientes de una palabra de lápiz.<br/>                                                                                                                    |
| <span id="GUID_CNP_MIDLINE"></span><span id="guid_cnp_midline"></span><dl> <dt>**GUID \_ CNP \_ MIDLINE**</dt> </dl>                                  | Línea media de una palabra de lápiz.<br/>                                                                                                                       |
| <span id="GUID_CNP_NODEDATA"></span><span id="guid_cnp_nodedata"></span><dl> <dt>**GUID \_ CNP \_ NODEDATA**</dt> </dl>                               | Datos de imagen o datos de texto de una imagen o una palabra de texto.<br/>                                                                                           |
| <span id="GUID_CNP_RECOGNIZEDSTRING"></span><span id="guid_cnp_recognizedstring"></span><dl> <dt>**GUID \_ CNP \_ RECOGNIZEDSTRING**</dt> </dl>       | Cadena reconocida.<br/>                                                                                                                            |
| <span id="GUID_CNP_ROTATEDBOUNDINGBOX"></span><span id="guid_cnp_rotatedboundingbox"></span><dl> <dt>**GUID \_ CNP \_ ROTATEDBOUNDINGBOX**</dt> </dl> | Cuadro de límite girado.<br/>                                                                                                                         |
| <span id="GUID_CNP_SEMANTICTYPE"></span><span id="guid_cnp_semantictype"></span><dl> <dt>**GUID \_ CNP \_ SEMANTICTYPE**</dt> </dl>                   | La propiedad contiene información sobre los tipos semánticos usados para definir una anotación, como si es una llamada, un comentario, y así sucesivamente.<br/> |
| <span id="GUID_CNP_SHAPENAME"></span><span id="guid_cnp_shapename"></span><dl> <dt>**GUID \_ CNP \_ SHAPENAME**</dt> </dl>                            | Nombre de forma de un nodo de dibujo de lápiz.<br/>                                                                                                            |



## <a name="remarks"></a>Comentarios

Estos GUID se usan para identificar las propiedades que [**IInkAnalyzer**](iinkanalyzer.md) puede establecer en [**un IContextNode**](icontextnode.md). El analizador de entrada de lápiz establece algunos datos de propiedad en función del tipo del nodo de contexto (vea [**IContextNode::GetType).**](icontextnode-gettype.md)

Para obtener o establecer propiedades específicas de los nodos de sugerencias de análisis, vea [**Propiedades de la sugerencia de análisis**](analysis-hint-properties.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Header<br/>                   | <dl> <dt>Iaguid.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de sugerencias de análisis](analysis-hint-properties.md)
</dt> <dt>

[Tipos de nodo de contexto](context-node-types.md)
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

 

 




