---
description: Estas constantes definen valores que especifican el tipo de objetos IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipos de nodos de contexto (Iaguid.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 2bb2064cc72b398d290fa78606b31bd37208535e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256820"
---
# <a name="context-node-types"></a>Tipos de nodo de contexto

Estas constantes definen valores que especifican el tipo de [**objetos IContextNode.**](icontextnode.md)




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt><dt>(AnalysisHint)</dt></dl> | Representa un nodo que contiene información de contexto adicional para una región que <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> usa para mejorar su análisis.<br /> | 
| <span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt><dt>(CustomRecognizer)</dt></dl> | Representa un nodo utilizado para una única operación de reconocimiento.<br /> Todos los trazos y nodos que se encuentran dentro de un nodo de reconocedor personalizado se reconocen mediante una operación de reconocimiento independiente y no se analizan mediante <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.<br /> Un nodo de reconocedor personalizado debe ser el elemento secundario directo del nodo raíz del analizador de entrada de lápiz.<br /> Un nodo de reconocedor personalizado puede contener los siguientes tipos de elementos secundarios:<br /><ul><li>Cualquier número de nodos UnclassifiedInk.</li><li>Cualquier número de nodos de objeto.</li><li>Cualquier número de nodos de línea.</li><li>Cualquier número de nodos InkWord.</li><li>Cualquier número de nodos con un valor GUID desconocido.</li></ul> | 
| <span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl><dt><strong>GUID_CNT_IMAGE</strong></dt><dt>(imagen)</dt></dl> | Representa un nodo para una región bidimensional donde pueden existir imágenes que no son de entrada manuscrita en el documento.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no genera nodos de imagen. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode para</strong></a> agregar un nodo de imagen al árbol de nodos de contexto. A <strong>continuación, IInkAnalyzer</strong> usa las regiones definidas por el nodo de imagen para determinar si alguna entrada de lápiz anota la imagen que no es de entrada manuscrita.<br /> Un nodo de imagen no puede tener ningún elemento secundario.<br /> | 
| <span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl><dt><strong>GUID_CNT_INKBULLET</strong></dt><dt>(Ink Yaet)</dt></dl> | Ink Holoet ContextNodeType representa una colección de trazos que constituye una viñeta en una lista con viñetas.<br /> Un ContextNode de tipo InkNode no puede tener elementos secundarios. Solo puede ser un elemento secundario de un ContextNode de párrafo. Solo puede aparecer un Ink InkEt en un único contextNode de párrafo.<br /> | 
| <span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl><dt><strong>GUID_CNT_INKDRAWING</strong></dt><dt>(InkDrawing)</dt></dl> | Representa un nodo para una colección de trazos que constituye un dibujo.<br /> Los dibujos son trazos que se determinan como formas o bocetos abstractos. Por lo general, son trazos que no se clasifican como trazos de escritura.<br /> Un nodo de dibujo de entrada de lápiz no puede tener ningún elemento secundario.<br /> | 
| <span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl><dt><strong>GUID_CNT_INKWORD</strong></dt><dt>(InkWord)</dt></dl> | Representa un nodo para una colección de trazos que constituye una agrupación lógica para formar una palabra reconocible.<br /> Un nodo de palabra de entrada de lápiz no puede contener ningún elemento secundario.<br /> | 
| <span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl><dt><strong>GUID_CNT_LINE</strong></dt><dt>(línea)</dt></dl> | Representa un nodo para una línea de palabras.<br /> Un nodo de línea puede contener los siguientes tipos de elementos secundarios:<br /><ul><li>Cualquier número de nodos de palabras manuscrita.</li><li>Cualquier número de nodos de palabras de texto.</li><li>Cualquier número de nodos con un <strong>valor GUID</strong> desconocido.</li></ul> | 
| <span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl><dt><strong>GUID_CNT_OBJECT</strong></dt><dt>(objeto)</dt></dl> | Representa un nodo para un objeto que se devuelve desde un reconocedor personalizado de "objeto".<br /> Un nodo de objeto no puede contener ningún elemento secundario.<br /> Solo los nodos de reconocedor personalizados pueden contener nodos de objeto.<br /> | 
| <span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl><dt><strong>GUID_CNT_PARAGRAPH</strong></dt><dt>(párrafo)</dt></dl> | Representa un nodo para una colección de nodos que constituye una agrupación lógica de líneas.<br /> La definición exacta de un párrafo viene determinada por los motores de análisis. En general, un párrafo contiene grupos de líneas que se cambiarían de tamaño si se cambiase el tamaño del cuadro que contiene las líneas.<br /> Un nodo de párrafo puede contener los siguientes tipos de elementos secundarios:<br /><ul><li>Cualquier número de nodos de viñeta de lápiz.</li><li>Cualquier número de nodos de línea.</li><li>Cualquier número de nodos con un <strong>valor GUID</strong> desconocido.</li></ul> | 
| <span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl><dt><strong>GUID_CNT_ROOT</strong></dt><dt>(raíz)</dt></dl> | Representa un nodo para el nodo superior de un árbol de nodos que describen los resultados del análisis de entrada de lápiz.<br /> Por lo general, los nodos raíz se obtienen del <a href="iinkanalyzer-getrootnode.md"><strong>método IInkAnalyzer::GetRootNode.</strong></a><br /> Un nodo raíz puede contener los siguientes tipos de elementos secundarios:<br /><ul><li>Cualquier número de nodos de sugerencia de análisis.</li><li>Cualquier número de nodos de reconocedor personalizados.</li><li>Cualquier número de nodos de imagen.</li><li>Cualquier número de nodos de dibujo de lápiz.</li><li>Cualquier número de nodos de región de escritura.</li><li>Cualquier número de nodos de entrada de lápiz sin clasificar.</li><li>Cualquier número de nodos con un <strong>valor GUID</strong> desconocido.</li></ul> | 
| <span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl><dt><strong>GUID_CNT_TEXTWORD</strong></dt><dt>(TextWord)</dt></dl> | Representa un nodo para la región bidimensional donde puede existir cualquier texto que no sea de entrada manuscrita en el documento.<br /> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no genera nodos de palabras de texto. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode para</strong></a> agregar un nodo de palabra de texto al árbol de nodos de contexto. A <strong>continuación, IInkAnalyzer</strong> usa las regiones definidas por el nodo de palabra de texto para determinar si alguna entrada de lápiz anota el texto que no es de entrada manuscrita.<br /> Los reconocedores futuros pueden usar la región definida por un nodo de palabra de texto para determinar si alguna entrada de lápiz anota la palabra que no es de entrada manuscrita.<br /> Un nodo de palabra de texto no puede tener ningún elemento secundario<br /> | 
| <span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt><dt>(UnclassifiedInk)</dt></dl> | Representa un nodo para los trazos que aún no se han clasificado o reconocido.<br /> Un nodo de entrada de lápiz sin clasificar no puede tener ningún elemento secundario.<br /> | 




## <a name="remarks"></a>Observaciones

Para obtener más información sobre los distintos tipos de nodos de contexto, vea [Ink Analysis Overview](ink-analysis-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Iaguid.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode::GetType**](icontextnode-gettype.md)
</dt> <dt>

[**IInkAnalyzer::CreateAnalysisHint (Método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::CreateCustomRecognizer (Método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfType (Método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeForStrokes (Método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesOfTypeInSubTree (Método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Referencia de análisis de entrada de lápiz](ink-analysis-reference.md)
</dt> </dl>

 

 




