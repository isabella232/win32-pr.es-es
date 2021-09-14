---
title: Modificador /U
description: El modificador /U quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si lo hubiera hecho una directiva \undefine.
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
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159700"
---
# <a name="u-switch"></a>Modificador /U

El **modificador /U** quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si lo hubiera hecho una **\# directiva undefine.**

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*name* 
</dt> <dd>

Especifica un nombre definido que se va a pasar al preprocesador de C como si lo hubiera creado **\# una directiva undefine.** El nombre está predefinido por el preprocesador de C o definido previamente por el usuario.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se pueden usar varias directivas **/U** en una línea de comandos. El espacio en blanco entre **el modificador /U** y el nombre no definido es opcional.

Cuando el modificador [**/cpp \_ cmd**](-cpp-cmd.md) está presente y el modificador [**/cpp \_ opt**](-cpp-opt.md) no lo está, el compilador midL concatena la cadena especificada por el modificador /cpp cmd con las opciones \_ [**/I**](-i.md), [**/D**](-d.md)y **/U** y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF. El modificador del compilador **MIDL /U** se omite cuando se especifica el modificador del compilador MIDL **/no \_ cpp** o **/cpp \_ opt.**

## <a name="examples"></a>Ejemplos

**midl /UUNICODE filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




