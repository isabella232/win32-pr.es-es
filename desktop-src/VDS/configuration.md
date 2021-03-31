---
description: Información general de configuración
ms.assetid: 5cdc21a1-ff55-4c36-8106-b045256778ce
title: Información general de configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4db13827bf08ee65ed8015f0c19ba2980a9a71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001074"
---
# <a name="configuration-overview"></a>Información general de configuración

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Si no está familiarizado con los objetos definidos por VDS, consulte el modelo de [objetos de VDS](vds-object-model.md).

La complejidad de la configuración de un disco virtual puede variar de muy fácil a ajustar. Los discos virtuales de empresa, sin necesidad de asistencia y de asistencia médica, definen tres perspectivas de configuración típicas. Cada perspectiva presenta requisitos ligeramente diferentes:

-   Los discos virtuales sin asistencia se configuran de manera ligera, quizás solo para automatizar la creación de particiones y el formato de discos nuevos, o para crear temporalmente un volumen reflejado para migrar datos de un disco a otro sin tiempo de inactividad. Estos discos son buenos para equipos portátiles y otros sistemas con uno o varios discos.
-   Los discos virtuales gratuitos proporcionan almacenamiento que aparece autoconfigurable, recuperación automática y disponible; usa volúmenes seccionados y LUN para lograr un mejor rendimiento; utiliza volúmenes reflejados y LUN para lograr una mejor disponibilidad. y usa los paquetes para que los modos de error se limpien y contengan. Este nivel de configuración es ideal cuando se reemplazan los discos del sistema antiguos, pequeños y lentos con discos nuevos, grandes y rápidos. También es ideal para la creación de reflejo de datos con la reserva activa automatizada: un único eje de reserva puede proteger muchos ejes. Para obtener más información, consulte [reserva activa](hot-sparing.md).

    Las San a pequeña escala dependen de la flexibilidad y la automatización que ofrece este nivel de configuración, al igual que los dispositivos de almacenamiento conectado a la red (NAS). Los discos virtuales gratuitos de asistencia simplifican la tarea de consolidar el almacenamiento de aplicaciones, por ejemplo, el almacenamiento de SQL y Exchange, sin consolidar los servidores.

-   Los discos virtuales de empresa contienen configuraciones empresariales muy grandes o complejas con requisitos adicionales específicos del sitio o específicos de la aplicación. Los administradores ajustan el subsistema de almacenamiento para una aplicación única que podría ejecutarse solo con poca frecuencia, como un trabajo de informes de Batch mensual en un sistema de transacciones que toma un pedido. Los discos virtuales empresariales deben escalarse, Mostrar la actividad en tiempo real del subsistema de almacenamiento y cumplir los requisitos de los administradores prácticos.

Para obtener más información acerca de los reflejos, las franjas y las demás opciones de configuración de VDS, consulte [enlace de volumen y LUN](volume-and-lun-binding.md). Una técnica de configuración avanzada, denominada apilamiento, le permite combinar las configuraciones que están asociadas a volúmenes y LUN existentes. Para obtener más información, consulte [Stacking de configuración](configuration-stacking.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de disco virtual](virtual-disk-service-portal.md)
</dt> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[Reserva activa](hot-sparing.md)
</dt> <dt>

[Enlace de volúmenes y LUN](volume-and-lun-binding.md)
</dt> <dt>

[Apilamiento de configuración](configuration-stacking.md)
</dt> </dl>

 

 
