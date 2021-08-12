---
description: Notificaciones VDS
ms.assetid: a0841215-3eb0-4769-b320-4da25b535362
title: Notificaciones VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 931731cc9c2b4aa73f7599c1fcbfad2f885bc74978ab15ba4e1efbf9d2a7522c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603122"
---
# <a name="vds-notifications"></a>Notificaciones VDS

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un proveedor puede enviar una notificación de eventos a VDS y VDS puede reenviar a su vez la notificación a las aplicaciones. El modelo de notificación que usa VDS es similar al modelo de punto de conexión que usan los objetos COM.

VDS genera notificaciones de servicio para eventos como una asignación de letra de unidad o la llegada de un disco sin asignar. Una vez que VDS asigna un disco a un proveedor, el proveedor es responsable de generar las notificaciones asociadas. En la ilustración siguiente se muestran las interfaces y los métodos usados en el modelo de notificación VDS.

![Diagrama que muestra la interfaz y los métodos (Advise, OnLoad y OnNotify) entre aplicaciones, servicios de disco virtual y proveedores de VD S.](images/vdsnotification.png)

Para recibir notificaciones, VDS registra su interfaz [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con el objeto de proveedor llamando al método [**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) y pasando un puntero a la interfaz. Cuando se produce un evento de notificación, como la llegada de un nuevo volumen o unidad, el proveedor pasa la estructura de notificación adecuada a VDS como un parámetro de método [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

El proceso es similar entre una aplicación y VDS. En concreto, para recibir notificaciones, una aplicación registra su interfaz [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink) con VDS llamando al método [**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) y pasando un puntero a la interfaz. Cuando VDS recibe una notificación de un proveedor, pasa la estructura de notificación adecuada a las aplicaciones registradas como un parámetro de método [**IVdsAdviseSink::OnNotify.**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)

> [!Note]  
> Una aplicación que llama [**a Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise) debe llamar finalmente al [**método IVdsService::Unadvise.**](/windows/desktop/api/Vds/nf-vds-ivdsservice-unadvise) Lo ideal es llamar **a Unadvise** en cuanto ya no necesite recibir notificaciones.

 

En la tabla siguiente se enumeran las notificaciones generadas por el proveedor por tipo de objeto.



| Object     | Notificación                              | Value | Vínculo a la descripción del evento                                             |
|------------|-------------------------------------------|-------|-----------------------------------------------------------------------|
| Pack       | **VDS \_ NF \_ PACK \_ ARRIVE**                 | 1     | [**NOTIFICACIÓN DE VDS \_ \_ PACK**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **VDS \_ NF \_ PACK \_ DEPART**                 | 2     | [**NOTIFICACIÓN DE VDS \_ \_ PACK**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Pack       | **MODIFICACIÓN DEL \_ PAQUETE VDS NF \_ \_**                 | 3     | [**NOTIFICACIÓN DE VDS \_ \_ PACK**](/windows/desktop/api/Vds/ns-vds-vds_pack_notification)              |
| Volumen     | **LLEGAN \_ VOLÚMENES VDS NF \_ \_**               | 4     | [**NOTIFICACIÓN POR \_ VOLUMEN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **VDS \_ NF \_ VOLUME \_ DEPART**               | 5     | [**NOTIFICACIÓN POR \_ VOLUMEN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **MODIFICACIÓN DEL \_ VOLUMEN VDS NF \_ \_**               | 6     | [**NOTIFICACIÓN POR \_ VOLUMEN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Volumen     | **PROGRESO DE \_ RECOMPILACIÓN DE VOLUMEN VDS NF \_ \_ \_** | 7     | [**NOTIFICACIÓN POR \_ VOLUMEN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_volume_notification)          |
| Disco       | **LLEGAN DISCOS \_ VDS NF \_ \_**                 | 8     | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **VDS \_ NF \_ DISK \_ DEPART**                 | 9     | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Disco       | **MODIFICACIÓN DEL \_ DISCO VDS NF \_ \_**                 | 10    | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)              |
| Partition  | **LLEGAN PARTICIONES \_ VDS NF \_ \_**            | 11    | [**NOTIFICACIÓN DE \_ PARTICIÓN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **VDS \_ NF \_ PARTITION \_ DEPART**            | 12    | [**NOTIFICACIÓN DE \_ PARTICIÓN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Partition  | **MODIFICACIÓN DE \_ LA PARTICIÓN VDS NF \_ \_**            | 13    | [**NOTIFICACIÓN DE \_ PARTICIÓN VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_partition_notification)    |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ ARRIVE**          | 101   | [**NOTIFICACIÓN DEL \_ SUBS \_ SISTEMA \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ DEPART**          | 102   | [**NOTIFICACIÓN DEL \_ SUBS \_ SISTEMA \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Subsystem  | **VDS \_ NF \_ SUB \_ SYSTEM \_ MODIFY**          | 151   | [**NOTIFICACIÓN DEL \_ SUBS \_ SISTEMA \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_sub_system_notification) |
| Controller | **LLEGADA DEL \_ CONTROLADOR VDS NF \_ \_**           | 103   | [**NOTIFICACIÓN DEL \_ CONTROLADOR VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **SALIDA DEL \_ CONTROLADOR VDS NF \_ \_**           | 104   | [**NOTIFICACIÓN DEL \_ CONTROLADOR VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **MODIFICACIÓN DEL \_ CONTROLADOR VDS NF \_ \_**           | 350   | [**NOTIFICACIÓN DEL \_ CONTROLADOR VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Controller | **CONTROLADOR \_ VDS NF \_ \_ ELIMINADO**          | 351   | [**NOTIFICACIÓN DEL \_ CONTROLADOR VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_controller_notification)  |
| Port       | **MODIFICACIÓN DEL \_ PUERTO VDS NF \_ \_**                 | 352   | [**NOTIFICACIÓN DE \_ PUERTO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Port       | **SE HA QUITADO \_ EL PUERTO VDS NF. \_ \_**                | 353   | [**NOTIFICACIÓN DE \_ PUERTO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_port_notification)              |
| Unidad      | **LLEGA LA \_ UNIDAD VDS NF \_ \_**                | 105   | [**NOTIFICACIÓN DE UNIDAD \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **VDS \_ NF \_ DRIVE \_ DEPART**                | 106   | [**NOTIFICACIÓN DE UNIDAD \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **MODIFICACIÓN DE \_ UNIDAD VDS NF \_ \_**                | 107   | [**NOTIFICACIÓN DE UNIDAD \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| Unidad      | **UNIDAD \_ VDS NF \_ \_ ELIMINADA**               | 354   | [**NOTIFICACIÓN DE UNIDAD \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_notification)            |
| LUN        | **LLEGAN \_ LUN VDS NF \_ \_**                  | 108   | [**NOTIFICACIÓN VDS \_ LUN \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **VDS \_ NF \_ LUN \_ DEPART**                  | 109   | [**NOTIFICACIÓN VDS \_ LUN \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |
| LUN        | **MODIFICACIÓN DE \_ LUN VDS NF \_ \_**                  | 110   | [**NOTIFICACIÓN VDS \_ LUN \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                |



 

VDS genera las notificaciones restantes. En la tabla siguiente se enumeran las constantes de notificación basadas en servicios por categoría.



| Category     | Notificación                                | Value | Vínculo a la descripción del evento                                                 |
|--------------|---------------------------------------------|-------|---------------------------------------------------------------------------|
| Disco         | **LLEGAN DISCOS \_ VDS NF \_ \_**                   | 8     | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **VDS \_ NF \_ DISK \_ DEPART**                   | 9     | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Disco         | **MODIFICACIÓN DEL \_ DISCO VDS NF \_ \_**                   | 10    | [**NOTIFICACIÓN DE \_ DISCO VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_disk_notification)                  |
| Letra de unidad | **LETRA DE \_ UNIDAD VDS NF \_ SIN \_ \_ LETRA**            | 201   | [**NOTIFICACIÓN DE LETRA DE UNIDAD VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Letra de unidad | **ASIGNACIÓN DE \_ LETRA DE UNIDAD VDS NF \_ \_ \_**          | 202   | [**NOTIFICACIÓN DE LETRA DE UNIDAD VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification) |
| Sistema de archivos  | **MODIFICACIÓN DEL \_ SISTEMA DE ARCHIVOS VDS NF \_ \_ \_**           | 203   | [**NOTIFICACIÓN DEL \_ SISTEMA DE \_ ARCHIVOS \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Sistema de archivos  | **PROGRESO DEL \_ FORMATO DEL SISTEMA DE ARCHIVOS VDS NF \_ \_ \_ \_** | 204   | [**NOTIFICACIÓN DEL \_ SISTEMA DE \_ ARCHIVOS \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification)   |
| Volumen       | **CAMBIO DE \_ LOS PUNTOS DE MONTAJE DE VDS NF \_ \_ \_**          | 205   | [**NOTIFICACIÓN DE \_ PUNTO DE \_ MONTAJE VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification)   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)
</dt> <dt>

[**IVdsAdviseSink::OnNotify**](/windows/desktop/api/Vds/nf-vds-ivdsadvisesink-onnotify)
</dt> <dt>

[**IVdsProviderPrivate::OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> <dt>

[**IVdsService::Advise**](/windows/desktop/api/Vds/nf-vds-ivdsservice-advise)
</dt> </dl>

 

 
