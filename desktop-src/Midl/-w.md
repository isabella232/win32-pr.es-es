---
title: Modificador/w
description: El modificador/W especifica el nivel de advertencia del compilador de MIDL. El nivel de advertencia indica la gravedad de la advertencia.
ms.assetid: ee894d73-cbd1-455f-9836-a6d80cfc95f9
keywords:
- /W modificador MIDL
topic_type:
- apiref
api_name:
- /W
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00b1f15ae0c28722adaca8c4b0651606681ce3af
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105685636"
---
# <a name="w-switch"></a>Modificador/w

El modificador **/w** especifica el nivel de advertencia del compilador de MIDL. El nivel de advertencia indica la gravedad de la advertencia.

``` syntax
midl /W level
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de advertencia, un entero en el intervalo comprendido entre 0 y 4. No hay espacio entre el modificador **/w** y el dígito que indica el valor de nivel de advertencia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los niveles de advertencia oscilan entre 1 y 4, y el valor cero significa que no se muestra ninguna información de advertencia. La advertencia de mayor gravedad es el nivel 1. En la tabla siguiente se describen las advertencias para cada nivel de advertencia.



| Nivel de advertencia | Descripción                                             | Ejemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| W0 (            | Sin advertencias.                                            |                                                                           |
| W1            | ADVERTENCIAS graves que pueden provocar errores en la aplicación.      | No se especificó ningún identificador de enlace, punteros sin atributos, modificadores en conflicto. |
| W2            | Puede causar problemas en el entorno operativo del usuario. | La longitud del identificador supera los 31 caracteres. No se especificó ningún brazo de Unión predeterminado.  |
| W3            | Reservado.                                               |                                                                           |
| W4            | Nivel de advertencia más bajo.                                   | Construcciones no ANSI C.                                                    |



 

Las advertencias son distintas de los errores. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

El nivel de advertencia establecido por el modificador **/w** se puede usar con el modificador [**/WX**](-wx.md) para que el compilador MIDL detenga el procesamiento del archivo IDL.

El modificador **/w** se comporta igual que el modificador [**/WARN**](-warn.md) .

## <a name="examples"></a>Ejemplos

**MIDL/W2 nombrearchivo. idl**

**barra de/W4 de MIDL. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/WARN**](-warn.md)
</dt> </dl>

 

 




