---
title: Modificador /no_def_idir
description: Cuando se especifican directorios con el modificador /I, el modificador /no def idir indica al compilador MIDL que busque solo los directorios especificados con el modificador \_ \_ /I.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir switch MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811305"
---
# <a name="no_def_idir-switch"></a>Modificador /no \_ def \_ idir

Cuando se especifican directorios con el modificador [**/I,**](-i.md) el modificador **/no \_ def \_ idir** indica al compilador MIDL que busque solo los directorios especificados con el modificador **/I,** omitiendo el directorio actual, así como los directorios especificados por la variable de entorno INCLUDE.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Cuando no se especifica ningún directorio con el modificador [**/I,**](-i.md) el modificador **/no \_ def \_ idir** indica al compilador MIDL que busque solo el directorio actual.

## <a name="examples"></a>Ejemplos

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




