---
title: modificador/no_def_idir
description: Cuando se especifican directorios con el modificador/I, \_ el \_ modificador/no Def Idir indica al compilador de MIDL que solo busque en los directorios especificados con el modificador/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir modificador MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62ed845c73c36fbbfe4ea7dea952ee4541b043a7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904194"
---
# <a name="no_def_idir-switch"></a>/no \_ Def \_ Idir modificador

Cuando se especifican directorios con el modificador [**/i**](-i.md) , el modificador **/no \_ Def \_ Idir** indica al compilador de MIDL que busque solo los directorios especificados con el modificador **/i** , omitiendo el directorio actual, así como los directorios especificados por la variable de entorno include.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Cuando no se especifica ningún directorio con el modificador [**/i**](-i.md) , el modificador **/no \_ Def \_ Idir** indica al compilador de MIDL que busque solo el directorio actual.

## <a name="examples"></a>Ejemplos

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




