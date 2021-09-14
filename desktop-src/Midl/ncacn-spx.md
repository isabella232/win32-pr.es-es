---
title: ncacn_spx atributo
description: La palabra clave ncacn \_ spx identifica SPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.
ms.assetid: 45e93e25-e84d-4242-80b0-c4b61e80f716
keywords:
- ncacn_spx atributo MIDL
topic_type:
- apiref
api_name:
- ncacn_spx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09d27cc746df906ff6b1a3290e41d860c76dc362
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159464"
---
# <a name="ncacn_spx-attribute"></a>Atributo ncacn \_ spx

La **palabra clave ncacn \_ spx** identifica SPX como la familia de protocolos para el punto de conexión. Esta familia de protocolos está obsoleta y no debe usarse en nuevas aplicaciones.

``` syntax
endpoint("ncacn_spx:link-address[port-name]")
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*link-address* 
</dt> <dd>

Especifica el servidor host. Puede ser una cadena de caracteres (el nombre del servidor) o un número hexadecimal de 20 dígitos que consta de la dirección de red del servidor host (8 dígitos) concatenada con la dirección del nodo (12 dígitos). Consulte Comentarios para obtener instrucciones sobre cómo obtener la dirección de red y la dirección del nodo. Una **cadena NULL** especifica el equipo local.

</dd> <dt>

*port-name* 
</dt> <dd>

Especifica un número opcional de 16 bits que representa la dirección del socket. Los valores pueden oscilar entre 1 y 65 535. Cuando no se especifica ningún valor, el servicio de asignación de puntos de conexión selecciona un valor *de nombre de puerto* válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando se usa el **transporte ncacn \_ spx,** el nombre del servidor es exactamente el mismo que el nombre de Windows 32 bits. Sin embargo, dado que los nombres se distribuyen mediante protocolos de Nociones, deben ajustarse a las convenciones de nomenclatura de Nociones. Si un nombre de servidor no es un nombre válido de Noé, los servidores no podrán crear puntos de conexión con el **transporte ncacn \_ spx.** A continuación se muestra una lista parcial de caracteres prohibidos en los nombres de servidor de Byte:

" \* + . / : ; < = > ? \[ \] \\ \|

La versión de NWLink proporcionada con MS Client 3.0 no admite el transporte **ncacn \_ spx.**

Las aplicaciones cliente de Windows de 16 bits que usan el transporte **de \_ spx ncacn** requieren que el archivo Nwipxspx.dll se instale para ejecutarse en el subsistema WOW. Póngase en contacto con Llegar a Para obtener este archivo.

> [!Note]  
> Para obtener las direcciones de red y nodo, use la utilidad de comprobación **comCheck** de Asíns o la API **ipXGetInternetAddress** definida por Cookies. En Windows, también puede obtener estas direcciones con el **comando ipxroute config.**

 

La sintaxis de la cadena de puerto de transporte de SPX, como todas las cadenas de puerto, se define independientemente de la especificación de IDL. El compilador realiza alguna comprobación de sintaxis, pero no garantiza que la especificación del punto de conexión sea correcta. Algunos errores se pueden notifican en tiempo de ejecución en lugar de en tiempo de compilación.

## <a name="examples"></a>Ejemplos

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_spx:[1000]") 
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

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[enlace de cadena](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 