---
description: Incluye el contenido de una macro o un archivo en la salida generada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include [elemento]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8029f58d9d1627a315fcfd02aa4f311d0a717361abf587aa92c52134b78e5958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856595"
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



| Atributo            | Tipo                         | Requerido      | Descripción                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **file**<br/>  | cadena \_ de caracteres<br/> | No<br/> | Ruta de acceso al archivo que se incluirá.<br/> <br/>  |
| **Macro**<br/> | cadena \_ de caracteres<br/> | No<br/> | Nombre de la macro que se incluirá.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Indica al generador de código que genere un archivo y especifica el nombre del archivo de salida.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Se debe **especificar el** **atributo** de macro o el atributo de archivo. No especifique ambos atributos.

WsdCodeGen define una macro denominada **DoNotModify.** Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.

## <a name="examples"></a>Ejemplos

En el xml siguiente se muestra cómo incluir la macro **DoNotModify.** Este XML se puede agregar a un archivo de configuración XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




