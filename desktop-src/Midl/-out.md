---
title: /out (modificador)
description: El modificador /out especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out switch MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b29c97438c0db1a60d94a8ae88ed99f73c33ea16a820d1aec5ca7a6be737e5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014103"
---
# <a name="out-switch"></a>/out (modificador)

El **modificador /out** especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*path-specification* 
</dt> <dd>

Especifica la ruta de acceso al directorio en el que se generan los archivos de código auxiliar, encabezado y modificador. Se puede especificar una especificación de unidad, una ruta de acceso de directorio absoluta o ambas. Las rutas de acceso se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El directorio de salida se puede especificar con una letra de unidad, un nombre de ruta de acceso absoluto o ambos. La **opción /out** se puede usar con cualquiera de los modificadores que habilitan la especificación del archivo de salida individual.

Cuando no se especifica el modificador **/out,** los archivos se escriben en el directorio actual.

El directorio predeterminado especificado por el modificador **/out** se puede reemplazar por un nombre de ruta de acceso explícito especificado como parte del modificador [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub.**](-sstub.md)

## <a name="examples"></a>Ejemplos

**midl /out c: \\ mydir \\ mysubdir \\ subdir2 deeper filename.idl**

**midl /out c: filename.idl**

**midl /out \\ mydir \\ mysubdir \\ another filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




