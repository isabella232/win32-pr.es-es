---
title: Modificador/u
description: El modificador/U quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si se tratase de una directiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U modificador MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148915"
---
# <a name="u-switch"></a>Modificador/u

El modificador **/u** quita cualquier definición anterior de un nombre pasando el nombre al preprocesador de C como si se tratase de una directiva **\# undefine** .

``` syntax
midl /U name
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*name* 
</dt> <dd>

Especifica un nombre definido que se va a pasar al preprocesador de C como si se realizara una directiva **\# undefine** . El preprocesador de C o el predefinido por el usuario predefine el nombre.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se pueden usar varias directivas de **/u** en una línea de comandos. El espacio en blanco entre el modificador **/u** y el nombre no definido es opcional.

Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el \_ modificador/CPP cmd con las opciones [**/i**](-i.md), [**/d**](-d.md)y **/u** y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF. El modificador del compilador de MIDL se omite cuando se especifica **el modificador** del compilador de MIDL **/no \_ CPP** o **/CPP \_ OPC** .

## <a name="examples"></a>Ejemplos

**MIDL/UUNICODE nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ OPC**](-cpp-opt.md)
</dt> <dt>

[**/D.**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/no \_ CPP**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




