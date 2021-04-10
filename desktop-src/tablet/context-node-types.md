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
# <a name="context-node-types"></a><span data-ttu-id="90f1a-103">Tipos de nodo de contexto</span><span class="sxs-lookup"><span data-stu-id="90f1a-103">Context Node Types</span></span>

<span data-ttu-id="90f1a-104">Estas constantes definen valores que especifican el tipo de objetos [**IContextNode**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="90f1a-104">These constants define values that specify the type of [**IContextNode**](icontextnode.md) objects.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="90f1a-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="90f1a-105">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="90f1a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="90f1a-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <span data-ttu-id="90f1a-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(ANALYSISHINT)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-107"><dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(AnalysisHint)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-108">Representa un nodo que contiene información de contexto adicional para una región que utiliza el <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> para mejorar su análisis.</span><span class="sxs-lookup"><span data-stu-id="90f1a-108">Represents a node that contains additional context information for a region that the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> uses to improve its analysis.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <span data-ttu-id="90f1a-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CUSTOMRECOGNIZER)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-109"><dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(CustomRecognizer)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-110">Representa un nodo que se usa para una única operación de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="90f1a-110">Represents a node used for a single recognition operation.</span></span><br/> <span data-ttu-id="90f1a-111">Todos los trazos y nodos que se encuentran dentro de un nodo de reconocedor personalizado se reconocen mediante una operación de reconocimiento independiente y no se analizan mediante el <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="90f1a-111">All strokes and nodes that are within a custom recognizer node are recognized by an independent recognition operation and are not analyzed by the <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a>.</span></span><br/> <span data-ttu-id="90f1a-112">Un nodo de reconocedor personalizado debe ser el elemento secundario directo del nodo raíz del analizador de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-112">A custom recognizer node must be the direct child of ink analyzer's root node.</span></span><br/> <span data-ttu-id="90f1a-113">Un nodo de reconocedor personalizado puede contener los siguientes tipos de elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="90f1a-113">A custom recognizer node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="90f1a-114">Cualquier número de nodos UnclassifiedInk.</span><span class="sxs-lookup"><span data-stu-id="90f1a-114">Any number of UnclassifiedInk nodes.</span></span></li>
<li><span data-ttu-id="90f1a-115">Cualquier número de nodos de objeto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-115">Any number of Object nodes.</span></span></li>
<li><span data-ttu-id="90f1a-116">Cualquier número de nodos de línea.</span><span class="sxs-lookup"><span data-stu-id="90f1a-116">Any number of Line nodes.</span></span></li>
<li><span data-ttu-id="90f1a-117">Cualquier número de nodos InkWord.</span><span class="sxs-lookup"><span data-stu-id="90f1a-117">Any number of InkWord nodes.</span></span></li>
<li><span data-ttu-id="90f1a-118">Cualquier número de nodos con un valor GUID desconocido.</span><span class="sxs-lookup"><span data-stu-id="90f1a-118">Any number of nodes with an unknown Guid value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <span data-ttu-id="90f1a-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(imagen)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-119"><dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(Image)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-120">Representa un nodo para una región bidimensional en la que puede haber cualquier imagen que no sea de tinta en el documento.</span><span class="sxs-lookup"><span data-stu-id="90f1a-120">Represents a node for a two-dimensional region where any non-ink images can exist in the document.</span></span><br/> <span data-ttu-id="90f1a-121"><a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no crea nodos de imagen.</span><span class="sxs-lookup"><span data-stu-id="90f1a-121">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce image nodes.</span></span> <span data-ttu-id="90f1a-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para agregar un nodo de imagen al árbol de nodos de contexto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-122">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add an image node to the context node tree.</span></span> <span data-ttu-id="90f1a-123">A continuación, el <strong>IInkAnalyzer</strong> usa las regiones definidas por el nodo de la imagen para determinar si alguna tinta anota la imagen que no es de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-123">The <strong>IInkAnalyzer</strong> then uses the regions defined by the image node to determine if any ink annotates the non-ink image.</span></span><br/> <span data-ttu-id="90f1a-124">Un nodo de imagen no puede tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-124">An image node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <span data-ttu-id="90f1a-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(INKBULLET)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-125"><dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(InkBullet)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-126">InkBullet ContextNodeType representa una colección de trazos que forman una viñeta en una lista con viñetas.</span><span class="sxs-lookup"><span data-stu-id="90f1a-126">The InkBullet ContextNodeType represents a collection of strokes that make up a bullet in a bulleted list.</span></span><br/> <span data-ttu-id="90f1a-127">Un ContextNode de tipo InkBullet no puede tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-127">A ContextNode of type InkBullet cannot have any children.</span></span> <span data-ttu-id="90f1a-128">Solo puede ser un elemento secundario de un párrafo ContextNode.</span><span class="sxs-lookup"><span data-stu-id="90f1a-128">It can only be a child of a Paragraph ContextNode.</span></span> <span data-ttu-id="90f1a-129">Solo puede aparecer un InkBullet en un único párrafo ContextNode.</span><span class="sxs-lookup"><span data-stu-id="90f1a-129">Only one InkBullet can appear in a single Paragraph ContextNode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <span data-ttu-id="90f1a-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(INKDRAWING)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-130"><dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(InkDrawing)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-131">Representa un nodo para una colección de trazos que constituye un dibujo.</span><span class="sxs-lookup"><span data-stu-id="90f1a-131">Represents a node for a collection of strokes that constitutes a drawing.</span></span><br/> <span data-ttu-id="90f1a-132">Los dibujos son trazos que se determinan como formas o bocetos abstractos.</span><span class="sxs-lookup"><span data-stu-id="90f1a-132">Drawings are strokes that are determined to be shapes or abstract sketches.</span></span> <span data-ttu-id="90f1a-133">Por lo general, los trazos no se clasifican como trazos de escritura.</span><span class="sxs-lookup"><span data-stu-id="90f1a-133">They are generally any strokes that are not classified as writing strokes.</span></span><br/> <span data-ttu-id="90f1a-134">Un nodo de dibujo de tinta no puede tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-134">An ink drawing node cannot have any child elements.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <span data-ttu-id="90f1a-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(INKWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-135"><dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(InkWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-136">Representa un nodo para una colección de trazos que constituye una agrupación lógica para formar una palabra reconocible.</span><span class="sxs-lookup"><span data-stu-id="90f1a-136">Represents a node for a collection of strokes that constitutes a logical grouping to form a recognizable word.</span></span><br/> <span data-ttu-id="90f1a-137">Un nodo de palabra de tinta no puede contener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-137">An ink word node cannot contain any child elements.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <span data-ttu-id="90f1a-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(línea)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-138"><dt><strong>GUID_CNT_LINE</strong></dt> <dt>(Line)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-139">Representa un nodo para una línea de palabras.</span><span class="sxs-lookup"><span data-stu-id="90f1a-139">Represents a node for a line of words.</span></span><br/> <span data-ttu-id="90f1a-140">Un nodo de línea puede contener los siguientes tipos de elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="90f1a-140">A line node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="90f1a-141">Cualquier número de nodos de palabra de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-141">Any number of ink word nodes.</span></span></li>
<li><span data-ttu-id="90f1a-142">Cualquier número de nodos de palabra de texto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-142">Any number of text word nodes.</span></span></li>
<li><span data-ttu-id="90f1a-143">Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</span><span class="sxs-lookup"><span data-stu-id="90f1a-143">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <span data-ttu-id="90f1a-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(objeto)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-144"><dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(Object)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-145">Representa un nodo de un objeto devuelto por un &quot; &quot; reconocedor personalizado de objeto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-145">Represents a node for an object that is returned from an &quot;object&quot; custom recognizer.</span></span><br/> <span data-ttu-id="90f1a-146">Un nodo de objeto no puede contener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-146">An object node cannot contain any child elements.</span></span><br/> <span data-ttu-id="90f1a-147">Solo los nodos de reconocedor personalizados pueden contener nodos de objeto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-147">Only custom recognizer nodes can contain object nodes.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <span data-ttu-id="90f1a-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(párrafo)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-148"><dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(Paragraph)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-149">Representa un nodo para una colección de nodos que constituye una agrupación lógica de líneas.</span><span class="sxs-lookup"><span data-stu-id="90f1a-149">Represents a node for a collection of nodes that constitutes a logical grouping of lines.</span></span><br/> <span data-ttu-id="90f1a-150">Los motores de análisis determinan la definición exacta de un párrafo.</span><span class="sxs-lookup"><span data-stu-id="90f1a-150">The exact definition of a paragraph is determined by the analyzing engines.</span></span> <span data-ttu-id="90f1a-151">En general, un párrafo contiene grupos de líneas que se retransmiten conjuntamente si se cambia el tamaño del cuadro que contiene las líneas.</span><span class="sxs-lookup"><span data-stu-id="90f1a-151">In general, a paragraph contains groups of lines that would reflow together if the box that contains the lines were resized.</span></span><br/> <span data-ttu-id="90f1a-152">Un nodo de párrafo puede contener los siguientes tipos de elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="90f1a-152">A paragraph node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="90f1a-153">Cualquier número de nodos de viñeta de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-153">Any number of ink bullet nodes.</span></span></li>
<li><span data-ttu-id="90f1a-154">Cualquier número de nodos de línea.</span><span class="sxs-lookup"><span data-stu-id="90f1a-154">Any number of line nodes.</span></span></li>
<li><span data-ttu-id="90f1a-155">Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</span><span class="sxs-lookup"><span data-stu-id="90f1a-155">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <span data-ttu-id="90f1a-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(raíz)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-156"><dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(Root)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-157">Representa un nodo para el nodo superior de un árbol de nodos que describen los resultados del análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-157">Represents a node for the top node of a tree of nodes that describe the results of ink analysis.</span></span><br/> <span data-ttu-id="90f1a-158">Los nodos raíz generalmente se obtienen del método <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer:: GetRootNode Method</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="90f1a-158">Root nodes are generally obtained from the <a href="iinkanalyzer-getrootnode.md"><strong>IInkAnalyzer::GetRootNode Method</strong></a> method.</span></span><br/> <span data-ttu-id="90f1a-159">Un nodo raíz puede contener los siguientes tipos de elementos secundarios:</span><span class="sxs-lookup"><span data-stu-id="90f1a-159">A root node can contain the following types of child elements:</span></span><br/>
<ul>
<li><span data-ttu-id="90f1a-160">Cualquier número de nodos de sugerencia de análisis.</span><span class="sxs-lookup"><span data-stu-id="90f1a-160">Any number of analysis hint nodes.</span></span></li>
<li><span data-ttu-id="90f1a-161">Cualquier número de nodos de reconocedor personalizados.</span><span class="sxs-lookup"><span data-stu-id="90f1a-161">Any number of custom recognizer nodes.</span></span></li>
<li><span data-ttu-id="90f1a-162">Cualquier número de nodos de imagen.</span><span class="sxs-lookup"><span data-stu-id="90f1a-162">Any number of image nodes.</span></span></li>
<li><span data-ttu-id="90f1a-163">Cualquier número de nodos de dibujo de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-163">Any number of ink drawing nodes.</span></span></li>
<li><span data-ttu-id="90f1a-164">Cualquier número de nodos de la región de escritura.</span><span class="sxs-lookup"><span data-stu-id="90f1a-164">Any number of writing region nodes.</span></span></li>
<li><span data-ttu-id="90f1a-165">Cualquier número de nodos de entrada de lápiz sin clasificar.</span><span class="sxs-lookup"><span data-stu-id="90f1a-165">Any number of unclassified ink nodes.</span></span></li>
<li><span data-ttu-id="90f1a-166">Cualquier número de nodos con un valor <strong>GUID</strong> desconocido.</span><span class="sxs-lookup"><span data-stu-id="90f1a-166">Any number of nodes with an unknown <strong>GUID</strong> value.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <span data-ttu-id="90f1a-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TEXTWORD)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-167"><dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(TextWord)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-168">Representa un nodo para la región bidimensional en la que puede haber cualquier texto que no sea de tinta en el documento.</span><span class="sxs-lookup"><span data-stu-id="90f1a-168">Represents a node for the two-dimensional region where any non-ink text can exist in the document.</span></span><br/> <span data-ttu-id="90f1a-169">El <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> no crea nodos de texto de Word.</span><span class="sxs-lookup"><span data-stu-id="90f1a-169">The <a href="iinkanalyzer.md"><strong>IInkAnalyzer</strong></a> does not produce text word nodes.</span></span> <span data-ttu-id="90f1a-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode:: CreateSubNode</strong></a> para agregar un nodo de texto de Word al árbol de nodo de contexto.</span><span class="sxs-lookup"><span data-stu-id="90f1a-170">Use <a href="icontextnode-createsubnode.md"><strong>IContextNode::CreateSubNode</strong></a> to add a text word node to the context node tree.</span></span> <span data-ttu-id="90f1a-171">A continuación, el <strong>IInkAnalyzer</strong> usa las regiones definidas por el nodo Text Word para determinar si alguna tinta anota el texto que no es de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-171">The <strong>IInkAnalyzer</strong> then uses the regions defined by the text word node to determine if any ink annotates the non-ink text.</span></span><br/> <span data-ttu-id="90f1a-172">Los reconocedores futuros pueden usar la región definida por un nodo de palabra de texto para determinar si alguna tinta anota la palabra que no es de tinta.</span><span class="sxs-lookup"><span data-stu-id="90f1a-172">Future recognizers may use the region defined by a text word node to determine if any ink annotates the non-ink word.</span></span><br/> <span data-ttu-id="90f1a-173">Un nodo Text Word no puede tener elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90f1a-173">A text word node cannot have any child elements</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <span data-ttu-id="90f1a-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span><span class="sxs-lookup"><span data-stu-id="90f1a-174"><dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(UnclassifiedInk)</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="90f1a-175">Representa un nodo para los trazos que todavía no se han clasificado o reconocido.</span><span class="sxs-lookup"><span data-stu-id="90f1a-175">Represents a node for any strokes that have not yet been classified or recognized.</span></span><br/> <span data-ttu-id="90f1a-176">Un nodo de tinta sin clasificar no puede tener elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="90f1a-176">An unclassified ink node cannot have any child elements.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="90f1a-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="90f1a-177">Remarks</span></span>

<span data-ttu-id="90f1a-178">Para obtener más información sobre los distintos tipos de nodo de contexto, consulte [información general del análisis de tinta](ink-analysis-overview.md).</span><span class="sxs-lookup"><span data-stu-id="90f1a-178">For more information about the different context node types, see [Ink Analysis Overview](ink-analysis-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="90f1a-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90f1a-179">Requirements</span></span>



| <span data-ttu-id="90f1a-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="90f1a-180">Requirement</span></span> | <span data-ttu-id="90f1a-181">Value</span><span class="sxs-lookup"><span data-stu-id="90f1a-181">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="90f1a-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90f1a-182">Minimum supported client</span></span><br/> | <span data-ttu-id="90f1a-183">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="90f1a-183">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="90f1a-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="90f1a-184">Minimum supported server</span></span><br/> | <span data-ttu-id="90f1a-185">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="90f1a-185">None supported</span></span><br/>                                                           |
| <span data-ttu-id="90f1a-186">Encabezado</span><span class="sxs-lookup"><span data-stu-id="90f1a-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="90f1a-187"><dt>Iaguid. h</dt></span><span class="sxs-lookup"><span data-stu-id="90f1a-187"><dt>Iaguid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90f1a-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="90f1a-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90f1a-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="90f1a-189">**IContextNode::CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[<span data-ttu-id="90f1a-190">**IContextNode::CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="90f1a-190">**IContextNode::CreateSubNode**</span></span>](icontextnode-createsubnode.md)
</dt> <dt>

[<span data-ttu-id="90f1a-191">**IContextNode:: GetType**</span><span class="sxs-lookup"><span data-stu-id="90f1a-191">**IContextNode::GetType**</span></span>](icontextnode-gettype.md)
</dt> <dt>

[<span data-ttu-id="90f1a-192">**IInkAnalyzer:: CreateAnalysisHint (método)**</span><span class="sxs-lookup"><span data-stu-id="90f1a-192">**IInkAnalyzer::CreateAnalysisHint Method**</span></span>](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[<span data-ttu-id="90f1a-193">**IInkAnalyzer:: CreateCustomRecognizer (método)**</span><span class="sxs-lookup"><span data-stu-id="90f1a-193">**IInkAnalyzer::CreateCustomRecognizer Method**</span></span>](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[<span data-ttu-id="90f1a-194">**IInkAnalyzer:: FindNodesOfType (método)**</span><span class="sxs-lookup"><span data-stu-id="90f1a-194">**IInkAnalyzer::FindNodesOfType Method**</span></span>](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[<span data-ttu-id="90f1a-195">**IInkAnalyzer:: FindNodesOfTypeForStrokes (método)**</span><span class="sxs-lookup"><span data-stu-id="90f1a-195">**IInkAnalyzer::FindNodesOfTypeForStrokes Method**</span></span>](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[<span data-ttu-id="90f1a-196">**IInkAnalyzer:: FindNodesOfTypeInSubTree (método)**</span><span class="sxs-lookup"><span data-stu-id="90f1a-196">**IInkAnalyzer::FindNodesOfTypeInSubTree Method**</span></span>](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[<span data-ttu-id="90f1a-197">Referencia de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="90f1a-197">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

 




