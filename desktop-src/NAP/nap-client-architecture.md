---
title: Arquitectura de cliente NAP
description: Un cliente NAP es un equipo que ejecuta Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 que incluye la plataforma NAP.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be876cf7f0cf53c1c3c5885d94c43f45c1f79759d80490a0647d5e7d7678fba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037624"
---
# <a name="nap-client-architecture"></a>Arquitectura de cliente NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Un cliente NAP es un equipo que ejecuta Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 que incluye la plataforma NAP.

En esta ilustración se muestra la arquitectura de la plataforma NAP en un cliente NAP.

![arquitectura de la plataforma nap en un cliente nap](images/nap-client-side-arch.png)

La arquitectura de cliente NAP consta de lo siguiente:

-   Una capa de componentes de Cliente de cumplimiento (EC)

    Cada NAP EC se define para un tipo diferente de acceso a la red. Por ejemplo, hay una NAP EC para la configuración DHCP y una NAP EC para las conexiones VPN de acceso remoto. Nap EC puede coincidir con un tipo específico de punto de cumplimiento de NAP. Por ejemplo, NAP EC de DHCP está diseñado para funcionar con un punto de cumplimiento de NAP basado en DHCP. Algunos ECs de NAP se proporcionan con la plataforma NAP y los proveedores de software de terceros o Microsoft pueden proporcionar otros.

-   Una capa de componentes del Agente de mantenimiento del sistema (SHA)

    Un componente SHA mantiene e informa de uno o varios elementos del estado del sistema. Por ejemplo, podría haber un SHA para las firmas antivirus y un SHA para las actualizaciones del sistema operativo. Un SHA puede coincidir con un servidor de corrección, que es un equipo que contiene recursos de actualización de estado a los que los clientes NAP pueden acceder para corregir su estado no conforme. Por ejemplo, un SHA para comprobar las firmas antivirus coincide con el servidor que contiene el archivo de firma antivirus más reciente. Las SHA no tienen que tener un servidor de corrección correspondiente. Por ejemplo, un SHA puede comprobar la configuración del sistema local para asegurarse de que un firewall basado en host está habilitado. Windows Vista y Windows XP Service Pack 3 incluyen Seguridad de Windows Health Agent (WSHA) que supervisa la configuración del centro de Seguridad de Windows. Los proveedores de software de terceros o Microsoft pueden proporcionar SHA adicionales a la plataforma NAP.

-   Agente NAP

    Mantiene la información de estado de mantenimiento actual del cliente NAP y facilita la comunicación entre las capas NAP EC y SHA. El agente NAP se proporciona con la plataforma NAP.

-   API del agente de estado del sistema

    Proporciona un conjunto de funciones que permiten a los SHA registrarse con el agente NAP, indicar el estado de mantenimiento del sistema, responder a las consultas del estado de mantenimiento del sistema del agente NAP y para que el Agente NAP pase información de corrección de estado del sistema a un SHA. La API de SHA permite a los proveedores crear e instalar SHA adicionales. La API de SHA se proporciona con la plataforma NAP. Vea las siguientes interfaces nap: [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)e [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md).

Para indicar el estado de mantenimiento de un SHA específico, un SHA crea una instrucción de mantenimiento [**(SoH)**](/windows/win32/api/naptypes/ns-naptypes-soh)y la pasa al agente NAP. Un SoH puede contener uno o varios elementos del estado del sistema. Por ejemplo, sha para un programa antivirus puede crear un SoH que contenga el estado del software antivirus que se ejecuta en el equipo, su versión y la última actualización de firma antivirus recibida. Cada vez que un SHA actualiza su estado, crea un nuevo SoH y lo pasa al agente NAP. Para indicar el estado de mantenimiento general de un cliente NAP, el agente NAP usa una declaración de estado del sistema (SSoH), que incluye información de versión para el cliente NAP y el conjunto de soHs para las SHA instaladas.

En las secciones siguientes se describen los componentes de la arquitectura de cliente NAP con más detalle.

## <a name="nap-enforcement-client"></a>Cliente de cumplimiento de NAP

Un cliente de cumplimiento nap (EC) solicita algún nivel de acceso a una red, pasa el estado de mantenimiento del equipo a un punto de cumplimiento nap que proporciona el acceso a la red. Los puntos de cumplimiento de NAP son equipos o dispositivos de acceso a la red que usan NAP o se pueden usar con NAP para requerir la evaluación del estado de mantenimiento de un cliente NAP y proporcionar acceso o comunicación de red restringidos. Si el estado del equipo no es compatible, NAP EC indica el estado restringido del cliente NAP a otros componentes de la arquitectura de cliente NAP.

Los ECs de NAP para la plataforma NAP proporcionados en Windows XP con SP3, Windows Vista y Windows Server 2008 son los siguientes:

