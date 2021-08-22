---
title: ncadg_ipx atributo
description: La palabra clave ncadg \_ ipx identifica IPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 6b136eb9-4e18-43ff-993b-a2ad005273f1
keywords:
- ncadg_ipx atributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbca1ef3cb5f51e54fe8b95aa16326c6438903ff9717258edea9fac491eebafa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067055"
---
# <a name="ncadg_ipx-attribute"></a>Atributo ipx de ncadg \_

La **palabra clave ncadg \_ ipx** identifica IPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncadg_ipx:link-address[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*link-address* 
</dt> <dd>

Especifica el servidor host. Puede ser una cadena de caracteres (el nombre del servidor) o un número hexadecimal de 20 dígitos que consta de la dirección de red del servidor host (8 dígitos) concatenada con la dirección del nodo (12 dígitos). Consulte Comentarios para obtener instrucciones sobre cómo obtener la dirección de red y la dirección del nodo. Una **cadena NULL** especifica el equipo local.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un número opcional de 16 bits que representa la dirección del socket. Los valores pueden oscilar entre 1 y 65535. Cuando no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor de *nombre de puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las restricciones siguientes se aplican a los protocolos de datagrama, **ncadg \_ ipx** y [**ncadg \_ ip \_ udp**](ncadg-ip-udp.md):

-   No admiten devoluciones de llamada. Se producirá un error en todas las funciones que usen **\[** [**el**](callback.md) atributo de **\]** devolución de llamada.
-   No admiten el uso del constructor [**de tipo**](pipe.md) de canalización.

Cuando se usa **el transporte de ncadg \_ ipx,** el nombre del servidor es exactamente el mismo que el nombre del servidor Windows de 32 bits. Sin embargo, dado que los nombres se distribuyen mediante protocolos de Kerberos, deben ajustarse a las convenciones de nomenclatura de Kerberos. Si el nombre de un servidor no es válido, los servidores no podrán crear puntos de conexión con el **\_ transporte ipx de ncadg.** A continuación se muestra una lista parcial de caracteres prohibidos en los nombres de servidor de Byte:

" \* + . / : ; < = > ? \[ \] \\ \|

El **transporte de ncadg \_ ipx** es compatible con la versión de NWLink proporcionada con MS Client 3.0.

Las aplicaciones cliente de Windows de 16 bits que usan el transporte **\_ ipx de ncadg** requieren que el archivo Nwipxspx.dll se instale para ejecutarse en el subsistema WOW. Póngase en contacto con Llegar a Para obtener este archivo.

Para obtener las direcciones de red y nodo, use la utilidad **comcheck de** Hexadecimal o la API **IPXGetInternetAddress** definida por Asín. En Windows, también puede obtener estas direcciones con el **comando ipxroute config.**

La sintaxis de la cadena de puerto de transporte TCP/IP, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del extremo sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

> [!Note]  
> Esta familia de protocolos no se admite en Windows XP.

 

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ipx:[1000]") 
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

[**ncacn \_ en \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 