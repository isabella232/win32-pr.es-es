---
description: Acerca de VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Acerca de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890433"
---
# <a name="about-vds"></a>Acerca de VDS

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Virtual Disk Service es un servicio de microsoft Windows que realiza operaciones de consulta y configuración a petición de usuarios finales, scripts y aplicaciones. El servicio amplía las funcionalidades de almacenamiento existentes de los Windows operativos server de las maneras siguientes:

-   Proporciona una API a las características de administración de volúmenes y discos existentes en Windows.
-   Unifica la administración de volúmenes y la administración de la matriz redundante de hardware de discos independientes (RAID) en una sola API.

VDS no realiza las siguientes actividades de administración de almacenamiento:

-   Administración del subsistema de hardware, como la supervisión de temperatura o la supervisión de estadísticas de rendimiento para matrices de discos.
-   Storage Administración del tejido de red de área (SAN), como la seguridad y la Host-Based adaptador de red de área (HBA).

En las secciones siguientes se describe la arquitectura de VDS, el rol de los proveedores de VDS y la API.

## <a name="service-architecture"></a>Arquitectura del servicio

VDS define tres interfaces: una única interfaz entre el nivel de aplicación y el servicio, y dos interfaces entre los programas de servicio y proveedor de la capa de datos. En la ilustración siguiente se muestra el límite de aplicación a servicio y el límite de servicio a proveedor.

![Diagrama que muestra la arquitectura del servicio dividida en las secciones "Aplicaciones", "Servicio de disco virtual" y "Proveedores vds".](images/vdsoverview.png)

La arquitectura de n niveles permite que VDS se coordine con las funciones del sistema de archivos, sincronice las actividades del proveedor y entre las aplicaciones. Al estar entre la aplicación y el proveedor, VDS presenta una funcionalidad uniforme a las aplicaciones, aunque algunos proveedores subyacentes podrían carecer de dicha uniformidad.

El servicio implementa una funcionalidad común: dar formato a volúmenes, agregar y quitar letras de unidad o carpetas montadas, así como administrar discos sin asignar, discos que no tienen información de partición. VDS también devuelve notificaciones de eventos a las aplicaciones registradas. Para obtener más información, [vea Vds Notifications](vds-notification-model.md).

## <a name="role-of-providers"></a>Rol de proveedores

VDS define dos interfaces de proveedor, una para un proveedor de software y otra para un proveedor de hardware. Cada proveedor implementa una parte diferente de la API definida por VDS:

-   Un *proveedor de software* es un programa basado en host que es compatible con un controlador en modo kernel en la pila de E/S de almacenamiento. El tiempo de ejecución del kernel del proveedor interactúa con el administrador de montaje en tiempo de arranque o con el administrador de Plug and Play (PnP) en tiempo de detección para reclamar cada disco. Los proveedores de software operan en volúmenes, discos y particiones de disco.

    VDS incluye dos tipos de proveedor. El proveedor de software básico administra discos básicos y no ofrece ningún enlace tolerante a errores. El proveedor de software dinámico administra discos dinámicos y ofrece administración de errores si procede. El comportamiento del proveedor de software es coherente con el comportamiento de los discos básicos y dinámicos en el host. Por ejemplo, si el sistema operativo de un host determinado admite discos dinámicos tolerantes a errores, VDS también admite este comportamiento en el host.

-   Un *proveedor de hardware* implementa los métodos que se usan para administrar un subsistema de almacenamiento: una matriz de disco de hardware o una tarjeta de adaptador que permite la creación de discos lógicos configurados para mejorar el rendimiento, la disponibilidad de datos o la recuperación de datos. Muchos fabricantes principales de gabinetes RAID han producido un proveedor de hardware diseñado para su uso con VDS. Los consumidores de servicios deben obtener un proveedor de hardware y hardware asociado del fabricante.

    Las funcionalidades de un proveedor de hardware dependen de las funcionalidades del hardware subyacente. Por lo tanto, el grado en que cada fabricante implementa la API puede variar. Por ejemplo, los fabricantes pueden incluir métodos adicionales para optimizar las configuraciones, supervisar y ajustar dinámicamente el rendimiento, automatizar la administración de errores o proporcionar otra funcionalidad beneficiosa.

    Los proveedores de hardware ofrecen varias opciones de configuración que no están disponibles para los proveedores de software. Lo más destacado es el modelo de configuración de automagic, que presenta una vista basada en atributos del almacenamiento a cada aplicación. Las sugerencias de enlace, como "lecturas principalmente" o "recuperación rápida de bloqueos necesarias" reemplazan la complejidad del enlace del almacenamiento físico al almacenamiento virtual. Cada proveedor de hardware realiza la asignación de extensiones, la asignación de espacio y la selección de tipos de enlace en función de las sugerencias enviadas por una aplicación. Para obtener la descripción completa del proveedor de hardware, incluidas las opciones de configuración, consulte la documentación proporcionada por el fabricante del subsistema.

## <a name="application-programming-interface"></a>Interfaz de programación de aplicaciones

Las aplicaciones pueden invocar métodos VDS para consultar y configurar discos basados en host, almacenamiento RAID o ambos. Para obtener información general sobre la API, vea [VdS Object Model](vds-object-model.md).

Las aplicaciones típicas para VDS resuelven problemas de supervisión y administración de configuración, y van desde sistemas de administración de almacenamiento dedicados hasta aplicaciones de back-office que buscan un mejor control sobre la configuración o la administración de errores. Las aplicaciones siguientes usan VDS hoy en día:

-   El complemento Administración de discos configura y administra los discos controlados por un equipo host. Los administradores del sistema y los usuarios finales pueden consultar y configurar discos y volúmenes locales (o remotos) con esta herramienta de interfaz de usuario (UI).
-   Diskpart.exe es una utilidad de línea de comandos que configura y administra discos, volúmenes y particiones.
-   Diskraid.exe es una utilidad de línea de comandos que configura y administra subsistemas RAID de hardware. Esta utilidad puede interactuar con cualquier hardware de almacenamiento que vaya acompañado de un proveedor de hardware VDS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Notificaciones VDS](vds-notification-model.md)
</dt> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> </dl>

 

 
