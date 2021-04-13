---
title: Enlace de cadenas
description: El enlace de cadenas es una cadena de caracteres sin signo formada por cadenas que representan el UUID del objeto de enlace, la secuencia de protocolo RPC, la dirección de red y las opciones de extremo y extremo.
ms.assetid: 5e55ddd0-d71c-42ef-90cc-dd1f0b9ed305
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d804fe614185b054b8041e13069e900501342a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421196"
---
# <a name="string-binding"></a>Enlace de cadenas

El enlace de cadenas es una cadena de caracteres sin signo formada por cadenas que representan el UUID del objeto de enlace, la secuencia de protocolo RPC, la dirección de red y las opciones de extremo y extremo.

*ObjectUUID* @ *ProtocolSequence*:el \[ *punto de conexión* NetworkAddress,*opción*\]

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="ObjectUUID"></span><span id="objectuuid"></span><span id="OBJECTUUID"></span>*ObjectUUID*
</dt> <dd>

[UUID](/windows/desktop/Midl/uuid) del objeto en el que opera la llamada a procedimiento remoto. En el servidor, la biblioteca en tiempo de ejecución de RPC asigna el tipo de objeto a un vector de punto de entrada de administrador (una matriz de punteros de función) para invocar la rutina de administrador correcta. Para obtener una explicación de cómo asignar los UUID de objeto a los vectores de punto de entrada del administrador, consulte [registrar interfaces](registering-interfaces.md).

</dd> <dt>

<span id="ProtocolSequence"></span><span id="protocolsequence"></span><span id="PROTOCOLSEQUENCE"></span>*ProtocolSequence*
</dt> <dd>

Cadena de caracteres que representa una combinación válida de un protocolo RPC (como ncacn), un protocolo de transporte (como TCP) y un protocolo de red (como IP). Microsoft RPC admite los siguientes protocolos especificados en [constantes de secuencia de protocolo](protocol-sequence-constants.md).

</dd> <dt>

<span id="NetworkAddress"></span><span id="networkaddress"></span><span id="NETWORKADDRESS"></span>*NetworkAddress*
</dt> <dd>

Dirección de red del sistema para recibir llamadas a procedimientos remotos.

> [!Note]  
> Las siguientes secuencias de Protocolo no se admiten a partir de Windows XP:

 

-   [\_TCP NB \_ ncacn](/windows/desktop/Midl/ncacn-nb-tcp)
-   [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)
-   [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)
-   [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp)
-   [ncacn \_ redes virtuales \_ spp](/windows/desktop/Midl/ncacn-vns-spp)
-   [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)
-   [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)

El formato y el contenido de la dirección de red dependen de la secuencia de protocolos especificada como se indica a continuación.



