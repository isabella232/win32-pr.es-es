---
description: Volver a enumerar y actualizar
ms.assetid: 67d34946-47df-43e2-8ca7-628d0671b869
title: Volver a enumerar y actualizar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f19d28d44234b773988f3038666212caf447fb45dee39435b0d99169f92212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125925"
---
# <a name="reenumerating-and-refreshing"></a>Volver a enumerar y actualizar

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio virtual [de](virtual-disk-service-portal.md) disco se reemplaza por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

La operación de reenumeración detecta los dispositivos recién conectados y recién desconectados. La operación de actualización actualiza la información de configuración de los dispositivos existentes.

**Para volver a enumerar objetos de proveedor de software**

-   Llame al [**método IVdsService::Reenumerate.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) Este método detecta todos los discos recién conectados y desconectados y las unidades de CD-ROM, y garantiza que todos los discos tengan el propietario adecuado. VDS posee discos sin procesar o discos con errores; el proveedor básico posee discos básicos; y el proveedor dinámico posee discos dinámicos. Esta operación puede implicar el examen de los bus del subsistema interno y la espera de tiempos de espera.

**Para volver a enumerar y actualizar objetos de proveedor de software**

-   Llame al [**método IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) y, a continuación, llame al [**método IVdsService::Refresh.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) Además de detectar los discos recién conectados y desconectados y las unidades de CD-ROM, esta combinación de métodos actualiza toda la información de disco, volumen y plex en la caché de VDS para los discos que no se han conectado o desconectado recientemente. Llame **a Refresh** solo para actualizar la información de propiedades de los objetos existentes en la memoria caché. Esta operación puede implicar el examen de los bus del subsistema interno y la espera de tiempos de espera. Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación. Además, llamar **a Refresh** en respuesta a una notificación VDS podría provocar que se enviara un bucle infinito de notificaciones. Por estos motivos, **solo se** debe llamar a Refresh cuando parezca que la memoria caché no se está actualizando correctamente.

**Para volver a enumerar subsistemas de hardware**

-   Llame al [**método IVdsHwProvider::Reenumerate.**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate) Dependiendo del proveedor, esta operación puede implicar el envío de paquetes de red y la espera de tiempos de espera, volver a examinar los bus SCSI y esperar tiempos de espera, y así sucesivamente.

**Para volver a enumerar los objetos del subsistema de hardware**

-   Llame al [**método IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate) para inventariar los objetos (normalmente unidades) del subsistema. Dependiendo del subsistema, esta operación puede implicar el examen de los bus del subsistema interno y la espera de tiempos de espera.

**Para actualizar subsistemas de hardware y objetos de subsistema**

-   Llame al [**método IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh) para actualizar la memoria caché de VDS de información sobre los subsistemas existentes administrados por proveedores de hardware VDS. Tenga en cuenta que VDS actualiza la memoria caché automáticamente cada vez que se produce un cambio que desencadena una notificación. Además, llamar [**a Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh) en respuesta a una notificación VDS podría provocar que se enviara un bucle infinito de notificaciones. Por estos motivos, **solo se** debe llamar a Refresh cuando parezca que la memoria caché no se está actualizando correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsService::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdsservice-refresh)
</dt> <dt>

[**IVdsHwProvider::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-reenumerate)
</dt> <dt>

[**IVdsSubSystem::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-reenumerate)
</dt> <dt>

[**IVdsHwProvider::Refresh**](/windows/desktop/api/Vds/nf-vds-ivdshwprovider-refresh)
</dt> </dl>

 

 
