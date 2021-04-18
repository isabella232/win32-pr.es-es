---
description: Dirige el generador de código para generar un archivo y especifica el nombre del archivo de salida.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: elemento de archivo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc20f7d6853ccd52b231e19c99d60fe4b71d15b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715809"
---
# <a name="file-element"></a>elemento de archivo

Dirige el generador de código para generar un archivo y especifica el nombre del archivo de salida.

## <a name="usage"></a>Uso

``` syntax
<file
  name = "pathname string">
  child elements
</file>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                       | Obligatorio       | Descripción                                                                                                                         |
|---------------------|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **name**<br/> | cadena pathname<br/> | Sí<br/> | Nombre de archivo de salida para el contenido generado. La cadena de nombre de archivo debe incluir la información de ruta de acceso completa.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                 | Descripción                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CDATA**<br/>                                                                                    | Las secciones Text y CDATA se copian en el archivo sin modificación alguna. El código fuente que no es una función de los datos de entrada del contrato se puede Agregar a los archivos de salida mediante secciones de texto y CDATA.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Genera declaraciones de C para los valores de todos los tipos enumerados.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Genera declaraciones para las funciones que crean clases de origen de eventos.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Genera funciones que crean clases de origen de eventos.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Genera una declaración para una función que crea un host con tipo.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Genera una función que crea un host con tipo.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                       |
| [**inclui**](include.md)<br/>                                                                   | Incluye el contenido de una macro o un archivo en la salida generada.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Genera declaraciones para QueryInterface, AddRef y Release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Genera implementaciones para QueryInterface, AddRef y Release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Coloca una instrucción include de C o IDL en el código generado. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definiciones de estructura de C para los tipos de mensaje.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos de mensaje.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera constantes de C para las tablas de esquemas XML para los tipos de mensaje.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Genera declaraciones de C para las tablas de espacio de nombres.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Genera definiciones de C para las tablas de espacios de nombres.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera declaraciones de constantes de C para los tipos de puerto.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera constantes de C para los tipos de puerto.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Genera declaraciones de funciones para crear servidores proxy con tipo.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Genera funciones para crear servidores proxy con tipo.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Genera una declaración adelantada para los metadatos de hospedaje especificados en el elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Genera una definición de constante de C para los metadatos de hospedaje especificados en el elemento [**hostMetadata**](hostmetadata.md) . <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Genera declaraciones de estructura de C para los tipos conocidos.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Genera definiciones de estructura de C para los tipos conocidos.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera declaraciones de implementación para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera declaraciones IDL para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementaciones para las funciones de proxy de suscripción y cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Las secciones Text y CDATA se copian en el archivo sin modificación alguna. El código fuente que no es una función de los datos de entrada del contrato se puede Agregar a los archivos de salida mediante secciones de texto y CDATA.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Genera una declaración adelantada para la constante de C para los metadatos del fabricante especificados en el elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Genera una constante de C para los metadatos del fabricante especificados en el elemento [**thisModelMetadata**](thismodelmetadata.md) .<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Genera declaraciones de constantes de C para las tablas de esquemas XML para los tipos conocidos.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Genera constantes de C para las tablas de esquemas XML para los tipos conocidos.<br/> <br/>                                                                                                                                   |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  text, 
  CDATA, 
  namespaceDeclarations*, 
  namespaceDefinitions*, 
  structDeclarations*, 
  structDefinitions*, 
  typeTableDeclarations*, 
  typeTableDefinitions*, 
  thisModelMetadataDeclaration*, 
  thisModelMetadataDefinition*, 
  portTypeDeclarations*, 
  portTypeDefinitions*, 
  messageStructureDefinitions*, 
  messageTypeDeclarations*, 
  messageTypeDefinitions*, 
  idlFunctionDeclarations*, 
  subscriptionIdlFunctionDeclarations*, 
  functionDeclarations*, 
  subscriptionFunctionDeclarations*, 
  proxyFunctionImplementations*, 
  subscriptionProxyFunctionImplementations*, 
  stubDeclarations*, 
  stubDefinitions*, 
  enumerationValueDeclarations*, 
  include*, 
  IUnknownDeclarations*, 
  IUnknownDefinitions*, 
  relationshipMetadataDeclaration*, 
  relationshipMetadataDefinition*, 
  proxyBuilderDeclarations*, 
  proxyBuilderImplementations*, 
  hostBuilderDeclaration*, 
  hostBuilderImplementation*, 
  eventSourceBuilderDeclarations*, 
  eventSourceBuilderImplementations*, 
  literalInclude*
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

El nombre del archivo viene determinado por el valor del atributo name o del elemento secundario. El contenido del archivo lo determinan los demás elementos secundarios, Text y CDATA en el elemento **File** . Text y CDATA se copian en el archivo sin modificar. Los elementos secundarios se reemplazan por código generado. Los elementos de texto, CDATA y secundarios pueden aparecer en cualquier orden y pueden repetirse indefinidamente.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




