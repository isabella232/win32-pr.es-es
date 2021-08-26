---
title: Modificador /W
description: El modificador /W especifica el nivel de advertencia del compilador MIDL. El nivel de advertencia indica la gravedad de la advertencia.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W switch MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e03b2d4a762a7fbb1bba00f8804e8e43a77ad8183a744add63fcf0d37c86d54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913675"
---
# <a name="w-switch"></a>Modificador /W

El **modificador /W** especifica el nivel de advertencia del compilador MIDL. El nivel de advertencia indica la gravedad de la advertencia.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de advertencia, un entero en el intervalo de 0 a 4. No hay espacio entre el modificador **/W** y el dígito que indica el valor de nivel de advertencia.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Los niveles de advertencia oscilan entre 1 y 4, con un valor de cero significado para no mostrar ninguna información de advertencia. La advertencia de gravedad más alta es el nivel 1. En la tabla siguiente se describen las advertencias de cada nivel de advertencia.



| Nivel de advertencia | Descripción                                             | Ejemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0            | Sin advertencias.                                            |                                                                           |
| W1            | Advertencias graves que pueden provocar errores de aplicación.      | No se ha especificado ningún identificador de enlace, punteros sin atributos, modificadores en conflicto. |
| W2            | Puede causar problemas en el entorno operativo del usuario. | La longitud del identificador supera los 31 caracteres. No se ha especificado ningún arm de unión predeterminado.  |
| W3            | Reservado.                                               |                                                                           |
| W4            | Nivel de advertencia más bajo.                                   | Construcciones C que no son ANSI.                                                    |



 

Las advertencias son diferentes de los errores. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

El nivel de advertencia establecido por el modificador **/W** se puede usar con el modificador [**/WX**](-wx.md) para hacer que el compilador MIDL detenga el procesamiento del archivo IDL.

El **modificador /W** se comporta igual que el [**modificador /warn.**](-warn.md)

## <a name="examples"></a>Ejemplos

**midl /W2 filename.idl**

**midl /W4 bar.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/warn**](-warn.md)
</dt> </dl>

 

 




