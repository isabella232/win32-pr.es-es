---
title: Seguridad (guía para desarrolladores de Windows 7)
description: Windows 7 incluye características de seguridad nuevas y mejoradas que facilitan a los desarrolladores la mejora, el uso y la administración de la seguridad de sus aplicaciones.
ms.assetid: c3f19338-8ada-4ded-82a9-ca0869ad469d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a3b317f2fe0c7d42559245108bae6a5dbf0e6f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105685813"
---
# <a name="security-windows-7-developer-guide"></a>Seguridad (guía para desarrolladores de Windows 7)

Windows 7 incluye características de seguridad nuevas y mejoradas que facilitan a los desarrolladores la mejora, el uso y la administración de la seguridad de sus aplicaciones. Incluye una variedad de nuevas características de seguridad que no solo ayudan a protegerse frente a amenazas, sino que también limitan los daños que los atacantes pueden realizar si obtienen acceso a un equipo.

Las mejoras en la plataforma de filtrado de Windows permiten a los desarrolladores crear aplicaciones que interactúan con el procesamiento de paquetes en la pila de red del sistema operativo. Se pueden filtrar y modificar datos de red antes de que lleguen a su destino.

Además, debido a los cambios en el modelo de privilegios de Windows, la seguridad del sistema es más fácil de administrar tanto por parte de los desarrolladores como de sus usuarios finales. Las nuevas mejoras facilitan la identificación de los mensajes críticos para garantizar que los usuarios puedan acceder a las aplicaciones y características que necesitan sin poner en peligro sus sistemas. (Consulte el [Centro para desarrolladores de seguridad de MSDN](https://msdn.microsoft.com/security/default.aspx)).

## <a name="windows-filtering-platform"></a>Plataforma de filtrado de Windows

En Windows 7, la plataforma de filtrado de Windows se ha mejorado para ofrecer a los desarrolladores más control sobre la funcionalidad del firewall. El nivel de filtrado ha aumentado y los *ISV* ahora pueden conectar la protección y la detección personalizadas en los niveles inferiores. Además, los desarrolladores de Firewall pueden activar o desactivar partes del firewall de Windows de forma selectiva.

Con la plataforma de filtrado de Windows, los desarrolladores pueden crear firewalls, sistemas de detección de intrusiones, programas antivirus, herramientas de supervisión de red y controles parentales en sus aplicaciones. La plataforma de filtrado de Windows se integra con y proporciona compatibilidad con una amplia variedad de características de firewall, incluida la comunicación autenticada y la configuración de Firewall dinámica basada en el uso de las aplicaciones de sockets API (directiva basada en aplicaciones). La plataforma de filtrado de Windows también proporciona una infraestructura para la administración de directivas, las notificaciones de cambios, el diagnóstico de red y el filtrado con estado.

La arquitectura inicial de la plataforma de filtrado de Windows en Windows Vista proporcionaba funcionalidades para el tráfico basado en IP. Otros protocolos que no son IP, como los protocolos de nivel de protocolo de resolución de direcciones (ARP) y Media Access Control (*Mac*) para la autenticación y la administración de redes, también requieren filtrado, inspección o registro. En Windows 7, se ha proporcionado un nivel de inspección de *NDIS* que admite el filtrado de *Mac* y *Ethernet* para satisfacer esta necesidad. (Consulte [plataforma de filtrado de Windows](../fwp/windows-filtering-platform-start-page.md)).

## <a name="user-account-control"></a>Control de cuentas de usuario

Control de cuentas de usuario (UAC) es un componente de seguridad de Windows 7 que permite a los desarrolladores crear aplicaciones que permiten a los usuarios realizar tareas comunes como no administradores. Los desarrolladores pueden reducir los riesgos de seguridad mediante la ejecución de aplicaciones bajo un token de usuario estándar, lo que reduce los riesgos de errores o ataques.

Las cuentas de usuario que son miembros del grupo local *administradores* ejecutarán la mayoría de las aplicaciones como un usuario estándar. Al separar las funciones de usuario y de administrador al habilitar la productividad, UAC ofrece a los desarrolladores un mayor control sobre el nivel de acceso que tienen los usuarios sobre las áreas protegidas de una aplicación. UAC solicita credenciales en un modo de *escritorio seguro* , donde toda la pantalla está protegida para evitar la suplantación de la interfaz de usuario o el mouse. (Consulte [actualizaciones del cuadro de diálogo control de cuentas de usuario](../win7appqual/user-interface---user-account-control-dialog-updates.md) y [control de cuentas de usuario y WMI](../wmisdk/user-account-control-and-wmi.md)).

 

 
