---
title: modificador/dlldata
description: El modificador/dlldata se usa para especificar el nombre de archivo del archivo dlldata generado para un archivo DLL de proxy. Si no se especifica el modificador/dlldata, se usa el nombre de archivo predeterminado dlldata. c.
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata modificador MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e9c1d7f27c56f81905081fd9ef24c8c490391b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784228"
---
# <a name="dlldata-switch"></a>modificador/dlldata

El modificador **/dlldata** se usa para especificar el nombre de archivo del archivo dlldata generado para un archivo dll de proxy. Si no se especifica el modificador **/dlldata** , se usa el nombre de archivo predeterminado dlldata. c.

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*nombre de archivo* 
</dt> <dd>

Nombre del archivo de código fuente de C que generará el compilador MIDL para la DLL del proxy.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El archivo especificado por *nombre-archivo* debe estar vinculado al archivo DLL del proxy. El archivo dlldata contiene puntos de entrada y estructuras de datos requeridos por el generador de clases para la DLL del proxy. Estas estructuras de datos especifican las interfaces de objeto incluidas en el archivo DLL del proxy. El archivo dlldata también especifica el identificador de clase del generador de clases para la DLL del proxy. Siempre es el UUID (IID) de la primera interfaz del primer archivo proxy (por orden alfabético).

Se debe especificar el mismo archivo dlldata al invocar a MIDL en todos los archivos IDL que vayan a un archivo DLL de proxy determinado. El archivo dlldata se crea o se actualiza durante cada compilación de MIDL, lo que genera incrementalmente una lista de las interfaces que Irán a la DLL de proxy.

## <a name="examples"></a>Ejemplos

**datos/dlldata de MIDL. c**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




