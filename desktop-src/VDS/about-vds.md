---
description: Acerca de VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Acerca de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104568264"
---
# <a name="about-vds"></a>Acerca de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El servicio de disco virtual es un servicio de Microsoft Windows que realiza operaciones de consulta y configuración en la solicitud de usuarios finales, scripts y aplicaciones. El servicio extiende las capacidades de almacenamiento existentes de los sistemas operativos Windows Server de las siguientes maneras:

-   Proporciona una API a las características de administración de volúmenes y discos existentes en Windows.
-   Unifica la administración de volúmenes y la administración de la matriz redundante de discos independientes (RAID) en una sola API.

VDS no realiza las siguientes actividades de administración de almacenamiento:

-   Administración de subsistemas de hardware, como la supervisión de temperatura o la supervisión de estadísticas de rendimiento para matrices de discos.
-   Administración del tejido de la red de área de almacenamiento (SAN), como la seguridad y la zona del adaptador de Host-Based (HBA).

En las secciones siguientes se describe la arquitectura de VDS, el rol de los proveedores de VDS y la API.

## <a name="service-architecture"></a>Arquitectura del servicio

VDS define tres interfaces: una única interfaz entre el nivel de aplicación y el servicio, y dos interfaces entre el servicio y los programas de proveedor en la capa de datos. En la ilustración siguiente se muestra el límite de aplicación a servicio y el límite de servicio a proveedor.

![Diagrama que muestra la arquitectura de servicio dividida en las secciones ' aplicaciones ', ' servicio de disco virtual ' y ' proveedores de VDS '.](images/vdsoverview.png)

La arquitectura de N niveles permite a VDS coordinar con las funciones del sistema de archivos, sincronizar las actividades del proveedor y arbitrar entre las aplicaciones. Al estar entre la aplicación y el proveedor, VDS presenta una funcionalidad uniforme a las aplicaciones, aunque algunos de los proveedores subyacentes no tengan tal uniformidad.

El servicio implementa la funcionalidad común: el formato de volúmenes, la adición y eliminación de Letras de unidad o carpetas montadas, así como la administración de discos sin asignar: discos que no tienen información de partición. VDS también devuelve notificaciones de eventos a las aplicaciones registradas. Para obtener más información, consulte [notificaciones de VDS](vds-notification-model.md).

## <a name="role-of-providers"></a>Rol de los proveedores

VDS define dos interfaces de proveedor, una para un proveedor de software y otra para un proveedor de hardware. Cada proveedor implementa una parte diferente de la API definida por VDS:

-   Un *proveedor de software* es un programa basado en host que es compatible con un controlador en modo kernel en la pila de e/s de almacenamiento. El tiempo de ejecución del proveedor-kernel interactúa con el administrador de montaje en el momento del arranque o con el administrador de Plug and Play (PnP) en el momento de la detección para reclamar cada disco. Los proveedores de software operan en volúmenes, discos y particiones de disco.

    VDS incluye dos tipos de proveedor. El proveedor de software básico administra los discos básicos y no ofrece ningún enlace tolerante a errores. El proveedor de software dinámico administra los discos dinámicos y ofrece administración de errores, si procede. El comportamiento del proveedor de software es coherente con el comportamiento de los discos básicos y dinámicos en el host. Por ejemplo, si el sistema operativo de un host determinado admite discos dinámicos tolerantes a errores, VDS también admite este comportamiento en el host.

-   Un *proveedor de hardware* implementa los métodos que se usan para administrar un subsistema de almacenamiento, una matriz de discos de hardware o una tarjeta adaptadora que permite la creación de discos lógicos configurados para mejorar el rendimiento, la disponibilidad de los datos o la recuperación de datos. Muchos principales fabricantes de contenedores de RAID han creado un proveedor de hardware diseñado para su uso con VDS. Los consumidores del servicio deben obtener un proveedor de hardware y el hardware asociado del fabricante.

    Las capacidades de un proveedor de hardware dependen de las capacidades del hardware subyacente. Por consiguiente, el grado en el que cada fabricante implementa la API puede variar. Por ejemplo, los fabricantes pueden incluir métodos adicionales para optimizar las configuraciones, supervisar y ajustar dinámicamente el rendimiento, automatizar la administración de errores o proporcionar otra funcionalidad beneficiosa.

    Los proveedores de hardware ofrecen varias opciones de configuración que no están disponibles para los proveedores de software. Lo más notable es el modelo de configuración de automagic, que presenta una vista de almacenamiento basada en atributos para cada aplicación. Las sugerencias de enlace, como "lecturas mayoritarias" o "Fast Crash Recovery Required", reemplazan la complejidad de enlazar el almacenamiento físico en el almacenamiento virtual. Cada proveedor de hardware realiza la asignación de extensiones, la asignación de espacio y la selección del tipo de enlace en función de las sugerencias que envía una aplicación. Para obtener una descripción completa del proveedor de hardware, incluidas las opciones de configuración, consulte la documentación proporcionada por el fabricante del subsistema.

## <a name="application-programming-interface"></a>Interfaz de programación de aplicaciones

Las aplicaciones pueden invocar métodos VDS para consultar y configurar discos basados en host, almacenamiento RAID o ambos. Para obtener información general sobre la API, consulte el [modelo de objetos de VDS](vds-object-model.md).

Las aplicaciones típicas de VDS resuelven los problemas de administración y supervisión de la configuración y van desde sistemas de administración de almacenamiento dedicados hasta aplicaciones de Back-Office que buscan un mejor control sobre la configuración o la administración de errores. Las aplicaciones siguientes usan VDS hoy:

-   El complemento Administración de discos configura y administra los discos controlados por un equipo host. Los administradores del sistema y los usuarios finales pueden consultar y configurar discos y volúmenes locales (o remotos) con esta herramienta de interfaz de usuario (IU).
-   Diskpart.exe es una utilidad de línea de comandos que configura y administra discos, volúmenes y particiones.
-   Diskraid.exe es una utilidad de línea de comandos que configura y administra los subsistemas RAID de hardware. Esta utilidad puede interactuar con cualquier hardware de almacenamiento que esté acompañado de un proveedor de hardware de VDS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Notificaciones de VDS](vds-notification-model.md)
</dt> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> </dl>

 

 
