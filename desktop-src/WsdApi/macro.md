---
description: Define el texto o el CDATA que va a reutilizar el elemento include.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: elemento macro
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277116"
---
# <a name="macro-element"></a>elemento macro

Define el texto o el CDATA que va a reutilizar el elemento [**include**](include.md) .

## <a name="usage"></a>Uso

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Atributos



| Atributo           | Tipo                         | Obligatorio       | Descripción                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | cadena de caracteres \_<br/> | Sí<br/> | Nombre de la macro.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

WsdCodeGen define una macro denominada **DoNotModify**. Cuando se incluye esta macro, el código generado contiene un bloque de comentarios de alta visibilidad que indica a los desarrolladores que no modifiquen el código generado.

El siguiente XML muestra cómo incluir la macro **DoNotModify** . Este XML se puede Agregar a un archivo de configuración XML para WsdCodeGen.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




