---
title: modificador/h
description: La opción/h es equivalente funcionalmente a la opción/header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h (modificador) MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076845"
---
# <a name="h-switch"></a>modificador/h

La opción **/h** es equivalente funcionalmente a la opción [**/Header**](-header.md) .

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/h** especifica *filename* como el nombre de un archivo de encabezado que contiene todas las definiciones incluidas en el archivo IDL, sin la sintaxis IDL. Este archivo se puede usar como un archivo de encabezado de C o C++.

## <a name="examples"></a>Ejemplos

**MIDL/h tlibhead. h nombreDeArchivo. idl**

**MIDL/h "MIDL. h" FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




