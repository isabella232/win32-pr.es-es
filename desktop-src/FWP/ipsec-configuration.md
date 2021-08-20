---
title: Configuración de IPsec
description: Windows Plataforma de filtrado (WFP) es la plataforma subyacente para Windows Firewall con seguridad avanzada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cf20fc8c95aafe3c387195b02468cec3ce884cc97287adde44a594305ee189
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069024"
---
# <a name="ipsec-configuration"></a>Configuración de IPsec

Windows Plataforma de filtrado (WFP) es la plataforma subyacente para Windows Firewall con seguridad avanzada. WFP se usa para configurar reglas de filtrado de red, que incluyen reglas que rigen la protección del tráfico de red con IPsec. Los desarrolladores de aplicaciones pueden configurar IPsec directamente mediante la API de WFP, con el fin de aprovechar un modelo de filtrado de tráfico de red más granular que el modelo expuesto a través del complemento Microsoft Management Console (MMC) para Windows Firewall con seguridad avanzada.

## <a name="what-is-ipsec"></a>¿Qué es IPsec?

Internet Protocol Security (IPsec) es un conjunto de protocolos de seguridad que se usan para transferir paquetes IP confidencialmente a través de Internet. IPsec es obligatorio para todas las implementaciones de IPv6 y opcional para IPv4.

El tráfico IP protegido tiene dos encabezados IPsec opcionales, que identifican los tipos de protección criptográfica aplicada al paquete IP e incluyen información para lacoding del paquete protegido.

El encabezado Encapsulating Security Payload (ESP) se usa para la privacidad y la protección frente a modificaciones malintencionadas mediante la autenticación y el cifrado opcional. Se puede usar para el tráfico que atraviesa los enrutadores de traducción de direcciones de red (NAT).

El encabezado de autenticación (AH) solo se usa para la protección contra modificaciones malintencionadas mediante la autenticación. No se puede usar para el tráfico que atraviesa los enrutadores NAT.

Para más información sobre IPsec, consulte también:

<dl>

