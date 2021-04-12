---
title: Arquitectura de cliente de NAP
description: Un cliente NAP es un equipo que ejecuta Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 que incluye la plataforma NAP.
ms.assetid: 163c33c9-b18b-49f9-a2a1-fd90a1dc0826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15862eaa6ae4f4c1f79c53cf9d540aedec295e8a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357578"
---
# <a name="nap-client-architecture"></a>Arquitectura de cliente de NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Un cliente NAP es un equipo que ejecuta Windows XP con Service Pack 3 (SP3), Windows Vista o Windows Server 2008 que incluye la plataforma NAP.

En esta ilustración se muestra la arquitectura de la plataforma NAP en un cliente NAP.

![arquitectura de la plataforma NAP en un cliente NAP](images/nap-client-side-arch.png)

La arquitectura de cliente de NAP consta de lo siguiente:

-   Una capa de componentes de cliente de cumplimiento (EC)

    Cada NAP EC se define para un tipo de acceso de red diferente. Por ejemplo, hay un NAP EC para la configuración de DHCP y un NAP EC para conexiones VPN de acceso remoto. Se puede hacer coincidir el NAP EC con un tipo específico de punto de cumplimiento NAP. Por ejemplo, el NAP de DHCP EC está diseñado para funcionar con un punto de cumplimiento NAP basado en DHCP. Algunos de NAP se proporcionan con la plataforma NAP y proveedores de software de terceros, o bien Microsoft puede proporcionar a otros usuarios.

-   Una capa de componentes del agente de mantenimiento del sistema (SHA)

    Un componente SHA mantiene e informa de uno o varios elementos de mantenimiento del sistema. Por ejemplo, puede haber un SHA para las firmas de antivirus y un SHA para las actualizaciones del sistema operativo. Un SHA puede coincidir con un servidor de actualizaciones, que es un equipo que contiene recursos de actualización de estado a los que los clientes NAP pueden acceder para corregir su estado no compatible. Por ejemplo, un SHA para comprobar las firmas de antivirus coincide con el servidor que contiene el archivo de firma de antivirus más reciente. Los Sha no tienen que tener un servidor de actualizaciones correspondiente. Por ejemplo, un SHA solo puede comprobar la configuración del sistema local para asegurarse de que está habilitado un firewall basado en host. Windows Vista y Windows XP Service Pack 3 incluyen el agente de mantenimiento de seguridad de Windows (WSHA) que supervisa la configuración de la Security Center de Windows. Los proveedores de software de terceros o Microsoft pueden proporcionar Sha adicionales a la plataforma NAP.

-   Agente NAP

    Mantiene la información de estado de mantenimiento actual del cliente NAP y facilita la comunicación entre las capas NAP EC y SHA. El agente NAP se proporciona con la plataforma NAP.

-   API del agente de mantenimiento del sistema

    Proporciona un conjunto de funciones que permiten que los Sha se registren en el agente NAP para indicar el estado del sistema, responder a las consultas del estado de mantenimiento del sistema del agente NAP y para que el agente NAP pase información de corrección de mantenimiento del sistema a SHA. La API SHA permite a los proveedores crear e instalar Sha adicionales. La API SHA se proporciona con la plataforma NAP. Consulte las siguientes interfaces NAP: [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md), [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)y [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md).

Para indicar el estado de mantenimiento de un SHA específico, un SHA crea un informe de mantenimiento ([**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh)) y lo pasa al agente NAP. Un SoH puede contener uno o varios elementos de mantenimiento del sistema. Por ejemplo, el SHA de un programa antivirus puede crear un SoH que contenga el estado del software antivirus que se ejecuta en el equipo, su versión y la última actualización de la firma antivirus recibida. Cada vez que un SHA actualiza su estado, crea un nuevo SoH y lo pasa al agente NAP. Para indicar el estado de mantenimiento general de un cliente NAP, el agente NAP usa un informe de mantenimiento del sistema (SSoH), que incluye información de versión para el cliente NAP y el conjunto de SOH para los Sha instalados.

En las secciones siguientes se describen con más detalle los componentes de la arquitectura de cliente de NAP.

## <a name="nap-enforcement-client"></a>Cliente de cumplimiento NAP

Un cliente de cumplimiento NAP (EC) solicita cierto nivel de acceso a una red, pasa el estado de mantenimiento del equipo a un punto de cumplimiento NAP que proporciona el acceso a la red. Los puntos de cumplimiento NAP son equipos o dispositivos de acceso a la red que usan NAP o se pueden usar con NAP para requerir la evaluación del estado de mantenimiento de un cliente NAP y proporcionar acceso de red restringido o comunicación. Si el estado del equipo no es conforme, NAP EC indica el estado restringido del cliente NAP a otros componentes de la arquitectura del cliente NAP.

El EC de NAP para la plataforma NAP proporcionada en Windows XP con SP3, Windows Vista y Windows Server 2008 son los siguientes:

