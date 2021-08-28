---
title: Modificador /cpp_opt
description: El modificador /cpp \_ opt especifica las opciones que se pasan al preprocesador de C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /cpp_opt switch MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3b7845feb36cd09d96fc64cb7397e4daf001957f6ce7a6f5e797707caafd32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105662"
---
# <a name="cpp_opt-switch"></a>/cpp \_ opt switch

El **modificador /cpp \_ opt** especifica las opciones que se pasan al preprocesador de C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*Opción \_ de preprocesador de C \_* 
</dt> <dd>

Especifica la opción de línea de comandos asociada al preprocesador invocado. 

**Nota:** Para los preprocesadores de Microsoft C/C++, debe proporcionar el modificador como parte de la cadena de opción `/E` *de \_ \_ preprocesador de C.* 

Las comillas son necesarias cuando se usa más de una opción y para los espacios.

</dd> </dl>

## <a name="remarks"></a>Comentarios

No use este modificador a menos que haya una razón específica para hacerlo. Consulte [Requisitos de preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md) para obtener información importante sobre el preprocesamiento.

El **modificador /cpp \_ opt** se puede usar con o sin el modificador [**/cpp \_ cmd.**](-cpp-cmd.md) Consulte **/cpp \_ cmd para** obtener más información sobre cómo se construye la línea de comandos del preprocesador en cualquier caso.

El **modificador /cpp \_ opt,** si se especifica, siempre debe incluir `/E` para funcionar correctamente.

## <a name="examples"></a>Ejemplos

**midl /cpp \_ cmd d: \\ nt tools \\ \\ ia64 \\cl.exe /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ cmd "mycpp" /DFLAG=TRUE /Ic: \\ inc filename.idl**

**midl /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

**midl /cpp \_ cmd "cl" /cpp \_ opt "/E /DFLAG=TRUE /Ic: \\ inc" filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[Requisitos de preprocesador de C para MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