-   Una EC de NAP de IPsec para comunicaciones protegidas por IPsec.
-   Una EC DE NAP de EAPHost para conexiones autenticadas por 802.1X.
-   Una VPN NAP EC para conexiones VPN de acceso remoto.
-   Una EC NAP de DHCP para la configuración de direcciones IPv4 basadas en DHCP.
-   Nap EC de puerta de enlace de TS para conexiones de puerta de enlace de TS.

Para Windows XP con SP3, hay TARJETAS NAP independientes para conexiones cableadas e inalámbricas autenticadas con 802.1X.

### <a name="ipsec-nap-ec"></a>IPsec NAP EC

IPsec NAP EC es un componente que obtiene el SSoH del agente NAP y lo envía a una entidad de registro de estado (HRA), un equipo que ejecuta Windows Server 2008 y Internet Information Services (IIS) que obtiene certificados de mantenimiento de una entidad de certificación (CA) para equipos compatibles. La EC de NAP de IPsec se conoce como EC del usuario de confianza de IPsec en el complemento Configuración de cliente nap. Nap EC de IPsec también interactúa con lo siguiente:

-   Almacén de certificados para almacenar el certificado de mantenimiento.
-   Los componentes IPsec de Windows para asegurarse de que el certificado de mantenimiento se usa para la comunicación protegida con IPsec.
-   El firewall basado en host (por ejemplo, Windows firewall) para que el firewall permita el tráfico protegido por IPsec.

### <a name="eaphost-nap-ec"></a>EAPHost NAP EC

EAPHost NAP EC es un componente que obtiene el SSoH del agente NAP y lo envía como un mensaje PEAP-Type-Length-Value (TLV) para las conexiones autenticadas por 802.1X. EAPHost NAP EC se conoce como EAP Quarantine EC en el complemento Configuración de cliente NAP.

### <a name="vpn-nap-ec"></a>VPN NAP EC

VPN NAP EC es una funcionalidad del servicio Connection Manager de acceso remoto que obtiene el SSoH del agente NAP y lo envía como un mensaje PEAP-TLV para las conexiones VPN de acceso remoto. La VPN NAP EC se conoce como la EC de cuarentena de acceso remoto en el complemento Configuración de cliente NAP.

### <a name="dhcp-nap-ec"></a>DHCP NAP EC

NAP EC de DHCP es una funcionalidad del servicio cliente DHCP que usa mensajes DHCP estándar del sector para intercambiar mensajes de estado del sistema e información de acceso de red limitada. La EC DHCP de IPsec se conoce como DHCP Quarantine EC en el complemento Configuración de cliente NAP. LA EC DE NAP DE DHCP obtiene el SSoH del agente NAP. El servicio cliente DHCP fragmenta el SSoH, si es necesario, y coloca cada fragmento en una opción DHCP específica del proveedor de Microsoft que se envía en los mensajes DHCPDiscover, DHCPRequest o DHCPInform. Los mensajes DHCPDecline y DHCPRelease no contienen el SSoH.

## <a name="system-health-agent"></a>Agente de mantenimiento del sistema

Un agente de mantenimiento del sistema (SHA) realiza actualizaciones de estado del sistema y publica su estado en forma de SoH para el agente NAP. El SoH contiene información que el servidor de directivas de mantenimiento nap puede usar para comprobar que el equipo cliente está en el estado de mantenimiento necesario. Un SHA coincide con un validador de estado del sistema (SHV) en el lado servidor de la arquitectura de la plataforma NAP. La SHV correspondiente puede devolver una respuesta SoH (SoHR) al cliente NAP, que pasa la EC de NAP y el agente NAP al SHA, informándose de lo que debe hacer si sha no se encuentra en un estado de mantenimiento necesario. Por ejemplo, el SoHR enviado por una SHV antivirus podría indicar al antivirus SHA correspondiente que consulte un servidor de firmas antivirus para obtener la versión más reciente del archivo de firma antivirus. El SoHR también puede incluir el nombre o la dirección IP del servidor de firma antivirus que se consulta.

Un SHA puede usar un cliente de directiva instalado localmente para ayudar en las funciones de administración de estado del sistema junto con un servidor de directivas. Por ejemplo, una actualización de software SHA puede usar el software cliente de software instalado localmente (el cliente de directiva) para realizar la comprobación de versiones y las funciones de instalación y actualización con el servidor de actualización de software (el servidor de directivas).

## <a name="nap-agent"></a>Agente NAP

El agente NAP proporciona los siguientes servicios:

-   Recopila los soH de cada SHA y los almacena en caché. La memoria caché de SoH se actualiza cada vez que sha proporciona un SoH nuevo o actualizado.
-   Almacena el SSoH y lo proporciona a los ECs de NAP a petición.
-   Pasa notificaciones a las SHA cuando cambia el estado restringido.
-   Mantiene el estado restringido del sistema y recopila información de estado de cada SHA.
-   Pasa soHR al SHA adecuado.

 

 




