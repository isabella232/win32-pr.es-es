---
description: Desarrolle aplicaciones de escritorio más seguras mediante las API y los servicios de Windows.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Seguridad e identidad
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: 5b8fccc4039794fe76dabb34d88fa6d475a3b22a
ms.sourcegitcommit: 7f0c005e444c17f69b5ead403c43814f3bbe047a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "104421678"
---
# <a name="security-and-identity"></a>Seguridad e identidad

Desarrolle aplicaciones de escritorio más seguras mediante las API y los servicios de Windows. Estas API proporcionan:

- Autenticación
- Authorization
- Criptografía
- Servicios de directorio, identidad y acceso
- Control parental
- Rights management

En esta sección también se proporcionan procedimientos recomendados y otros artículos de seguridad.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
| ----- | ----------- |
| [Interfaz de detección antimalware](./amsi/antimalware-scan-interface-portal.md) | La interfaz de detección antimalware (AMSI) es una interfaz genérica estándar que permite a las aplicaciones y servicios integrarse con cualquier producto antimalware presente en un equipo. Proporciona protección contra malware mejorada para los usuarios y sus datos, aplicaciones y cargas de trabajo. |
| [Autenticación](./secauthn/authentication-portal.md) | La autenticación es el proceso por el que el sistema valida la información de inicio de sesión de un usuario. El nombre y la contraseña de un usuario se comparan con una lista autorizada y, si el sistema detecta una coincidencia, se concede el acceso a la extensión especificada en la lista de permisos para ese usuario. |
| [Autorización](./secauthz/authorization-portal.md) | La autorización es el derecho concedido a un individuo para usar el sistema y los datos almacenados en él. La autorización normalmente la configura un administrador del sistema y la comprueba el equipo en función de alguna forma de identificación de usuario, como un número de código o una contraseña. |
| [Prácticas recomendadas para las API de seguridad](./secbp/best-practices-for-the-security-apis.md) | Proporciona procedimientos recomendados para desarrollar aplicaciones más seguras. |
| [API de inscripción de certificado](./seccertenroll/certenroll-portal.md) | La API de inscripción de certificados se puede usar para crear una aplicación cliente para solicitar un certificado e instalar una respuesta de certificado. |
| [Protección de flujo de control (CFG) ](./secbp/control-flow-guard.md) | La protección de flujo de control (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para combatir vulnerabilidades de daños en la memoria. |
| [Criptografía](./seccrypto/cryptography-portal.md) | La criptografía es el uso de códigos para convertir datos de modo que solo un destinatario específico pueda leerlo, mediante una clave. CryptoAPI permite a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros como Internet. |
| [Cryptography API: próxima generación](./seccng/cng-portal.md) | Cryptography API: Next Generation (CNG) permite a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros, como Internet. |
| [Extensibilidad del desarrollador de Access Control dinámico](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | El escenario de Access Control dinámico (DAC), tal y como se entrega en Windows Server 2012, tiene una variedad de puntos de extensibilidad de desarrollador que agregan posibilidades de personalización para el desarrollo de aplicaciones. |
| [Servicios de directorio, identidad y acceso](./srvnodes/directory--identity--and-access-services.md) | Los administradores de red pueden usar los servicios de directorio para automatizar las tareas administrativas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos en los recursos de red.<br/> Los fabricantes de software independientes y los desarrolladores de usuarios finales pueden usar los servicios de directorio para habilitar los productos y las aplicaciones en el directorio. Los servicios pueden publicarse en un directorio, los clientes pueden usar el directorio para buscar servicios y ambos pueden usar el directorio para buscar y manipular otros objetos.<br/> Forefront Identity Manager (FIM) proporciona una solución integrada y completa para administrar todo el ciclo de vida de las identidades de usuario y sus credenciales asociadas.<br/> Identity Lifecycle Manager (ILM) permite a las organizaciones de ti reducir el costo de administrar el ciclo de vida de identidad y acceso al proporcionar una vista única de la identidad de un usuario en toda la empresa heterogénea y a través de la automatización de tareas comunes.<br/> Active Directory Servicio de federación (AD FS) permite a la administración de identidades y accesos federados compartir de forma segura los derechos de identidad y derechos digitales en los límites de seguridad y empresariales. |
| [Protocolo de autenticación extensible](./eap/extensible-authentication-protocol-reference.md) | El protocolo de autenticación extensible (EAP) es un estándar que admiten varios componentes del sistema. EAP es fundamental para proteger la seguridad de la red inalámbrica (802.1 X) y las LAN cableadas, acceso telefónico y redes privadas virtuales (VPN). |
| [Host del Protocolo de autenticación extensible](./eaphost/about-eap-host.md) | EAPHost es un componente de red de Microsoft Windows que proporciona una infraestructura de protocolo de autenticación extensible (EAP) para la autenticación de implementaciones de protocolo de "suplicante" como 802.1 X y punto a punto (PPP). |
| [API de administración de contraseñas MS-CHAP](/previous-versions/windows/desktop/mschap/portal) | Puede usar la API de administración de contraseñas MS-CHAP para crear aplicaciones con el fin de cambiar las contraseñas de los usuarios en red en estaciones de trabajo remotas. |
| [Protección de acceso a redes](./nap/network-access-protection-start-page.md) | Protección de acceso a redes (NAP) es un conjunto de componentes del sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas. La plataforma NAP proporciona una manera integrada de evaluar el estado de mantenimiento del sistema de un cliente de red que está intentando conectarse o comunicarse en una red y restringir el acceso del cliente de red hasta que se hayan cumplido los requisitos de la Directiva de mantenimiento. |
| [Servidor de directivas de redes](./nps/portal.md) | El servidor de directivas de redes (NPS) es la implementación de Microsoft de un servidor y proxy de servicio de autenticación remota telefónica de usuario (RADIUS). Es el sucesor del servicio de autenticación de Internet (IAS). |
| [Controles parentales](./parcon/parental-controls-portal.md) | La tecnología de controles parentales de Windows está pensada para ayudar a los padres o tutores a garantizar el acceso a los materiales adecuados por edad o nivel de madurez para los que están en su tutela. Proporciona una infraestructura extensible además de funcionalidades integradas. |
| [Rights Management](./srvnodes/rights-management.md) | Ahora hay disponibles tres generaciones de Rights Management SDK, así como un mapa de ruta de todos los ejemplos de código y herramientas de desarrollo de RMS proporcionados por Microsoft en todos los sistemas operativos compatibles. Android, iOS/OS X, Windows Phone y escritorio de Windows. |
| [Ciclo de vida de desarrollo de seguridad (SDL)-Guía de procesos](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Ciclo de vida de desarrollo de seguridad (SDL) de Microsoft es un proceso de garantía de seguridad de software líder del sector. Una iniciativa de todo el mundo de Microsoft y una directiva obligatoria desde 2004, SDL ha desempeñado un papel fundamental en la inserción de seguridad y privacidad en el software y la cultura de Microsoft. Mediante la combinación de un enfoque holístico y práctico, SDL introduce la seguridad y la privacidad en el principio y en todas las fases del proceso de desarrollo. |
| [Administración de seguridad](./secmgmt/management-portal.md) | Las tecnologías de administración de seguridad se pueden usar para administrar la Directiva de la Directiva de seguridad local (LSA) y la Directiva de filtro de contraseña, consultar la capacidad de los programas de orígenes externos y datos adjuntos de servicio que amplían la funcionalidad de la herramienta de configuración de seguridad. |
| [Proveedores de seguridad WMI](./secprov/secprov-portal.md) | Los proveedores de seguridad de WMI permiten a los administradores y programadores configurar Cifrado de unidad BitLocker (BDE) y el Módulo de plataforma segura (TPM) mediante Instrumental de administración de Windows (WMI). |
| [Glosario de seguridad](./secgloss/security-glossary.md) | Proporciona un glosario de términos de seguridad. |
| [Servicios base de TPM](./tbs/tpm-base-services-portal.md) | La característica de servicios base de Módulo de plataforma segura (TBS) centraliza el acceso de TPM entre las aplicaciones. La característica TBS usa las prioridades especificadas al llamar a las aplicaciones para programar el acceso de TPM de forma cooperativa. |
| [API del Marco biométrico de Windows](./secbiomet/biometric-service-api-portal.md) | Puede usar la API de Plataforma de biometría de Windows para crear aplicaciones cliente que capturen, guarden y comparen de forma segura la información biométrica del usuario final. |
| [Artículos técnicos de seguridad](https://msdn.microsoft.com/library/hh322936.aspx) | Artículos sobre seguridad y criptografía. |



 

 

 