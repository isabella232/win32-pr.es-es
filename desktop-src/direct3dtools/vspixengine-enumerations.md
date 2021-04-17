---
description: Las enumeraciones siguientes se declaran en vspixengine. h.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeraciones de la interfaz de captura de diagnóstico de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 059f91aa806afd60d5efe755d015495eb2f445f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686419"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Enumeraciones de la interfaz de captura de diagnóstico de Direct3D

Las enumeraciones siguientes se declaran en vspixengine. h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Tema</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>Identificadores de cadena de recursos establecidos por el llamador para que se devuelvan en datos XML para visualizar objetos</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Define los identificadores de recursos para los recursos de cadena compartidos. Estos se pasan al motor de captura desde el host. Se usan para mostrar cadenas en la superposición de HUD de la aplicación que se captura o para pasar valores de registro de las opciones de Visual Studio al engi de captura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Valor</strong></a></p></td><td><p>Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>Enumeración que se usa para la comunicación entre el motor de captura y un host (como Visual Studio Diagnóstico de gráficos).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixPipeResponse</strong></a></p></td><td><p>Enumeración que se usa para enviar las respuestas del motor de captura a Diagnóstico de gráficos.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>Enumeración que se usa para indicar qué versión del protocul remoto se está usando.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>Enumeración que se usa para indicar por qué se rechazó un píxel.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>Una enumeración que contiene marcas que se usan para describir un resultado del historial de píxeles. Vea PixelHistoryOperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>Enumeración que se usa para indicar los identificadores de columna conocidos; Estos son los identificadores de columna que deben admitir todas las implementaciones.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>OBJECTSTATETYPE</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>Enumeración que se usa para indicar las propiedades de los datos devueltos por una solicitud de tabla de objetos. Para obtener más información, vea IObjectTableRequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>FASES</strong></a></p></td><td><p>Enumeración que se usa para indicar una fase de la canalización de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>Enumeración que se usa para indicar el algoritmo de suma de comprobación que se va a utilizar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EVENTTYPE</strong></a></p></td><td><p>Enumeración que se usa para indicar el tipo de un evento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Una enumeración que se usa para indicar un encabezado coumn en el visor del montón descriptor.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Enumeración que se usa para indicar una columna en el visor del montón descriptor.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>Enumeración que se usa para indicar qué tipo de búfer IGenericBufferDataRequest devuelve.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Enumeración que se usa para indicar la topología de una malla. Vea MeshDataVertCallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>Una enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>Enumeración que se usa para indicar el origen de la información de gráficos para el análisis de fotogramas.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Referencia de la interfaz de captura de diagnóstico de Direct3D](vspixengine-reference.md)

 

 
