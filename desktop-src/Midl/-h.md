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
ms.openlocfilehash: a71bf02668a583b330684338cbc3f639fbbda5a340c7226e10956233aa8dc9ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105615"
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

## <a name="remarks"></a>Comentarios

El **modificador /h** especifica *filename* como nombre de un archivo de encabezado que contiene todas las definiciones contenidas en el archivo IDL, sin la sintaxis IDL. Este archivo se puede usar como un archivo de encabezado de C o C++.

## <a name="examples"></a>Ejemplos

**midl /h tlibhead.h filename.idl**

**midl /h "midl.h" filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




