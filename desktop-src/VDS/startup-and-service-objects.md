---
description: VDS proporciona objetos para realizar actividades relacionadas con el servicio. En este tema se describe cada objeto.
ms.assetid: ae4d18f2-4d50-480c-bc7a-4eec0334707d
title: Objetos de inicio y servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92beb0a4f825f767299a7ced74d43ef2487fa252
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890385"
---
# <a name="startup-and-service-objects"></a>Objetos de inicio y servicio

\[A partir de Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se reemplaza [por el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

VDS proporciona objetos para realizar actividades relacionadas con el servicio. En este tema se describe cada objeto.

## <a name="service-loader-object"></a>Objeto Service Loader

El objeto del cargador de servicios proporciona los métodos que usan las aplicaciones para cargar e inicializar VDS. Para preparar VDS para su uso, una aplicación debe realizar las siguientes operaciones:

-   Cree una instancia del objeto del cargador de servicios, que devuelve la [**interfaz IVdsServiceLoader.**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader)
-   Llame al [**método IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) para cargar el servicio.

Para obtener un ejemplo de código, vea [Carga de VDS.](loading-vds.md)

Permita siempre que el servicio se inicialice completamente antes de llamar a los métodos expuestos por el objeto de servicio. Use el [**método IVdsService::IsServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-isserviceready) para determinar el estado del proceso de carga. Use el [**método IVdsService::WaitForServiceReady**](/windows/desktop/api/Vds/nf-vds-ivdsservice-waitforserviceready) para bloquear las llamadas a objetos VDS hasta que se complete la inicialización.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas.

| Tipo                                              | Elemento                                         |
|---------------------------------------------------|-------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsServiceLoader**](/windows/desktop/api/Vds/nn-vds-ivdsserviceloader). |
| Enumeraciones asociadas                           | Ninguno.                                           |
| Estructuras asociadas                             | Ninguno.                                           |



 

## <a name="service-object"></a>Objeto de servicio

El objeto de servicio es un objeto multifuncional que es fundamental para todas las aplicaciones VDS. Con este objeto, un llamador puede realizar las siguientes operaciones:

-   Determine el estado de la inicialización del servicio.
-   Recupere todos los proveedores de hardware o software registrados con VDS.
-   Informe sobre discos sin asignar.
-   Devuelve el tipo de sistema de archivos y la letra de unidad asociadas a los volúmenes de un disco.
-   Quite las rutas de acceso en modo de usuario no utilizadas y las carpetas montadas del Registro y actualice los discos.
-   Recibir notificaciones VDS.
-   Reinicie el host.
-   Recupere Canal de fibra HBA o adaptadores de iniciador iSCSI en el equipo local.
-   Prepare los LUN expuestos de forma segura como discos en el equipo local para su eliminación.

Las estructuras de notificación vds pasan GUID de objeto a todas las aplicaciones registradas con VDS para recibir notificaciones. Use el [**método IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) para convertir un GUID de objeto en un puntero de objeto. Para obtener una descripción más completa del modelo de notificación, vea [VdS Notifications](vds-notification-model.md).

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                                                   | Elemento                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                      | [**IVdsService**](/windows/desktop/api/Vds/nn-vds-ivdsservice), [**IVdsServiceHba,**](/windows/desktop/api/Vds/nn-vds-ivdsservicehba) \* [**IVdsServiceIscsi,**](/windows/desktop/api/Vds/nn-vds-ivdsserviceiscsi) \* [**IVdsServiceUninstallDisk**](/windows/desktop/api/Vds/nn-vds-ivdsserviceuninstalldisk) \* .                                                                                                                                                                                                           |
| Interfaces que siempre se implementan pero no se exponen a las aplicaciones | [**IVdsAdmin**](/windows/desktop/api/VdsHwPrv/nn-vdshwprv-ivdsadmin)                                                                                                                                                                                                                                                                                                                                                                            |
| Enumeraciones asociadas                                                | [**VDS \_ QUERY \_ PROVIDER \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_query_provider_flag), [**VDS OBJECT \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_object_type), [**VDS SERVICE \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_service_flag), [**VDS DRIVE LETTER \_ \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_drive_letter_flag), [**VDS FILE SYSTEM \_ \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_file_system_flag), [**VDS FILE SYSTEM PROP \_ \_ \_ \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_file_system_prop_flag).                                                      |
| Estructuras asociadas                                                  | [**VDS \_ SERVICE \_ PROP,**](/windows/desktop/api/Vds/ns-vds-vds_service_prop) [**VDS \_ FILE SYSTEM \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_prop), [**VDS FILE SYSTEM \_ TYPE \_ \_ \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_file_system_type_prop), [**VDS DRIVE LETTER \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_drive_letter_notification), [**VDS FILE SYSTEM \_ \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_file_system_notification), [**VDS \_ MOUNT POINT \_ \_ NOTIFICATION**](/windows/desktop/api/Vds/ns-vds-vds_mount_point_notification). |



 

**\* Windows Server 2003:** estas interfaces no se admiten hasta Windows Server 2003 R2.

## <a name="initiator-adapter-object"></a>Objeto adaptador del iniciador

Un objeto de adaptador iniciador modela un adaptador de iniciador iSCSI en la máquina host del servicio VDS. El servicio VDS solo puede ver los adaptadores del iniciador en la máquina local. El rol de un objeto de adaptador de iniciador es administrar sesiones de inicio de sesión desde el equipo local a destinos iSCSI.

En la tabla siguiente se enumeran interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsIscsiInitiatorAdapter**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatoradapter) \* .                                                                                                        |
| Enumeraciones asociadas                           | [**VDS \_ TIPO DE INICIO \_ DE \_ SESIÓN ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_type). [**VDS \_ MARCA DE \_ INICIO DE \_ SESIÓN ISCSI,**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_login_flag)TIPO [**DE \_ \_ AUTENTICACIÓN VDS \_ ISCSI**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_auth_type). |
| Estructuras asociadas                             | [**VDS \_ PROP DEL ADAPTADOR \_ \_ DEL \_ INICIADOR ISCSI.**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_adapter_prop)                                                                                        |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="initiator-portal-object"></a>Objeto del portal iniciador

