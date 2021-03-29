---
title: /WARN (modificador)
description: El modificador/WARN especifica el nivel de advertencia del compilador de MIDL.
ms.assetid: b1e26e67-8c47-40a2-8f34-22273ddfaa1d
keywords:
- /WARN (modificador MIDL)
topic_type:
- apiref
api_name:
- /warn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebb2effd65175bf7bf54cb74cb63a56af0278784
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783736"
---
# <a name="warn-switch"></a>/WARN (modificador)

El modificador **/WARN** especifica el nivel de advertencia del compilador de MIDL.

``` syntax
midl /warn level
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*level* 
</dt> <dd>

Especifica el nivel de advertencia, un entero en el intervalo comprendido entre 0 y 4. No hay espacio entre el modificador **/WARN** y el dígito que indica el valor de nivel de advertencia.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nivel de advertencia indica la gravedad de la advertencia. Los niveles de advertencia oscilan entre 1 y 4, y el valor cero significa que no se muestra ninguna información de advertencia. La advertencia de mayor gravedad es el nivel 1. En la tabla siguiente se describen las advertencias para cada nivel de advertencia.



| Nivel de advertencia | Descripción                                             | Ejemplo                                                                   |
|---------------|---------------------------------------------------------|---------------------------------------------------------------------------|
| 0             | Sin advertencias.                                            |                                                                           |
| 1             | ADVERTENCIAS graves que pueden provocar errores en la aplicación.      | No se especificó ningún identificador de enlace, punteros sin atributos, modificadores en conflicto. |
| 2             | Puede causar problemas en el entorno operativo del usuario. | La longitud del identificador supera los 31 caracteres. No se especificó ningún brazo de Unión predeterminado.  |
| 3             | Reservado.                                               |                                                                           |
| 4             | Nivel de advertencia más bajo.                                   | Construcciones no ANSI C.                                                    |



 

Las advertencias son distintas de los errores. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

El nivel de advertencia establecido por el modificador **/WARN** se puede usar con el modificador [**WX**](-wx.md) para hacer que el compilador MIDL detenga el procesamiento del archivo IDL.

El modificador **/WARN** se comporta igual que el modificador [**/w**](-w.md) .

## <a name="examples"></a>Ejemplos

**MIDL/warn2 nombrearchivo. idl**

**barra de/warn4 de MIDL. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




