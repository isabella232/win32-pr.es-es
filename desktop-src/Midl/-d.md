---
title: /D (modificador)
description: El modificador/D define un nombre y un valor opcional que se va a pasar al preprocesador de C como si se realizara una directiva \ define. Se pueden usar varias directivas/D en una línea de comandos.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D modificador MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148938"
---
# <a name="d-switch"></a>/D (modificador)

El modificador **/d** define un nombre y un valor opcional que se va a pasar al preprocesador de C como si se realizara una directiva de **\# definición** . Se pueden usar varias directivas **/d** en una línea de comandos.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*name* 
</dt> <dd>

Especifica un nombre definido que se pasa al preprocesador de C cuando el modificador [**\_ cmd/CPP**](-cpp-cmd.md) está presente y el modificador [**/CPP \_ OPC**](-cpp-opt.md) no está presente.

</dd> <dt>

*definición* 
</dt> <dd>

Especifica un valor asociado al nombre definido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El espacio en blanco entre el modificador **/d** y el nombre definido es opcional.

Cuando el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) está presente y el modificador [**\_ OPT de/CPP**](-cpp-opt.md) no es, el compilador MIDL concatena la cadena especificada por el modificador **/CPP \_ cmd** con las opciones [**/i**](-i.md), **/d** y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF.

Se omite el modificador de compilador de MIDL **/d** cuando se especifica el modificador del compilador MIDL [/no \_ CPP](-no-cpp-nocpp.md) o [**/CPP \_ OPC**](-cpp-opt.md) .

## <a name="examples"></a>Ejemplos

**MIDL-DUNICODE nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ OPC**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[**/U**](-u.md)
</dt> </dl>

 

 




