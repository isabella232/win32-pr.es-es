---
title: Arquitectura del lado servidor NAP
description: Arquitectura del lado servidor NAP
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104149101"
---
# <a name="nap-server-side-architecture"></a>Arquitectura del lado servidor NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La arquitectura de la plataforma del servidor NAP usa equipos que ejecutan Windows Server 2008. En la ilustración siguiente se muestra la arquitectura de la compatibilidad del lado servidor para la plataforma NAP, que consta de puntos de cumplimiento NAP basados en Windows y un servidor de directivas de mantenimiento NAP.

![arquitectura de la compatibilidad del lado servidor para la plataforma NAP](images/nap-server-side-arch.png)

Un punto de cumplimiento NAP basado en Windows tiene una capa de componentes de servidor de cumplimiento NAP. Cada NAP se define para un tipo diferente de acceso o comunicación de red. Por ejemplo, hay un NAP para conexiones VPN de acceso remoto y un NAP para la configuración de DHCP. Normalmente, NAP se hace coincidir con un tipo específico de cliente compatible con NAP. Por ejemplo, el NAP de DHCP está diseñado para funcionar con un cliente de cumplimiento NAP basado en DHCP (EC). Los proveedores de software de terceros o Microsoft pueden proporcionar un ESs de NAP adicional para la plataforma NAP. Un NAP se obtiene del informe de mantenimiento del sistema (SSoH) de su correspondiente NAP EC y lo envía a un servidor de directivas de mantenimiento de NAP como un atributo específico del proveedor (VSA) de servicio de autenticación remota telefónica de usuario (RADIUS) de [radius Access-Request mensaje](https://www.ietf.org/rfc/rfc2865.txt?number=2865) .

Como se muestra en la ilustración de la arquitectura del lado servidor, el servidor de directivas de mantenimiento de NAP tiene los siguientes componentes:

-   Servicio del servidor de directivas de redes (NPS)

    Recibe el mensaje de Access-Request de RADIUS, extrae SSoH y lo pasa al componente de servidor de administración de NAP. El servicio NPS se proporciona con Windows Server 2008.

-   Servidor de administración de NAP

    Facilita la comunicación entre el servicio NPS y los validadores de mantenimiento del sistema (SHV). El componente del servidor de administración de NAP se proporciona con la plataforma NAP.

-   Una capa de componentes de SHV

    Cada SHV se define para uno o varios tipos de información de mantenimiento del sistema y se puede hacer coincidir con un SHA. Por ejemplo, podría haber un SHV para un programa antivirus. Un SHV podría coincidir con uno o varios servidores de requisitos de mantenimiento. Por ejemplo, un SHV para comprobar las firmas de antivirus coincide con el servidor que contiene el archivo de firma más reciente. Los SHV no tienen que tener un servidor de requisitos de mantenimiento correspondiente. Un SHV solo puede indicar a los clientes compatibles con NAP que comprueben la configuración del sistema local para asegurarse de que hay un firewall basado en host habilitado. Windows Server 2008 incluye el validador de mantenimiento de seguridad de Windows (WSHV). Otros proveedores de software o Microsoft proporcionan otros SHV como complementos para la plataforma NAP.

-   API DE SHV

    Proporciona un conjunto de llamadas de función que permiten a los SHV registrarse con el componente de servidor de administración de NAP, recibir informes de mantenimiento (SOH) del componente de servidor de administración de NAP y enviar las respuestas de informe de mantenimiento (SoHRs) al componente de servidor de administración de NAP. La API de SHV se proporciona con la plataforma NAP. Consulte las siguientes interfaces NAP: [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) y [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).

Tal y como se ha descrito anteriormente, la configuración más común para la infraestructura del servidor NAP consiste en puntos de cumplimiento NAP que proporcionan acceso a la red o comunicación de un tipo específico y servidores de directivas de mantenimiento de NPS independientes que proporcionan validación y corrección del mantenimiento del sistema. Es posible instalar el servicio NPS como un servidor de directivas de mantenimiento de NAP en puntos de cumplimiento NAP basados en Windows individuales. Sin embargo, en esta configuración, cada punto de cumplimiento NAP se debe configurar por separado con las directivas de acceso y mantenimiento de la red. La configuración recomendada es usar servidores de directivas de mantenimiento de NAP independientes.

La arquitectura general de NAP consta de los siguientes conjuntos de componentes:

-   Los tres componentes de cliente de NAP (una capa SHA, el agente NAP y un nivel NAP EC).
-   Los cuatro componentes del lado servidor NAP (una capa SHV, el servidor de administración de NAP, el servicio NPS y una capa NAP ES en puntos de cumplimiento NAP basados en Windows).
-   Servidores de requisitos de mantenimiento, que son equipos que pueden proporcionar los requisitos actuales de mantenimiento del sistema para los servidores de directivas de mantenimiento de NAP.
-   Servidores de actualizaciones, que son equipos que contienen recursos de actualización de estado a los que los clientes NAP pueden acceder para corregir su estado no compatible.

En la siguiente ilustración se muestran las relaciones entre los componentes de la plataforma NAP.

![relaciones entre los componentes de la plataforma NAP](images/nap-components.png)

Observe la coincidencia de los siguientes conjuntos de componentes:

-   NAP para NAP y el ESs de NAP suelen coincidir.

    Por ejemplo, el NAP de DHCP EC en el cliente NAP coincide con el NAP de DHCP del servidor DHCP.

-   Se puede hacer coincidir los servidores SHA y de corrección.

    Por ejemplo, un antivirus SHA en el cliente se hace coincidir con un servidor de actualizaciones de firma antivirus.

-   Se puede hacer coincidir los SHV y los servidores de requisitos de mantenimiento.

    Por ejemplo, se puede hacer coincidir un SHV de antivirus en el servidor de directivas de mantenimiento de NAP con un servidor de requisitos de mantenimiento del antivirus.

Los proveedores de software de terceros pueden extender la plataforma NAP de las siguientes maneras:

-   Cree un nuevo método por el que se evalúe el estado de un cliente NAP.

    Los proveedores de software de terceros deben crear un SHA para el cliente NAP, un SHV para el servidor de directivas de mantenimiento NAP y, si es necesario, los requisitos de mantenimiento y los servidores de actualizaciones. Si el requisito de mantenimiento o los servidores de actualizaciones ya existen, como un servidor de distribución de firmas de antivirus, solo deben crearse los componentes SHA y SHV correspondientes. En algunos casos, los requisitos de mantenimiento o los servidores de actualizaciones no son necesarios.

-   Cree un nuevo método para aplicar los requisitos de mantenimiento para el acceso a la red o la comunicación.

    Los proveedores de software de terceros deben crear un NAP EC en el cliente NAP. Si el método de cumplimiento usa un servicio basado en Windows, los proveedores de software de terceros deben crear un NAP correspondiente que se comunique con un servidor de directivas de mantenimiento de NAP mediante el protocolo RADIUS o mediante el servicio NPS instalado en el punto de cumplimiento NAP como proxy RADIUS.

En las secciones siguientes se describen con más detalle los componentes de la arquitectura del lado servidor NAP.

## <a name="nap-enforcement-server"></a>Servidor de cumplimiento NAP

Un servidor de cumplimiento NAP permite cierto nivel de acceso a la red o comunicación, puede pasar el estado de mantenimiento de un cliente NAP al servidor de directivas de mantenimiento de red para su evaluación y, en función de la respuesta, puede proporcionar la aplicación de acceso limitado a la red.

El ESs de NAP incluido con Windows Server 2008 es el siguiente:

-   Un NAP de IPsec para las comunicaciones protegidas por IPsec.

    Para la comunicación protegida por IPsec, la autoridad de registro de mantenimiento (HRA), un equipo que ejecuta Windows Server 2008 y Internet Information Services (IIS) que obtiene los certificados de mantenimiento de una entidad de certificación (CA) para equipos compatibles, pasa la información de estado de mantenimiento del cliente NAP al servidor de directivas de mantenimiento de NAP.

-   Un NAP de DHCP para la configuración de direcciones IP basadas en DHCP.

    El NAP de DHCP es una funcionalidad en el servicio del servidor DHCP que usa mensajes DHCP estándar del sector para comunicarse con el NAP de DHCP en un cliente NAP. El cumplimiento de DHCP para el acceso limitado a la red se realiza a través de las opciones de DHCP.

-   Un NAP de puerta de enlace Terminal Services (TS) para las conexiones basadas en servidor de puerta de enlace de TS.

En el caso de las conexiones de VPN de acceso remoto y autenticadas por 802.1 X, la funcionalidad del servicio NPS usa mensajes PEAP-TLV entre los clientes NAP y el servidor de directivas de mantenimiento de NAP. La aplicación de VPN se realiza a través de los filtros de paquetes IP que se aplican a la conexión VPN. la aplicación de 802.1 x se realiza en el dispositivo de acceso a la red 802.1 X mediante la aplicación de filtros de paquetes IP a la conexión o mediante la asignación de un identificador de VLAN que corresponde a la red restringida.

## <a name="nap-administration-server"></a>Servidor de administración de NAP

El componente del servidor de administración de NAP proporciona los siguientes servicios:

-   Obtiene el SSoHs de NAP a través del servicio NPS.
-   Distribuye el SOH de SSoHs a los validadores de mantenimiento del sistema (SHV) adecuados.
-   Recopila SoHRs de los SHV y los pasa al servicio NPS para su evaluación.

## <a name="nps-service"></a>Servicio NPS

RADIUS es un protocolo ampliamente implementado que permite la autenticación centralizada, la autorización y las cuentas para el acceso a la red que se describe en las solicitudes de comentarios (RFC) 2865 y 2866. Originalmente desarrollado para el acceso telefónico remoto, RADIUS ahora es compatible con los puntos de acceso inalámbricos, autenticar conmutadores Ethernet, servidores VPN, servidores de acceso de línea de suscriptor digital (ADSL) y otros servidores de acceso a la red.

NPS es la implementación de un servidor RADIUS y un proxy en Windows Server 2008. NPS reemplaza el servicio de autenticación de Internet (IAS) en Windows Server 2003. Para la plataforma NAP, el servicio NPS incluye el componente de servidor de administrador de NAP, la compatibilidad con la API de SHV y los SHV instalables, y las opciones para configurar las directivas de mantenimiento.

Según el SoHRs de los SHV y las directivas de mantenimiento configuradas, el servicio NPS crea un informe de respuesta de estado del sistema (SSoHR), que indica si el cliente NAP es compatible o no compatible e incluye el conjunto de SoHRs de los SHV.

## <a name="system-health-validator-shv"></a>Validador de mantenimiento del sistema (SHV)

Un SHV recibe un SoH del servidor de administración de NAP y compara la información de estado de mantenimiento del sistema con el estado de mantenimiento del sistema requerido. Por ejemplo, si el SoH proviene de un archivo SHA de antivirus y contiene el número de versión del último archivo de firma de virus, el SHV del antivirus correspondiente puede comprobar con el servidor de requisitos de mantenimiento del antivirus el número de versión más reciente para validar el SoH del cliente NAP.

El SHV devuelve un SoHR al servidor de administración de NAP. El SoHR puede contener información acerca de cómo el SHA correspondiente en el cliente NAP puede cumplir los requisitos actuales de mantenimiento del sistema. Por ejemplo, el SoHR enviado por el programa antivirus SHV podría indicar al antivirus SHA en el cliente NAP que solicite la versión más reciente del archivo de firma de antivirus de un servidor de firmas antivirus específico por nombre o dirección IP.

 

 




