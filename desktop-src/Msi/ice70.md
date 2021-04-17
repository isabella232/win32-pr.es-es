---
description: ICE70 comprueba que los valores enteros de las entradas del registro se especifican correctamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668069"
---
# <a name="ice70"></a>ICE70

ICE70 comprueba que los valores enteros de las entradas del registro se especifican correctamente. \# \# No se validan los valores del formato Str, \# % sin expandir. Se validan los valores de la forma \# xhex, \# xhex, \# Integer y \# \[ Property \] . En la tabla siguiente se proporciona una breve introducción.



| Value                 | Validación                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#CAD               | válido                                                                         |
| \#% de Str no expandido     | válido                                                                         |
| \#xHex, \# xHex         | Valide los caracteres hexadecimales válidos (0-9, a-f, A-F). Aquí se permiten las propiedades. |
| \#+ int, \# -int, \# int | Valide los caracteres numéricos válidos (0-9). Aquí se permiten las propiedades.     |



 

La sintaxis de un valor entero que se va a escribir en el registro es un \# entero en el que el entero es numérico.

## <a name="result"></a>Resultado

ICE70 informa de un error si los valores enteros de las entradas del registro no se especifican correctamente.

## <a name="example"></a>Ejemplo

ICE70 notifica los siguientes errores para el ejemplo dado.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

Para corregir este error: Si desea que el valor sea numérico, cambie el valor para usar todos los caracteres numéricos. Si desea que el valor sea una cadena, debe ir precedido por dos ' \# ' ( \# \# ) en lugar de solo uno.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

Para corregir este error: los caracteres hexadecimales válidos son 0-9, A-F y a-f. Solo estos caracteres pueden seguir a \# x (o \# x).

[Tabla del registro](registry-table.md) (parcial)



| Registro | Value    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Observaciones

-   \#\[Property \] es válido.
-   \#\[propiedad no válida (falta el corchete de cierre).
-   \#\[myprop1 \] \[ myprop2 es válido. (Aunque en la última vez falta el corchete de cierre, myprop1 podría evaluarse como \# Str, por lo que tendría \# \# Str \[ myprop2, que es válido.
-   \#\]propiedad \[ no válida
-   Cualquier propiedad incrustada en una cadena de valor no puede estar en la \[ \] forma $compkey, \[ \# filekey \] o \[ ! filekey \] porque no son numéricas. Sin embargo, hay una excepción, el \# \[ $compkey de propiedad \] \[ \] (o \[ \# filekey \] o \[ ! filekey \] ) es válido porque, como con el anterior, la \[ propiedad se \] puede evaluar como \# Str.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



