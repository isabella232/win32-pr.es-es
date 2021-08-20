---
description: Información general sobre la configuración
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Información general sobre la configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b742cb5ca2f287cd8b50b9f248d0ebec1174bfd71b59f0630bd9fb98864309c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007955"
---
# <a name="configuration-overview"></a>Información general sobre la configuración

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Si no está familiarizado con los objetos definidos por VDS, vea [VdS Object Model](vds-object-model.md).

La complejidad de la configuración de un disco virtual puede oscilar entre muy simple y precisa. Los discos virtuales empresariales, sin cuidado y sin cuidado definen tres perspectivas de configuración típicas. Cada perspectiva presenta requisitos ligeramente diferentes:

-   Los discos virtuales sin cuidado están ligeramente configurados, quizás solo para automatizar la creación de particiones y el formato de discos nuevos, o para crear temporalmente un volumen reflejado para migrar datos de un disco a otro sin tiempo de inactividad. Estos discos son buenos para equipos de cuadernos y otros sistemas con uno o varios discos.
-   Los discos virtuales sin asistencia proporcionan almacenamiento que parece autoconfiguración, recuperación automática y disponible. usa volúmenes seccionados y LUN para lograr un mejor rendimiento. usa volúmenes reflejados y LUN para lograr una mejor disponibilidad. y usa paquetes para que los modos de error se limpien y contengan. Este nivel de configuración es ideal cuando se reemplazan discos del sistema antiguos, pequeños y lentos por discos nuevos, grandes y rápidos. También es ideal para la creación de reflejo de los datos con una zona de acceso caliente automatizada: un solo eje de reserva puede proteger muchos ejes. Para obtener más información, vea [Hot Sparing](hot-sparing.md).

    Las REDES SAN a pequeña escala dependen de la flexibilidad y la automatización que ofrece este nivel de configuración, al igual que los dispositivos conectados a Storage (NAS). Los discos virtuales sin cuidado simplifican la tarea de consolidar el almacenamiento de aplicaciones(por ejemplo, el almacenamiento para SQL y Exchange) sin consolidar los servidores.

-   Enterprise discos virtuales contienen configuraciones empresariales muy grandes o complejas con requisitos adicionales específicos del sitio o específicos de la aplicación. Los administradores ajusten el subsistema de almacenamiento para una sola aplicación que podría ejecutarse con poca frecuencia, como un trabajo de informes por lotes mensual en un sistema de transacciones de pedidos. Enterprise discos virtuales deben escalarse, mostrar la actividad en tiempo real del subsistema de almacenamiento y satisfacer los requisitos de los administradores activos.

Para obtener información adicional sobre los reflejos, las franjas y las otras opciones de configuración de VDS, vea [Enlace de volumen y LUN.](volume-and-lun-binding.md) Una técnica de configuración avanzada, denominada apilamiento, permite combinar las configuraciones asociadas a volúmenes y LUN existentes. Para obtener más información, vea [Apilado de configuración.](configuration-stacking.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[Hot Sparing](hot-sparing.md)
</dt> <dt>

[Enlace de volúmenes y LUN](volume-and-lun-binding.md)
</dt> <dt>

[Apilamiento de configuración](configuration-stacking.md)
</dt> </dl>

 

 
