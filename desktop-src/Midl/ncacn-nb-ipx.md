---
title: ncacn_nb_ipx atributo
description: La palabra clave ncacn \_ nb \_ ipx identifica NetBIOS sobre IPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8be67485d86a6094e2a41c01d5e0cf78cdabe5e251a3ab9ae046a47ed05d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642235"
---
# <a name="ncacn_nb_ipx-attribute"></a>Atributo ncacn \_ nb \_ ipx

La **palabra clave ncacn \_ nb \_ ipx** identifica NetBIOS sobre IPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*port-name* 
</dt> <dd>

Especifica un valor opcional de 8 bits que va de 1 a 254. Los valores de menos de 0x20 están reservados. Si no *se especifica el valor de nombre* de puerto, el servicio de asignación de puntos de conexión selecciona el valor del puerto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La sintaxis de la cadena de puerto NetBIOS, como todas las cadenas de puerto, se define mediante la implementación de transporte y es independiente de la especificación de IDL. El compilador MIDL realiza una comprobación de sintaxis limitada, pero no garantiza que la especificación del punto de conexión sea correcta. Algunas clases de errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
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

[Archivo de definición de interfaz (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ en \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 