---
description: Las enumeraciones siguientes se declaran en vspixengine.h.
MS-HAID: vspixengine.vspixengine\_enumerations
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeraciones de interfaz de captura de diagnósticos de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.assetid: A67402DE-8CBF-470A-97B4-3CF531731F24
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 94b5e656a1012f8b48cd4fbc34f34d94a145872d
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626171"
---
# <a name="span-idvspixenginevspixengine_enumerationsspandirect3d-diagnostics-capture-interface-enumerations"></a><span id="vspixengine.vspixengine_enumerations"></span>Enumeraciones de interfaz de captura de diagnósticos de Direct3D

Las enumeraciones siguientes se declaran en vspixengine.h.

## <a name="span-idin_this_sectionspanin-this-section"></a><span id="in_this_section"></span>En esta sección

<table><colgroup><col  /><col  /></colgroup><thead><tr class="header"><th>Tema</th><th>Descripción</th></tr></thead><tbody><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/xml-resource-ids"><strong>Xml_Resource_Ids</strong></a></p></td><td><p>Identificadores de cadena de recursos establecidos por el autor de la llamada que se devolverán en datos xml para visualizar objetos</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/resource-id"><strong>Resource_Id</strong></a></p></td><td><p>Define los identificadores de recursos para los recursos de cadena compartida. Se pasan al motor de captura desde el host. Se usan para mostrar cadenas en la superposición de HUD de la aplicación que se captura o para pasar valores del Registro Visual Studio opciones a la configuración de captura.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/hresult"><strong>Hresult</strong></a></p></td><td><p>Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/remotecommandtype"><strong>RemoteCommandType</strong></a></p></td><td><p>Enumeración que se usa para comunicarse entre el motor de captura y un host (por ejemplo, Visual Studio Diagnóstico de gráficos).</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/callbackcommandtype"><strong>CallbackCommandType</strong></a></p></td><td><p>Enumeración que se usa para comunicarse entre el motor de captura y un host (por ejemplo, Visual Studio Diagnóstico de gráficos).</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixpiperesponse"><strong>PixelPipeResponse</strong></a></p></td><td><p>Enumeración que se usa para enviar respuestas desde el motor de captura a Diagnóstico de gráficos.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/remotingversion"><strong>REMOTINGVERSION</strong></a></p></td><td><p>Enumeración que se usa para indicar qué versión del protocul de comunicación remota se usa.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/pixelkillreason"><strong>PIXELKILLREASON</strong></a></p></td><td><p>Enumeración usada para indicar por qué se rechazó un píxel.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pixelhistoryflags"><strong>PIXELHISTORYFLAGS</strong></a></p></td><td><p>Enumeración que contiene marcas usadas para describir un resultado del historial de píxeles. Consulte PixelHistoryOperation.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/eventcolumnid"><strong>EVENTCOLUMNID</strong></a></p></td><td><p>Enumeración que se usa para indicar los id. de columna conocidos; son los id. de columna que todas las implementaciones deben admitir.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/objectstatetype"><strong>OBJECTSTATETYPE</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/objecttablecolumnid"><strong>OBJECTTABLECOLUMNID</strong></a></p></td><td><p>Enumeración que se usa para indicar las propiedades de los datos devueltos desde una solicitud de tabla de objetos. Para obtener más información, vea IObjectTableRequest.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/pipelinestages"><strong>PIPELINESTAGES</strong></a></p></td><td><p>Enumeración que se usa para indicar una fase de la canalización de gráficos.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/checksumalgorithm"><strong>CHECKSUMALGORITHM</strong></a></p></td><td><p>Enumeración que se usa para indicar el algoritmo de suma de comprobación que se va a usar.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/eventtype"><strong>EVENTTYPE</strong></a></p></td><td><p>Enumeración que se usa para indicar el tipo de un evento.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-header-columns"><strong>DESCRIPTOR_HEAP_HEADER_COLUMNS</strong></a></p></td><td><p>Enumeración que se usa para indicar un encabezado coumn en el visor del montón descriptor</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/descriptor-heap-columns"><strong>DESCRIPTOR_HEAP_COLUMNS</strong></a></p></td><td><p>Enumeración que se usa para indicar una columna en el visor del montón descriptor.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttype"><strong>EXPERIMENTTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/dumpertype"><strong>DUMPERTYPE</strong></a></p></td><td><p>Enumeración que se usa para indicar qué tipo de búfer devuelve IGenericBufferDataRequest.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/experimenttriggertype"><strong>EXPERIMENTTRIGGERTYPE</strong></a></p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/register-format"><strong>REGISTER_FORMAT</strong></a></p></td><td><p>Interno</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/primitive-topology"><strong>PRIMITIVE_TOPOLOGY</strong></a></p></td><td><p>Enumeración que se usa para indicar la topología de una malla. Vea MeshDataVertCallback.</p></td></tr><tr class="odd"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysisstage"><strong>OFFLINEANALYSISSTAGE</strong></a></p></td><td><p>Enumeración que se usa para indicar las fases de progreso en el análisis de fotogramas.</p></td></tr><tr class="even"><td><p><a href="/windows/desktop/direct3dtools/offlineanalysissource"><strong>OFFLINEANALYSISSOURCE</strong></a></p></td><td><p>Enumeración que se usa para indicar el origen de la información de gráficos para el análisis de fotogramas.</p></td></tr></tbody></table>

 

## <a name="span-idrelated_topicsspanrelated-topics"></a><span id="related_topics"></span>Temas relacionados

[Referencia de la interfaz de captura de diagnósticos de Direct3D](vspixengine-reference.md)

 

 
