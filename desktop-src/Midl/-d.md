---
title: Modificador /D
description: El modificador /D define un nombre y un valor opcional que se pasarán al preprocesador de C como si lo hubiera una directiva \define. Se pueden usar varias directivas /D en una línea de comandos.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D switch MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa8bc01a978949ec0f0cc4ff78289a1cb442046966f1cea954c6b65cc232f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385782"
---
# <a name="d-switch"></a>Modificador /D

El **modificador /D** define un nombre y un valor opcional que se pasarán al preprocesador de C como si lo hubiera creado una **\# directiva define.** Se pueden usar varias directivas **/D** en una línea de comandos.

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*name* 
</dt> <dd>

Especifica un nombre definido que se pasa al preprocesador de C cuando el modificador [**/cpp \_ cmd**](-cpp-cmd.md) está presente y el modificador [**/cpp \_ opt**](-cpp-opt.md) no está presente.

</dd> <dt>

*Definición* 
</dt> <dd>

Especifica un valor asociado al nombre definido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El espacio en blanco entre **el modificador /D** y el nombre definido es opcional.

Cuando el modificador [**/cpp \_ cmd**](-cpp-cmd.md) está presente y el modificador [**/cpp \_ opt**](-cpp-opt.md) no lo está, el compilador MIDL concatena la cadena especificada por el modificador **/cpp \_ cmd** con las opciones [**/I,**](-i.md) **/D** y [**/U**](-u.md) y usa esta cadena concatenada para invocar el preprocesador de C para cada archivo de origen IDL y ACF.

El modificador del compilador **MIDL /D** se omite cuando se especifica el modificador del compilador MIDL [/no \_ cpp](-no-cpp-nocpp.md) o [**/cpp \_ opt.**](-cpp-opt.md)

## <a name="examples"></a>Ejemplos

**midl -DUNICODE filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**/u**](-u.md)
</dt> </dl>

 

 




