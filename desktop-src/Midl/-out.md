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
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159720"
---
# <a name="out-switch"></a>/out (modificador)

El **modificador /out** especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*path-specification* 
</dt> <dd>

Especifica la ruta de acceso al directorio en el que se generan los archivos de código auxiliar, encabezado y modificador. Se puede especificar una especificación de unidad, una ruta de acceso de directorio absoluta o ambas. Las rutas de acceso se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El directorio de salida se puede especificar con una letra de unidad, un nombre de ruta de acceso absoluto o ambos. La **opción /out** se puede usar con cualquiera de los modificadores que habilitan la especificación individual del archivo de salida.

Cuando no se especifica el modificador **/out,** los archivos se escriben en el directorio actual.

El directorio predeterminado especificado por el modificador **/out** se puede reemplazar por un nombre de ruta de acceso explícito especificado como parte del modificador [**/cstub**](-cstub.md), [**/header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub.**](-sstub.md)

## <a name="examples"></a>Ejemplos

**midl /out c: \\ mydir \\ mysubdir \\ subdir2 deeper filename.idl**

**midl /out c: filename.idl**

**midl /out \\ mydir \\ mysubdir \\ another filename.idl**

## <a name="see-also"></a>Consulte también

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

 

 




