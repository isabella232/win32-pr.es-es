---
description: Incluye el contenido de una macro o un archivo en la salida generada.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include [elemento]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995782"
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



 

 




