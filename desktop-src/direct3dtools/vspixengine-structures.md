---
description: Las siguientes estructuras se declaran en vspixengine. h.
MS-HAID: vspixengine.vspixengine\_structures
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Estructuras de interfaz de captura de diagnóstico de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 97F142F6-FED1-4AF4-B9E3-BB1E30F3FAD2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e1cefcf539996765b2e8055060277665f3cb9d31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537281"
---
# <a name="span-idvspixenginevspixengine_structuresspandirect3d-diagnostics-capture-interface-structures"></a><span id="vspixengine.vspixengine_structures"></span>Estructuras de interfaz de captura de diagnóstico de Direct3D

Las siguientes estructuras se declaran en vspixengine. h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Tema</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/resourcepair"><strong>ResourcePair</strong></a></p></td><td><p>Representa un recurso compartido que está codificado como una cadena COM.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptorheaprecord"><strong>DescriptorHeapRecord</strong></a></p></td><td><p>Representa la información del montón de descriptor.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestageerror"><strong>PipeLineStageError</strong></a></p></td><td><p>Representa un error en una fase de canalización.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pipelinestage"><strong>PipeLineStage</strong></a></p></td><td><p>Representa una fase de canalización, incluidos los detalles del sombreador utilizado.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/experimenttrigger"><strong>ExperimentTrigger</strong></a></p></td><td><p>Representa la información del desencadenador del experimento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/packedcallpkg"><strong>PackedCallPkg</strong></a></p></td><td><p>Representa un paquete de cuatro llamadas.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/symbolserverinfo"><strong>SymbolServerInfo</strong></a></p></td><td><p>Representa información sobre el servidor de símbolos de depuración.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/callstackframe"><strong>CallStackFrame</strong></a></p></td><td><p>Representa información sobre un marco en la pila de llamadas.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/sourcefileinfo"><strong>SourceFileInfo</strong></a></p></td><td><p>Representa información sobre un archivo de código fuente.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/summaryitem"><strong>SummaryItem</strong></a></p></td><td><p>Representa la información de resumen sobre un evento.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/debugshader"><strong>DebugShader</strong></a></p></td><td><p>Representa información sobre un sombreador en el depurador.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experiment"><strong>Experimento</strong></a></p></td><td><p>Representa información sobre un experimento (captura).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/issue"><strong>Problema</strong></a></p></td><td><p>Representa información sobre un problema.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/point2d"><strong>Point2D</strong></a></p></td><td><p>Representa un punto 2D con coordenadas de enteros sin signo.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/threaddata3d"><strong>ThreadData3D</strong></a></p></td><td><p>Representa un índice 3D en los datos del subproceso</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/inputlayoutstruct"><strong>InputLayoutStruct</strong></a></p></td><td><p>Representa los campos de diseño de entrada de un búfer de vértice, uno por campo en el búfer de vértices.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryoperation"><strong>PixelHistoryOperation</strong></a></p></td><td><p>Representa información sobre el historial de píxeles.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryintersection"><strong>PixelHistoryIntersection</strong></a></p></td><td><p>Representa información sobre un determinado</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/meshdatabufferlayoutentry"><strong>MeshDataBufferLayoutEntry</strong></a></p></td><td><p>Representa información sobre una única entrada en el diseño de búfer de una malla.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/debugshaderrequestinfo"><strong>DebugShaderRequestInfo</strong></a></p></td><td><p>Representa información sobre una solicitud del depurador de sombreador.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixengineint4"><strong>PixEngineInt4</strong></a></p></td><td><p>Representa un vector 4D con coordenadas de entero con signo.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginepoint4d"><strong>PixEnginePoint4D</strong></a></p></td><td><p>Representa un punto 4D con coordenadas de punto flotante (Double) de 64 bits.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginechanneldesc"><strong>PixEngineChannelDesc</strong></a></p></td><td><p>Representa una descripción de un canal de color (ejemplo).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureformatdesc"><strong>PixEngineTextureFormatDesc</strong></a></p></td><td><p>Representa una descripción de un formato de textura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturedescriptor"><strong>PixEngineTextureDescriptor</strong></a></p></td><td><p>Representa una descripción de un recurso de textura.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginetextureslicedescriptor"><strong>PixEngineTextureSliceDescriptor</strong></a></p></td><td><p>Representa una descripción de un segmento de textura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixenginetexturesliceindex"><strong>PixEngineTextureSliceIndex</strong></a></p></td><td><p>Representa el índice de un segmento de textura.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixenginehistogram"><strong>PixEngineHistogram</strong></a></p></td><td><p>Representa un histograma de una textura.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Referencia de la interfaz de captura de diagnóstico de Direct3D](vspixengine-reference.md)

 

 
