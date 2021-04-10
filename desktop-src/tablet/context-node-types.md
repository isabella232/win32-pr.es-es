---
description: Estas constantes definen valores que especifican el tipo de objetos IContextNode.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Tipos de nodo de contexto (Iaguid. h)
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
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153595"
---
# <a name="context-node-types"></a>Tipos de nodo de contexto

Estas constantes definen valores que especifican el tipo de objetos [**IContextNode**](icontextnode.md) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo que contiene información de contexto adicional para una región que utiliza el <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> para mejorar su análisis.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo que se usa para una única operación de reconocimiento.<br/> Todos los trazos y nodos que se encuentran dentro de un nodo de reconocedor personalizado se reconocen mediante una operación de reconocimiento independiente y no se analizan mediante el <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.<br/> Un nodo de reconocedor personalizado debe ser el elemento secundario directo del nodo raíz del analizador de tinta.<br/> Un nodo de reconocedor personalizado puede contener los siguientes tipos de elementos secundarios:<br/>
<ul>
<li>Cualquier número de nodos UnclassifiedInk.</li>
<li>Cualquier número de nodos de objeto.</li>
<li>Cualquier número de nodos de línea.</li>
<li>Cualquier número de nodos InkWord.</li>
<li>Cualquier número de nodos con un valor GUID desconocido.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(imagen)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para una región bidimensional en la que puede haber cualquier imagen que no sea de tinta en el documento.<br/> <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no crea nodos de imagen. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para agregar un nodo de imagen al árbol de nodos de contexto. A continuación, el <strong>IInkAnalyzer</strong> usa las regiones definidas por el nodo de la imagen para determinar si alguna tinta anota la imagen que no es de tinta.<br/> Un nodo de imagen no puede tener elementos secundarios.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </dl></td>
<td style="text-align: left;">InkBullet ContextNodeType representa una colección de trazos que forman una viñeta en una lista con viñetas.<br/> Un ContextNode de tipo InkBullet no puede tener elementos secundarios. Solo puede ser un elemento secundario de un párrafo ContextNode. Solo puede aparecer un InkBullet en un único párrafo ContextNode.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para una colección de trazos que constituye un dibujo.<br/> Los dibujos son trazos que se determinan como formas o bocetos abstractos. Por lo general, los trazos no se clasifican como trazos de escritura.<br/> Un nodo de dibujo de tinta no puede tener elementos secundarios.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(INKWORD)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para una colección de trazos que constituye una agrupación lógica para formar una palabra reconocible.<br/> Un nodo de palabra de tinta no puede contener elementos secundarios.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <dt><strong>GUID_CNT_LINE</strong></dt> <dt>(línea)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para una línea de palabras.<br/> Un nodo de línea puede contener los siguientes tipos de elementos secundarios:<br/>
<ul>
<li>Cualquier número de nodos de palabra de tinta.</li>
<li>Cualquier número de nodos de palabra de texto.</li>
<li>Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(objeto)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo de un objeto devuelto por un &quot; &quot; reconocedor personalizado de objeto.<br/> Un nodo de objeto no puede contener elementos secundarios.<br/> Solo los nodos de reconocedor personalizados pueden contener nodos de objeto.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(párrafo)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para una colección de nodos que constituye una agrupación lógica de líneas.<br/> Los motores de análisis determinan la definición exacta de un párrafo. En general, un párrafo contiene grupos de líneas que se retransmiten conjuntamente si se cambia el tamaño del cuadro que contiene las líneas.<br/> Un nodo de párrafo puede contener los siguientes tipos de elementos secundarios:<br/>
<ul>
<li>Cualquier número de nodos de viñeta de tinta.</li>
<li>Cualquier número de nodos de línea.</li>
<li>Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(raíz)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para el nodo superior de un árbol de nodos que describen los resultados del análisis de tinta.<br/> Los nodos raíz generalmente se obtienen del método <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer:: GetRootNode Method</strong></a> .<br/> Un nodo raíz puede contener los siguientes tipos de elementos secundarios:<br/>
<ul>
<li>Cualquier número de nodos de sugerencia de análisis.</li>
<li>Cualquier número de nodos de reconocedor personalizados.</li>
<li>Cualquier número de nodos de imagen.</li>
<li>Cualquier número de nodos de dibujo de tinta.</li>
<li>Cualquier número de nodos de la región de escritura.</li>
<li>Cualquier número de nodos de entrada de lápiz sin clasificar.</li>
<li>Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TEXTWORD)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para la región bidimensional en la que puede haber cualquier texto que no sea de tinta en el documento.<br/> El <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no crea nodos de texto de Word. Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para agregar un nodo de texto de Word al árbol de nodo de contexto. A continuación, el <strong>IInkAnalyzer</strong> usa las regiones definidas por el nodo Text Word para determinar si alguna tinta anota el texto que no es de tinta.<br/> Los reconocedores futuros pueden usar la región definida por un nodo de palabra de texto para determinar si alguna tinta anota la palabra que no es de tinta.<br/> Un nodo Text Word no puede tener elementos secundarios<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </dl></td>
<td style="text-align: left;">Representa un nodo para los trazos que todavía no se han clasificado o reconocido.<br/> Un nodo de tinta sin clasificar no puede tener elementos secundarios.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Observaciones

Para obtener más información sobre los distintos tipos de nodo de contexto, consulte [información general del análisis de tinta](ink-analysis-overview.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Iaguid. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::CreateSubNode**](icontextnode-createsubnode.md)
</dt> <dt>

[**IContextNode:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**IInkAnalyzer:: CreateAnalysisHint (método)**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer:: CreateCustomRecognizer (método)**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfType (método)**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Referencia de análisis de tinta](ink-analysis-reference.md)
</dt> </dl>

 

 




