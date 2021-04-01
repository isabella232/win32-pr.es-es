---
description: Las extensiones de sockets seguros para Winsock permiten a una aplicación de socket controlar la seguridad de su tráfico a través de una red.
ms.assetid: 023a9f96-814f-40c3-a186-ae0a0c9baef2
title: Extensiones Winsock Secure Socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b62ee593b3abbb3bb0f8dbf27b79d6868f04fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082110"
---
# <a name="winsock-secure-socket-extensions"></a>Extensiones Winsock Secure Socket

Las extensiones de sockets seguros para Winsock permiten a una aplicación de socket controlar la seguridad de su tráfico a través de una red. Estas extensiones permiten a una aplicación proporcionar los requisitos y la Directiva de seguridad para el tráfico de red y consultar la configuración de seguridad aplicada. Por ejemplo, una aplicación puede utilizar estas extensiones para consultar el token de seguridad del mismo nivel que se puede usar para realizar comprobaciones de acceso de nivel de aplicación.

Las extensiones de sockets seguros están diseñadas para integrar los servicios proporcionados por IPsec y otros protocolos de seguridad con el marco Winsock. Antes de Windows Vista, en Windows Server 2003 y Windows XP, un administrador ha configurado IPsec a través de directivas locales y de dominio. En Windows Vista, las extensiones de sockets seguros permiten a las aplicaciones configurar por completo o parcialmente y controlar la seguridad del tráfico de red en el nivel de socket.

Las aplicaciones ya pueden proteger el tráfico de red mediante el uso de API públicas, como la administración de IPsec, la plataforma de filtrado de Windows y la interfaz del proveedor de compatibilidad para seguridad (SSPI). Sin embargo, el uso de estas API puede dificultar el desarrollo de la aplicación y hacer que sea más difícil de configurar e implementar. Las extensiones Winsock Secure Socket se han diseñado para simplificar el desarrollo de aplicaciones de red que requieran tráfico de red seguro, ya que permiten a Winsock administrar la mayor parte de la complejidad.

Estas extensiones de sockets seguros están disponibles en Windows Vista y versiones posteriores.

## <a name="secure-socket-functions"></a>Funciones de socket seguro

Las funciones de extensión de sockets seguros son las siguientes:

-   [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname)
-   [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer)
-   [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity)
-   [**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation)
-   [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)
-   [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity)

> [!Note]  
> Actualmente, las funciones de socket seguro solo admiten el protocolo IPsec y están disponibles en Windows Vista y versiones posteriores.

 

Las estructuras y enumeraciones utilizadas por las funciones de sockets seguros son las siguientes:

-   [**\_nombre de \_ destino del mismo nivel de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_peer_target_name)
-   [**\_Protocolo de seguridad de socket \_**](/windows/desktop/api/Mstcpip/ne-mstcpip-socket_security_protocol)
-   [**\_información de \_ consulta de seguridad de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_info)
-   [**\_plantilla de \_ consulta de seguridad de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_query_template)
-   [**\_configuración de seguridad de socket \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings)
-   [**configuración de seguridad de SOCKETs \_ \_ \_ IPSec**](/windows/desktop/api/Mstcpip/ns-mstcpip-socket_security_settings_ipsec)

Las funciones de sockets seguros son fáciles de usar para las aplicaciones normales y son lo suficientemente flexibles para las aplicaciones que necesitan un alto grado de control sobre la seguridad. Estas funciones permiten mantener oculto el mecanismo de seguridad subyacente de la aplicación. Una aplicación puede especificar los requisitos de seguridad genéricos y dejar que el administrador controle el protocolo de seguridad que se usa para admitir los requisitos. Aunque es posible extender estas funciones para agregar otros protocolos de seguridad, actualmente solo IPsec se integra con las funciones de socket seguro.

La función [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) permite a una aplicación habilitar la seguridad y aplicar la configuración de seguridad antes de que se establezca una conexión.

La función [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) permite a una aplicación especificar el nombre de destino correspondiente a una entidad del mismo nivel. El protocolo de seguridad seleccionado usará esta información al autenticar al mismo nivel. Esta característica soluciona los problemas de ataques de tipo "Man in the Middle".

La función [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) se usa para eliminar un nombre del mismo nivel especificado previamente para un socket.

Una vez establecida una conexión, la función [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) permite que una aplicación consulte las propiedades de seguridad de la conexión, que pueden incluir el acceso del mismo nivel o el token de acceso al equipo.

Una vez establecida una conexión, la función [**WSAImpersonateSocketPeer**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) permite a una aplicación suplantar la entidad de seguridad correspondiente a un socket del mismo nivel para realizar la autorización en el nivel de la aplicación.

[**WSARevertImpersonation**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) permite a una aplicación finalizar la suplantación de un socket del mismo nivel.

## <a name="secure-socket-architecture"></a>Arquitectura de sockets seguros

![arquitectura básica de las extensiones Winsock Secure Socket](images/ss-arch.png)

-   Una aplicación llama a las funciones de socket seguro para establecer o consultar la configuración de seguridad de un socket.
-   Las funciones de socket seguro son un conjunto de funciones de extensión con seguridad de tipos que encapsulan llamadas a la función [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) con valores recién definidos para el parámetro *DwIoControlCode* disponible en Windows Vista y versiones posteriores. Estos ioctl se controlan por la pila de red.
-   La pila de red dirigirá la llamada a la aplicación de [capa de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md) junto con el identificador de extremo. En el caso de las funciones [**WSADeleteSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname), [**WSASetSocketPeerTargetName**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname)y [**WSASetSocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) , Ale configurará la configuración de la aplicación en el punto de conexión local. En el caso de la función [**WSAQuerySocketSecurity**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) , Ale leerá la información solicitada de los puntos de conexión locales y remotos aplicables.
-   En función de los eventos de socket, el cumplimiento del nivel de aplicación (ALE) aplica directivas para la arquitectura de sockets seguros mediante la plataforma de filtrado de Windows. Para obtener más información, vea [acerca de la plataforma de filtrado de Windows](../fwp/about-windows-filtering-platform.md) y el [cumplimiento del nivel de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la plataforma de filtrado de Windows](../fwp/about-windows-filtering-platform.md)
</dt> <dt>

[Ejemplos avanzados de Winsock con extensiones de socket seguras](advanced-winsock-samples-using-secure-socket-extensions.md)
</dt> <dt>

[Aplicación del nivel de aplicación (ALE)](../fwp/application-layer-enforcement--ale-.md)
</dt> <dt>

[Configuración de IPsec](../fwp/ipsec-configuration.md)
</dt> <dt>

[Funciones de IPsec](../fwp/fwp-ipsec-functions.md)
</dt> <dt>

[Programación de Winsock segura](secure-winsock-programming.md)
</dt> <dt>

[Interfaz del proveedor de compatibilidad con seguridad (SSPI)](../rpc/security-support-provider-interface-sspi-.md)
</dt> <dt>

[Uso de extensiones de socket seguras](using-secure-socket-extensions.md)
</dt> <dt>

[Plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md)
</dt> <dt>

[Funciones de la API de la plataforma de filtrado de Windows](../fwp/fwp-functions.md)
</dt> </dl>

 

 
