---
title: ncacn_dnet_nsp atributo
description: La palabra clave ncacn \_ dnet \_ nsp identifica DECnet como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4fa7448ff9d0cf3946ad3d0293ade19a5c2c0c407ca157d79c2c425f4a8ef6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642766"
---
# <a name="ncacn_dnet_nsp-attribute"></a>Atributo ncacn \_ dnet \_ nsp

La **palabra clave ncacn \_ dnet \_ nsp** identifica DECnet como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*server-name* 
</dt> <dd>

Especifica el nombre o la dirección de Internet del servidor o host del equipo. El nombre es una cadena de caracteres.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un nombre de objeto de DECnet o un número de objeto. El nombre del objeto puede constar de hasta 16 caracteres. Los números de objeto pueden ir precedido por el signo de la pera ( \# ).

</dd> </dl>

## <a name="remarks"></a>Comentarios

La sintaxis de la cadena de puerto de transporte de DECnet, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Extremo**](endpoint.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 