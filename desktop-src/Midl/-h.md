---
title: Modificador /h
description: La opción /h es funcionalmente equivalente a la opción /header.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h switch MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159755"
---
# <a name="h-switch"></a>Modificador /h

La **opción /h** es funcionalmente equivalente a la [**opción /header.**](-header.md)

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de encabezado que invalida el nombre de archivo de encabezado predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /h** especifica *filename* como nombre de un archivo de encabezado que contiene todas las definiciones contenidas en el archivo IDL, sin la sintaxis IDL. Este archivo se puede usar como un archivo de encabezado de C o C++.

## <a name="examples"></a>Ejemplos

**midl /h tlibhead.h filename.idl**

**midl /h "midl.h" filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