Un objeto del portal del iniciador modela un portal del iniciador iSCSI en un iniciador iSCSI. Un portal iniciador es la combinación de una dirección IP y un puerto a través del cual un equipo host se conecta a un portal en un subsistema iSCSI. El rol de un objeto de portal iniciador es actuar como uno de los puntos de conexión de una ruta de acceso de MPIO y configurar las opciones de seguridad de IPSEC.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas. 

| Tipo                                              | Elemento                                                                                                                                                                         |
|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsIscsiInitiatorPortal**](/windows/desktop/api/Vds/nn-vds-ivdsiscsiinitiatorportal) \* .                                                                                                                 |
| Enumeraciones asociadas                           | [**VDS \_ MARCA \_ ISCSI \_ IPSEC**](/windows/desktop/api/Vds/ne-vds-vds_iscsi_ipsec_flag).                                                                                                                        |
| Estructuras asociadas                             | [**VDS \_ ISCSI \_ INITIATOR \_ PORTAL \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_initiator_portal_prop), [**VDS \_ ISCSI \_ IPSEC \_ KEY**](/windows/desktop/api/Vds/ns-vds-vds_iscsi_ipsec_key), [**VDS \_ IPADDRESS**](/windows/desktop/api/Vds/ns-vds-vds_ipaddress). |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="hba-port-object"></a>Objeto de puerto HBA

El objeto de puerto HBA modela un Canal de fibra adaptador de bus host (HBA).

Use el [**método IVdsServiceHba::QueryHbaPorts**](/windows/desktop/api/Vds/nf-vds-ivdsservicehba-queryhbaports) para determinar los puertos HBA conocidos por VDS en el equipo local.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.

| Tipo                                              | Elemento                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto | [**IVdsHbaPort**](/windows/desktop/api/Vds/nn-vds-ivdshbaport) \* .                                                                                                                            |
| Enumeraciones asociadas                           | [**VDS \_ HBAPORT \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_type), [**VDS \_ HBAPORT \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_status), [**VDS \_ HBAPORT \_ SPEED \_ FLAG**](/windows/desktop/api/Vds/ne-vds-vds_hbaport_speed_flag). |
| Estructuras asociadas                             | [**VDS \_ HBAPORT \_ PROP**](/windows/desktop/api/Vds/ns-vds-vds_hbaport_prop).                                                                                                                  |



 

**\* Windows Server 2003:** esta interfaz no se admite hasta Windows Server 2003 R2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de objetos VDS](vds-object-model.md)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[Carga de VDS](loading-vds.md)
</dt> <dt>

[**IVdsService::GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject)
</dt> <dt>

[Notificaciones VDS](vds-notification-model.md)
</dt> </dl>

 

 
