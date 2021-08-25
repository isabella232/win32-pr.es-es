---
title: Modificador /U
description: El modificador /U quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si lo hubiera hecho una directiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U switch MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895775"
---
# <a name="u-switch"></a>Modificador /U

El **modificador /U** quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si lo hubiera hecho una **\# directiva undefine.**

``` syntax
midl /U name
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*name* 
</dt> <dd>

Especifica un nombre definido que se pasará al preprocesador de C como si lo hubiera una **\# directiva undefine.** El nombre está predefinido por el preprocesador de C o definido previamente por el usuario.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se pueden usar varias directivas **/U** en una línea de comandos. El espacio en blanco entre **el modificador /U** y el nombre no definido es opcional.

Cuando el modificador [**/cpp \_ cmd**](-cpp-cmd.md) está presente y el modificador [**/cpp \_ opt**](-cpp-opt.md) no lo está, el compilador MIDL concatena la cadena especificada por el modificador /cpp cmd con las opciones \_ [**/I,**](-i.md) [**/D**](-d.md)y **/U** y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF. El modificador del compilador **MIDL /U** se omite cuando se especifica el modificador del compilador MIDL **/no \_ cpp** o **/cpp \_ opt.**

## <a name="examples"></a>Ejemplos

**midl /UUNICODE filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/d**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




