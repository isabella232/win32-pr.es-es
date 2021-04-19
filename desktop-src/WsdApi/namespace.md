---
description: Describe un espacio de nombres.
ms.assetid: 8e31526a-639f-481b-91f1-fcd376818cbf
title: nameSpace, elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2414919f699bb60c2cf1e48bc52030c36cf67a0
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380849"
---
# <a name="namespace-element"></a>nameSpace, elemento

Describe un espacio de nombres. Este espacio de nombres se puede usar para la generación de código o para las \<wsdl:import> directivas de control.

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
| **uri**<br/> | cadena \_ de caracteres<br/> | Sí<br/> | URI único del espacio de nombres.<br/> <br/> |



## <a name="child-elements"></a>Elementos secundarios



| Elemento                                               | Descripción                                                                                              |
|-------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>               | Nombre que se va a usar para identificar el espacio de nombres en el código generado.<br/> <br/>                  |
| [**macroPrefix**](macroprefix.md)<br/>         | Prefijo que se va a usar en el código generado para los nombres de macros en el espacio de nombres .<br/> <br/> |
| [**Nombre**](name.md)<br/>                       | Nombre completo en el espacio de nombres .<br/> <br/>                                                |
| [**preferredPrefix**](preferredprefix.md)<br/> | Prefijo al que se debe asignar el espacio de nombres para que el XML sea más legible.<br/> <br/> |



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
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Elemento raíz de un archivo de script XML del generador de código WSDAPI.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este elemento se puede usar para proporcionar al generador de código información adicional sobre los espacios de nombres que encuentra en los archivos WSDL y XSD o para introducir nuevos espacios de nombres.

Los espacios de nombres implícitos en la reflexión de tipos o especificados en los archivos WSDL y XSD se analizan automáticamente por el generador de código y no tienen que definirse explícitamente en el script. En algunos casos, este elemento se puede usar para agregar propiedades o nombres adicionales a un espacio de nombres al que hace referencia la reflexión de tipos o WSDL/XSD. El generador de código no lo considera un conflicto.

El xml siguiente muestra un elemento nameSpace (con elementos secundarios omitidos por brevedad).

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



 

 




