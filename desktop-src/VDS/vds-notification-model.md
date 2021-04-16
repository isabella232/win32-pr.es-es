---
description: Notificaciones de VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notificaciones de VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa99751912f110a77b061d50134135413baf2894
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104550840"
---
# <a name="vds-notifications"></a>Notificaciones de VDS

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un proveedor puede enviar una notificación de eventos a VDS y VDS, a su vez, puede reenviar la notificación a las aplicaciones. El modelo de notificación que usa VDS es similar al modelo de punto de conexión utilizado por los objetos COM.

VDS genera notificaciones de servicio para eventos como una asignación de letra de unidad o la llegada de un disco sin asignar. Una vez que VDS asigna un disco a un proveedor, el proveedor es responsable de generar las notificaciones asociadas. En la ilustración siguiente se muestran las interfaces y los métodos utilizados en el modelo de notificación de VDS.

![Diagrama que muestra la interfaz y los métodos (Advise, OnLoad y alnotify) entre las aplicaciones, el servicio de disco virtual y los proveedores de V D S.](images/vdsnotification.png)

Para recibir notificaciones, VDS registra su interfaz [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con el objeto de proveedor llamando al método [**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) y pasando un puntero a la interfaz. Cuando se produce un evento de notificación, como la llegada de una unidad o volumen nuevo, el proveedor pasa la estructura de notificación adecuada a VDS como un parámetro de método [**IVdsAdviseSink:: alnotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

El proceso es similar entre una aplicación y VDS. En concreto, para recibir notificaciones, una aplicación registra su interfaz [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con Vds llamando al método [**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) y pasando un puntero a la interfaz. Cuando VDS recibe una notificación de un proveedor, pasa la estructura de notificación adecuada a las aplicaciones registradas como un parámetro de método [**IVdsAdviseSink:: alnotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify) .

> [!Note]  
> Una aplicación que llama a [**Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) debe llamar finalmente al método [**IVdsService:: Unadvise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) . Idealmente, debería llamar a **Unadvise** en cuanto ya no necesite recibir notificaciones.

 

En la tabla siguiente se enumeran las notificaciones generadas por el proveedor por tipo de objeto.



| Object     | notificación                              | Value | Vínculo a la descripción del evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **\_llegada del \_ paquete de NF de VDS \_**                 | 1     | [**\_notificación del paquete VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_componente del \_ paquete de NF de VDS \_**                 | 2     | [**\_notificación del paquete VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **\_ \_ modificar paquete de NF de VDS \_**                 | 3     | [**\_notificación del paquete VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volumen     | **llegada del volumen de VDS \_ NF \_ \_**               | 4     | [**\_notificación de volumen de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **descomponente de volumen de VDS \_ NF \_ \_**               | 5     | [**\_notificación de volumen de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **modificación del volumen de VDS \_ NF \_ \_**               | 6     | [**\_notificación de volumen de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **progreso de la regeneración del volumen de VDS \_ NF \_ \_ \_** | 7     | [**\_notificación de volumen de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **\_llegada del \_ disco \_ NF de VDS**                 | 8     | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **descomponente de \_ disco NF de VDS \_ \_**                 | 9     | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **modificación de disco de VDS \_ NF \_ \_**                 | 10    | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partición  | **llegada de la partición de VDS \_ NF \_ \_**            | 11    | [**\_notificación de partición de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partición  | **PARTE de la partición de VDS \_ NF \_ \_**            | 12    | [**\_notificación de partición de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partición  | **partición de VDS \_ NF \_ \_ modificate**            | 13    | [**\_notificación de partición de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **el \_ \_ \_ subsistema VDS NF \_ llega**          | 101   | [**\_notificación de \_ subsistema de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **subsistema VDS NF de VDS \_ \_ \_ \_**          | 102   | [**\_notificación de \_ subsistema de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **\_ \_ \_ modificación del subsistema de NF de VDS \_**          | 151   | [**\_notificación de \_ subsistema de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **\_llegada del \_ controlador VDS NF \_**           | 103   | [**\_notificación del controlador VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **COMPONENTE de controlador de VDS \_ NF \_ \_**           | 104   | [**\_notificación del controlador VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **modificación del controlador de VDS \_ NF \_ \_**           | 350   | [**\_notificación del controlador VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **controlador de VDS \_ NF \_ \_ quitado**          | 351   | [**\_notificación del controlador VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Port       | **\_ \_ modificar puerto de VDS NF \_**                 | 352   | [**\_notificación de Puerto VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Port       | **\_Puerto VDS \_ NF \_ quitado**                | 353   | [**\_notificación de Puerto VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Unidad      | **llegada de la \_ unidad VDS NF \_ \_**                | 105   | [**\_notificación de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **PARTE de la \_ unidad VDS NF \_ \_**                | 106   | [**\_notificación de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **\_unidad VDS \_ NF \_ Modify**                | 107   | [**\_notificación de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **\_unidad VDS \_ NF \_ quitada**               | 354   | [**\_notificación de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **llegada del LUN de VDS \_ NF \_ \_**                  | 108   | [**\_notificación de LUN de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **desformar LUNs de VDS \_ NF \_ \_**                  | 109   | [**\_notificación de LUN de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **modificación de LUN de VDS \_ NF \_ \_**                  | 110   | [**\_notificación de LUN de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS genera las notificaciones restantes. En la tabla siguiente se enumeran las constantes de notificación basadas en el servicio por categoría.



| Category     | notificación                                | Value | Vínculo a la descripción del evento                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disco         | **\_llegada del \_ disco \_ NF de VDS**                   | 8     | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **descomponente de \_ disco NF de VDS \_ \_**                   | 9     | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **modificación de disco de VDS \_ NF \_ \_**                   | 10    | [**\_notificación de disco de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Letra de unidad | **Letra de unidad de VDS \_ NF \_ \_ \_ gratis**            | 201   | [**\_notificación de \_ letra de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Letra de unidad | **\_asignación de \_ letra de unidad \_ \_ de VDS NF**          | 202   | [**\_notificación de \_ letra de unidad de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Sistema de archivos  | **\_ \_ \_ modificación del sistema de archivos de VDS NF \_**           | 203   | [**\_ \_ notificación del sistema de archivos VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Sistema de archivos  | **\_ \_ \_ progreso del formato del sistema de archivos \_ de VDS NF \_** | 204   | [**\_ \_ notificación del sistema de archivos VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volumen       | **cambios en los puntos de montaje de VDS \_ NF \_ \_ \_**          | 205   | [**\_notificación de \_ punto de montaje de VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink:: alnotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate:: OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService:: Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
