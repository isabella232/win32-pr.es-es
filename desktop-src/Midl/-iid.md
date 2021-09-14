---
title: Modificador /iid
description: El modificador /iid especifica el nombre del archivo de identificador de interfaz para una interfaz COM, reemplazando el nombre predeterminado obtenido agregando i.c al nombre de \_ archivo IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /iid switch MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159747"
---
# <a name="iid-switch"></a>Modificador /iid

El **modificador /iid** especifica el nombre del archivo de identificador de interfaz para una interfaz COM, reemplazando el nombre predeterminado obtenido agregando i.c al nombre de \_ archivo IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Opciones de cambio

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de identificador de interfaz que invalida el nombre de archivo del identificador de interfaz predeterminado para una interfaz COM. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El **modificador /iid** no afecta a las interfaces RPC.

Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el [**modificador /out.**](-out.md) Una ruta de acceso explícita en *el nombre de* archivo invalida la especificación del modificador **/out.**

## <a name="examples"></a>Ejemplos

**midl /iid "my \_ iid.c" filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




