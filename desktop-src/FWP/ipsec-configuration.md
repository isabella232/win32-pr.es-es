---
title: Configuración de IPsec
description: La plataforma de filtrado de Windows (WFP) es la plataforma subyacente para Firewall de Windows con seguridad avanzada.
ms.assetid: d54b5caa-daea-4231-9909-7a8d388df661
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af8e3d0a23713c0505082555fe260bc562dfa4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995197"
---
# <a name="ipsec-configuration"></a>Configuración de IPsec

La plataforma de filtrado de Windows (WFP) es la plataforma subyacente para Firewall de Windows con seguridad avanzada. WFP se usa para configurar reglas de filtrado de red, que incluyen reglas que rigen la protección del tráfico de red con IPsec. Los desarrolladores de aplicaciones pueden configurar IPsec directamente mediante la API de WFP, con el fin de aprovechar un modelo de filtrado de tráfico de red más granular que el modelo expuesto a través del complemento Microsoft Management Console (MMC) para Firewall de Windows con seguridad avanzada.

## <a name="what-is-ipsec"></a>Qué es IPsec

El protocolo de seguridad de Internet (IPsec) es un conjunto de protocolos de seguridad que se usan para transferir paquetes IP de forma confidencial a través de Internet. IPsec es obligatorio para todas las implementaciones de IPv6 y opcional para IPv4.

El tráfico IP protegido tiene dos encabezados IPsec opcionales, que identifican los tipos de protección criptográfica aplicadas al paquete IP e incluyen información para descodificar el paquete protegido.

El encabezado de carga de seguridad encapsuladora (ESP) se usa para la privacidad y la protección frente a modificaciones malintencionadas mediante la autenticación y el cifrado opcional. Se puede usar para el tráfico que atraviesa los enrutadores de traducción de direcciones de red (NAT).

El encabezado de autenticación (AH) solo se usa para la protección contra modificaciones malintencionadas mediante la autenticación de. No se puede usar para el tráfico que atraviesa los enrutadores NAT.

Para obtener más información acerca de IPsec, vea también:

<dl>

[Referencia técnica de IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc740240(v=ws.10))  
</dl>

## <a name="what-is-ike"></a>Qué es IKE

Intercambio de claves por red (IKE) es un protocolo de intercambio de claves que forma parte del conjunto de protocolos IPsec. IKE se usa al configurar una conexión segura y realiza el intercambio seguro de claves secretas y otros parámetros relacionados con la protección sin la intervención del usuario.

Para obtener más información sobre IKE, vea también:

<dl>

[Intercambio de claves por red](/previous-versions/windows/it-pro/windows-server-2003/cc784994(v=ws.10))  
</dl>

## <a name="what-is-authip"></a>Qué es AuthIP

Protocolo de Internet autenticado (AuthIP) es un nuevo protocolo de intercambio de claves que expande IKE como se indica a continuación.

<dl> Aunque IKE solo es compatible con las credenciales de autenticación de equipo, AuthIP también admite:

-   Credenciales de usuario: NTLM, Kerberos, certificados.
-   Certificados de mantenimiento de protección de acceso a redes (NAP).
-   Credencial anónima, que se usa para la autenticación opcional.
-   Combinación de credenciales; por ejemplo, una combinación de credenciales de Kerberos de equipo y de usuario.

  
AuthIP tiene un mecanismo de reintento de autenticación que comprueba todos los métodos de autenticación configurados antes de que se produzca un error en la conexión.  
AuthIP se puede usar con sockets seguros para implementar el tráfico protegido por IPsec basado en la aplicación. Proporciona:

-   Cifrado y autenticación por Socket. Vea [**WSASetSocketSecurity**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) para obtener más información.
-   Suplantación del cliente. (IPsec suplanta el contexto de seguridad en el que se crea el socket).
-   Validación del nombre del mismo nivel entrante y saliente. Vea [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) para obtener más información.

  
</dl>

Para obtener más información sobre AuthIP, vea también:

<dl>

[AuthIP en Windows Vista](https://www.microsoft.com/technet/community/columns/cableguy/cg0806.mspx)  
</dl>

## <a name="what-is-an-ipsec-policy"></a>Qué es una directiva de IPsec

Una directiva IPsec es un conjunto de reglas que determinan el tipo de tráfico IP que debe protegerse mediante IPsec y cómo proteger ese tráfico. Solo una directiva IPsec está activa en un equipo al mismo tiempo.

Para obtener más información acerca de la implementación de directivas IPsec, abra el complemento de MMC Directiva de seguridad local (SECPOL. msc), presione F1 para mostrar la ayuda y, a continuación, seleccione crear y usar directivas IPsec en la tabla de contenido.

Para obtener más información sobre las directivas IPsec, vea también:

<dl>

[Información general sobre los conceptos de la directiva IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))  
[Descripción de una directiva IPsec](/previous-versions/windows/it-pro/windows-server-2003/cc781593(v=ws.10))  
</dl>

