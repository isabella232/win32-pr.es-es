---
description: Reenumerar y actualizar
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Reenumerar y actualizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4a6302c817390ea2eb6bda3d5da0302c4bfefbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697261"
---
# <a name="reenumerating-and-refreshing"></a>Reenumerar y actualizar

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La operación de reenumeración detecta los dispositivos recién conectados y recién desconectados. La operación de actualización actualiza la información de configuración de los dispositivos existentes.

**Para reenumerar objetos de proveedor de software**

-   Llame al método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) . Este método detecta todos los discos y unidades de CD-ROM recién conectados y desconectados, y garantiza que todos los discos tienen el propietario adecuado. VDS posee discos sin procesar o discos con errores. el proveedor básico posee los discos básicos; y el proveedor dinámico posee discos dinámicos. Esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera.

**Para reenumerar y actualizar objetos de proveedor de software**

-   Llame al método [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) y, después, llame al método [**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) . Además de detectar discos y unidades de CD-ROM recién conectados y desconectados, esta combinación de métodos actualiza toda la información de disco, volumen y Plex en la memoria caché de VDS para los discos que no se han conectado o desconectado recientemente. Llame solo a **Actualizar** para actualizar la información de propiedades de los objetos existentes en la memoria caché. Esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera. Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación. Además, llamar a **Refresh** en respuesta a una notificación de VDS podría provocar que se envíe un bucle interminable de notificaciones. Por estos motivos, solo se debe llamar a **Refresh** cuando parezca que la memoria caché no se está actualizando correctamente.

**Para reenumerar los subsistemas de hardware**

-   Llame al método [**IVdsHwProvider:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) . En función del proveedor, esta operación puede implicar el envío de paquetes de red y la espera de tiempos de espera, el reexamen de buses SCSI y la espera de tiempos de espera, etc.

**Para reenumerar objetos de subsistema de hardware**

-   Llame al método [**IVdsSubSystem:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) para inventariar los objetos (normalmente unidades) del subsistema. En función del subsistema, esta operación puede implicar la exploración de buses internos del subsistema y la espera de tiempos de espera.

**Para actualizar subsistemas de hardware y objetos de subsistema**

-   Llame al método [**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) para actualizar la memoria caché de VDS de la información sobre los subsistemas existentes administrados por los proveedores de hardware de Vds. Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación. Además, llamar a [**Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) en respuesta a una notificación de VDS podría provocar que se envíe un bucle interminable de notificaciones. Por estos motivos, solo se debe llamar a **Refresh** cuando parezca que la memoria caché no se está actualizando correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[**IVdsService:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem:: reenumerar**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider:: Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
