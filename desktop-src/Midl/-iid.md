---
title: modificador/IID
description: El modificador/IID especifica el nombre del archivo de identificador de interfaz para una interfaz COM, invalidando el nombre predeterminado obtenido agregando \_ i. c al nombre de archivo IDL.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID modificador MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419648"
---
# <a name="iid-switch"></a>modificador/IID

El modificador **/IID** especifica el nombre del archivo de identificador de interfaz para una interfaz com, invalidando el nombre predeterminado obtenido agregando \_ i. c al nombre de archivo IDL.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*filename* 
</dt> <dd>

Especifica un nombre de archivo de identificador de interfaz que invalida el nombre de archivo del identificador de interfaz predeterminado para una interfaz COM. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El modificador **/IID** no afecta a las interfaces RPC.

Si *filename* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) . Una ruta de acceso explícita en *filename* invalida la especificación del modificador **/out** .

## <a name="examples"></a>Ejemplos

**/IID de MIDL "My \_ IID. c" FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