[Referencia técnica de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>¿Qué es IKE?

Internet Key Exchange (IKE) es un protocolo de intercambio de claves que forma parte del conjunto de protocolos IPsec. IKE se usa al configurar una conexión segura y realiza el intercambio seguro de claves secretas y otros parámetros relacionados con la protección sin la intervención del usuario.

Para obtener más información sobre IKE, vea también:

<dl>

[Clave de Internet Exchange](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>¿Qué es AuthIP?

protocolo de Internet autenticado (AuthIP) es un nuevo protocolo de intercambio de claves que expande IKE como se muestra a continuación.

<dl> Aunque IKE solo admite credenciales de autenticación de equipo, AuthIP también admite:

-   Credenciales de usuario: NTLM, Kerberos, certificados.
-   Certificados de mantenimiento de Protección de acceso a redes (NAP).
-   Credencial anónima, que se usa para la autenticación opcional.
-   Combinación de credenciales; por ejemplo, una combinación de credenciales kerberos de máquina y usuario.

  
AuthIP tiene un mecanismo de reintento de autenticación que comprueba todos los métodos de autenticación configurados antes de dar error a la conexión.  
AuthIP se puede usar con sockets seguros para implementar el tráfico protegido por IPsec basado en la aplicación. Proporciona:

-   Autenticación y cifrado por socket. Vea [**WSASetSocketSecurity para**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) obtener más información.
-   Suplantación de cliente. (IPsec suplanta el contexto de seguridad en el que se crea el socket).
-   Validación de nombres del mismo nivel entrantes y salientes. Vea [**WSASetSocketPeerTargetName para**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) obtener más información.

  
</dl>

Para obtener más información sobre AuthIP, consulte también:

<dl>

[AuthIP en Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>¿Qué es una directiva de IPsec?

Una directiva de IPsec es un conjunto de reglas que determinan qué tipo de tráfico IP debe protegerse mediante IPsec y cómo proteger ese tráfico. Solo una directiva IPsec está activa en un equipo a la vez.

Para obtener más información sobre cómo implementar directivas de IPsec, abra el complemento MMC de directiva de seguridad local (secpol.msc), presione F1 para mostrar la Ayuda y, a continuación, seleccione Crear y usar directivas IPsec en la tabla de contenido.

Para más información sobre las directivas de IPsec, consulte también:

<dl>

[Introducción a los conceptos de directivas de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descripción de una directiva de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Cómo usar WFP para configurar directivas de IPsec

La implementación de Microsoft de IPsec usa Windows de filtrado para configurar directivas de IPsec. Las directivas de IPsec se implementan mediante la adición de filtros en varias capas de WFP como se muestra a continuación.

-   En las capas FWPM LAYER IXTXT V{4 6} se agregan filtros que especifican las directivas de negociación que usan los módulos de clave \_ \_ \_ (IKE/AuthIP) durante los intercambios del modo principal \| (MM). Los métodos de autenticación y los algoritmos criptográficos se especifican en estas capas.
-   En las capas FWPM \_ LAYER \_ IPSEC V{4 6} se agregan filtros que especifican las directivas de negociación que usan los módulos de clave durante los intercambios de modo rápido (QM) y modo extendido \_ \| (EM). Los encabezados IPsec (AH/ESP) y los algoritmos criptográficos se especifican en estas capas.

    Una directiva de negociación se especifica como contexto de proveedor de directivas asociado al filtro. El módulo de claves enumera los contextos del proveedor de directivas en función de las características de tráfico y obtiene la directiva que se usará para la negociación de seguridad.

    > [!Note]  
    > La API de WFP se puede usar para especificar las asociaciones de seguridad (AS) directamente y, por tanto, para omitir la directiva de negociación del módulo de claves.

     

-   En las capas FWPM \_ LAYER \_ INBOUND TRANSPORT \_ \_ V{4 \| 6} y FWPM LAYER OUTBOUND \_ TRANSPORT \_ \_ \_ V{4 \| 6} se agregan filtros que invocan llamadas y determinan qué flujo de tráfico se debe proteger.
-   En las capas FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} se agregan filtros que implementan el filtrado de identidades y la directiva por aplicación.

En el diagrama siguiente se muestra la interacción de los distintos componentes de WFP con respecto a la operación de IPsec.![Configuración de ipsec mediante la plataforma de filtrado de Windows](images/ipsec-configuration.jpg)

Una vez configurado IPsec, se integra con WFP y amplía las funcionalidades de filtrado de WFP proporcionando información que se usará como condiciones de filtrado en las capas de autorización de aplicación de cumplimiento de la capa de aplicación (ALE). Por ejemplo, IPsec proporciona el usuario remoto y la identidad de la máquina remota, que WFP expone en las capas de conexión y aceptación de ALE. Esta información se puede usar para la autorización de identidad remota específica mediante una implementación de firewall basada en WFP.

A continuación se muestra una directiva de aislamiento de ejemplo que se puede implementar mediante IPsec:

-   CAPA DE FWPM \_ \_ IXTXT \_ V{4 \| 6} capas: autenticación Kerberos.
-   CAPA FWPM \_ \_ IPSEC \_ V{4 \| 6} capas – AH/SHA-1.
-   FWPM \_ LAYER INBOUND TRANSPORT \_ \_ \_ V{4 \| 6} y FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6} capas: detección de negociación para todo el tráfico de red.
-   FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV ACCEPT \_ \_ V{4 6} layers - IPsec required for all network traffic (RECV ACCEPT V{4 \| 6} layers: IPsec obligatorio para todo el tráfico de red).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Capas de WFP**
</dt> <dt>

[**Filtrar identificadores de capa**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Capas de ALE](ale-layers.md)
</dt> <dt>

**Escenarios de directivas de IPsec implementados mediante la API de WFP:**
</dt> <dt>

[modo de transporte](regular-transport-mode.md)
</dt> <dt>

[Modo de transporte de detección de negociación](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modo de transporte de detección de negociación en modo de límite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Tunnel Modo](tunnel-mode.md)
</dt> <dt>

[Cifrado garantizado](guaranteed-encryption.md)
</dt> <dt>

[Autorización de identidad remota](remote-identity-authorization.md)
</dt> <dt>

[SAs de IPsec manuales](manual-ipsec-sas.md)
</dt> <dt>

[Exenciones de IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluciones de IPsec:**
</dt> <dt>

[Aislamiento de servidor y dominio](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 