---
description: Indica al generador de código que genere un archivo y especifica el nombre del archivo de salida.
ms.assetid: d2ee6886-995f-453d-8121-f849b2d910ec
title: elemento de archivo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afd3fbd3f52bb2fba10f77f0589016267703811808d5eb51b90cf2a59f1425bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117920769"
---
# <a name="file-element"></a>elemento de archivo

Indica al generador de código que genere un archivo y especifica el nombre del archivo de salida.

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
| **name**<br/> | cadena pathname<br/> | Sí<br/> | Nombre de archivo de salida del contenido generado. La cadena de nombre de archivo debe incluir información de ruta de acceso completa.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                                                                 | Descripción                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Cdata**<br/>                                                                                    | Las secciones text y CDATA se copian en el archivo sin modificaciones. El código fuente que no es una función de los datos de entrada del contrato se puede agregar a los archivos de salida mediante las secciones text y CDATA.<br/> <br/> |
| [**enumerationValueDeclarations**](enumerationvaluedeclarations.md)<br/>                         | Genera declaraciones de C para los valores de todos los tipos enumerados.<br/> <br/>                                                                                                                                   |
| [**eventSourceBuilderDeclarations**](eventsourcebuilderdeclarations.md)<br/>                     | Genera declaraciones para las funciones que crean clases de origen de eventos.<br/> <br/>                                                                                                                         |
| [**eventSourceBuilderImplementations**](eventsourcebuilderimplementations.md)<br/>               | Genera funciones que crean clases de origen de eventos.<br/> <br/>                                                                                                                                          |
| [**functionDeclarations**](functiondeclarations.md)<br/>                                         | Genera declaraciones de implementación para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                            |
| [**hostBuilderDeclaration**](hostbuilderdeclaration.md)<br/>                                     | Genera una declaración para una función que crea un host con tipo.<br/> <br/>                                                                                                                              |
| [**hostBuilderImplementation**](hostbuilderimplementation.md)<br/>                               | Genera una función que crea un host con tipo.<br/> <br/>                                                                                                                                                |
| [**idlFunctionDeclarations**](idlfunctiondeclarations.md)<br/>                                   | Genera declaraciones IDL para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                       |
| [**incluír**](include.md)<br/>                                                                   | Incluye el contenido de una macro o un archivo en la salida generada.<br/> <br/>                                                                                                                              |
| [**IUnknownDeclarations**](iunknowndeclarations.md)<br/>                                         | Genera declaraciones para QueryInterface, AddRef y Release.<br/> <br/>                                                                                                                                 |
| [**IUnknownDefinitions**](iunknowndefinitions.md)<br/>                                           | Genera implementaciones para QueryInterface, AddRef y Release.<br/> <br/>                                                                                                                              |
| [**literalInclude**](literalinclude.md)<br/>                                                     | Coloca una instrucción include de C o IDL en el código generado. <br/> <br/>                                                                                                                                    |
| [**messageStructureDefinitions**](messagestructuredefinitions.md)<br/>                           | Genera definiciones de estructura de C para tipos de mensaje.<br/> <br/>                                                                                                                                           |
| [**messageTypeDeclarations**](messagetypedeclarations.md)<br/>                                   | Genera declaraciones constantes de C para tablas de esquema XML para tipos de mensaje.<br/> <br/>                                                                                                                     |
| [**messageTypeDefinitions**](messagetypedefinitions.md)<br/>                                     | Genera constantes de C para tablas de esquema XML para tipos de mensaje.<br/> <br/>                                                                                                                                 |
| [**namespaceDeclarations**](namespacedeclarations.md)<br/>                                       | Genera declaraciones de C para tablas de espacio de nombres.<br/> <br/>                                                                                                                                                 |
| [**namespaceDefinitions**](namespacedefinitions.md)<br/>                                         | Genera definiciones de C para tablas de espacio de nombres.<br/> <br/>                                                                                                                                                  |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/>                                         | Genera declaraciones constantes de C para tipos de puerto.<br/> <br/>                                                                                                                                              |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>                                           | Genera constantes de C para los tipos de puerto.<br/> <br/>                                                                                                                                                          |
| [**proxyBuilderDeclarations**](proxybuilderdeclarations.md)<br/>                                 | Genera declaraciones para que las funciones creen servidores proxy con tipo.<br/> <br/>                                                                                                                                  |
| [**proxyBuilderImplementations**](proxybuilderimplementations.md)<br/>                           | Genera funciones para crear servidores proxy con tipo.<br/> <br/>                                                                                                                                                   |
| [**proxyFunctionImplementations**](proxyfunctionimplementations.md)<br/>                         | Genera implementaciones para las funciones de proxy para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                        |
| [**relationshipMetadataDeclaration**](relationshipmetadatadeclaration.md)<br/>                   | Genera una declaración de reenvío para los metadatos de hospedaje especificados en el [**elemento hostMetadata.**](hostmetadata.md) <br/> <br/>                                                                       |
| [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md)<br/>                     | Genera una definición de constante de C para los metadatos de hospedaje especificados en el [**elemento hostMetadata.**](hostmetadata.md) <br/> <br/>                                                                     |
| [**structDeclarations**](structdeclarations.md)<br/>                                             | Genera declaraciones de estructura de C para tipos conocidos.<br/> <br/>                                                                                                                                            |
| [**structDefinitions**](structdefinitions.md)<br/>                                               | Genera definiciones de estructura de C para tipos conocidos.<br/> <br/>                                                                                                                                             |
| [**stubDeclarations**](stubdeclarations.md)<br/>                                                 | Genera declaraciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                            |
| [**stubDefinitions**](stubdefinitions.md)<br/>                                                   | Genera implementaciones para las funciones de código auxiliar para las operaciones de tipo de puerto.<br/> <br/>                                                                                                                         |
| [**subscriptionFunctionDeclarations**](subscriptionfunctiondeclarations.md)<br/>                 | Genera declaraciones de implementación para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                         |
| [**subscriptionIdlFunctionDeclarations**](subscriptionidlfunctiondeclarations.md)<br/>           | Genera declaraciones IDL para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                                    |
| [**subscriptionProxyFunctionImplementations**](subscriptionproxyfunctionimplementations.md)<br/> | Genera implementaciones para las funciones de proxy de suscripción o cancelación de suscripción para las operaciones de notificación de tipo de puerto.<br/> <br/>                                                                                     |
| **text**<br/>                                                                                     | Las secciones text y CDATA se copian en el archivo sin modificaciones. El código fuente que no es una función de los datos de entrada del contrato se puede agregar a los archivos de salida mediante las secciones text y CDATA.<br/> <br/> |
| [**thisModelMetadataDeclaration**](thismodelmetadatadeclaration.md)<br/>                         | Genera una declaración de reenvío para la constante de C para los metadatos del fabricante especificados en el [**elemento thisModelMetadata.**](thismodelmetadata.md)<br/> <br/>                                      |
| [**thisModelMetadataDefinition**](thismodelmetadatadefinition.md)<br/>                           | Genera una constante de C para los metadatos del fabricante especificados en el [**elemento thisModelMetadata.**](thismodelmetadata.md)<br/> <br/>                                                                  |
| [**typeTableDeclarations**](typetabledeclarations.md)<br/>                                       | Genera declaraciones constantes de C para tablas de esquema XML para tipos conocidos.<br/> <br/>                                                                                                                       |
| [**typeTableDefinitions**](typetabledefinitions.md)<br/>                                         | Genera constantes de C para tablas de esquema XML para tipos conocidos.<br/> <br/>                                                                                                                                   |



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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

El nombre del archivo viene determinado por el valor del atributo name o del elemento secundario. El contenido del archivo viene determinado por los demás elementos secundarios, text y CDATA del **elemento de** archivo. El texto y CDATA se copian en el archivo sin modificar. Los elementos secundarios se reemplazan por código generado. El texto, CDATA y los elementos secundarios pueden aparecer en cualquier orden y se pueden repetir indefinidamente.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Valor |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




