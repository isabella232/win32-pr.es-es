---
description: Las extensiones de sockets seguros de Winsock permiten que una aplicación de socket controle la seguridad de su tráfico a través de una red.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensiones de socket seguro de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967223"
---
# <a name="winsock-secure-socket-extensions"></a>Extensiones de socket seguro de Winsock

Las extensiones de sockets seguros de Winsock permiten que una aplicación de socket controle la seguridad de su tráfico a través de una red. Estas extensiones permiten a una aplicación proporcionar directivas de seguridad y requisitos para su tráfico de red, y consultar la configuración de seguridad aplicada. Por ejemplo, una aplicación puede usar estas extensiones para consultar el token de seguridad del mismo nivel que se puede usar para realizar comprobaciones de acceso a nivel de aplicación.

Las extensiones de socket seguro están diseñadas para integrar los servicios proporcionados por IPsec y otros protocolos de seguridad con el marco Winsock. Antes de Windows Vista, en Windows Server 2003 y Windows XP, un administrador ha configurado IPsec a través de directivas locales y de dominio. En Windows Vista, las extensiones de socket seguro permiten a las aplicaciones configurar y controlar total o parcialmente la seguridad de su tráfico de red en el nivel de socket.

Las aplicaciones ya pueden proteger el tráfico de red mediante API públicas, como la administración de IPsec, la plataforma Windows filtrado y la interfaz del proveedor de compatibilidad de seguridad (SSPI). Sin embargo, el uso de estas API puede dificultar el desarrollo de la aplicación y puede dificultar la configuración y la implementación. Las extensiones de sockets seguros de Winsock se han diseñado para simplificar el desarrollo de aplicaciones de red que requieren tráfico de red seguro al permitir que Winsock controle la mayor parte de la complejidad.

Estas extensiones de socket seguro están disponibles en Windows Vista y versiones posteriores.

## <a name="secure-socket-functions"></a>Funciones de socket seguro

Las funciones de extensión de socket seguro son las siguientes:

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Actualmente, las funciones de socket seguro solo admiten el protocolo IPsec y están disponibles en Windows Vista y versiones posteriores.

 

Las estructuras y enumeraciones usadas por las funciones de socket seguro son las siguientes:

-   [**NOMBRE DE \_ DESTINO DEL MISMO NIVEL DE \_ \_ SOCKET**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**PROTOCOLO DE \_ SEGURIDAD DE \_ SOCKET**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**INFORMACIÓN DE \_ CONSULTA DE SEGURIDAD DE \_ \_ SOCKET**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**PLANTILLA DE \_ CONSULTA DE SEGURIDAD DE \_ \_ SOCKET**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**CONFIGURACIÓN \_ DE SEGURIDAD DE \_ SOCKETS**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**CONFIGURACIÓN \_ DE SEGURIDAD DE SOCKET \_ \_ IPSEC**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Las funciones de sockets seguros son fáciles de usar para las aplicaciones normales y son lo suficientemente flexibles para las aplicaciones que necesitan un alto grado de control sobre su seguridad. Estas funciones hacen posible mantener oculto el mecanismo de seguridad subyacente de la aplicación. Una aplicación puede especificar requisitos de seguridad genéricos y permitir que el administrador controle el protocolo de seguridad que se usa para admitir los requisitos. Aunque es posible ampliar estas funciones para agregar otros protocolos de seguridad, actualmente solo IPsec se integra con las funciones de socket seguro.

La [**función WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permite a una aplicación habilitar la seguridad y aplicar la configuración de seguridad antes de establecer una conexión.

La [**función WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permite a una aplicación especificar el nombre de destino correspondiente a una entidad del mismo nivel. El protocolo de seguridad seleccionado usará esta información al autenticar el elemento del mismo nivel. Esta característica aborda las preocupaciones sobre los ataques de confianza de tipo "Man in the middle".

La [**función WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) se usa para eliminar un nombre del mismo nivel especificado previamente para un socket.

Una vez establecida una conexión, la función [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permite a una aplicación consultar las propiedades de seguridad de la conexión, lo que puede incluir el acceso del mismo nivel o el token de acceso al equipo.

Una vez establecida una conexión, la función [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permite a una aplicación suplantar la entidad de seguridad correspondiente a un socket del mismo nivel para realizar la autorización en el nivel de aplicación.

[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permite a una aplicación finalizar la suplantación de un socket del mismo nivel.

## <a name="secure-socket-architecture"></a>Arquitectura de sockets seguros

![arquitectura básica de las extensiones de socket seguro winsock](images/ss-arch.png)

-   Una aplicación llama a las funciones de socket seguro para establecer o consultar la configuración de seguridad de un socket.
-   Las funciones de socket seguro son un conjunto de funciones de extensión con seguridad de tipos que encapsulan las llamadas a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mediante valores recién definidos para el parámetro *dwIoControlCode* disponible en Windows Vista y versiones posteriores. Estos IOCTL se controlan mediante la pila de red.
-   La pila de red dirigirá la llamada a Aplicación de la capa de [aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md) junto con el identificador del punto de conexión. Para las funciones [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)y [**WSASetSocketSecurity,**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) ALE configurará los valores de la aplicación en el punto de conexión local. Para la [**función WSAQuerySocketSecurity,**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) ALE leerá la información solicitada de los puntos de conexión locales y remotos aplicables.
-   En función de los eventos de socket, el cumplimiento de la capa de aplicación (ALE) aplica directivas para la arquitectura de sockets seguros mediante la plataforma Windows filtrado de aplicaciones. Para obtener más información, vea [Acerca de Windows filtrado de](../fwp/about-windows-filtering-platform.md) aplicaciones y aplicación de la capa de aplicación [(ALE).](../fwp/application-layer-enforcement--ale-.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Windows de filtrado](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Ejemplos avanzados de Winsock con extensiones de sockets seguros](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Aplicación de la capa de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuración de IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Funciones de IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Programación segura de Winsock](secure-winsock-programming.md)
</dt> <dt>

[Interfaz del proveedor de compatibilidad con seguridad (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Uso de extensiones de sockets seguros](using-secure-socket-extensions.md)
</dt> <dt>

[Plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Windows Filtrado de funciones de API de plataforma](../fwp/fwp-functions.md)
</dt> </dl>

 

 
