---
title: Tipos complejos de esquema eventManifest
description: A continuación se enumeran los tipos complejos que define el esquema EventManifest.
ms.assetid: 25facfdd-3846-4215-9b84-a833d86c39ef
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 69200d90253b27f9e73035a14ba5817917b24e1367d3bc4a54fff37e15d112ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590065"
---
# <a name="eventmanifest-schema-complex-types"></a>Tipos complejos de esquema eventManifest

A continuación se enumeran los tipos complejos que define el esquema EventManifest.



| Tipo complejo                                                                                       | Descripción                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BitMapType**](eventmanifestschema-bitmaptype-complextype.md)                                   | Define una lista de asignaciones de nombre y valor entre valores de bits y valores de cadena.<br/>                                                                                                                                                  |
| [**BitMapValueType**](eventmanifestschema-bitmapvaluetype-complextype.md)                         | Define la asignación entre un valor de bits y un valor de cadena.<br/>                                                                                                                                                                  |
| [**ChannelListType**](eventmanifestschema-channellisttype-complextype.md)                         | Define una lista de canales en los que los proveedores pueden registrar eventos.<br/>                                                                                                                                                                |
| [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)                   | Define las propiedades del archivo de registro que hace una copia de seguridad del canal, como su capacidad y si es secuencial o circular.<br/>                                                                                                |
| [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)             | Define las propiedades de registro de la sesión que usa el canal.<br/>                                                                                                                                                        |
| [**ChannelType**](eventmanifestschema-channeltype-complextype.md)                                 | Define un canal en el que los proveedores pueden registrar eventos.<br/>                                                                                                                                                                         |
| [**DataDefinitionType**](eventmanifestschema-datadefinitiontype-complextype.md)                   | Define un elemento de datos que desea incluir con el evento .<br/>                                                                                                                                                                 |
| [**DefinitionType**](eventmanifestschema-definitiontype-complextype.md)                           | Define una lista de eventos que el proveedor puede registrar.<br/>                                                                                                                                                                         |
| [**EventDefinitionType**](eventmanifestschema-eventdefinitiontype-complextype.md)                 | Define un evento que el proveedor puede escribir.<br/>                                                                                                                                                                               |
| [**EventsType**](eventmanifestschema-eventstype-complextype.md)                                   | Contiene una lista de proveedores que se definen en el manifiesto.<br/>                                                                                                                                                               |
| [**FilterType**](eventmanifestschema-filtertype-complextype.md)                                   | Define un filtro de datos que una sesión usa para filtrar eventos en función de los datos de eventos.<br/>                                                                                                                                              |
| [**FilterListType**](eventmanifestschema-filterlisttype-complextype.md)                           | Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.<br/>                                                                                                       |
| [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md)                     | Identifica un canal definido por otro proveedor o en un manifiesto que contiene una sección de metadatos.<br/>                                                                                                            |
| [**InputType**](eventmanifestschema-inputtype-complextype.md)                                     | Define un tipo de datos de entrada.<br/>                                                                                                                                                                                                  |
| [**InputTypeListType**](eventmanifestschema-inputtypelisttype-complextype.md)                     | Define una lista de tipos de entrada.<br/>                                                                                                                                                                                               |
| [**InstrumentationManifestType**](eventmanifestschema-instrumentationmanifesttype-complextype.md) | Define el tipo base para el [**elemento instrumentationManifest.**](eventmanifestschema-instrumentationmanifest-element.md)<br/>                                                                                                |
| [**InstrumentationType**](eventmanifestschema-instrumentationtype-complextype.md)                 | Define el contenido de la sección de instrumentación del manifiesto.<br/>                                                                                                                                                         |
| [**KeywordListType**](eventmanifestschema-keywordlisttype-complextype.md)                         | Define una lista de palabras clave que clasifican los eventos.<br/>                                                                                                                                                                           |
| [**KeywordType**](eventmanifestschema-keywordtype-complextype.md)                                 | Define una palabra clave que identifica una categoría de eventos.<br/>                                                                                                                                                                      |
| [**LevelListType**](eventmanifestschema-levellisttype-complextype.md)                             | Define una lista de niveles de gravedad que especifican el nivel de detalle de un evento.<br/>                                                                                                                                                    |
| [**LevelType**](eventmanifestschema-leveltype-complextype.md)                                     | Define un valor de gravedad que determina el nivel de detalle de los eventos que se registran.<br/>                                                                                                                                           |
| [**LocalizationType**](eventmanifestschema-localizationtype-complextype.md)                       | Define un grupo de recursos localizados a los que se hace referencia en el manifiesto.<br/>                                                                                                                                                  |
| [**MapType**](eventmanifestschema-maptype-complextype.md)                                         | Define una lista de pares nombre-valor.<br/>                                                                                                                                                                                          |
| [**MetadataType**](eventmanifestschema-metadatatype-complextype.md)                               | Define los tipos de metadatos que puede definir en la sección de metadatos del manifiesto.<br/>                                                                                                                                      |
| [**NamedQueryType**](eventmanifestschema-namedquerytype-complextype.md)                           | Define una lista de consultas con nombre que consultan la cadena del mensaje de evento para obtener un valor y realizan una acción especificada si se encuentran.<br/>                                                                                                     |
| [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md)                           | Define una lista de códigos de operación que se usan para identificar las operaciones de un componente de la aplicación.<br/>                                                                                                                        |
| [**OpcodeType**](eventmanifestschema-opcodetype-complextype.md)                                   | Define una operación dentro de un componente de la aplicación.<br/>                                                                                                                                                                  |
| [**OutputType**](eventmanifestschema-outputtype-complextype.md)                                   | Define un tipo de datos de salida que determina cómo se representan los datos.<br/>                                                                                                                                                        |
| [**PatternMapListType**](eventmanifestschema-patternmaplisttype-complextype.md)                   | Define una lista de pares de expresiones regulares que se usan para modificar la cadena del mensaje.<br/>                                                                                                                                        |
| [**PatternMapType**](eventmanifestschema-patternmaptype-complextype.md)                           | Define una asignación entre dos expresiones regulares. Una expresión se usa para buscar una cadena que coincida en la cadena del mensaje y la otra se usa para modificar la cadena antes de que el servicio la vuelva a coloca en la cadena del mensaje.<br/> |
| [**PatternMapValueType**](eventmanifestschema-patternmapvaluetype-complextype.md)                 | Define las expresiones regulares usadas para buscar una cadena que coincida en la cadena del mensaje y modificarla.<br/>                                                                                                                           |
| [**ProviderType**](eventmanifestschema-providertype-complextype.md)                               | Define un proveedor y los metadatos que usa para definir sus eventos.<br/>                                                                                                                                                       |
| [**StringTableType**](eventmanifestschema-stringtabletype-complextype.md)                         | Define una lista de cadenas localizadas a las que puede hacer referencia en el manifiesto.<br/>                                                                                                                                                 |
| [**StructDefinitionType**](eventmanifestschema-structdefinitiontype-complextype.md)               | Define una estructura que incluye uno o varios elementos de datos que desea incluir con el evento .<br/>                                                                                                                            |
| [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md)         | Define un evento específico de la tarea que el proveedor puede registrar.<br/>                                                                                                                                                                    |
| [**TaskListType**](eventmanifestschema-tasklisttype-complextype.md)                               | Define una lista de tareas que se usan para identificar los componentes de una aplicación.<br/>                                                                                                                                          |
| [**TaskType**](eventmanifestschema-tasktype-complextype.md)                                       | Define un componente o subcomponente de una aplicación.<br/>                                                                                                                                                                       |
| [**TemplateItemType**](eventmanifestschema-templateitemtype-complextype.md)                       | Plantilla que define los datos que se incluirán con un evento .<br/>                                                                                                                                                                   |
| [**TemplateListType**](eventmanifestschema-templatelisttype-complextype.md)                       | Define una lista de plantillas que especifican los datos que se incluirán con los eventos.<br/>                                                                                                                                                |
| [**TypeListType**](eventmanifestschema-typelisttype-complextype.md)                               | Define los tipos que se usan en el manifiesto.<br/>                                                                                                                                                                             |
| [**ValueMapType**](eventmanifestschema-valuemaptype-complextype.md)                               | Define una lista de asignaciones de nombre y valor entre valores enteros y valores de cadena.<br/>                                                                                                                                              |
| [**ValueMapValueType**](eventmanifestschema-valuemapvaluetype-complextype.md)                     | Define la asignación entre un valor entero y un valor de cadena.<br/>                                                                                                                                                             |
| [**XmlType**](eventmanifestschema-xmltype-complextype.md)                                         | Define un fragmento XML.<br/>                                                                                                                                                                                                     |
| [**XmlTypeListType**](eventmanifestschema-xmltypelisttype-complextype.md)                         | Define los tipos de salida de una lista que el servicio usa para determinar cómo representar un tipo de datos de entrada.<br/>                                                                                                                             |



 

 

 





