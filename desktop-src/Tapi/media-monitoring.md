---
description: Cuando una llamada está en el estado connected, los datos se pueden transportar a través de la llamada. El tipo de medio de llamada proporciona una indicación del tipo de datos (por ejemplo, su tipo de datos o protocolo de nivel superior) de este flujo multimedia.
ms.assetid: 3281387e-3f72-4fda-8199-b3ce6e45e910
title: Supervisión de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb54989306fd80c48c0b99c9f8285a83b40bed25
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678638"
---
# <a name="media-monitoring"></a>Supervisión de medios

Cuando una llamada está en el estado *Connected* , los datos se pueden transportar a través de la llamada. El tipo de medio de llamada proporciona una indicación del tipo de datos (por ejemplo, su tipo de datos o protocolo de nivel superior) de este flujo multimedia.

TAPI permite que se proporcionen aplicaciones con una notificación sobre los cambios en el tipo de archivo multimedia de una llamada. La notificación proporciona una indicación del nuevo tipo de medio de la llamada. El proveedor de servicios decide cómo desea tomar esta decisión. Por ejemplo, el proveedor de servicios podría usar el procesamiento de señales de la secuencia de medios para determinar el tipo de medio o podría basarse en patrones de timbre distintivos asignados a diferentes transmisiones multimedia o en elementos de información pasados en un protocolo de señal fuera de banda. Independientemente de cómo se alcance la determinación del tipo de medio, la aplicación simplemente está informada sobre los cambios de tipo de medio en una llamada existente.

Para obtener más información y una lista de los modos o tipos de medios TAPI definidos actualmente, vea [ \_ constantes LINEMEDIAMODE](linemediamode--constants.md). Los proveedores de servicios pueden implementar tipos de medios específicos del proveedor para dispositivos muy especializados. Encontrará información en la documentación del dispositivo.

Los tipos de medios definidos por TAPI incluyen:

-   Desconocido. El tipo de medio de la llamada no se conoce actualmente; la llamada no está clasificada.
-   Voz interactiva. Se ha detectado energía de voz en la llamada y la llamada se trata como una llamada de voz interactiva con una persona en el extremo de la aplicación.
-   Voz automatizada. Se ha detectado energía de voz en la llamada, y se trata de una llamada de voz, pero sin ninguna persona en el extremo de la aplicación, como con una aplicación de equipo que responde.
-   Módem de datos. Una sesión de módem en la llamada. Los protocolos de módem actuales requieren que la estación llamada inicie el protocolo de enlace. En el caso de una llamada de módem de datos de entrada, la aplicación normalmente no puede hacer ninguna detección positiva. La forma en que el proveedor de servicios toma esta decisión es su elección. Por ejemplo, se puede usar un período de silencio justo después de responder a una llamada entrante como heurística para decidir que esto podría ser una llamada de módem de datos.
-   Fax G3. Una sesión de fax del grupo 3 en la llamada.
-   Fax G4. Una sesión de fax de grupo 4 en la llamada.
-   TDD. El flujo multimedia de la llamada usa los dispositivos de telefonía para el protocolo sordos.
-   Datos digitales. Flujo de datos digitales del formato no especificado.
-   Teletexto, Videotex, télex, mixto. Estos se corresponden con los servicios telemáticos del mismo nombre.
-   Editor ADSI. Una sesión de interfaz de servicios de pantalla analógica en la llamada. ADSI mejora las llamadas de voz con información alfanumérica descargada en el teléfono y el uso de botones flexibles en el teléfono.

Una aplicación puede habilitar o deshabilitar la supervisión de medios en una llamada especificada con [**lineMonitorMedia**](/windows/desktop/api/Tapi/nf-tapi-linemonitormedia). La aplicación especifica qué tipos de medios está interesado en la supervisión y, cuando se habilita la supervisión multimedia, la detección de un cambio de tipo de medio hace que la aplicación reciba una notificación con el mensaje [**line \_ MONITORMEDIA**](line-monitormedia.md) . Este mensaje proporciona el identificador de llamada en el que se detectó el cambio de tipo de medio, así como el nuevo tipo de medio.

Existe una diferencia entre el tipo de medio de una llamada notificado por [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) y los informes de eventos de tipo de medio por \_ mensajes MONITORMEDIA de línea. El tipo de medio de una llamada lo determinan exclusivamente las aplicaciones propietarias de la llamada y los eventos de supervisión de medios no cambian automáticamente. La única excepción es la determinación del tipo de medio inicial que puede realizar la biblioteca de vínculos dinámicos TAPI para seleccionar el primer propietario de una llamada. En este caso, se puede argumentar que la biblioteca es el propietario de la llamada.

La supervisión del tipo de medio predeterminado se realiza para los tipos de medios para los que se ha abierto el dispositivo de línea. Esto permite determinar el tipo de archivo multimedia de una llamada entrante antes de que la llamada se entregue a una aplicación en función de lo que la aplicación requiera. El ámbito de la supervisión multimedia de una llamada está limitado por la duración de la llamada. La supervisión multimedia en una llamada finaliza en cuanto la llamada se *desconecta* o se queda *inactiva*.

Una aplicación puede obtener los identificadores de dispositivo para varias clases de dispositivo asociadas a una línea abierta llamando a [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid). Esta función toma un identificador de línea, una dirección o un identificador de llamada y una descripción de clase de dispositivo. Devuelve el identificador de dispositivo para el dispositivo de la clase de dispositivo determinada que está asociada con el dispositivo, la dirección o la llamada de línea abierta. Si la clase de dispositivo es "TAPI/línea", se devuelve el identificador de dispositivo del dispositivo de línea. Si la clase de dispositivo es "MCI/Wave", se devuelve el identificador de dispositivo de un dispositivo MCI WaveAudio (si se admite), lo que permite actividades como la grabación o reproducción de audio sobre la llamada en la línea.

La aplicación puede usar el identificador de dispositivo devuelto con la API multimedia correspondiente para consultar las capacidades del dispositivo y, posteriormente, abrir el dispositivo multimedia. Por ejemplo, si la aplicación necesita usar la línea como un dispositivo de forma de onda, primero debe llamar a [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) y/o [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps) para determinar las capacidades de la forma de onda del dispositivo. El formato de datos de forma de onda típico que admite telefonía en Norteamérica es la ley de 8 bits m-Law en 8000 muestras por segundo, aunque el controlador de dispositivo de onda puede convertir esta velocidad de ejemplo y companding a otros formatos de audio multimedia más comunes.

Para abrir posteriormente un dispositivo de línea para la reproducción de audio mediante la API de onda, una aplicación llama a [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen). La implementación de **waveOutOpen** es específica del dispositivo y hay una variedad de opciones para implementar esta función.

 

 
