---
title: Arquitectura del lado servidor NAP
description: Arquitectura del lado servidor NAP
ms.assetid: b05c52d5-1f90-41d4-a540-d20e70e54bcb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dac585d3c455a1a40f2037b71c0e33cd2bd4847
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161252"
---
# <a name="nap-server-side-architecture"></a>Arquitectura del lado servidor NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La arquitectura de la plataforma del lado servidor NAP usa equipos que ejecutan Windows Server 2008. En la ilustración siguiente se muestra la arquitectura de la compatibilidad del lado servidor con la plataforma NAP, que consta de puntos de cumplimiento de NAP basados en Windows y un servidor de directivas de mantenimiento nap.

![arquitectura de la compatibilidad del lado servidor con la plataforma nap](images/nap-server-side-arch.png)

Un Windows de cumplimiento nap basado en el servidor de cumplimiento de NAP tiene una capa de componentes de NAP Enforcement Server (ES). Cada ES de NAP se define para un tipo diferente de acceso o comunicación de red. Por ejemplo, hay un NAP ES para las conexiones VPN de acceso remoto y un NAP ES para la configuración DHCP. El ES de NAP suele coincidir con un tipo específico de cliente compatible con NAP. Por ejemplo, DHCP NAP ES está diseñado para trabajar con un cliente de cumplimiento nap (EC) basado en DHCP. Los proveedores de software de terceros o Microsoft pueden proporcionar sistemas electrónicos nap adicionales para la plataforma NAP. Un ES de NAP obtiene la declaración de estado del sistema (SSoH) de su NAP EC correspondiente y la envía a un servidor de directivas de mantenimiento NAP como un atributo específico del proveedor (VSA) del Servicio de usuario de autenticación remota de acceso telefónico (RADIUS) del mensaje de Access-Request [RADIUS.](https://www.ietf.org/rfc/rfc2865.txt?number=2865)

Como se muestra en la ilustración de arquitectura del lado servidor, el servidor de directivas de mantenimiento nap tiene los siguientes componentes:

-   Servicio servidor de directivas de red (NPS)

    Recibe el mensaje Access-Request RADIUS, extrae el SSoH y lo pasa al componente servidor de administración de NAP. El servicio NPS se proporciona con Windows Server 2008.

-   Servidor de administración nap

    Facilita la comunicación entre el servicio NPS y los validadores de estado del sistema (SHV). El componente servidor de administración de NAP se proporciona con la plataforma NAP.

-   Una capa de componentes shv

    Cada SHV se define para uno o varios tipos de información de mantenimiento del sistema y puede coincidir con un SHA. Por ejemplo, podría haber un SHV para un programa antivirus. Una SHV podría coincidir con uno o varios servidores de requisitos de estado. Por ejemplo, un SHV para comprobar las firmas antivirus coincide con el servidor que contiene el archivo de firma más reciente. Los SHV no tienen que tener un servidor de requisitos de mantenimiento correspondiente. Una SHV solo puede indicar a los clientes compatibles con NAP que comprueben la configuración del sistema local para asegurarse de que está habilitado un firewall basado en host. Windows Server 2008 incluye el validador Seguridad de Windows health (WSHV). Los fabricantes de software de terceros o Microsoft proporcionan SHV adicionales como complementos a la plataforma NAP.

-   SHV API

    Proporciona un conjunto de llamadas de función que permiten a los SHV registrarse con el componente servidor de administración de NAP, recibir instrucciones de mantenimiento (SOH) del componente servidor de administración nap y enviar respuestas de instrucción de estado (SOHR) al componente servidor de administración nap. La API de SHV se proporciona con la plataforma NAP. Vea las siguientes interfaces nap: [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) e [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md).

Como se ha descrito anteriormente, la configuración más común para la infraestructura del lado servidor NAP consta de puntos de cumplimiento nap que proporcionan acceso a la red o comunicación de un tipo específico y servidores de directivas de mantenimiento NPS independientes que proporcionan validación y corrección del estado del sistema. Es posible instalar el servicio NPS como un servidor de directivas de mantenimiento nap en puntos de cumplimiento Windows NAP basados en el servidor. Sin embargo, en esta configuración, cada punto de cumplimiento de NAP debe configurarse por separado con directivas de mantenimiento y acceso a la red. La configuración recomendada es usar servidores de directivas de mantenimiento NAP independientes.

La arquitectura nap general consta de los siguientes conjuntos de componentes:

-   Los tres componentes de cliente NAP (una capa SHA, el agente NAP y una capa NAP EC).
-   Los cuatro componentes del lado servidor NAP (una capa shv, el servidor de administración nap, el servicio NPS y una capa de NAP ES en Windows de cumplimiento nap basados en el servidor).
-   Los servidores de requisitos de mantenimiento, que son equipos que pueden proporcionar los requisitos de mantenimiento del sistema actuales para los servidores de directivas de mantenimiento nap.
-   Servidores de corrección, que son equipos que contienen recursos de actualización de estado a los que los clientes NAP pueden acceder para corregir su estado no conforme.

En la ilustración siguiente se muestran las relaciones entre los componentes de la plataforma NAP.

![relaciones entre los componentes de la plataforma nap](images/nap-components.png)

Observe la coincidencia de los siguientes conjuntos de componentes:

-   Los ECs y los ES de NAP suelen coincidir.

    Por ejemplo, la NAP EC DE DHCP en el cliente NAP coincide con la ES de NAP DHCP en el servidor DHCP.

-   Se pueden hacer coincidir los servidores SHA y de corrección.

    Por ejemplo, un SHA antivirus en el cliente coincide con un servidor de corrección de firma antivirus.

-   Se pueden coincidir los SHV y los servidores de requisitos de estado.

    Por ejemplo, un SHV antivirus en el servidor de directivas de mantenimiento NAP puede coincidir con un servidor de requisitos de mantenimiento antivirus.

Los proveedores de software de terceros pueden ampliar la plataforma NAP de las maneras siguientes:

-   Cree un nuevo método por el que se evalúe el estado de un cliente NAP.

    Los proveedores de software de terceros deben crear un SHA para el cliente NAP, un SHV para el servidor de directivas de mantenimiento nap y, si es necesario, los servidores de corrección y requisitos de mantenimiento. Si ya existen los requisitos de mantenimiento o los servidores de corrección, como un servidor de distribución de firmas antivirus, solo es necesario crear los componentes SHA y SHV correspondientes. En algunos casos, no se necesitan servidores de corrección ni requisitos de mantenimiento.

-   Cree un nuevo método para aplicar los requisitos de mantenimiento para el acceso a la red o la comunicación.

    Los proveedores de software de terceros deben crear una NAP EC en el cliente NAP. Si el método de cumplimiento usa un servicio basado en Windows, los proveedores de software de terceros deben crear un ES de NAP correspondiente que se comunique con un servidor de directivas de mantenimiento nap mediante el protocolo RADIUS o mediante el servicio NPS instalado en el punto de cumplimiento nap como proxy RADIUS.

En las secciones siguientes se describen con más detalle los componentes de la arquitectura del lado servidor NAP.

## <a name="nap-enforcement-server"></a>Servidor de cumplimiento de NAP

Un servidor de cumplimiento nap (ES) permite cierto nivel de acceso o comunicación de red, puede pasar el estado de mantenimiento de un cliente NAP al servidor de directivas de mantenimiento de red para su evaluación y, en función de la respuesta, puede proporcionar el cumplimiento del acceso de red limitado.

Los ES nap incluidos con Windows Server 2008 son los siguientes:

-   Un ES de NAP de IPsec para comunicaciones protegidas por IPsec.

    Para la comunicación protegida por IPsec, la entidad de registro de estado (HRA), un equipo que ejecuta Windows Server 2008 y Internet Information Services (IIS) que obtiene certificados de mantenimiento de una entidad de certificación (CA) para equipos compatibles, pasa la información de estado de mantenimiento del cliente NAP al servidor de directivas de mantenimiento nap.

-   Un NAP DE DHCP ES para la configuración de direcciones IP basadas en DHCP.

    DHCP NAP ES es una funcionalidad del servicio de servidor DHCP que usa mensajes DHCP estándar del sector para comunicarse con DHCP NAP EC en un cliente NAP. El cumplimiento de DHCP para el acceso limitado a la red se realiza a través de las opciones DHCP.

-   Nap ES de puerta de enlace de Terminal Services (TS) para conexiones basadas en servidor de puerta de enlace de TS.

Para las conexiones autenticadas mediante VPN de acceso remoto y 802.1X, la funcionalidad del servicio NPS usa mensajes PEAP-TLV entre los clientes NAP y el servidor de directivas de mantenimiento nap. La aplicación de VPN se realiza a través de filtros de paquetes IP que se aplican a la conexión VPN. El cumplimiento de 802.1X se realiza en el dispositivo de acceso a la red 802.1X mediante la aplicación de filtros de paquetes IP a la conexión o asignando a la conexión un identificador de VLAN correspondiente a la red restringida.

## <a name="nap-administration-server"></a>Servidor de administración nap

El componente Servidor de administración nap proporciona los siguientes servicios:

-   Obtiene los SSoH de NAP ES a través del servicio NPS.
-   Distribuye los soHs de los SSoHs a los validadores de estado del sistema (SHV) adecuados.
-   Recopila los SOHR de los SHV y los pasa al servicio NPS para su evaluación.

## <a name="nps-service"></a>Servicio NPS

RADIUS es un protocolo ampliamente implementado que permite la autenticación centralizada, la autorización y la contabilidad del acceso a la red que se describe en Solicitudes de comentarios (RFC) 2865 y 2866. Desarrollado originalmente para el acceso remoto de acceso telefónico, RADIUS ahora es compatible con puntos de acceso inalámbricos, conmutadores Ethernet de autenticación, servidores VPN, servidores de acceso de línea de suscriptor digital (DSL) y otros servidores de acceso a la red.

NPS es la implementación de un servidor RADIUS y un proxy en Windows Server 2008. NPS reemplaza el Servicio de autenticación de Internet (IAS) en Windows Server 2003. Para la plataforma NAP, el servicio NPS incluye el componente Servidor administrador nap, compatibilidad con la API de SHV y SHV instalables, y opciones para configurar directivas de mantenimiento.

En función de los SOHR de los SHV y las directivas de mantenimiento configuradas, el servicio NPS crea una instrucción de respuesta de estado del sistema (SSoHR), que indica si el cliente NAP es compatible o no compatible e incluye el conjunto de SOHR de los SHV.

## <a name="system-health-validator-shv"></a>Validador de mantenimiento del sistema (SHV)

Un SHV recibe un SoH del servidor de administración nap y compara la información de estado de mantenimiento del sistema con el estado de mantenimiento del sistema necesario. Por ejemplo, si el SoH es de un SHA antivirus y contiene el número de versión del último archivo de firma de virus, el SHV antivirus correspondiente puede comprobar con el servidor de requisitos de mantenimiento del antivirus el número de versión más reciente para validar el SoH del cliente NAP.

El SHV devuelve un SoHR al servidor de administración nap. El SoHR puede contener información sobre cómo el SHA correspondiente en el cliente NAP puede cumplir los requisitos de mantenimiento del sistema actuales. Por ejemplo, el SoHR enviado por el SHV antivirus podría indicar al sha antivirus en el cliente NAP que solicite la versión más reciente del archivo de firma del antivirus desde un servidor de firma antivirus específico por nombre o dirección IP.

 

 