| Secuencia de protocolos                       | Dirección de red                                                                                                                                  | Ejemplos                                               |
|-----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_TCP NB \_ ncacn](/windows/desktop/Midl/ncacn-nb-tcp)     | Nombre del equipo                                                                                                                                    | myserver                                               |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | Nombre del equipo                                                                                                                                    | myserver                                               |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | Nombre del equipo                                                                                                                                    | myserver                                               |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Dirección de Internet de cuatro octetos o nombre de host. Si la pila de red IPv6 está instalada, IPv6 es totalmente compatible y también se acepta una dirección IPv6. | 128.10.2.30 anynode.microsoft.com                      |
| [NP de ncacn \_](/windows/desktop/Midl/ncacn-np)              | Nombre del servidor (las dos barras diagonales inversas iniciales son opcionales)                                                                                            | myotherserver de servidor \\ \\                             |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Dirección de Internet IPX o nombre de servidor                                                                                                             | ~ 0000000108002B30612C mi Server                         |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Sintaxis de área y nodo                                                                                                                             | 4,120                                                  |
| [ncacn \_ en \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Nombre del equipo, seguido opcionalmente de @ y el nombre de la zona de AppleTalk. El valor predeterminado es @ \* , la zona del cliente, si no se proporciona ninguna zona.                     | servername@zonename ServerName                         |
| [ncacn \_ redes virtuales \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Nombre del servidor StreetTalk con el formato item@group@organization                                                                                       | printserver@sdkdocs@microsoft                          |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Nombre de servidor                                                                                                                                      | myserver                                               |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Dirección de Internet (con cuatro octetos o nombre descriptivo, o nombre de servidor local)                                                                       | 128.10.2.30 somesvr@anywhere.com mylocalsvr<br/> |
| [ncadg \_ IP \_ UDP](/windows/desktop/Midl/ncadg-ip-udp)     | Dirección de Internet de cuatro octetos, o nombre de host                                                                                                        | 128.10.2.30 anynode.microsoft.com                      |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Dirección de Internet IPX o nombre de servidor                                                                                                             | ~ 0000000108002B30612C mi Server                         |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Nombre de equipo                                                                                                                                     | thismachine                                            |



 

El campo de dirección de red es opcional. Cuando no se especifica una dirección de red, el enlace de cadena hace referencia al host local. Es posible especificar el nombre del equipo local cuando se usa la secuencia del protocolo **ncalrpc** , pero no es necesario hacerlo por completo.

</dd> <dt>

<span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>*Finales*
</dt> <dd>

Extremo, o dirección, del proceso para recibir llamadas a procedimientos remotos. Un punto de conexión puede ir precedido de la palabra clave **Endpoint =**. Especificar el extremo es opcional si el servidor ha registrado sus enlaces con el asignador de extremos. Vea [**RpcEpRegister**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepregister).

El formato y el contenido de un punto de conexión dependen de la secuencia de protocolos especificada, tal como se muestra en la siguiente tabla de extremos/opciones.

</dd> <dt>

<span id="Option"></span><span id="option"></span><span id="OPTION"></span>*Desea*
</dt> <dd>

Opciones específicas del protocolo. El campo de opción no es necesario. Cada opción se especifica mediante un par {nombre, valor} que usa el valor de la opción nombre de la *opción* de sintaxis = . Las opciones se definen para cada secuencia de protocolo, tal y como se muestra en la siguiente tabla de puntos de conexión/opción.



| Secuencia de protocolos                       | Punto de conexión                                                                                           | Ejemplos             | Nombre de la opción                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------|----------------------|--------------------------------------------------------|
| [\_TCP NB \_ ncacn](/windows/desktop/Midl/ncacn-nb-tcp)     | Entero entre 1 y 254. Microsoft reserva muchos valores entre 0 y 32.                 | 100                  | None                                                   |
| [ncacn \_ NB \_ IPX](/windows/desktop/Midl/ncacn-nb-ipx)     | (como arriba)                                                                                         | (como arriba)           | None                                                   |
| [ncacn \_ NB \_ NB](/windows/desktop/Midl/ncacn-nb-nb)       | (como arriba)                                                                                         | (como arriba)           | None                                                   |
| [\_TCP IP \_ ncacn](/windows/desktop/Midl/ncacn-ip-tcp)     | Número de puerto de Internet.                                                                              | 1025                 | None                                                   |
| [NP de ncacn \_](/windows/desktop/Midl/ncacn-np)              | Canalización con nombre. El nombre debe comenzar por " \\ \\ canalización".                                                       | \\\\canalización \\ \\ pipename | Seguridad                                               |
| [ncacn \_ SPX](/windows/desktop/Midl/ncacn-spx)            | Entero entre 1 y 65535.                                                                       | 5000                 | None                                                   |
| [ncacn \_ dnet \_ NSP](/windows/desktop/Midl/ncacn-dnet-nsp) | Número de objeto de la fase IV de DECnet (debe ir precedido del \# carácter) o nombre de objeto.              | MailServer \# 17      | None                                                   |
| [ncacn \_ en \_ DSP](/windows/desktop/Midl/ncacn-at-dsp)     | Una cadena de caracteres de hasta 22 bytes de longitud.                                                           | myservicesendpoint   | None                                                   |
| [ncacn \_ redes virtuales \_ spp](/windows/desktop/Midl/ncacn-vns-spp)   | Número de puerto de Vines SPP entre 250 y 511.                                                         | 500                  | None                                                   |
| [ncadg \_ MQ](/windows/desktop/Midl/ncadg-mq)              | Entero entre 1 y 65535.                                                                       | 5000                 | None                                                   |
| [\_http ncacn](/windows/desktop/Midl/ncacn-http)          | Número de puerto de Internet.                                                                              | 2215                 | Nombres de servidor proxy RPC y HTTP, opción HttpConnection |
| [ncadg \_ IP \_ UDP](/windows/desktop/Midl/ncadg-ip-udp)     | Número de puerto de Internet.                                                                              | 1025                 | None                                                   |
| [ncadg \_ IPX](/windows/desktop/Midl/ncadg-ipx)            | Entero entre 1 y 65535.                                                                       | 5000                 | None                                                   |
| [ncalrpc](/windows/desktop/Midl/ncalrpc)                 | Cadena que especifica el nombre de la aplicación o del servicio. La cadena no puede incluir caracteres de barra diagonal inversa. | mi \_ impresora          | Seguridad                                               |



 

El nombre de la opción **HttpConnectionOption** , admitido para la \_ secuencia del protocolo http ncacn, toma el valor siguiente.



| Nombre de la opción       | Value            |
|-------------------|------------------|
| HttpConnectOption | **UseHttpProxy** |



 

El **HttpConnectionOption** le permite dirigir el comportamiento de RPC al realizar conexiones http. El valor **UseHttpProxy** indica a RPC que enrute su tráfico a través del proxy http en todo momento, incluso cuando el cliente tiene las opciones de Internet establecidas en Internet Explorer para omitir el servidor proxy para las direcciones locales.  Esta opción indica al cliente que se conecte forzosamente al proxy RPC a través del proxy http. Esto acelera el tiempo de establecer una conexión, ya que omite cualquier retraso que busque el servidor RPC directamente antes de usar el proxy HTTP.

Si se usa esta opción **HttpConnectionOption** e Internet Explorer en el cliente no está configurado para usar ese proxy http, pueden producirse errores en las conexiones con **\_ \_ \_ \_ las opciones de red no válidas de RPC**.

``` syntax
HttpConnectOption=UseHttpProxy
```

Para obtener más información acerca de **HttpConnectionOption**, vea [usar http como transporte de RPC](using-http-as-an-rpc-transport.md).

El nombre de la opción de **seguridad** , compatible con las secuencias de protocolo ncalrpc, ncacn \_ NP, ncadg \_ IP \_ UDP y ncadg \_ IPX, toma los siguientes valores de opción.



| Nombre de la opción  | Valor de la opción                                                                               |
|--------------|--------------------------------------------------------------------------------------------|
| **Seguridad** | { \| \| suplantación anónima de identificación} {Dynamic \| static} {**true** \| **false**} |



 

Si se especifica el nombre de la opción de seguridad, también se debe proporcionar una entrada de cada uno de los conjuntos de valores de opciones de seguridad. Los valores de opción deben estar separados por un carácter de espacio único. Por ejemplo, los campos de *Opciones* siguientes son válidos:

``` syntax
Security=identification dynamic true
Security=impersonation static true
```

Los valores de la opción de seguridad tienen los significados siguientes.



| Valor de la opción de seguridad | Descripción                                                                                                                                                                                                                                                                                                                                              |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Anónimas             | El cliente es anónimo para el servidor.                                                                                                                                                                                                                                                                                                                   |
| Dinámica               | Los cambios en la identidad de seguridad del cliente se ven en el servidor cuando el servidor utiliza la seguridad de transporte. Este es el modo predeterminado para la seguridad del nivel de transporte de LRPC (ncalrpc) y para la seguridad de nivel de transporte de canalización con nombre local (ncacn \_ NP).                                                                                                             |
| **False**             | Efectiva = **false**; todos los valores de los privilegios de token, incluidos los establecidos en OFF, se incluyen en el token en el servidor y se pueden habilitar en el servidor. Los privilegios solo son relevantes para las llamadas RPC de la misma máquina.                                                                                                                                     |
| **Identificación**    | El servidor tiene información sobre el cliente pero no puede suplantar.                                                                                                                                                                                                                                                                                      |
| **Suplantación**     | El servidor puede actuar en nombre del cliente en el sistema local (la seguridad de nivel de transporte no admite la delegación).                                                                                                                                                                                                                               |
| **Estática**            | El servidor no detecta los cambios en la identidad de seguridad del cliente cuando el servidor utiliza la seguridad de transporte. Este es el único modo disponible para la seguridad del nivel de transporte de canalización con nombre remoto (ncacn \_ NP). La identidad del llamador se guarda durante la primera llamada a procedimiento remoto en ese identificador de enlace, no en el momento en que se crea el identificador de enlace. |
| **True**              | Efectiva = **true**; en el token del servidor solo se incluyen los valores de privilegios de token establecidos en ON. El servidor no puede activar los privilegios establecidos en OFF si se usa esta opción. Los privilegios solo son relevantes para las llamadas RPC de la misma máquina.                                                                                                         |



 

Para obtener más información sobre las opciones de seguridad, [seguridad](security.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

No se permiten espacios en blanco en los enlaces de cadena excepto cuando lo requiera la sintaxis de la *opción* . La configuración predeterminada de los campos *NetworkAddress*, *Endpoint* y *Option* varía según el valor del miembro *ProtocolSequence* .

En todos los campos de enlace de cadenas, un solo carácter de barra diagonal inversa ( \) se interpreta como un carácter de escape). Para especificar un solo carácter de barra diagonal inversa literal, debe proporcionar dos caracteres de barra diagonal inversa ( \\ \) .

Un enlace de cadena contiene la representación de caracteres de un identificador de enlace y, ocasionalmente, partes de un identificador de enlace. Los enlaces de cadena son útiles para representar partes de un identificador de enlace, pero no se pueden usar para realizar llamadas a procedimientos remotos. Primero se deben convertir en un identificador de enlace mediante una llamada a [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding).

Además, un enlace de cadena no contiene toda la información de un identificador de enlace. Por ejemplo, la información de autenticación, si existe, asociada a un identificador de enlace no se convierte en el enlace de cadena devuelto mediante una llamada a [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding).

Durante el desarrollo de una aplicación distribuida, los servidores pueden comunicar su información de enlace a los clientes mediante enlaces de cadena para establecer una relación cliente-servidor sin usar la base de datos de asignación de puntos de conexión o la base de datos de servicio de nombres. Para establecer este tipo de relación, utilice la función [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding) para convertir uno o varios identificadores de enlace de un vector de control de enlace en un enlace de cadena y proporcione el enlace de cadena al cliente.

## <a name="examples"></a>Ejemplos

A continuación se muestran ejemplos de enlaces de cadena válidos. En estos ejemplos, se usa *obj-UUID* para mayor comodidad a fin de representar un UUID válido en forma de cadena. En lugar de mostrar el UUID 308FB580-1EB2-11CA-923B-08002B1075A7, los ejemplos muestran *obj-UUID*.

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

[Usar HTTP como transporte RPC](using-http-as-an-rpc-transport.md)
</dt> </dl>

 

