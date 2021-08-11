---
description: Desarrolle aplicaciones de escritorio más seguras mediante Windows API y servicios.
ms.assetid: 1d078a53-250e-4f40-8a3b-83396f2201fc
title: Seguridad e identidad
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: ff19c113340af314177b821bfd8294036d752d90218a5255eb6a429e9b6312ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226340"
---
# <a name="security-and-identity"></a>Seguridad e identidad

Desarrolle aplicaciones de escritorio más seguras mediante Windows API y servicios. Estas API proporcionan:

- Authentication
- Authorization
- Criptografía
- Servicios de directorio, identidad y acceso
- Control parental
- Rights management

En esta sección también se proporcionan procedimientos recomendados y otros artículos de seguridad.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
| ----- | ----------- |
| [Antimalware Scan (Interfaz)](./amsi/antimalware-scan-interface-portal.md) | Antimalware Scan Interface (AMSI) es un estándar de interfaz genérico que permite que las aplicaciones y los servicios se integren con cualquier producto antimalware presente en una máquina. Proporciona protección contra malware mejorada para los usuarios y sus datos, aplicaciones y cargas de trabajo. |
| [Autenticación](./secauthn/authentication-portal.md) | La autenticación es el proceso por el que el sistema valida la información de inicio de sesión de un usuario. El nombre y la contraseña de un usuario se comparan con una lista autorizada y, si el sistema detecta una coincidencia, se concede acceso a la medida especificada en la lista de permisos para ese usuario. |
| [Autorización](./secauthz/authorization-portal.md) | La autorización es el derecho concedido a un individuo para usar el sistema y los datos almacenados en él. Normalmente, un administrador del sistema configura la autorización y la comprueba el equipo en función de algún tipo de identificación del usuario, como un número de código o una contraseña. |
| [Procedimientos recomendados para las API de seguridad](./secbp/best-practices-for-the-security-apis.md) | Proporciona procedimientos recomendados para desarrollar aplicaciones más seguras. |
| [API de inscripción de certificado](./seccertenroll/certenroll-portal.md) | La API de inscripción de certificados se puede usar para crear una aplicación cliente para solicitar un certificado e instalar una respuesta de certificado. |
| [Protección de flujo de control (CFG) ](./secbp/control-flow-guard.md) | Control Flow Guard (CFG) es una característica de seguridad de plataforma altamente optimizada que se creó para evitar vulnerabilidades de daños en la memoria. |
| [Criptografía](./seccrypto/cryptography-portal.md) | La criptografía es el uso de códigos para convertir datos para que solo un destinatario específico pueda leerlo, mediante una clave. CryptoAPI permite a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros, como Internet. |
| [Cryptography API: Next Generation](./seccng/cng-portal.md) | Cryptography API: Next Generation (CNG) permite a los usuarios crear e intercambiar documentos y otros datos en un entorno seguro, especialmente en medios no seguros como Internet. |
| [Extensibilidad Access Control desarrolladores dinámicos](/previous-versions/windows/desktop/dacx/dynamic-access-control-developer-extensibility-roadmap) | El escenario Access Control dinámico (DAC), tal como se entrega en Windows Server 2012, tiene una variedad de puntos de extensibilidad para desarrolladores que agregan potencial de personalización para el desarrollo de aplicaciones. |
| [Directorio, identidad y Access Services](./srvnodes/directory--identity--and-access-services.md) | Los administradores de red pueden usar servicios de directorio para automatizar tareas administrativas comunes, como agregar usuarios y grupos, administrar impresoras y establecer permisos en los recursos de red.<br/> Los proveedores de software independientes y los desarrolladores de usuarios finales pueden usar servicios de directorio para habilitar sus productos y aplicaciones. Los servicios pueden publicarse en un directorio, los clientes pueden usar el directorio para buscar servicios y ambos pueden usar el directorio para buscar y manipular otros objetos.<br/> Forefront Identity Manager (FIM) proporciona una solución integrada y completa para administrar todo el ciclo de vida de las identidades de usuario y sus credenciales asociadas.<br/> Identity Lifecycle Manager (ILM) permite a las organizaciones de TI reducir el costo de administrar el ciclo de vida de identidad y acceso proporcionando una vista única de la identidad de un usuario en la empresa heterogéneo y mediante la automatización de tareas comunes.<br/> Active Directory Servicio de federación (AD FS) permite federated Identity and Access Management al compartir de forma segura los derechos y la identidad digital a través de los límites de seguridad y empresa. |
| [Protocolo de autenticación extensible](./eap/extensible-authentication-protocol-reference.md) | El Protocolo de autenticación extensible (EAP) es un estándar compatible con varios componentes del sistema. EAP es fundamental para proteger la seguridad de redes privadas inalámbricas (802.1X) y cableadas, acceso telefónico y redes privadas virtuales (VPN). |
| [Host del protocolo de autenticación extensible](./eaphost/about-eap-host.md) | EAPHost es un componente de redes de Microsoft Windows que proporciona una infraestructura de Protocolo de autenticación extensible (EAP) para la autenticación de implementaciones de protocolo "suplicante", como 802.1X y punto a punto (PPP). |
| [Contraseña de MS-CHAP API de Administración](/previous-versions/windows/desktop/mschap/portal) | Puede usar la contraseña de MS-CHAP API de Administración para crear aplicaciones para cambiar las contraseñas de los usuarios en red en estaciones de trabajo remotas. |
| [Protección de acceso a redes](./nap/network-access-protection-start-page.md) | Protección de acceso a redes (NAP) es un conjunto de componentes de sistema operativo que proporcionan una plataforma para el acceso protegido a redes privadas. La plataforma NAP proporciona una manera integrada de evaluar el estado de mantenimiento del sistema de un cliente de red que intenta conectarse o comunicarse en una red y restringir el acceso del cliente de red hasta que se cumplen los requisitos de la directiva de mantenimiento. |
| [Servidor de directivas de redes](./nps/portal.md) | Servidor de directivas de red (NPS) es la implementación de Microsoft de un servidor y proxy del Servicio de acceso telefónico de usuario de autenticación remota (RADIUS). Es el sucesor del Servicio de autenticación de Internet (IAS). |
| [Controles parentales](./parcon/parental-controls-portal.md) | La tecnología de controles parentales de Windows está diseñada para ayudar a los padres diligentes o guardianes a garantizar el acceso a los materiales adecuados por edad o nivel de madurez para los que están bajo su protección. Proporciona una infraestructura extensible además de funcionalidades integradas. |
| [Rights Management](./srvnodes/rights-management.md) | Ahora hay tres generaciones de SDK de Rights Management disponibles, así como una hoja de ruta general para los ejemplos de código RMS proporcionados por Microsoft y las herramientas para desarrolladores en todos los sistemas operativos compatibles. Android, iOS/OS X, Windows Phone y Windows Desktop. |
| [Ciclo de vida de desarrollo de seguridad (SDL): guía de procesos](/previous-versions/windows/desktop/cc307891(v=msdn.10)) | Ciclo de vida de desarrollo de seguridad de Microsoft (SDL) es un proceso de control de seguridad de software líder del sector. Una iniciativa de todo Microsoft y una directiva obligatoria desde 2004, sdl ha desempeñado un papel fundamental en la inserción de seguridad y privacidad en el software y la cultura de Microsoft. Combinando un enfoque holístico y práctico, sdl introduce la seguridad y la privacidad al principio y a lo largo de todas las fases del proceso de desarrollo. |
| [Administración de seguridad](./secmgmt/management-portal.md) | Las tecnologías de administración de seguridad se pueden usar para administrar la directiva de autoridad de seguridad local (LSA) y la directiva de filtro de contraseñas, consultar la capacidad de los programas de orígenes externos y los datos adjuntos de servicio que amplían la funcionalidad de la herramienta de configuración de seguridad. |
| [Proveedores WMI de seguridad](./secprov/secprov-portal.md) | Los proveedores WMI de seguridad permiten a los administradores y programadores configurar Cifrado de unidad BitLocker (BDE) y el Módulo de plataforma segura (TPM) mediante Windows Management Instrumentation (WMI). |
| [Glosario de seguridad](./secgloss/security-glossary.md) | Proporciona un glosario de términos de seguridad. |
| [Servicios base de TPM](./tbs/tpm-base-services-portal.md) | La característica Módulo de plataforma segura base (TPM) Base Services (TBS) centraliza el acceso de TPM entre aplicaciones. La característica TBS usa prioridades especificadas mediante una llamada a las aplicaciones para programar de forma cooperativa el acceso a TPM. |
| [API del Marco biométrico de Windows](./secbiomet/biometric-service-api-portal.md) | Puede usar la API Windows Biometric Framework para crear aplicaciones cliente que capturen, guarden y comparen información biométrica del usuario final de forma segura. |
| [Artículos técnicos de seguridad](https://msdn.microsoft.com/library/hh322936.aspx) | Artículos sobre seguridad y criptografía. |



 

 

 