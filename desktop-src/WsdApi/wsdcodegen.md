---
description: Es el elemento raíz de un archivo de script XML del generador de código WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: wsdCodeGen, elemento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994682"
---
# <a name="wsdcodegen-element"></a>wsdCodeGen, elemento

Es el elemento raíz de un archivo de script XML del generador de código WSDAPI.

## <a name="usage"></a>Uso

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a>Atributos



| Atributo                        | Tipo                             | Obligatorio       | Descripción                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| **ConfigFileVersion**<br/> | Cualquier cadena de caracteres.<br/> | Sí<br/> | Versión del archivo de configuración. El único valor válido es "1.0".<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoStatic**](autostatic.md)<br/>                     | Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos. Esta opción está habilitada de manera predeterminada.<br/> <br/>                                                                 |
| [**Archivo**](file.md)<br/>                                 | Dirige al generador de código para generar un archivo.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | Número de la capa de código que se va a generar. Los números de capa se usan en tablas en tiempo de ejecución para distinguir una capa de código para otra. El propio WSDAPI usa código generado que tiene un número de capa de 0.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | Prefijo que se usará en el código generado para garantizar la unidad de los símbolos generados. WSDAPI usa el prefijo "WSD".<br/> <br/>                                                                                     |
| [**Macro**](macro.md)<br/>                               | Define el texto o CDATA que el elemento [**include**](include.md) va a reutilizar.<br/> <br/>                                                                                                                        |
| [**Nombres**](namespace.md)<br/>                       | Describe un espacio de nombres que se usará para la generación de código.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Describe el host y los metadatos hospedados para el dispositivo.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Metadatos del fabricante y del modelo para el dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).<br/> <br/>                                                                  |
| [**Wsdl**](wsdl.md)<br/>                                 | Especifica un archivo WSDL para procesar la información del contrato.<br/> <br/>                                                                                                                                           |
| [**Xsd**](xsd.md)<br/>                                   | Especifica un archivo XSD para procesar la información del contrato.<br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a>Elementos primarios

No hay elementos primarios.

## <a name="remarks"></a>Comentarios

En general, [**los elementos de**](file.md) archivo deben producirse en último lugar porque generan código que usa los datos especificados por los demás elementos.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




