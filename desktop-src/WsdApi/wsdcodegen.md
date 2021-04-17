---
description: Es el elemento raíz de un archivo de script XML del generador de código de WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: elemento wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715702"
---
# <a name="wsdcodegen-element"></a>elemento wsdCodeGen

Es el elemento raíz de un archivo de script XML del generador de código de WSDAPI.

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
| **ConfigFileVersion**<br/> | Cualquier cadena de caracteres.<br/> | Sí<br/> | Versión del archivo de configuración. El único valor válido es "1,0".<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                                         | Descripción                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**autoestática**](autostatic.md)<br/>                     | Indica si WsdCodeGen debe intentar marcar automáticamente determinados campos generados como estáticos. Esta opción está habilitada de manera predeterminada.<br/> <br/>                                                                 |
| [**archivo**](file.md)<br/>                                 | Dirige el generador de código para generar un archivo.<br/> <br/>                                                                                                                                                       |
| [**hostMetadata**](hostmetadata.md)<br/>                 | Los metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).<br/> <br/>                                                                                 |
| [**layerNumber**](layernumber.md)<br/>                   | Número de la capa de código que se va a generar. Los números de capa se utilizan en tablas en tiempo de ejecución para distinguir un nivel de código para otro. WSDAPI utiliza código generado que tiene un número de capa de 0.<br/> <br/> |
| [**layerPrefix**](layerprefix.md)<br/>                   | Prefijo que se va a usar en el código generado para garantizar la unicidad de los símbolos generados. WSDAPI usa el prefijo "WSD".<br/> <br/>                                                                                     |
| [**macro**](macro.md)<br/>                               | Define el texto o el CDATA que va a reutilizar el elemento [**include**](include.md) .<br/> <br/>                                                                                                                        |
| [**System.IO**](namespace.md)<br/>                       | Describe un espacio de nombres que se usará para la generación de código.<br/> <br/>                                                                                                                                                |
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Describe el host y los metadatos hospedados para el dispositivo.<br/> <br/>                                                                                                                                               |
| [**thisModelMetadata**](thismodelmetadata.md)<br/>       | Los metadatos del fabricante y del modelo para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).<br/> <br/>                                                                  |
| [**mencionados**](wsdl.md)<br/>                                 | Especifica un archivo WSDL que se va a procesar para la información del contrato.<br/> <br/>                                                                                                                                           |
| [**BTM**](xsd.md)<br/>                                   | Especifica un archivo XSD para procesar la información de contrato.<br/> <br/>                                                                                                                                           |



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

## <a name="remarks"></a>Observaciones

En general, los elementos de [**archivo**](file.md) deben aparecer en último lugar porque generan código que utiliza los datos especificados por los demás elementos.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




