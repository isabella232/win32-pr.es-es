---
title: Elementos de esquema de eventos
description: Estos son los elementos que define el esquema de eventos.
ms.assetid: 972c0a78-32d5-45b3-bcc3-6423b60bfa6f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 34149fae8ac273565f98c3f39adb31b61b406ade
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374383"
---
# <a name="event-schema-elements"></a>Elementos de esquema de eventos

Estos son los elementos que define el esquema de eventos. Esta sección contiene los nombres de los elementos que encontraría en un evento registrado; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.



| Elemento                                                                                                    | Descripción                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BinaryEventData (EventType)**](eventschema-binaryeventdata-eventtype-element.md)                       | Contiene los datos del evento como un blob binario.<br/>                                                                                                                                                   |
| [**Binary (EventDataType)**](eventschema-binary-eventdatatype-element.md)                                 | Blob de datos binarios para eventos que se escriben mediante [el registro de eventos](/windows/desktop/EventLog/event-logging).<br/>                                                                                                   |
| [**Channel (RenderingInfoType)**](eventschema-channel-renderinginfotype-element.md)                       | Cadena de mensaje representado del canal especificado en el evento.<br/>                                                                                                                          |
| [**Channel (SystemPropertiesType)**](eventschema-channel-systempropertiestype-element.md)                 | Canal en el que se registró el evento.<br/>                                                                                                                                                  |
| [**ComplexData (EventDataType)**](eventschema-complexdata-eventdatatype-element.md)                       | Estructura que se define en la plantilla para el evento.<br/>                                                                                                                                  |
| [**Componente (DebugDataType)**](eventschema-component-debugdatatype-element.md)                           | Nombre del componente que registró el mensaje de seguimiento.<br/>                                                                                                                                    |
| [**Equipo (SystemPropertiesType)**](eventschema-computer-systempropertiestype-element.md)               | nombre del equipo en el que se produjo el evento.<br/>                                                                                                                                       |
| [**Correlación (SystemPropertiesType)**](eventschema-correlation-systempropertiestype-element.md)         | Identificadores de actividad que los consumidores pueden usar para agrupar eventos relacionados.<br/>                                                                                                           |
| [**DataItemName (ProcessingErrorDataType)**](eventschema-dataitemname-processingerrordatatype-element.md) | Contiene el nombre del elemento de datos de evento que produjo un error cuando se procesaron los datos del evento.<br/>                                                                                            |
| [**Datos (ComplexDataType)**](eventschema-data-complexdatatype-element.md)                                 | Lista de elementos de datos de la estructura . La lista de elementos está en el mismo orden que se define en la plantilla.<br/>                                                                                |
| [**Datos (EventDataType)**](eventschema-data-eventdatatype-element.md)                                     | Elemento de datos de nivel superior que se define en la plantilla para el evento.<br/>                                                                                                                        |
| [**DebugData (EventType)**](eventschema-debugdata-eventtype-element.md)                                   | Contiene los datos que se pueden registrar para Windows de preprocesador de seguimiento de software (WPP).<br/>                                                                                                  |
| [**ErrorCode (ProcessingErrorDataType)**](eventschema-errorcode-processingerrordatatype-element.md)       | Contiene el código de error que se produjo cuando se produjo un error al procesar datos de eventos. <br/>                                                                                                     |
| [**Evento**](eventschema-event-element.md)                                                                 | Este es el nodo raíz de los datos de eventos representados.<br/>                                                                                                                                           |
| [**EventData (EventType)**](eventschema-eventdata-eventtype-element.md)                                   | Contiene los datos del evento.<br/>                                                                                                                                                                    |
| [**EventID (SystemPropertiesType)**](eventschema-eventid-systempropertiestype-element.md)                 | Identificador que el proveedor usó para identificar el evento.<br/>                                                                                                                                |
| [**EventPayload (ProcessingErrorDataType)**](eventschema-eventpayload-processingerrordatatype-element.md) | Contiene datos de eventos binarios para el evento que produjo un error cuando se procesaron los datos del evento. <br/>                                                                                           |
| [**EventRecordID (SystemPropertiesType)**](eventschema-eventrecordid-systempropertiestype-element.md)     | Número de registro asignado al evento cuando se registró.<br/>                                                                                                                                 |
| [**Ejecución (SystemPropertiesType)**](eventschema-execution-systempropertiestype-element.md)             | Contiene información sobre el proceso y el subproceso que registró el evento.<br/>                                                                                                                    |
| [**FileLine (DebugDataType)**](eventschema-fileline-debugdatatype-element.md)                             | Nombre del archivo de origen y la línea dentro del archivo de origen que registró el mensaje de seguimiento.<br/>                                                                                              |
| [**FlagName (DebugDataType)**](eventschema-flagname-debugdatatype-element.md)                             | Valor de marca pasado al proveedor cuando se ha habilitado.<br/>                                                                                                                                  |
| [**Función (DebugDataType)**](eventschema-function-debugdatatype-element.md)                             | Nombre de la función que registró el mensaje de seguimiento.<br/>                                                                                                                                     |
| [**Palabra clave (palabras clave)**](eventschema-keyword-keywords-element.md)                                         | Contiene una palabra clave representado.<br/>                                                                                                                                                                |
| [**Palabras clave (RenderingInfoType)**](eventschema-keywords-renderingtype-element.md)                         | Lista de palabras clave representados.<br/>                                                                                                                                                                |
| [**Palabras clave (SystemPropertiesType)**](eventschema-keywords-systempropertiestype-element.md)               | Máscara de bits de las palabras clave definidas en el evento .<br/>                                                                                                                                             |
| [**LevelName (DebugDataType)**](eventschema-levelname-debugdatatype-element.md)                           | Valor de nivel pasado al proveedor cuando se ha habilitado.<br/>                                                                                                                                 |
| [**Level (RenderingInfoType)**](eventschema-level-renderingtype-element.md)                               | Cadena de mensaje representado del nivel especificado en el evento.<br/>                                                                                                                            |
| [**Level (SystemPropertiesType)**](eventschema-level-systempropertiestype-element.md)                     | Contiene el nivel de gravedad del evento.<br/>                                                                                                                                                   |
| [**Message (DebugDataType)**](eventschema-message-debugdatatype-element.md)                               | Cadena del mensaje. El XML contiene este elemento si el evento WPP especificó el campo FormattedString.<br/>                                                                                     |
| [**Message (RenderingInfoType)**](eventschema-message-renderingtype-element.md)                           | Contiene el mensaje de evento que se representa para el evento.<br/>                                                                                                                                  |
| [**Opcode (RenderingInfoType)**](eventschema-opcode-renderingtype-element.md)                             | Cadena de mensaje representado del código de operación especificado en el evento.<br/>                                                                                                                           |
| [**Opcode (SystemPropertiesType)**](eventschema-opcode-systempropertiestype-element.md)                   | Código de operación definido en el evento.<br/>                                                                                                                                                            |
| [**ProcessingErrorData (EventType)**](eventschema-processingerrordata-eventtype-element.md)               | Contiene detalles del error que se produjo al intentar representar el evento.<br/>                                                                                                               |
| [**Provider (SystemPropertiesType)**](eventschema-provider-systempropertiestype-element.md)               | Identifica el proveedor que registró el evento.<br/>                                                                                                                                              |
| [**Provider (RenderingInfoType)**](eventschema-publisher-renderinginfotype-element.md)                    | Cadena de mensaje representado para el proveedor.<br/>                                                                                                                                               |
| [**RenderingInfo (EventType)**](eventschema-renderinginfo-eventtype-element.md)                           | Contiene las cadenas de mensaje representados para el evento (incluye la cadena de mensaje del evento y las cadenas de mensaje para cualquiera de las propiedades del evento, como level, task y opcode).<br/>        |
| [**Seguridad (SystemPropertiesType)**](eventschema-security-systempropertiestype-element.md)               | Identifica el usuario que registró el evento.<br/>                                                                                                                                                  |
| [**SequenceNumber (DebugDataType)**](eventschema-sequencenumber-debugdatatype-element.md)                 | Número de secuencia local o global del mensaje de seguimiento.<br/>                                                                                                                                   |
| [**SubComponent (DebugDataType)**](eventschema-subcomponent-debugdatatype-element.md)                     | Especifica el campo de seguimiento de depuración WPP SubComponentName que se usa en eventos de depuración en canales de depuración.                                                                                                 |
| [**System (EventType)**](eventschema-system-eventtype-element.md)                                         | Contiene información que identifica el proveedor y cómo se ha habilitado, el evento, el canal en el que se escribió el evento y la información del sistema, como los identidades de proceso y subproceso.<br/> |
| [**Tarea (RenderingInfoType)**](eventschema-task-renderingtype-element.md)                                 | Cadena de mensaje representado de la tarea especificada en el evento .<br/>                                                                                                                             |
| [**Tarea (SystemPropertiesType)**](eventschema-task-systempropertiestype-element.md)                       | Tarea definida en el evento .<br/>                                                                                                                                                              |
| [**TimeCreated (SystemPropertiesType)**](eventschema-timecreated-systempropertiestype-element.md)         | Marca de tiempo que identifica cuándo se registró el evento.<br/>                                                                                                                                   |
| [**UserData (EventType)**](eventschema-userdata-eventtype-element.md)                                     | Contiene los datos del evento.<br/>                                                                                                                                                                    |
| [**Version (SystemPropertiesType)**](schema-version-systempropertiestype-element.md)                      | Contiene el número de versión de la definición del evento.<br/>                                                                                                                                      |



 

 

