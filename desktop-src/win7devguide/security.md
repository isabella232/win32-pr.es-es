---
title: Seguridad (Windows 7 Developer Guide)
description: Windows 7 incluye características de seguridad nuevas y mejoradas que facilitan a los desarrolladores mejorar, usar y administrar la seguridad de sus aplicaciones.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421256c23042ad1ea4bad57a616047e43276449bd93f771543d4eb41286c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329745"
---
# <a name="security-windows-7-developer-guide"></a>Seguridad (Windows 7 Developer Guide)

Windows 7 incluye características de seguridad nuevas y mejoradas que facilitan a los desarrolladores mejorar, usar y administrar la seguridad de sus aplicaciones. Incluye una variedad de nuevas características de seguridad que no solo ayudan a protegerse frente a amenazas, sino que también limitan los daños que los atacantes pueden hacer si obtienen acceso a un equipo.

Las mejoras en la plataforma de Windows permiten a los desarrolladores crear aplicaciones que interactúan con el procesamiento de paquetes en la pila de redes del sistema operativo. Se pueden filtrar y modificar datos de red antes de que lleguen a su destino.

Además, debido a los cambios en el modelo de privilegios Windows, tanto los desarrolladores como sus usuarios finales pueden administrar la seguridad del sistema. Las nuevas mejoras permiten identificar fácilmente mensajes críticos para asegurarse de que los usuarios pueden acceder a las aplicaciones y características que necesitan sin poner en peligro sus sistemas. (Consulte el [Centro para desarrolladores de seguridad de MSDN).](https://msdn.microsoft.com/security/default.aspx)

## <a name="windows-filtering-platform"></a>Plataforma de filtrado de Windows

En Windows 7, la plataforma de filtrado de Windows se ha mejorado para proporcionar a los desarrolladores más control sobre la funcionalidad del firewall. Se ha aumentado el nivel de filtrado y los *ISV* ahora pueden conectar la protección personalizada y la detección en niveles inferiores. Además, los desarrolladores de firewall pueden activar o desactivar de forma selectiva partes de Windows Firewall.

Con Windows de filtrado, los desarrolladores pueden crear firewalls, sistemas de detección de intrusiones, programas antivirus, herramientas de supervisión de red y controles parentales en sus aplicaciones. Windows Filtering Platform se integra con y proporciona compatibilidad con una amplia variedad de características de firewall, incluida la comunicación autenticada y la configuración dinámica del firewall basada en el uso de la API de sockets de las aplicaciones (directiva basada en aplicaciones). Windows La plataforma de filtrado también proporciona infraestructura para la administración de directivas, las notificaciones de cambios, los diagnósticos de red y el filtrado con estado.

La arquitectura inicial de Windows Filtering Platform en Windows Vista proporcionaba funcionalidades para el tráfico basado en IP. Otros protocolos que no son IP, como el Protocolo de resolución de direcciones (ARP) y los protocolos de nivel de acceso multimedia *(MAC)* para la administración y autenticación de red, también requieren filtrado, inspección o registro. En Windows 7, se ha proporcionado una capa de inspección *de NDIS* que admite el filtrado *DE MAC* y *ETHERNET* para satisfacer esta necesidad. (Vea [Windows plataforma de filtrado).](../fwp/windows-filtering-platform-start-page.md)

## <a name="user-account-control"></a>Control de cuentas de usuario

El control de cuentas de usuario (UAC) es un componente de seguridad de Windows 7 que permite a los desarrolladores compilar aplicaciones que permiten a los usuarios realizar tareas comunes como no administradores. Los desarrolladores pueden reducir los riesgos de seguridad mediante la ejecución de aplicaciones bajo un token de usuario estándar, lo que reduce los riesgos de errores o ataques.

Las cuentas de usuario que son miembros del grupo local *Administradores* ejecutarán la mayoría de las aplicaciones como un usuario estándar. Al separar las funciones de usuario y administrador al mismo tiempo que se habilita la productividad, UAC proporciona a los desarrolladores un mayor control sobre el nivel de acceso que los usuarios tienen sobre las áreas protegidas de una aplicación. UAC solicita credenciales  en un modo de escritorio seguro, donde toda la pantalla está protegida para evitar la suplantación de la interfaz de usuario o del mouse. (Vea Actualizaciones [del cuadro de diálogo Control de cuentas de usuario](../win7appqual/user-interface---user-account-control-dialog-updates.md) y Control de cuentas de usuario y [WMI).](../wmisdk/user-account-control-and-wmi.md)

 

 