-   Un NAP de IPsec para las comunicaciones protegidas por IPsec.
-   Un NAP de EAPHost EC para las conexiones autenticadas por 802.1 X.
-   Una VPN NAP EC para conexiones VPN de acceso remoto.
-   Un NAP de DHCP para la configuración de direcciones IPv4 basadas en DHCP.
-   Un NAP EC de puerta de enlace de TS para conexiones de puerta de enlace de TS.

En el caso de Windows XP con SP3, existen NAP para conexiones inalámbricas y cableadas autenticadas por 802.1 X.

### <a name="ipsec-nap-ec"></a>NAP para IPsec

NAP de IPsec es un componente que obtiene el SSoH del agente NAP y lo envía a una autoridad de registro de mantenimiento (HRA), un equipo que ejecuta Windows Server 2008 y Internet Information Services (IIS) que obtiene certificados de mantenimiento de una entidad de certificación (CA) para equipos compatibles. El NAP de IPsec EC se conoce como el usuario de confianza de IPsec en el complemento configuración del cliente de NAP. IPsec NAP EC también interactúa con lo siguiente:

-   El almacén de certificados para almacenar el certificado de mantenimiento.
-   Los componentes de IPsec en Windows para asegurarse de que el certificado de mantenimiento se usa para la comunicación protegida por IPsec.
-   El Firewall basado en host (como el Firewall de Windows) para que el Firewall permita el tráfico protegido por IPsec.

### <a name="eaphost-nap-ec"></a>NAP de EAPHost EC

El NAP de EAPHost EC es un componente que obtiene el SSoH del agente NAP y lo envía como un mensaje de tipo PEAP-Type-length-Value (TLV) para las conexiones autenticadas por 802.1 X. EAPHost NAP EC se conoce como la cuarentena de EAP EC en el complemento configuración del cliente de NAP.

### <a name="vpn-nap-ec"></a>NAP PARA VPN

La VPN NAP EC es una funcionalidad en el servicio Administrador de conexiones de acceso remoto que obtiene el SSoH del agente NAP y lo envía como un mensaje PEAP-TLV para las conexiones VPN de acceso remoto. La VPN NAP EC se conoce como cuarentena de acceso remoto EC en el complemento configuración del cliente de NAP.

### <a name="dhcp-nap-ec"></a>NAP PARA DHCP

El NAP de DHCP EC es una funcionalidad en el servicio de cliente DHCP que usa mensajes DHCP estándar del sector para intercambiar mensajes de mantenimiento del sistema e información de acceso a la red limitada. La EC DHCP de IPsec se conoce como la cuarentena de DHCP EC en el complemento configuración del cliente de NAP. El NAP de DHCP EC obtiene el SSoH del agente NAP. El servicio del cliente DHCP fragmenta el SSoH, si es necesario, y coloca cada fragmento en una opción DHCP específica del proveedor de Microsoft que se envía en los mensajes DHCPDiscover, DHCPRequest o DHCPInform. Los mensajes DHCPDecline y DHCPRelease no contienen SSoH.

## <a name="system-health-agent"></a>Agente de mantenimiento del sistema

Un agente de mantenimiento del sistema (SHA) realiza actualizaciones de mantenimiento del sistema y publica su estado en forma de SoH en el agente NAP. El SoH contiene información que el servidor de directivas de mantenimiento de NAP puede usar para comprobar que el equipo cliente se encuentra en el estado de mantenimiento requerido. Un SHA coincide con un validador de mantenimiento del sistema (SHV) en el lado servidor de la arquitectura de la plataforma NAP. El SHV correspondiente puede devolver una respuesta de SoH (SoHR) al cliente NAP, que se pasa por NAP EC y el agente NAP al SHA, lo que le informa de qué hacer si el SHA no tiene un estado de mantenimiento requerido. Por ejemplo, el SoHR enviado por un SHV de antivirus podría indicar a la SHA de antivirus correspondiente que consulte a un servidor de firmas antivirus para obtener la versión más reciente del archivo de firma de antivirus. El SoHR también puede incluir el nombre o la dirección IP del servidor de firma de antivirus que se va a consultar.

Un SHA puede usar un cliente de directivas instalado localmente para ayudar en las funciones de administración del mantenimiento del sistema junto con un servidor de directivas. Por ejemplo, una actualización de software SHA puede usar el software cliente de software instalado localmente (el cliente de directivas) para realizar la comprobación de la versión y la instalación y actualización de las funciones con el servidor de actualización de software (el servidor de directivas).

## <a name="nap-agent"></a>Agente NAP

El agente NAP proporciona los siguientes servicios:

-   Recopila el SOH de cada SHA y lo almacena en caché. La memoria caché de SoH se actualiza cada vez que un SHA proporciona un SoH nuevo o actualizado.
-   Almacena el SSoH y lo suministra a la solicitud de EC de NAP a petición.
-   Pasa las notificaciones a los Sha cuando cambia el estado restringido.
-   Mantiene el estado restringido del sistema y recopila información de estado de cada SHA.
-   Pasa SoHRs al SHA adecuado.

 

 




