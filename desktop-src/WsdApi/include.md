---
description: Incluye el contenido de una macro o un archivo en la salida generada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include [elemento]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083069"
---
# <a name="include-element"></a>include [elemento]

Incluye el contenido de una macro o un archivo en la salida generada.

## <a name="usage"></a>Uso

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo            | Tipo                         | Obligatorio      | Descripción                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | cadena de caracteres \_<br/> | No<br/> | Ruta de acceso al archivo que se va a incluir.<br/> <br/>  |
| **macro**<br/> | cadena de caracteres \_<br/> | No<br/> | Nombre de la macro que se va a incluir.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**archivo**](file.md)<br/> | Dirige el generador de código para generar un archivo y especifica el nombre del archivo de salida.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Se debe especificar el atributo de **macro** o el atributo de **archivo** . No especifique ninguno de los dos atributos.

WsdCodeGen define una macro denominada **DoNotModify**. Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.

## <a name="examples"></a>Ejemplos

El siguiente XML muestra cómo incluir la macro **DoNotModify** . Este XML se puede Agregar a un archivo de configuración XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




