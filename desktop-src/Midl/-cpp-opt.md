---
title: modificador/cpp_opt
description: El \_ modificador/CPP OPC especifica las opciones que se van a pasar al preprocesador de C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt modificador MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: 97d62bfd3213d9c4ce46c3cd2b1177caf720681a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "104421686"
---
# <a name="cpp_opt-switch"></a>/CPP \_ OPC

El modificador **/CPP \_ OPC** especifica las opciones que se van a pasar al preprocesador de C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_Opción de preprocesador de C \_* 
</dt> <dd>

Especifica la opción de línea de comandos asociada al preprocesador invocado. 

**Nota**: para los preprocesadores de Microsoft c/C++, debe proporcionar el `/E` modificador como parte de la cadena de *\_ \_ opción del preprocesador de c* . 

Se requieren comillas cuando se usa más de una opción y para espacios.

</dd> </dl>

## <a name="remarks"></a>Observaciones

No use este modificador a menos que haya un motivo específico para hacerlo. Consulte [los requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md) para obtener información importante sobre el preprocesamiento.

El modificador **\_ OPT/CPP** se puede usar con o sin el modificador [**\_ cmd de/CPP**](-cpp-cmd.md) . Consulte **/CPP \_ cmd** para obtener detalles sobre cómo se construye la línea de comandos del preprocesador en cualquier caso.

El modificador **\_ OPT de/CPP** , si se especifica, siempre debe incluirse `/E` para funcionar correctamente.

## <a name="examples"></a>Ejemplos

**MIDL/CPP \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc FILENAME. idl**

**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc FILENAME. idl**

**MIDL/CPP \_ OPT "/E/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**

**MIDL/CPP \_ cmd "CL"/CPP \_ OPT "/e/DFLAG = true/IC: \\ Inc" nombreDeArchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos del preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




