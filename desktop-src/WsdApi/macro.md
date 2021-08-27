---
description: Define el texto o CDATA que el elemento include va a reutilizar.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee876e04934a328e73b6e45d8442249ad3d749fc3b40fa45652c89979fcff6e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991725"
---
# <a name="macro-element"></a>macro, elemento

Define el texto o CDATA que el elemento [**include**](include.md) va a reutilizar.

## <a name="usage"></a>Uso

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                         | Requerido       | Descripción                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | cadena \_ de caracteres<br/> | Sí<br/> | Nombre de la macro.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Comentarios

WsdCodeGen define una macro denominada **DoNotModify.** Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.

En el xml siguiente se muestra cómo incluir la macro **DoNotModify.** Este XML se puede agregar a un archivo de configuración XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




