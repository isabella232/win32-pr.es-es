---
title: /out (modificador)
description: El modificador/out especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out (modificador) MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105676317"
---
# <a name="out-switch"></a>/out (modificador)

El modificador **/out** especifica el directorio predeterminado donde el compilador MIDL escribe los archivos de salida.

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*Especificación de ruta de acceso* 
</dt> <dd>

Especifica la ruta de acceso al directorio en el que se generan los archivos stub, header y switch. Se puede especificar una especificación de unidad, una ruta de acceso absoluta al directorio o ambos. Las rutas de acceso se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El directorio de salida se puede especificar con una letra de unidad, un nombre de ruta de acceso absoluta o ambos. La opción **/out** se puede usar con cualquiera de los modificadores que habilitan la especificación de archivo de salida individual.

Cuando no se especifica el modificador **/out** , los archivos se escriben en el directorio actual.

El directorio predeterminado especificado por el modificador **/out** puede reemplazarse por un nombre de ruta de acceso explícito especificado como parte del modificador [**/cstub**](-cstub.md), [**/Header**](-header.md), [**/proxy**](-proxy.md)o [**/sstub**](-sstub.md) .

## <a name="examples"></a>Ejemplos

**MIDL/out c: \\ myDir \\ mysubdir \\ subdir2 más profundo nombre de archivo. idl**

**MIDL/out c: nombrearchivo. idl**

**MIDL/out \\ myDir \\ mysubdir \\ otro nombre de archivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




