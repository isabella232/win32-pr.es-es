---
description: VDS proporciona objetos para realizar actividades relacionadas con el servicio. En este tema se describe cada objeto.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Inicio y objetos de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678422"
---
# <a name="startup-and-service-objects"></a>Inicio y objetos de servicio

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona objetos para realizar actividades relacionadas con el servicio. En este tema se describe cada objeto.

## <a name="service-loader-object"></a>Objeto de cargador de servicios

El objeto de cargador de servicios proporciona los métodos que usan las aplicaciones para cargar e inicializar VDS. Para preparar el VDS para su uso, una aplicación debe realizar las siguientes operaciones:

-   Cree una instancia del objeto de cargador de servicios, que devuelve la interfaz [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader) .
-   Llame al método [**IVdsServiceLoader:: LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para cargar el servicio.

Para obtener un ejemplo de código, consulte [carga de VDS](loading-vds.md).

Permita siempre que el servicio se inicialice completamente antes de llamar a los métodos expuestos por el objeto de servicio. Use el método [**IVdsService:: IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) para determinar el estado del proceso de carga. Use el método [**IVdsService:: WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para bloquear llamadas a objetos VDS hasta que se complete la inicialización.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Enumeraciones asociadas                           | Ninguno.                                           |
| Estructuras asociadas                             | Ninguno.                                           |



 

## <a name="service-object"></a>Objeto de servicio

El objeto de servicio es un objeto multifuncionable que es fundamental para todas las aplicaciones de VDS. Con este objeto, un llamador puede realizar las siguientes operaciones:

-   Determine el estado de la inicialización del servicio.
-   Recupere todos los proveedores de hardware o software registrados con VDS.
-   Informe en discos sin asignar.
-   Devuelve el tipo de sistema de archivos y la letra de unidad asociada a los volúmenes de un disco.
-   Quite las rutas de acceso de modo de usuario y las carpetas montadas no utilizadas del registro y actualice los discos.
-   Recibir notificaciones de VDS.
-   Reinicie el host.
-   Recupere Canal de fibra puertos HBA o adaptadores de iniciador iSCSI en el equipo local.
-   Preparar de forma segura los LUN expuestos como discos en el equipo local para su eliminación.

Las estructuras de notificación de VDS pasan los GUID de objeto a todas las aplicaciones que están registradas con VDS para recibir notificaciones. Use el método [**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para convertir un GUID de objeto en un puntero de objeto. Para obtener una descripción más completa del modelo de notificación, consulte [notificaciones de VDS](vds-notification-model.md).

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* , [**IVdsServiceIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* , [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfaces que siempre se implementan pero no se exponen a las aplicaciones | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumeraciones asociadas                                                | [**VDS \_ \_ \_ marca de proveedor de consultas**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**\_ \_ tipo de objeto VDS**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**\_ \_ marca de servicio VDS**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**\_ \_ \_ marca de letra de unidad VDS**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**\_ \_ \_ marca del sistema de archivos**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag)VDS, [**\_ \_ \_ \_ marca de Prop del sistema de archivos VDS**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Estructuras asociadas                                                  | [**VDS \_ \_prop de servicio**](/windows/desktop/api/Vds/ns-vds-vds_service_prop), [**\_ \_ \_ Prop del sistema de archivos VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), tipo de sistema de [**archivos VDS \_ \_ \_ \_ prop**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), [**\_ \_ \_ notificación de letra de unidad VDS**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), notificación [**\_ \_ del sistema \_ de archivos VDS**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**notificación de punto de montaje de VDS \_ \_ \_**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** estas interfaces no se admiten hasta Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Objeto de adaptador de iniciador

Un objeto de adaptador de iniciador modela un adaptador de iniciador iSCSI en el equipo host del servicio VDS. El servicio VDS solo puede ver los adaptadores de iniciador en el equipo local. El rol de un objeto de adaptador de iniciador es para administrar las sesiones de inicio de sesión del equipo local a los destinos iSCSI.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Enumeraciones asociadas                           | [**VDS \_ \_ \_ tipo de inicio de sesión iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ \_ \_ marca de inicio de sesión iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag), [**\_ \_ \_ tipo de autenticación iSCSI de VDS**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Estructuras asociadas                             | [**VDS \_ \_ \_ \_ prop. del adaptador del iniciador iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop).                                                                                        |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Objeto de portal iniciador

Un objeto de portal iniciador modela un portal del iniciador iSCSI en un iniciador iSCSI. Un portal de iniciador es la combinación de una dirección IP y un puerto a través del cual un equipo host se conecta a un portal en un subsistema iSCSI. El rol de un objeto de portal iniciador es servir como uno de los puntos de conexión de una ruta MPIO y para configurar las opciones de seguridad de IPSEC.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Enumeraciones asociadas                           | [**VDS \_ \_ \_ marca IPSec iSCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Estructuras asociadas                             | [**VDS \_ \_propuesta del \_ portal \_ del iniciador iSCSI**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**\_ \_ \_ clave IPSec iSCSI de VDS**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**\_ dirección IP de VDS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="hba-port-object"></a>Objeto de puerto HBA

El objeto de puerto HBA modela un puerto Canal de fibra adaptador de bus host (HBA).

Use el método [**IVdsServiceHba:: QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) para determinar los puertos HBA que se conocen en VDS en el equipo local.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Enumeraciones asociadas                           | [**VDS \_ \_tipo HBAPORT**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**\_ \_ Estado de HBAPORT de VDS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**\_ \_ \_ marca de velocidad de VDS HBAPORT**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Estructuras asociadas                             | [**VDS \_ \_prop HBAPORT**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos de VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Cargando VDS](loading-vds.md)
</dt> <dt>

[**IVdsService:: GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notificaciones de VDS](vds-notification-model.md)
</dt> </dl>

 

 