## <a name="how-to-use-wfp-to-configure-ipsec-policies"></a>Cómo usar WFP para configurar directivas IPsec

La implementación de Microsoft de IPsec usa la plataforma de filtrado de Windows para configurar las directivas de IPsec. Las directivas IPsec se implementan agregando filtros en varias capas de WFP como se indica a continuación.

-   En las capas de la \_ capa FWPM \_ IKEEXT \_ V {4 \| 6}, agregue filtros que especifiquen las directivas de negociación usadas por los módulos de claves (IKE/AuthIP) durante los intercambios del modo principal (mm). Los métodos de autenticación y los algoritmos criptográficos se especifican en estas capas.
-   En la capa de FWPM, las \_ \_ capas de IPSec \_ V {4 \| 6} agregan filtros que especifican las directivas de negociación utilizadas por los módulos de creación de claves durante el modo rápido (QM) y los intercambios de modo extendido (EM). Los encabezados IPsec (AH/ESP) y los algoritmos criptográficos se especifican en estas capas.

    Una directiva de negociación se especifica como un contexto de proveedor de directivas asociado al filtro. El módulo de creación de claves enumera los contextos del proveedor de directivas en función de las características del tráfico y obtiene la Directiva que se va a utilizar para la negociación de seguridad.

    > [!Note]  
    > La API de WFP se puede usar para especificar directamente las asociaciones de seguridad (SAs) y, por lo tanto, para omitir la Directiva de negociación del módulo de creación de claves.

     

-   En el nivel de FWPM de \_ \_ transporte de entrada \_ \_ v {4 \| 6} y el transporte de nivel FWPM de \_ salida de capa \_ \_ \_ v {4 \| 6} capas, agregue filtros que invoquen llamadas y determine qué flujo de tráfico debe protegerse.
-   En la capa de FWPM, la recepción de la \_ solicitud de aceptación de autenticación de \_ Ale \_ \_ \_ \_ V {4 \| 6} capas agrega filtros que implementan el filtrado de identidades y la Directiva por aplicación.

En el diagrama siguiente se muestra la interacción de los distintos componentes de WFP, con respecto a la operación de IPsec.![configuración de IPsec con la plataforma de filtrado de Windows](images/ipsec-configuration.jpg)

Una vez que se configura IPsec, se integra con WFP y extiende las capacidades de filtrado de WFP proporcionando la información que se va a usar como condiciones de filtrado en los niveles de autorización de cumplimiento del nivel de aplicación (ALE). Por ejemplo, IPsec proporciona el usuario remoto y la identidad de la máquina remota, que WFP expone en los niveles de autorización de conexión y aceptación de ALE. Esta información se puede usar para la autorización de identidad remota específica mediante una implementación de Firewall basada en WFP.

A continuación se muestra una directiva de aislamiento de ejemplo que se puede implementar mediante IPsec:

-   FWPM de nivel de la capa de la versión de reversión \_ \_ \_ V {4 \| 6}: autenticación Kerberos.
-   \_Nivel \_ de FWPM IPSec \_ V {4 \| 6} capas: Ah/SHA-1.
-   \_Transporte de \_ entrada de capa FWPM \_ \_ v {4 \| 6} y \_ \_ transporte de salida de capa FWPM \_ \_ v {4 \| 6} capas: detección de negociación para todo el tráfico de red.
-   \_La recepción de la auth de Ale de la capa FWPM \_ \_ \_ \_ acepta \_ V {4 \| 6} niveles: IPSec necesario para todo el tráfico de red.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Capas de WFP**
</dt> <dt>

[**Filtrado de identificadores de capas**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[Niveles ALE](ale-layers.md)
</dt> <dt>

**Escenarios de directivas IPsec implementados mediante la API de WFP:**
</dt> <dt>

[modo de transporte](regular-transport-mode.md)
</dt> <dt>

[Modo de transporte de detección de negociación](negotiation-discovery-transport-mode.md)
</dt> <dt>

[Modo de transporte de detección de negociación en modo de límite](negotiation-discovery-transport-mode-in-boundary-mode.md)
</dt> <dt>

[Modo de túnel](tunnel-mode.md)
</dt> <dt>

[Cifrado garantizado](guaranteed-encryption.md)
</dt> <dt>

[Autorización de identidad remota](remote-identity-authorization.md)
</dt> <dt>

[SAs de IPsec manual](manual-ipsec-sas.md)
</dt> <dt>

[Exenciones de IKE/AuthIP](ike-exemptions.md)
</dt> <dt>

**Soluciones IPsec:**
</dt> <dt>

[Aislamiento de servidor y dominio](/previous-versions/windows/it-pro/windows-server-2003/cc776080(v=ws.10))
</dt> </dl>

 

 