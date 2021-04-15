---
title: ncacn_nb_nb atributo)
description: La \_ \_ palabra clave ncacn NB NB identifica NetBEUI en NetBIOS como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c562bb0acd546fd2c8f92a92074e599c8a505dc9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105665819"
---
# <a name="ncacn_nb_nb-attribute"></a>\_atributo ncacn NB \_ NB

La palabra clave **ncacn \_ NB \_ NB** identifica NetBEUI en NetBIOS como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un valor de 8 bits opcional comprendido entre 1 y 255. Los valores de menor que 0x20 están reservados. Si no se especifica el valor de *nombre de Puerto* , el servicio de asignación de puntos de conexión selecciona el valor de puerto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La sintaxis de la cadena de puerto NetBIOS, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Es posible que se notifiquen algunas clases de errores en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_nb:[100]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**finales**](endpoint.md)
</dt> <dt>

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**\_TCP NB \_ ncacn**](ncacn-nb-tcp.md)
</dt> <dt>

[**NP de ncacn \_**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 