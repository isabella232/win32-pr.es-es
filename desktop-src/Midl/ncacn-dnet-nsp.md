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
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159478"
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

Especifica un nombre de objeto de DECnet o un número de objeto. El nombre del objeto puede constar de hasta 16 caracteres. Los números de objeto pueden ir precedido del signo de perd ( \# ).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto de transporte de DECnet, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del extremo sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

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

[**endpoint**](endpoint.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 