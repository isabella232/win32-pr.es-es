---
title: ncacn_nb_nb atributo
description: La palabra clave ncacn \_ nb \_ nb identifica NetBEUI sobre NetBIOS como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 8bab2784-44ba-4356-85c1-5bd17e75d6a8
keywords:
- ncacn_nb_nb atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_nb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84a2ea48bc1472d69c2247f227b94193326927481838894e24efbce9e09afc87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642160"
---
# <a name="ncacn_nb_nb-attribute"></a>Atributo ncacn \_ nb \_ nb

La **palabra clave ncacn \_ nb \_ nb** identifica NetBEUI sobre NetBIOS como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_nb_nb:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*port-name* 
</dt> <dd>

Especifica un valor opcional de 8 bits que va de 1 a 255. Los valores de menos de 0x20 están reservados. Si no *se especifica el valor port-name,* el servicio de asignación de puntos de conexión selecciona el valor del puerto.

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
    endpoint("ncacn_nb_nb:[100]") 
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

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**enlace de cadena**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 