---
title: Funciones de administración de redes
description: Las funciones de administración de red se pueden agrupar de la manera siguiente.
ms.assetid: dd159e2e-f37e-46b2-b980-008b73d40b39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a169d097fbe86c95aa9aa3120c3f732a8edd2c0
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "105685806"
---
# <a name="network-management-functions"></a>Funciones de administración de redes

Las funciones de administración de red se pueden agrupar de la manera siguiente.

## <a name="alert-functions"></a>Funciones de alerta



| Función                                   | Descripción                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a todos los clientes registrados que se ha producido un evento determinado.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Simplifica la notificación a los clientes registrados de que se ha producido un evento determinado, porque, a diferencia de **NetAlertRaise**, **NetAlertRaiseEx** no requiere una estructura de [**\_ alerta STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

## <a name="api-buffer-functions"></a>Funciones de búfer de API



| Función                                                 | Descripción                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**NetApiBufferAllocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | Asigna memoria del montón. Llame a esta función cuando necesite compatibilidad con la función **NetApiBufferFree** . |
| [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | Libera memoria asignada por la función **NetApiBufferAllocate** y otras funciones de administración de redes.                   |
| [**NetApiBufferReallocate**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | Cambia el tamaño de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .                                |
| [**NetApiBufferSize**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | Devuelve el tamaño, en bytes, de un búfer asignado por una llamada a la función **NetApiBufferAllocate** .                     |



 

## <a name="azure-active-directory-join-information-functions"></a>Azure Active Directory funciones de información de combinación



| Función                                                       | Descripción                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetFreeAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netfreeaadjoininformation) | Libera la memoria asignada para la estructura especificada de [**\_ \_ información de combinación de DSREG**](/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info) , que contiene información de combinación de un inquilino y que se ha recuperado mediante una llamada a la función [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation) . |
| [**NetGetAadJoinInformation**](/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation)   | Recupera la información de combinación del inquilino especificado. Esta función examina la información de la combinación de Microsoft Azure Active Directory y la cuenta profesional agregada por el usuario actual.                                                                     |



 

## <a name="directory-service-and-domain-join-functions"></a>Funciones de combinación de dominio y servicio de directorio



| Función                                                                             | Descripción                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)                   | Agrega un nombre alternativo para el equipo especificado.                                                                                                                                                                                                                      |
| [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                  | Aprovisiona una cuenta de equipo para su uso posterior en una operación de unión a un dominio sin conexión.                                                                                                                                                                                        |
| [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)                       | Enumera los nombres del equipo especificado.                                                                                                                                                                                                                            |
| [**NetGetJoinableOUs**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoinableous)                                       | Recupera una lista de unidades organizativas (OU) en las que se puede crear una cuenta de equipo.                                                                                                                                                                              |
| [**NetGetJoinInformation**](/windows/desktop/api/Lmjoin/nf-lmjoin-netgetjoininformation)                               | Recupera información de estado de la Unión para el equipo especificado.                                                                                                                                                                                                           |
| [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)                                               | Une un equipo a un grupo de trabajo o dominio.                                                                                                                                                                                                                              |
| [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)                   | Aprovisiona una cuenta de equipo para su uso posterior en una operación de unión a un dominio sin conexión.                                                                                                                                                                                       |
| [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)             | Quita un nombre alternativo para el equipo especificado.                                                                                                                                                                                                                   |
| [**NetRenameMachineInDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrenamemachineindomain)                         | Cambia el nombre de un equipo en un dominio.                                                                                                                                                                                                                             |
| [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)                   | Se ejecuta localmente en un equipo para modificar una imagen de sistema operativo Windows montada en un volumen. El registro se carga para la imagen y se escriben los datos del BLOB de aprovisionamiento donde se pueden recuperar durante la fase de finalización de una operación de unión al dominio sin conexión.     |
| [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall) | Se ejecuta localmente en un equipo para modificar una imagen de sistema operativo Windows montada en un volumen. El registro se carga desde la imagen y se escriben los datos del paquete de aprovisionamiento, donde se pueden recuperar durante la fase de finalización de una operación de unión al dominio sin conexión. |
| [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)                       | Establece el nombre del equipo principal para el equipo especificado.                                                                                                                                                                                                              |
| [**NetUnjoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netunjoindomain)                                           | Quita la Unión de un equipo de un grupo de trabajo o un dominio.                                                                                                                                                                                                                        |
| [**NetValidateName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netvalidatename)                                           | Comprueba la validez de un nombre de equipo, nombre de grupo de trabajo o nombre de dominio.                                                                                                                                                                                               |



 

## <a name="get-functions"></a>Funciones Get



| Función                                                               | Descripción                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetGetAnyDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Devuelve el nombre de cualquier controlador de dominio para un dominio que sea de confianza directa para un servidor especificado.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Devuelve el nombre del controlador de dominio principal (PDC) para el dominio especificado.                                                        |
| [**NetGetDisplayInformationIndex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Devuelve el índice de la primera entrada de información de visualización cuyo nombre comienza con una cadena especificada o que sigue alfabéticamente a la cadena. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Devuelve la información de la cuenta de usuario, equipo o grupo global.                                                                             |



 

## <a name="group-functions"></a>Funciones de grupo



| Función                                     | Descripción                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | Crea un grupo global.                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | Agrega un usuario a un grupo global existente.                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | Quita un grupo global tanto si el grupo tiene como si no.                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | Quita un nombre de usuario de un grupo global.                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | Enumera todos los grupos globales en un servidor.                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | Devuelve información sobre un grupo global determinado.                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | Enumera todos los miembros de un grupo global determinado.                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | Establece información general sobre un grupo global.                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | Asigna miembros a un nuevo grupo global; reemplaza los miembros de un grupo existente. |



 

## <a name="local-group-functions"></a>Funciones de grupo local



| Función                                                   | Descripción                                                             |
|------------------------------------------------------------|-------------------------------------------------------------------------|
| [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd)               | Crea un grupo local.                                                  |
| [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers) | Agrega uno o más usuarios o grupos globales a un grupo local existente.     |
| [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel)               | Elimina un grupo local, quitando todos los miembros existentes del grupo.    |
| [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers) | Quita uno o más miembros de un grupo local existente.               |
| [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)             | Devuelve información acerca de cada cuenta de grupo local en un servidor.         |
| [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)       | Devuelve información acerca de una cuenta de grupo local determinada en un servidor. |
| [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers) | Enumera todos los miembros de un grupo local especificado.                           |
| [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo)       | Establece información general sobre un grupo local.                           |
| [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers) | Asigna miembros a un grupo local.                                       |



 

## <a name="message-functions"></a>Funciones de mensajes



| Función                                               | Descripción                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | Envía un mensaje a un alias de mensaje registrado.                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | Registra un alias de mensaje en la tabla de nombres de mensaje.                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | Elimina un alias de mensaje de la tabla de nombres de mensaje.                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | Enumera todos los alias de mensajes almacenados en la tabla de nombres de mensaje.                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | Devuelve información sobre un alias de mensaje determinado en la tabla de nombres de mensaje. |



 

## <a name="netfile-functions"></a>Funciones de NetFile



| Función                                | Descripción                                                          |
|-----------------------------------------|----------------------------------------------------------------------|
| [**NetFileClose**](/windows/desktop/api/lmshare/nf-lmshare-netfileclose)     | Fuerza el cierre de un recurso.                                          |
| [**NetFileEnum**](/windows/desktop/api/lmshare/nf-lmshare-netfileenum)       | Devuelve información acerca de los archivos abiertos en un servidor.                    |
| [**NetFileGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netfilegetinfo) | Devuelve información sobre una apertura determinada de un recurso de servidor. |



 

## <a name="remote-utility-functions"></a>Funciones de utilidad remota



| Función                                                       | Descripción                                                                             |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**NetRemoteComputerSupports**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotecomputersupports) | Consulta el redirector para recuperar las características opcionales que admite un sistema remoto. |
| [**NetRemoteTOD**](/windows/desktop/api/Lmremutl/nf-lmremutl-netremotetod)                           | Permite a las aplicaciones tener acceso a la información de hora del día en un servidor remoto.          |



 

## <a name="schedule-functions"></a>Funciones de programación



| Función                                                                     | Descripción                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Envía un trabajo para que se ejecute en una fecha y hora futuras especificadas.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Cancela un intervalo de trabajos en cola para ejecutarse en un equipo.             |
| [**NetScheduleJobEnum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Enumera los trabajos en cola en un equipo especificado.                   |
| [**NetScheduleJobGetInfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Devuelve información acerca de un trabajo determinado en cola en un equipo. |
| [**GetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Recupera el nombre de la cuenta de servicio de AT.                           |
| [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Establece el nombre y la contraseña de la cuenta de servicio en.                   |



 

## <a name="server-functions"></a>Funciones de servidor



| Función                                       | Descripción                                                                        |
|------------------------------------------------|------------------------------------------------------------------------------------|
| [**NetServerDiskEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverdiskenum) | Devuelve una lista de unidades de disco locales en un servidor.                                   |
| [**NetServerEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netserverenum)         | Enumera todos los servidores visibles de un tipo (o tipos) determinado en el dominio especificado. |
| [**NetServerGetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netservergetinfo)   | Devuelve información de configuración sobre un servidor especificado.                        |
| [**NetServerSetInfo**](/windows/desktop/api/Lmserver/nf-lmserver-netserversetinfo)   | Establece los parámetros operativos para un servidor.                                        |



 

## <a name="server-and-workstation-transport-functions"></a>Funciones de transporte de servidor y estación de trabajo



| Función                                                     | Descripción                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetServerComputerNameAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernameadd) | Enlaza un nombre de servidor emulado a cada uno de los protocolos de transporte en los que un servidor está activo. (Combina la funcionalidad de la función [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum) y la función [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex) ).                                            |
| [**NetServerComputerNameDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservercomputernamedel) | Desconecta cada protocolo de transporte de red de un nombre de servidor emulado establecido por una llamada anterior a la función **NetServerComputerNameAdd** .                                                                                                                                                                               |
| [**NetServerTransportAdd**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportadd)       | Enlaza el servidor especificado al Protocolo de transporte. (Esta función solo admite el nivel de información de la información de [**transporte del servidor \_ \_ \_ 0**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_0) ).                                                                                                                                                |
| [**NetServerTransportAddEx**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportaddex)   | Enlaza el servidor especificado al Protocolo de transporte. (Esta función extendida es compatible con los niveles de información de transporte de servidor [**\_ \_ información \_ 1**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_1), información de [**transporte de servidor \_ \_ \_ 2**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_2)e información de [**transporte de servidor \_ \_ \_ 3**](/windows/desktop/api/Lmserver/ns-lmserver-server_transport_info_3) ). |
| [**NetServerTransportDel**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportdel)       | Desconecta el protocolo de transporte del servidor.                                                                                                                                                                                                                                                                         |
| [**NetServerTransportEnum**](/windows/desktop/api/Lmserver/nf-lmserver-netservertransportenum)     | Enumera los protocolos de transporte administrados por el servidor.                                                                                                                                                                                                                                                                   |
| [**NetWkstaTransportEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstatransportenum)       | Enumera los protocolos de transporte administrados por el redirector.                                                                                                                                                                                                                                                           |



 

## <a name="use-functions"></a>Usar funciones



| Función                               | Descripción                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Crea una conexión entre un equipo local y un servidor.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Finaliza una conexión a un recurso compartido.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Muestra todas las conexiones actuales entre el equipo local y los recursos de los servidores remotos. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Devuelve información sobre una conexión a un recurso compartido.                              |



 

## <a name="user-functions"></a>Funciones de usuario



| Función                                               | Descripción                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Agrega una cuenta de usuario y asigna una contraseña y un nivel de privilegios.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Cambia la contraseña de un usuario para un dominio o servidor de red especificado. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Elimina una cuenta de usuario del servidor.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Muestra todas las cuentas de usuario en un servidor.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Devuelve una lista de nombres de grupos globales a los que pertenece un usuario.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Devuelve información acerca de una cuenta de usuario determinada en un servidor.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Devuelve una lista de nombres de grupos locales a los que pertenece un usuario.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Establece la pertenencia a grupos globales para una cuenta de usuario especificada.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Establece la contraseña y otros elementos de una cuenta de usuario.             |



 

## <a name="user-modals-functions"></a>Funciones modales de usuario



| Función                                     | Descripción                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | Devuelve información global de todos los usuarios y grupos globales en la base de datos de seguridad, que es la base de datos del administrador de cuentas de seguridad (SAM) o, en el caso de los controladores de dominio, el Active Directory. |
| [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | Establece la información global de todos los usuarios y grupos globales en la base de datos de seguridad.                                                                                                                       |



 

## <a name="validation-functions"></a>Funciones de validación



| Función                                                               | Descripción                                                                                                                                                                                                                     |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libera la memoria que asigna la función [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) para el parámetro *OutputArg* .                                                                                      |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Habilita a una aplicación para comprobar el cumplimiento de contraseña en una base de datos de cuentas proporcionada por la aplicación y comprobar que las contraseñas cumplen los requisitos de complejidad, caducidad, longitud mínima y reutilización de historial de una directiva de contraseñas. |



 

## <a name="workstation-and-workstation-user-functions"></a>Funciones de usuario de estación de trabajo y estación de trabajo



| Función                                           | Descripción                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)         | Devuelve información sobre los elementos de configuración de una estación de trabajo.             |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo)         | Configura una estación de trabajo.                                                           |
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Muestra información acerca de todos los usuarios que han iniciado sesión actualmente en la estación de trabajo.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Devuelve información acerca de un usuario que ha iniciado sesión actualmente.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Establece la información específica del usuario para los elementos de configuración de una estación de trabajo. |



 

## <a name="obsolete-functions"></a>Funciones obsoletas

-   [**NetAccessAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessadd)
-   [**NetAccessCheck**](/previous-versions/windows/desktop/legacy/aa370291(v=vs.85))
-   [**NetAccessDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessdel)
-   [**NetAccessEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessenum)
-   [**NetAccessGetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetinfo)
-   [**NetAccessGetUserPerms**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccessgetuserperms)
-   [**NetAccessSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netaccesssetinfo)
-   [**NetAuditClear**](netauditclear.md)
-   [**NetAuditRead**](netauditread.md)
-   [**NetAuditWrite**](netauditwrite.md)
-   [**NetConfigGet**](netconfigget.md)
-   [**NetConfigGetAll**](netconfiggetall.md)
-   [**NetConfigSet**](netconfigset.md)
-   [**NetErrorLogClear**](neterrorlogclear.md)
-   [**NetErrorLogRead**](neterrorlogread.md)
-   [**NetErrorLogWrite**](neterrorlogwrite.md)
-   [**NetLocalGroupAddMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupaddmember)
-   [**NetLocalGroupDelMember**](/windows/desktop/api/lmaccess/nf-lmaccess-netlocalgroupdelmember)
-   [**NetServiceControl**](netservicecontrol.md)
-   [**NetServiceEnum**](netserviceenum.md)
-   [**NetServiceGetInfo**](netservicegetinfo.md)
-   [**NetServiceInstall**](netserviceinstall.md)
-   [**NetWkstaTransportAdd**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd)
-   [**NetWkstaTransportDel**](/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportdel)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de red de Windows](/windows/desktop/WNet/windows-networking-functions)
</dt> </dl>

 

 