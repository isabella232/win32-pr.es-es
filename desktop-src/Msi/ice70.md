---
description: ICE70 comprueba que los valores enteros de las entradas del Registro se especifican correctamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecd76d38b796650346a8651fe5a3817edfaa412dfe7772f2dba9c0295f7eebdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649275"
---
# <a name="ice70"></a>ICE70

ICE70 comprueba que los valores enteros de las entradas del Registro se especifican correctamente. Los valores del formato \# \# str, \# %unexpanded str no se validan. Se validan los valores de la forma \# \# xhex, Xhex, \# entero \# \[ y \] propiedad. En la tabla siguiente se proporciona una breve introducción.



| Valor                 | Validación                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#Str               | Válido                                                                         |
| \#%unexpanded str     | Válido                                                                         |
| \#xHex, \# XHex         | Valide si hay caracteres hexadecimales válidos (0-9,a-f,A-F). Aquí se permiten propiedades. |
| \#+int, \# -int, \# int | Valide si hay caracteres numéricos válidos (0-9). Aquí se permiten propiedades.     |



 

La sintaxis de un valor entero que se va a especificar en el registro es \# un entero donde integer es numérico.

## <a name="result"></a>Resultado

ICE70 notifica un error si los valores enteros de las entradas del Registro no se especifican correctamente.

## <a name="example"></a>Ejemplo

ICE70 notifica los siguientes errores para el ejemplo dado.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

Para corregir este error: si desea que el valor sea numérico, cambie el valor para que use todos los caracteres numéricos. Si desea que el valor sea una cadena, debe ir precedida de dos ' ' ( ) en \# \# \# lugar de solo una.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

Para corregir este error: los caracteres hexadecimales válidos son 0-9, A-F y a-f. Solo estos caracteres pueden seguir \# la x (o \# X).

[Tabla del Registro](registry-table.md) (parcial)



| Registro | Value    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Comentarios

-   \#\[myproperty \] es válida.
-   \#\[myproperty no es válida (falta el corchete final).
-   \#\[myprop1 \] \[ myprop2 es válido. (Aunque al último le falta el corchete final, myprop1 podría evaluarse como str, por lo que tendría \# \# \# str \[ myprop2, que es válido
-   \#\]myproperty \[ no es válida
-   Cualquier propiedad incrustada en una cadena de valor no puede \[ tener $compkey \] , \[ \# filekey o \] \[ !filekey \] porque no son numéricos. Sin embargo, hay una excepción, \# \[ myproperty \] \[ $compkey \] \[ \# (o filekey o \] \[ !filekey ) es válida \] porque, \[ \] \# al igual que con el anterior, myproperty puede evaluarse como str.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



