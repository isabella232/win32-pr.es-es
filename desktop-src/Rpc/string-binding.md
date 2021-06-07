---
title: Enlace de cadena
description: El enlace de cadena es una cadena de caracteres sin signo compuesta de cadenas que representan el UUID del objeto de enlace, la secuencia del protocolo RPC, la dirección de red y las opciones de punto de conexión y punto de conexión.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b3f925c03c85be3c47ab174a85f31e72e40d828
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386984"
---
# <a name="string-binding"></a>Enlace de cadena

El enlace de cadena es una cadena de caracteres sin signo compuesta de cadenas que representan el UUID del objeto de enlace, la secuencia del protocolo RPC, la dirección de red y las opciones de punto de conexión y punto de conexión.

*ObjectUUID* @ *ProtocolSequence:**Punto de conexión de NetworkAddress*, \[ *opción*\]

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID del](/windows/desktop/Midl/uuid) objeto operado por la llamada a procedimiento remoto. En el servidor, la biblioteca rpc en tiempo de ejecución asigna el tipo de objeto a un vector de punto de entrada de administrador (una matriz de punteros de función) para invocar la rutina de administrador correcta. Para obtener una explicación sobre cómo asignar UUD de objeto a vectores de punto de entrada de administrador, vea [Registrar interfaces](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Cadena de caracteres que representa una combinación válida de un protocolo RPC (como ncacn), un protocolo de transporte (como TCP) y un protocolo de red (como IP). Rpc de Microsoft admite los siguientes protocolos especificados en [Constantes de secuencia de protocolos](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Dirección de red del sistema para recibir llamadas a procedimiento remoto.

> [!Note]  
> Las siguientes secuencias de protocolo no se admiten desde Windows XP:

 

-   [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)

El formato y el contenido de la dirección de red dependen de la secuencia de protocolo especificada como se indica a continuación.



| Secuencia de protocolo                       | Dirección de red                                                                                                                                  | Ejemplos                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Nombre del equipo                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | Nombre del equipo                                                                                                                                    | Myserver                                               |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | Nombre del equipo                                                                                                                                    | Myserver                                               |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Dirección de Internet de cuatro octetos o nombre de host. Si la pila de red IPv6 está instalada, IPv6 es totalmente compatible y también se acepta una dirección IPv6. | 128.10.2.30 anynode.microsoft.com                      |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Nombre del servidor (las barras diagonales inversas dobles iniciales son opcionales)                                                                                            | myserver \\ \\ myotherserver                             |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Dirección ipx de Internet o nombre del servidor                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintaxis de área y nodo                                                                                                                             | 4.120                                                  |
| [ncacn \_ en \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Nombre del equipo, seguido opcionalmente de @ y el nombre de zona de AppleTalk. El valor predeterminado es @ \* , la zona del cliente, si no se proporciona ninguna zona.                     | servername@zonename Nombredeservidor                         |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nombre del servidor de StreetTalk del formulario item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Nombre del servidor                                                                                                                                      | Myserver                                               |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Dirección de Internet (nombre descriptivo o de cuatro octetos o nombre de servidor local)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Dirección de Internet de cuatro octetos o nombre de host                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Dirección ipx de Internet o nombre del servidor                                                                                                             | ~0000000108002B30612C myserver                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nombre de equipo                                                                                                                                     | thismachine                                            |



 

El campo de dirección de red es opcional. Cuando no se especifica una dirección de red, el enlace de cadena hace referencia al host local. Es posible especificar el nombre del equipo local cuando se usa la secuencia de protocolo **ncalrpc,** pero no es necesario hacerlo.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Extremo*
</dt> <dd>

Punto de conexión, o dirección, del proceso para recibir llamadas a procedimiento remoto. Un punto de conexión puede ir precedido de la palabra clave **endpoint=**. Especificar el punto de conexión es opcional si el servidor ha registrado sus enlaces con el asignador de puntos de conexión. Vea [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

El formato y el contenido de un punto de conexión dependen de la secuencia de protocolo especificada, como se muestra en la siguiente tabla endpoint/option.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Opción*
</dt> <dd>

Opciones específicas del protocolo. El campo de opción no es obligatorio. Cada opción se especifica mediante un par {name, value} que usa el valor de opción de *nombre de opción* de = *sintaxis*. Las opciones se definen para cada secuencia de protocolo, como se muestra en la tabla Endpoint/Option siguiente.



| Secuencia de protocolo                       | Punto de conexión                                                                                           | Ejemplos             | Nombre de la opción                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [ncacn \_ nb \_ tcp](/windows/desktop/Midl/ncacn-nb-tcp)     | Entero entre 1 y 254. Microsoft reserva muchos valores entre 0 y 32.                 | 100                  | Ninguno                                                   |
| [ncacn \_ nb \_ ipx](/windows/desktop/Midl/ncacn-nb-ipx)     | (como se mencionó anteriormente)                                                                                         | (como se mencionó anteriormente)           | Ninguno                                                   |
| [ncacn \_ nb \_ nb](/windows/desktop/Midl/ncacn-nb-nb)       | (como se mencionó anteriormente)                                                                                         | (como se mencionó anteriormente)           | Ninguno                                                   |
| [ncacn \_ ip \_ tcp](/windows/desktop/Midl/ncacn-ip-tcp)     | Número de puerto de Internet.                                                                              | 1025                 | Ninguno                                                   |
| [ncacn \_ np](/windows/desktop/Midl/ncacn-np)              | Canalización con nombre. El nombre debe comenzar por \\ \\ "pipe".                                                       | \\\\pipe \\ \\ pipename | Seguridad                                               |
| [ncacn \_ spx](/windows/desktop/Midl/ncacn-spx)            | Entero entre 1 y 65535.                                                                       | 5000                 | Ninguno                                                   |
| [ncacn \_ dnet \_ nsp](/windows/desktop/Midl/ncacn-dnet-nsp) | Número de objeto de la fase IV de DECnet (debe ir precedido del \# carácter) o el nombre del objeto.              | mailserver \# 17      | Ninguno                                                   |
| [ncacn \_ en \_ dsp](/windows/desktop/Midl/ncacn-at-dsp)     | Cadena de caracteres de hasta 22 bytes.                                                           | myservicesendpoint   | Ninguno                                                   |
| [ncacn \_ vns \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Número de puerto de SPP de Sepp entre 250 y 511.                                                         | 500                  | Ninguno                                                   |
| [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq)              | Entero entre 1 y 65535.                                                                       | 5000                 | Ninguno                                                   |
| [ncacn \_ http](/windows/desktop/Midl/ncacn-http)          | Número de puerto de Internet.                                                                              | 2215                 | Nombres de servidor proxy HTTP y RPC, opción HttpConnection |
| [ncadg \_ ip \_ udp](/windows/desktop/Midl/ncadg-ip-udp)     | Número de puerto de Internet.                                                                              | 1025                 | Ninguno                                                   |
| [ncadg \_ ipx](/windows/desktop/Midl/ncadg-ipx)            | Entero entre 1 y 65535.                                                                       | 5000                 | Ninguno                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Cadena que especifica el nombre de la aplicación o del servicio. La cadena no puede incluir caracteres de barra diagonal inversa. | mi \_ impresora          | Seguridad                                               |



 

El **nombre de la opción HttpConnectionOption,** compatible con la secuencia del protocolo http ncacn, toma el valor \_ siguiente.



| Nombre de la opción       | Valor            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

**HttpConnectionOption permite** dirigir el comportamiento de RPC al realizar conexiones HTTP. El **valor UseHttpProxy** indica a RPC que enruta su tráfico a través del proxy HTTP en todo momento, incluso cuando el cliente tiene las opciones de Internet establecidas en Internet Explorer en Omitir servidor proxy para direcciones locales.  Esta opción dirige al cliente a conectarse de forma forzar al proxy RPC a través del proxy HTTP. Esto acelera el tiempo para establecer una conexión, ya que omite cualquier retraso en la búsqueda del servidor RPC directamente antes de usar el proxy HTTP.

Si se usa esta opción **HttpConnectionOption** y Internet Explorer en el cliente no está configurado para usar ese proxy HTTP, las conexiones pueden producir un error con **RPC S INVALID NETWORK \_ \_ \_ \_ OPTIONS**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Para obtener más información sobre **HttpConnectionOption**, vea [Using HTTP as an RPC Transport](using-http-as-an-rpc-transport.md).

El **nombre** de la opción Seguridad, compatible con las secuencias de protocolo ncalrpc, ncacn \_ np, ncadg ip udp y \_ \_ ncadg ipx, toma los siguientes valores de \_ opción.



| Nombre de la opción  | Valor de la opción                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Seguridad** | \|{suplantación \| anónima de identificación} {dynamic \| static} {**true** \| **false**} |



 

Si se especifica el nombre de la opción de seguridad, también se debe proporcionar una entrada de cada uno de los conjuntos de valores de opción de seguridad. Los valores de opción deben estar separados por un carácter de un solo espacio. Por ejemplo, los siguientes *campos De* opción son válidos:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Los valores de la opción de seguridad tienen los significados siguientes.



| Valor de opción de seguridad | Descripción                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anónimo             | El cliente es anónimo para el servidor.                                                                                                                                                                                                                                                                                                                   |
| Dinámica               | El servidor ve los cambios en la identidad de seguridad del cliente cuando el servidor usa la seguridad de transporte. Este es el modo predeterminado para la seguridad del nivel de transporte LRPC (ncalrpc) y para la seguridad de nivel de transporte de canalización con nombre local (ncacn \_ np).                                                                                                             |
| **False**             | Effective = **FALSE**; todas las configuraciones de privilegios de token, incluidas las establecidas en OFF, se incluyen en el token en el servidor y el servidor puede habilitarla. Los privilegios solo son relevantes para las llamadas RPC de la misma máquina.                                                                                                                                     |
| **Identificación**    | El servidor tiene información sobre el cliente, pero no puede suplantar.                                                                                                                                                                                                                                                                                      |
| **Suplantación**     | El servidor puede actuar en nombre del cliente dentro del sistema local (la seguridad de nivel de transporte no admite la delegación).                                                                                                                                                                                                                               |
| **Estática**            | El servidor no ve los cambios en la identidad de seguridad del cliente cuando el servidor usa la seguridad de transporte. Este es el único modo disponible para la seguridad de nivel de transporte de canalización con nombre remoto (ncacn \_ np). La identidad del autor de la llamada se guarda durante la primera llamada a procedimiento remoto en ese identificador de enlace, no en el momento en que se crea el identificador de enlace. |
| **True**              | Effective = **TRUE**; solo la configuración de privilegios de token establecida en ON se incluye en el token en el servidor. El servidor no puede desactivar los privilegios establecidos en OFF si se usa esta opción. Los privilegios solo son relevantes para las llamadas RPC de la misma máquina.                                                                                                         |



 

Para obtener más información sobre las opciones de seguridad, [consulte Seguridad.](security.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

No se permite el espacio en blanco en los enlaces de cadena, excepto cuando lo requiera la sintaxis *Option.* La configuración predeterminada de los *campos NetworkAddress*, *Endpoint* y *Option* varía según el valor del *miembro ProtocolSequence.*

Para todos los campos de enlace de cadenas, un solo carácter de barra diagonal inversa ( \\ ) se interpreta como un carácter de escape. Para especificar un único carácter de barra diagonal inversa literal, debe proporcionar dos caracteres de barra diagonal inversa ( \\ \\ ).

Un enlace de cadena contiene la representación de caracteres de un identificador de enlace y, en ocasiones, partes de un identificador de enlace. Los enlaces de cadena son cómodos para representar partes de un identificador de enlace, pero no se pueden usar para realizar llamadas a procedimientos remotos. Primero se deben convertir en un identificador de enlace mediante una llamada a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Además, un enlace de cadena no contiene toda la información de un identificador de enlace. Por ejemplo, la información de autenticación, si existe, asociada a un identificador de enlace no se traduce en el enlace de cadena devuelto mediante una llamada a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Durante el desarrollo de una aplicación distribuida, los servidores pueden comunicar su información de enlace a los clientes mediante enlaces de cadena para establecer una relación cliente-servidor sin usar la base de datos de asignación de puntos de conexión o la base de datos de servicio de nombres. Para establecer esta relación, use la función [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) para convertir uno o varios identificadores de enlace de un vector de identificador de enlace en un enlace de cadena y proporcione el enlace de cadena al cliente.

## <a name="examples"></a>Ejemplos

A continuación se muestran ejemplos de enlaces de cadena válidos. En estos ejemplos, *obj-uuid* se usa por comodidad para representar un UUID válido en forma de cadena. En lugar de mostrar el UUID 308FB580-1EB2-11CA-923B-08002B1075A7, los ejemplos muestran *obj-uuid*.

``` syntax
obj-uuid@ncadg_mq:mymqserver
obj-uuid@ncacn_http:major7.microsoft.com[2225]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80]
obj_uuid@ncacn_http:major7.microsoft.com[,HttpProxy=proxysvr:80,
    RpcProxy=websvr1.microsoft.com:80,HttpConnectOption=UseHttpProxy]
obj-uuid@ncacn_ip_tcp:16.20.16.27[2001]
obj-uuid@ncacn_ip_tcp:16.20.16.27[endpoint=2001]
obj-uuid@ncacn_nb_nb:
obj-uuid@ncacn_nb_nb:[100]
obj-uuid@ncacn_np:
obj-uuid@ncacn_np:[\\pipe\\p3,Security=impersonation static true]
obj-uuid@ncacn_np:\\\\marketing[\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\marketing[endpoint=\\pipe\\p2\\p3\\p4]
obj-uuid@ncacn_np:\\\\sales
obj-uuid@ncacn_np:\\\\sales[\\pipe\\p1,Security=identification dynamic true]
obj-uuid@ncalrpc:
obj-uuid@ncalrpc:[object1_name_demonstrating_that_these_can_be_lengthy]
obj-uuid@ncalrpc:[object2_name,Security=anonymous static true]
obj-uuid@ncacn_vns_spp:server@group@org[500]
obj-uuid@ncacn_dnet_nsp:took[elf_server]
obj-uuid@ncacn_dnet_nsp:took[endpoint=elf_server]
obj-uuid@ncadg_ip_udp:128.10.2.30
obj-uuid@ncadg_ip_udp:maryos.microsoft.com[1025]
obj-uuid@ncadg_ipx: ~0000000108002B30612C[5000]
obj-uuid@ncadg_ipx:printserver
obj-uuid@ncacn_spx:annaw[4390]
obj-uuid@ncacn_spx:~0000000108002B30612C
```

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding)
</dt> <dt>

[**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding)
</dt> <dt>

[**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister)
</dt> <dt>

[Uso de HTTP como transporte RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

