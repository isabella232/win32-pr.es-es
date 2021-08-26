---
title: Modificador /dlldata
description: El modificador /dlldata se usa para especificar el nombre de archivo para el archivo dlldata generado para un archivo DLL de proxy. El nombre de archivo predeterminado Dlldata.c se usa si no se especifica el modificador /dlldata.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata switch MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105645"
---
# <a name="dlldata-switch"></a>Modificador /dlldata

El **modificador /dlldata** se usa para especificar el nombre de archivo para el archivo dlldata generado para un archivo DLL de proxy. El nombre de archivo predeterminado Dlldata.c se usa si no se especifica el modificador **/dlldata.**

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*file-name* 
</dt> <dd>

Nombre del archivo de origen de C que el compilador MIDL generará para el archivo DLL de proxy.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El archivo especificado por *file-name* debe estar vinculado al archivo DLL de proxy. El archivo dlldata contiene los puntos de entrada y las estructuras de datos requeridas por el generador de clases para el archivo DLL de proxy. Estas estructuras de datos especifican las interfaces de objeto contenidas en el archivo DLL de proxy. El archivo dlldata también especifica el identificador de clase del generador de clases para el archivo DLL de proxy. Este es siempre el UUID (IID) de la primera interfaz del primer archivo proxy (por orden alfabético).

Se debe especificar el mismo archivo dlldata al invocar MIDL en todos los archivos IDL que se van a incluir en un archivo DLL de proxy determinado. El archivo dlldata se crea o actualiza durante cada compilación MIDL, compilando de forma incremental una lista de las interfaces que irán al archivo DLL de proxy.

## <a name="examples"></a>Ejemplos

**midl /dlldata data.c**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




