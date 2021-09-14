---
title: /proxy switch
description: El modificador /proxy especifica el nombre del archivo proxy de interfaz para una interfaz COM.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /proxy switch MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159715"
---
# <a name="proxy-switch"></a>/proxy switch

El **modificador /proxy** especifica el nombre del archivo proxy de interfaz para una interfaz COM.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Cambiar opciones

<dl> <dt>

*nombre \_ de archivo \_ proxy* 
</dt> <dd>

Especifica un nombre de archivo que invalida el nombre de archivo proxy de interfaz predeterminado. Los nombres de archivo se pueden entrecomillar explícitamente mediante comillas dobles (") para evitar que el shell interprete los caracteres especiales.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El nombre de archivo especificado reemplaza el nombre de archivo predeterminado obtenido \_ agregando P.C al nombre del archivo IDL. El modificador [**/proxy**](proxy.md) no afecta a las interfaces RPC.

Si *el nombre del archivo \_ \_ proxy* no incluye una ruta de acceso explícita, el archivo se escribe en el directorio actual o en el directorio especificado por el [**modificador /out.**](-out.md) Una ruta de acceso explícita en *el nombre del archivo \_ \_ proxy* invalida la especificación del modificador **/out.**

Para obtener una descripción más detallada del archivo proxy de interfaz y otros archivos generados por el compilador de MIDL, vea Sintaxis general de la línea de comandos [de MIDL.](general-midl-command-line-syntax.md)

## <a name="examples"></a>Ejemplos

**midl /proxy my \_ proxy.c filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/iid**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




