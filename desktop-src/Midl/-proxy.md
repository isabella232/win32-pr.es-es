---
title: modificador/proxy
description: El modificador/proxy especifica el nombre del archivo de proxy de interfaz para una interfaz COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /proxy modificador MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904196"
---
# <a name="proxy-switch"></a>modificador/proxy

El modificador **/proxy** especifica el nombre del archivo de proxy de interfaz para una interfaz com.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Opciones de conmutador

<dl> <dt>

*\_nombre de archivo proxy \_* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre de archivo del proxy de interfaz predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente con comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado obtenido agregando \_ P. C al nombre del archivo IDL. El modificador/ [**proxy**](proxy.md) no afecta a las interfaces RPC.

Si *el \_ \_ nombre de archivo del proxy* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el modificador [**/out**](-out.md) . Una ruta de acceso explícita en el *\_ \_ nombre de archivo del proxy* invalida la especificación del modificador **/out** .

Para obtener una descripción más detallada del archivo de proxy de interfaz y otros archivos generados por el compilador MIDL, vea [Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md).

## <a name="examples"></a>Ejemplos

**MIDL/proxy My \_ proxy. c nombrearchivo. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




