---
title: ncacn_nb_ipx atributo)
description: La \_ \_ palabra clave de IPX ncacn NB identifica NetBIOS sobre IPX como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx el atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 156b5c460c4cc8638640e7eb3500ec9a7a9fa0b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105651370"
---
# <a name="ncacn_nb_ipx-attribute"></a>ncacn \_ NB de \_ atributo IPX

La palabra clave de **\_ \_ IPX Ncacn NB** identifica NetBIOS sobre IPX como la familia de protocolos para el extremo. Esta familia de protocolos está obsoleta y no debe usarse en aplicaciones nuevas.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*nombre del puerto* 
</dt> <dd>

Especifica un valor de 8 bits opcional comprendido entre 1 y 254. Los valores de menor que 0x20 están reservados. Si no se especifica el valor de *nombre de Puerto* , el servicio de asignación de puntos de conexión selecciona el valor de puerto.

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
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ en \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ SPX**](ncacn-spx.md)
</dt> <dt>

[**NP de ncacn \_**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IP \_ UDP**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**enlace de cadenas**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 