---
description: Describe un espacio de nombres.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: Espacio de nombres (elemento)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a8747a25988b880d5287d959273fa0f4d144045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544798"
---
# <a name="namespace-element"></a>Espacio de nombres (elemento)

Describe un espacio de nombres. Este espacio de nombres se puede usar para la generación de código o para controlar <las directivas WSDL: Import>.

## <a name="usage"></a>Uso

``` syntax
<nameSpace
  uri = "character_string">
  child elements
</nameSpace>
```

## <a name="attributes"></a>Atributos



| Atributo          | Tipo                         | Obligatorio       | Descripción                                             |
|--------------------|------------------------------|----------------|---------------------------------------------------------|
| **uri**<br/> | cadena de caracteres \_<br/> | Sí<br/> | Identificador URI único del espacio de nombres.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                               | Descripción                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Nombre**](codename.md)<br/>               | Nombre que se va a usar para identificar el espacio de nombres en el código generado.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | El prefijo que se va a utilizar en el código generado para los nombres de macros en el espacio de nombres.<br/> <br/> |
| [**name**](name.md)<br/>                       | Nombre completo en el espacio de nombres.<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | El prefijo al que se debe asignar el espacio de nombres para que el código XML sea más legible.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  preferredPrefix?, 
  macroPrefix?, 
  codeName?, 
  name*
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                     | Descripción                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código de WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento se puede usar para proporcionar al generador de código información adicional sobre los espacios de nombres que encuentra en los archivos WSDL y XSD, o para introducir nuevos espacios de nombres.

El generador de código analiza automáticamente los espacios de nombres implícitos en la reflexión de tipos o que se especifican en archivos WSDL y XSD y no es necesario que se definan explícitamente en el script. En algunos casos, este elemento se puede usar para agregar propiedades o nombres adicionales a un espacio de nombres al que se hace referencia mediante reflexión de tipos o WSDL/XSD. El generador de código no tiene en cuenta esto como un conflicto.

En el código XML siguiente se muestra un elemento nameSpace (con elementos secundarios omitidos por motivos de brevedad).

``` syntax
<nameSpace uri="https://www.example.com/namespace">
  ...
</nameSpace>
```

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




