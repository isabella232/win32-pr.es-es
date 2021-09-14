---
description: Describe los códigos de error 4000-5999 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Códigos de error del sistema (4000-5999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164594"
---
# <a name="system-error-codes-4000-5999"></a>Códigos de error del sistema (4000-5999)

> [!NOTE]
> Esta información está pensada para desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema para los errores 4000 a 5999. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR \_ WINS \_ INTERNAL**
</dt> <dd> <dl> <dt>

4000 (0xFA0)
</dt> <dt>



WINS encontró un error al procesar el comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR \_ CAN \_ NOT \_ DEL \_ LOCAL \_ WINS**
</dt> <dd> <dl> <dt>

4001 (0xFA1)
</dt> <dt>



No se puede eliminar wins local.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR \_ STATIC \_ INIT**
</dt> <dd> <dl> <dt>

4002 (0xFA2)
</dt> <dt>



Error en la importación del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR \_ COPIA DE SEGURIDAD DE \_ INC**
</dt> <dd> <dl> <dt>

4003 (0xFA3)
</dt> <dt>



Error en la copia de seguridad. ¿Se ha realizado una copia de seguridad completa antes?


</dt> </dl> </dd> <dt>

<span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**COPIA DE \_ SEGURIDAD \_ COMPLETA DE ERROR**
</dt> <dd> <dl> <dt>

4004 (0xFA4)
</dt> <dt>



Error en la copia de seguridad. Compruebe el directorio en el que va a realizar la copia de seguridad de la base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR \_ REC \_ NON \_ EXISTENT**
</dt> <dd> <dl> <dt>

4005 (0xFA5)
</dt> <dt>



El nombre no existe en la base de datos WINS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**RPL \_ DE ERROR NO \_ \_ PERMITIDO**
</dt> <dd> <dl> <dt>

4006 (0xFA6)
</dt> <dt>



No se permite la replicación con un asociado no configurado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**ERROR DE PEERDIST \_ \_ CONTENTINFO \_ VERSION \_ UNSUPPORTED**
</dt> <dd> <dl> <dt>

4050 (0xFD2)
</dt> <dt>



No se admite la versión de la información de contenido proporcionada.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**ERROR DE PEERDIST \_ NO SE PUEDE ANALIZAR \_ \_ \_ CONTENTINFO**
</dt> <dd> <dl> <dt>

4051 (0xFD3)
</dt> <dt>



La información de contenido proporcionada tiene un formato mal.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**ERROR DE PEERDIST: \_ \_ FALTAN \_ DATOS**
</dt> <dd> <dl> <dt>

4052 (0xFD4)
</dt> <dt>



Los datos solicitados no se pueden encontrar en cachés locales o del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST \_ ERROR \_ NO \_ MORE**
</dt> <dd> <dl> <dt>

4053 (0xFD5)
</dt> <dt>



No hay más datos disponibles o necesarios.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**ERROR DE PEERDIST \_ \_ NO \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

4054 (0xFD6)
</dt> <dt>



El objeto proporcionado no se ha inicializado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**ERROR DE PEERDIST \_ \_ YA \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

4055 (0xFD7)
</dt> <dt>



El objeto proporcionado ya se ha inicializado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST \_ ERROR \_ SHUTDOWN \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

4056 (0xFD8)
</dt> <dt>



Ya hay una operación de apagado en curso.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**ERROR DE PEERDIST \_ \_ INVALIDADO**
</dt> <dd> <dl> <dt>

4057 (0xFD9)
</dt> <dt>



El objeto proporcionado ya se ha invalidado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**EL ERROR PEERDIST \_ \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

4058 (0xFDA)
</dt> <dt>



Ya existe un elemento y no se ha reemplazado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**OPERACIÓN DE ERROR PEERDIST \_ \_ \_ NOTFOUND**
</dt> <dd> <dl> <dt>

4059 (0xFDB)
</dt> <dt>



No se puede cancelar la operación solicitada, ya que ya se ha completado.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**ERROR DE PEERDIST \_ \_ YA \_ COMPLETADO**
</dt> <dd> <dl> <dt>

4060 (0xFDC)
</dt> <dt>



No se puede realizar la operación de reqested porque ya se ha llevado a cabo.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**ERROR DE PEERDIST \_ \_ FUERA DE LOS \_ \_ LÍMITES**
</dt> <dd> <dl> <dt>

4061 (0xFDD)
</dt> <dt>



Una operación ha accedido a datos más allá de los límites de datos válidos.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**VERSIÓN DE ERROR DE PEERDIST \_ \_ NO \_ ADMITIDA**
</dt> <dd> <dl> <dt>

4062 (0xFDE)
</dt> <dt>



No se admite la versión solicitada.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**ERROR DE PEERDIST \_ \_ CONFIGURACIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

4063 (0xFDF)
</dt> <dt>



Un valor de configuración no es válido.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**ERROR DE PEERDIST \_ \_ SIN \_ LICENCIA**
</dt> <dd> <dl> <dt>

4064 (0xFE0)
</dt> <dt>



La SKU no tiene licencia.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**SERVICIO DE ERROR PEERDIST \_ \_ NO \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

4065 (0xFE1)
</dt> <dt>



PeerDist Service todavía se está inicializando y estará disponible en breve.


</dt> </dl> </dd> <dt>

<span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**ERROR DE PEERDIST \_ ERROR \_ DE \_ CONFIANZA**
</dt> <dd> <dl> <dt>

4066 (0xFE2)
</dt> <dt>



La comunicación con uno o varios equipos se bloqueará temporalmente debido a errores recientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR \_ DHCP \_ ADDRESS \_ CONFLICT**
</dt> <dd> <dl> <dt>

4100 (0x1004)
</dt> <dt>



El cliente DHCP ha obtenido una dirección IP que ya está en uso en la red. La interfaz local se deshabilitará hasta que el cliente DHCP pueda obtener una nueva dirección.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR \_ WMI \_ GUID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

4200 (0x1068)
</dt> <dt>



Un proveedor de datos WMI no reconoce el GUID pasado como válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**NO SE \_ ENCONTRÓ LA INSTANCIA WMI DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

4201 (0x1069)
</dt> <dt>



Un proveedor de datos WMI no ha reconocido el nombre de instancia pasado como válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR \_ WMI \_ ITEMID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

4202 (0x106A)
</dt> <dt>



El identificador de elemento de datos pasado no se reconoce como válido por un proveedor de datos WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR \_ WMI \_ TRY \_ AGAIN**
</dt> <dd> <dl> <dt>

4203 (0x106B)
</dt> <dt>



No se pudo completar la solicitud WMI y debe reinterse.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR \_ WMI \_ DP \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

4204 (0x106C)
</dt> <dt>



No se pudo encontrar el proveedor de datos WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR \_ WMI \_ UNRESOLVED \_ INSTANCE \_ REF**
</dt> <dd> <dl> <dt>

4205 (0x106D)
</dt> <dt>



El proveedor de datos WMI hace referencia a un conjunto de instancias que no se ha registrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**WMI \_ DE ERROR YA \_ \_ HABILITADO**
</dt> <dd> <dl> <dt>

4206 (0x106E)
</dt> <dt>



Ya se ha habilitado el bloque de datos WMI o la notificación de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**GUID \_ WMI DE ERROR \_ \_ DESCONECTADO**
</dt> <dd> <dl> <dt>

4207 (0x106F)
</dt> <dt>



El bloque de datos WMI ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR \_ SERVIDOR WMI NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

4208 (0x1070)
</dt> <dt>



El servicio de datos WMI no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR \_ DE WMI DP \_ \_ FAILED**
</dt> <dd> <dl> <dt>

4209 (0x1071)
</dt> <dt>



El proveedor de datos WMI no pudo llevar a cabo la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR \_ WMI \_ INVALID \_ MOF**
</dt> <dd> <dl> <dt>

4210 (0x1072)
</dt> <dt>



La información MOF de WMI no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR \_ WMI \_ INVALID \_ REGINFO**
</dt> <dd> <dl> <dt>

4211 (0x1073)
</dt> <dt>



La información de registro de WMI no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**WMI \_ DE ERROR YA \_ \_ DESHABILITADO**
</dt> <dd> <dl> <dt>

4212 (0x1074)
</dt> <dt>



El bloque de datos WMI o la notificación de eventos ya se han deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR \_ WMI \_ READ \_ ONLY**
</dt> <dd> <dl> <dt>

4213 (0x1075)
</dt> <dt>



El bloque de datos o elemento de datos WMI es de solo lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR \_ DEL CONJUNTO \_ WMI \_**
</dt> <dd> <dl> <dt>

4214 (0x1076)
</dt> <dt>



No se pudo cambiar el bloque de datos o elemento de datos WMI.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR \_ NOT \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4250 (0x109A)
</dt> <dt>



Esta operación solo es válida en el contexto de un contenedor de aplicaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR \_ APPCONTAINER \_ REQUIRED**
</dt> <dd> <dl> <dt>

4251 (0x109B)
</dt> <dt>



Esta aplicación solo se puede ejecutar en el contexto de un contenedor de aplicaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR \_ NO ADMITIDO EN \_ \_ \_ APPCONTAINER**
</dt> <dd> <dl> <dt>

4252 (0x109C)
</dt> <dt>



Esta funcionalidad no se admite en el contexto de un contenedor de aplicaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR \_ LONGITUD DEL \_ \_ SID DEL PAQUETE NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

4253 (0x109D)
</dt> <dt>



La longitud del SID proporcionado no es una longitud válida para los SID del contenedor de aplicaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR \_ MEDIOS NO \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

4300 (0x10CC)
</dt> <dt>



El identificador de medios no representa un medio válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR \_ BIBLIOTECA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

4301 (0x10CD)
</dt> <dt>



El identificador de biblioteca no representa una biblioteca válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR \_ GRUPO DE MEDIOS NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

4302 (0x10CE)
</dt> <dt>



El identificador del grupo de medios no representa un grupo de medios válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR DE \_ COINCIDENCIA DE MEDIOS DE UNIDAD DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

4303 (0x10CF)
</dt> <dt>



La unidad y el medio no son compatibles o existen en bibliotecas diferentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**MEDIOS DE \_ ERROR SIN \_ CONEXIÓN**
</dt> <dd> <dl> <dt>

4304 (0x10D0)
</dt> <dt>



El medio existe actualmente en una biblioteca sin conexión y debe estar en línea para realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**BIBLIOTECA DE ERRORES \_ \_ SIN CONEXIÓN**
</dt> <dd> <dl> <dt>

4305 (0x10D1)
</dt> <dt>



La operación no se puede realizar en una biblioteca sin conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR \_ VACÍO**
</dt> <dd> <dl> <dt>

4306 (0x10D2)
</dt> <dt>



La biblioteca, unidad o grupo de medios está vacía.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR \_ NO \_ VACÍO**
</dt> <dd> <dl> <dt>

4307 (0x10D3)
</dt> <dt>



La biblioteca, la unidad o el grupo de medios deben estar vacíos para realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**MEDIOS \_ DE ERROR NO \_ DISPONIBLES**
</dt> <dd> <dl> <dt>

4308 (0x10D4)
</dt> <dt>



Actualmente no hay ningún medio disponible en este grupo de medios o biblioteca.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**RECURSO DE \_ ERROR \_ DESHABILITADO**
</dt> <dd> <dl> <dt>

4309 (0x10D5)
</dt> <dt>



Se deshabilita un recurso necesario para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR \_ LIMPIEZA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

4310 (0x10D6)
</dt> <dt>



El identificador de medios no representa un limpiador válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR \_ NO SE PUEDE \_ \_ LIMPIAR**
</dt> <dd> <dl> <dt>

4311 (0x10D7)
</dt> <dt>



La unidad no se puede limpiar o no admite la limpieza.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**NO \_ SE ENCONTRÓ EL OBJETO DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

4312 (0x10D8)
</dt> <dt>



El identificador de objeto no representa un objeto válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR EN \_ LA BASE DE \_ DATOS**
</dt> <dd> <dl> <dt>

4313 (0x10D9)
</dt> <dt>



No se puede leer ni escribir en la base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR \_ DATABASE \_ FULL**
</dt> <dd> <dl> <dt>

4314 (0x10DA)
</dt> <dt>



La base de datos está llena.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR \_ MEDIA \_ INCOMPATIBLE**
</dt> <dd> <dl> <dt>

4315 (0x10DB)
</dt> <dt>



El medio no es compatible con el dispositivo o el grupo de medios.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**RECURSO \_ DE ERROR NO \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

4316 (0x10DC)
</dt> <dt>



El recurso necesario para esta operación no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR \_ OPERACIÓN NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

4317 (0x10DD)
</dt> <dt>



El identificador de la operación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**MEDIOS \_ DE ERROR NO \_ \_ DISPONIBLES**
</dt> <dd> <dl> <dt>

4318 (0x10DE)
</dt> <dt>



El medio no está montado ni listo para su uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR \_ EL DISPOSITIVO NO ESTÁ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

4319 (0x10DF)
</dt> <dt>



El dispositivo no está listo para su uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**SOLICITUD DE ERROR \_ \_ RECHAZADA**
</dt> <dd> <dl> <dt>

4320 (0x10E0)
</dt> <dt>



El operador o administrador ha rechazado la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR \_ OBJETO DE UNIDAD NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

4321 (0x10E1)
</dt> <dt>



El identificador de unidad no representa una unidad válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**BIBLIOTECA DE ERRORES \_ \_ COMPLETA**
</dt> <dd> <dl> <dt>

4322 (0x10E2)
</dt> <dt>



La biblioteca está llena. No hay ninguna ranura disponible para su uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**MEDIO DE ERROR \_ \_ NO \_ ACCESIBLE**
</dt> <dd> <dl> <dt>

4323 (0x10E3)
</dt> <dt>



El transporte no puede tener acceso al medio.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR \_ NO SE PUEDE CARGAR \_ \_ MEDIO \_**
</dt> <dd> <dl> <dt>

4324 (0x10E4)
</dt> <dt>



No se puede cargar el medio en la unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR \_ NO SE PUEDE REALIZAR EL INVENTARIO DE LA \_ \_ \_ UNIDAD**
</dt> <dd> <dl> <dt>

4325 (0x10E5)
</dt> <dt>



No se puede recuperar el estado de la unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR \_ NO SE PUEDE \_ \_ INVENTARIAR \_ LA RANURA**
</dt> <dd> <dl> <dt>

4326 (0x10E6)
</dt> <dt>



No se puede recuperar el estado de la ranura.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR \_ NO SE PUEDE \_ \_ INVENTARIAR \_ EL TRANSPORTE**
</dt> <dd> <dl> <dt>

4327 (0x10E7)
</dt> <dt>



No se puede recuperar el estado del transporte.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR \_ TRANSPORT \_ FULL**
</dt> <dd> <dl> <dt>

4328 (0x10E8)
</dt> <dt>



No se puede usar el transporte porque ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR \_ AL CONTROLAR \_ IEPORT**
</dt> <dd> <dl> <dt>

4329 (0x10E9)
</dt> <dt>



No se puede abrir o cerrar el puerto de inyección o expulsión.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR \_ NO SE PUEDE EXPULSAR EL MEDIO \_ \_ \_ \_ MONTADO**
</dt> <dd> <dl> <dt>

4330 (0x10EA)
</dt> <dt>



No se puede expulsar el medio porque está en una unidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**CONJUNTO DE \_ RANURAS \_ DE LIMPIEZA DE \_ ERRORES**
</dt> <dd> <dl> <dt>

4331 (0x10EB)
</dt> <dt>



Ya se ha reservado una ranura de limpieza.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR \_ CLEANER \_ SLOT \_ NOT \_ SET**
</dt> <dd> <dl> <dt>

4332 (0x10EC)
</dt> <dt>



No se reserva una ranura de limpieza.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR \_ CLEANER \_ CARTRIDGE \_ SPENT**
</dt> <dd> <dl> <dt>

4333 (0x10ED)
</dt> <dt>



El limpiador ha realizado el número máximo de limpiezas de unidades.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR \_ INESPERADO \_ OMID**
</dt> <dd> <dl> <dt>

4334 (0x10EE)
</dt> <dt>



Identificador en medio inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR \_ NO SE PUEDE ELIMINAR EL ÚLTIMO \_ \_ \_ ELEMENTO**
</dt> <dd> <dl> <dt>

4335 (0x10EF)
</dt> <dt>



No se puede eliminar el último elemento restante de este grupo o recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**EL \_ MENSAJE DE ERROR SUPERA EL TAMAÑO \_ \_ \_ MÁXIMO**
</dt> <dd> <dl> <dt>

4336 (0x10F0)
</dt> <dt>



El mensaje proporcionado supera el tamaño máximo permitido para este parámetro.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**EL \_ VOLUMEN DE ERROR CONTIENE ARCHIVOS \_ \_ SYS \_**
</dt> <dd> <dl> <dt>

4337 (0x10F1)
</dt> <dt>



El volumen contiene archivos de paginación o del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**TIPO \_ DE ERROR DE LA ZONA DE \_ ERROR**
</dt> <dd> <dl> <dt>

4338 (0x10F2)
</dt> <dt>



El tipo de medio no se puede quitar de esta biblioteca, ya que al menos una unidad de la biblioteca informa de que puede admitir este tipo de medio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR \_ NO \_ ADMITE \_ UNIDADES**
</dt> <dd> <dl> <dt>

4339 (0x10F3)
</dt> <dt>



Este medio sin conexión no se puede montar en este sistema, ya que no hay unidades habilitadas que se puedan usar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**INSTALACIÓN \_ DEL LIMPIADOR DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

4340 (0x10F4)
</dt> <dt>



Hay un limpiador más limpio en la biblioteca de cintas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR \_ IEPORT \_ FULL**
</dt> <dd> <dl> <dt>

4341 (0x10F5)
</dt> <dt>



No se puede usar el puerto de inyección o expulsión porque no está vacío.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ARCHIVO DE ERROR \_ \_ SIN CONEXIÓN**
</dt> <dd> <dl> <dt>

4350 (0x10FE)
</dt> <dt>



Este archivo no está disponible actualmente para su uso en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR \_ ALMACENAMIENTO REMOTO NO \_ \_ \_ ACTIVO**
</dt> <dd> <dl> <dt>

4351 (0x10FF)
</dt> <dt>



El servicio de almacenamiento remoto no está operativo en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR DE \_ MEDIOS \_ DE ALMACENAMIENTO \_ \_ REMOTO**
</dt> <dd> <dl> <dt>

4352 (0x1100)
</dt> <dt>



El servicio de almacenamiento remoto encontró un error multimedia.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR \_ NO ES UN PUNTO DE \_ \_ \_ REANARSE**
</dt> <dd> <dl> <dt>

4390 (0x1126)
</dt> <dt>



El archivo o directorio no es un punto de análisis.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR \_ REPARSE \_ ATTRIBUTE \_ CONFLICT**
</dt> <dd> <dl> <dt>

4391 (0x1127)
</dt> <dt>



No se puede establecer el atributo de punto de reanción porque entra en conflicto con un atributo existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR INVALID REPARSE DATA (DATOS \_ \_ DE ANÁLISIS NO \_ VÁLIDOS)**
</dt> <dd> <dl> <dt>

4392 (0x1128)
</dt> <dt>



Los datos presentes en el búfer de punto de análisis no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR \_ REPARSE \_ TAG \_ INVALID**
</dt> <dd> <dl> <dt>

4393 (0x1129)
</dt> <dt>



La etiqueta presente en el búfer de punto de reanidad no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR \_ REPARSE \_ TAG \_ MISMATCH**
</dt> <dd> <dl> <dt>

4394 (0x112A)
</dt> <dt>



Hay una discrepancia entre la etiqueta especificada en la solicitud y la etiqueta presente en el punto de reanche.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR \_ NO SE ENCONTRARON LOS DATOS DE LA \_ \_ \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

4400 (0x1130)
</dt> <dt>



No se encontraron datos de caché rápida.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR LOS \_ DATOS DE LA APLICACIÓN \_ \_ EXPIRARON**
</dt> <dd> <dl> <dt>

4401 (0x1131)
</dt> <dt>



Los datos de caché rápida expiraron.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**DATOS DE \_ LA APLICACIÓN DE ERROR \_ \_ DAÑADOS**
</dt> <dd> <dl> <dt>

4402 (0x1132)
</dt> <dt>



Datos de caché rápida dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**SE \_ SUPERÓ EL \_ LÍMITE DE DATOS DE LA APLICACIÓN DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

4403 (0x1133)
</dt> <dt>



Los datos de caché rápida han superado su tamaño máximo y no se pueden actualizar.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR SE \_ REQUIERE EL REINICIO DE DATOS DE LA \_ \_ \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

4404 (0x1134)
</dt> <dt>



La caché rápida se ha reiniciado y requiere un reinicio hasta que se pueda actualizar.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR \_ DE REVERSIÓN \_ DE SECUREBOOT \_ DETECTADA**
</dt> <dd> <dl> <dt>

4420 (0x1144)
</dt> <dt>



Arranque seguro detectó que se ha intentado revertir datos protegidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR \_ INFRACCIÓN DE LA \_ DIRECTIVA \_ SECUREBOOT**
</dt> <dd> <dl> <dt>

4421 (0x1145)
</dt> <dt>



El valor está protegido por la directiva de arranque seguro y no se puede modificar ni eliminar.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR \_ SECUREBOOT \_ INVALID \_ POLICY**
</dt> <dd> <dl> <dt>

4422 (0x1146)
</dt> <dt>



La directiva de arranque seguro no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL \_ \_ PUBLICADOR DE DIRECTIVAS \_ \_ SECUREBOOT**
</dt> <dd> <dl> <dt>

4423 (0x1147)
</dt> <dt>



Una nueva directiva de arranque seguro no contenía el publicador actual en su lista de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR \_ SECUREBOOT \_ POLICY \_ NOT \_ SIGNED**
</dt> <dd> <dl> <dt>

4424 (0x1148)
</dt> <dt>



La directiva de arranque seguro no está firmada o está firmada por un firmante que no es de confianza.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR \_ SECUREBOOT \_ NOT \_ ENABLED**
</dt> <dd> <dl> <dt>

4425 (0x1149)
</dt> <dt>



El arranque seguro no está habilitado en esta máquina.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR \_ SECUREBOOT \_ FILE \_ REPLACED**
</dt> <dd> <dl> <dt>

4426 (0x114A)
</dt> <dt>



El arranque seguro requiere que determinados archivos y controladores no se reemplazan por otros archivos o controladores.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR \_ OFFLOAD \_ READ \_ FLT \_ NOT \_ SUPPORTED**
</dt> <dd> <dl> <dt>

4440 (0x1158)
</dt> <dt>



La operación de lectura de descarga de copia no es compatible con un filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR \_ OFFLOAD \_ WRITE \_ FLT \_ NOT \_ SUPPORTED**
</dt> <dd> <dl> <dt>

4441 (0x1159)
</dt> <dt>



La operación de escritura de descarga de copia no es compatible con un filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**NO \_ SE ADMITE LA DESCARGA DE ARCHIVOS DE LECTURA DE \_ \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

4442 (0x115A)
</dt> <dt>



No se admite la operación de lectura de descarga de copia para el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR \_ DESCARGAR ARCHIVO DE ESCRITURA NO \_ \_ \_ \_ ADMITIDO**
</dt> <dd> <dl> <dt>

4443 (0x115B)
</dt> <dt>



No se admite la operación de escritura de descarga de copia para el archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**VOLUMEN \_ DE ERROR NO \_ \_ HABILITADO \_**
</dt> <dd> <dl> <dt>

4500 (0x1194)
</dt> <dt>



El Storage instancia única no está disponible en este volumen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**EXISTE \_ UN RECURSO DEPENDIENTE DEL \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5001 (0x1389)
</dt> <dt>



La operación no se puede completar porque otros recursos dependen de este recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**NO SE \_ ENCONTRÓ LA DEPENDENCIA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5002 (0x138A)
</dt> <dt>



No se encuentra la dependencia de recursos de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**LA DEPENDENCIA \_ DE ERROR \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

5003 (0x138B)
</dt> <dt>



El recurso de clúster no se puede hacer dependiente del recurso especificado porque ya es dependiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**RECURSO DE ERROR \_ \_ NO EN \_ LÍNEA**
</dt> <dd> <dl> <dt>

5004 (0x138C)
</dt> <dt>



El recurso de clúster no está en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**NODO \_ HOST DE ERROR NO \_ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

5005 (0x138D)
</dt> <dt>



Un nodo de clúster no está disponible para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**RECURSO \_ DE ERROR NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

5006 (0x138E)
</dt> <dt>



El recurso de clúster no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**RECURSO DE ERROR \_ \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5007 (0x138F)
</dt> <dt>



No se encontró el recurso de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR \_ SHUTDOWN \_ CLUSTER**
</dt> <dd> <dl> <dt>

5008 (0x1390)
</dt> <dt>



El clúster se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR \_ CANT \_ EVICT \_ ACTIVE \_ NODE**
</dt> <dd> <dl> <dt>

5009 (0x1391)
</dt> <dt>



Un nodo de clúster no se puede expulsar del clúster a menos que el nodo esté fuera de servicio o sea el último nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**EL OBJETO \_ DE ERROR \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

5010 (0x1392)
</dt> <dt>



El objeto ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**OBJETO \_ DE ERROR EN LA \_ \_ LISTA**
</dt> <dd> <dl> <dt>

5011 (0x1393)
</dt> <dt>



El objeto ya está en la lista.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**GRUPO \_ DE ERRORES NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

5012 (0x1394)
</dt> <dt>



El grupo de clústeres no está disponible para las nuevas solicitudes.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**GRUPO DE ERRORES \_ \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5013 (0x1395)
</dt> <dt>



No se encontró el grupo de clústeres.


</dt> </dl> </dd> <dt>

<span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**GRUPO DE \_ ERRORES \_ NO EN \_ LÍNEA**
</dt> <dd> <dl> <dt>

5014 (0x1396)
</dt> <dt>



No se pudo completar la operación porque el grupo de clústeres no está en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR \_ HOST \_ NODE \_ NOT \_ RESOURCE \_ OWNER**
</dt> <dd> <dl> <dt>

5015 (0x1397)
</dt> <dt>



Error en la operación porque el nodo de clúster especificado no es el propietario del recurso o el nodo no es un posible propietario del recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR \_ HOST \_ NODE \_ NOT \_ GROUP \_ OWNER**
</dt> <dd> <dl> <dt>

5016 (0x1398)
</dt> <dt>



Error en la operación; el nodo de clúster especificado no es el propietario del grupo o el nodo no es un propietario posible del grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR \_ AL CREAR RESMON \_ \_**
</dt> <dd> <dl> <dt>

5017 (0x1399)
</dt> <dt>



No se pudo crear el recurso de clúster en el monitor de recursos especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR \_ RESMON \_ ONLINE \_ FAILED**
</dt> <dd> <dl> <dt>

5018 (0x139A)
</dt> <dt>



El monitor de recursos no pudo puesto en línea el recurso de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**RECURSO DE ERROR \_ \_ EN LÍNEA**
</dt> <dd> <dl> <dt>

5019 (0x139B)
</dt> <dt>



No se pudo completar la operación porque el recurso de clúster está en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**RECURSO \_ DE CUÓRUM DE \_ ERROR**
</dt> <dd> <dl> <dt>

5020 (0x139C)
</dt> <dt>



No se pudo eliminar o desconectar el recurso de clúster porque es el recurso de cuórum.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR \_ NO COMPATIBLE CON \_ \_ CUÓRUM**
</dt> <dd> <dl> <dt>

5021 (0x139D)
</dt> <dt>



El clúster no pudo convertir el recurso especificado en un recurso de cuórum porque no es capaz de ser un recurso de cuórum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR \_ DE CIERRE DEL \_ CLÚSTER \_**
</dt> <dd> <dl> <dt>

5022 (0x139E)
</dt> <dt>



El software del clúster se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR \_ ESTADO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

5023 (0x139F)
</dt> <dt>



El grupo o recurso no está en el estado correcto para realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**PROPIEDADES DE \_ RECURSO \_ DE ERROR \_ ALMACENADAS**
</dt> <dd> <dl> <dt>

5024 (0x13A0)
</dt> <dt>



Las propiedades se almacenaron, pero no todos los cambios tendrán efecto hasta la próxima vez que el recurso se en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR \_ NOT \_ QUORUM \_ (CLASE)**
</dt> <dd> <dl> <dt>

5025 (0x13A1)
</dt> <dt>



El clúster no pudo convertir el recurso especificado en un recurso de cuórum porque no pertenece a una clase de almacenamiento compartido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**RECURSO DE ERROR \_ \_ CORE**
</dt> <dd> <dl> <dt>

5026 (0x13A2)
</dt> <dt>



No se pudo eliminar el recurso de clúster, ya que es un recurso principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR DE \_ QUORUM \_ RESOURCE ONLINE \_ \_ FAILED**
</dt> <dd> <dl> <dt>

5027 (0x13A3)
</dt> <dt>



El recurso de cuórum no se pudo establecer en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR \_ QUORUMLOG \_ OPEN \_ FAILED**
</dt> <dd> <dl> <dt>

5028 (0x13A4)
</dt> <dt>



No se pudo crear o montar correctamente el registro de cuórum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR \_ CLUSTERLOG \_ CORRUPT**
</dt> <dd> <dl> <dt>

5029 (0x13A5)
</dt> <dt>



El registro del clúster está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR \_ CLUSTERLOG \_ RECORD \_ EXCEEDS \_ MAXSIZE**
</dt> <dd> <dl> <dt>

5030 (0x13A6)
</dt> <dt>



No se pudo escribir el registro en el registro del clúster porque supera el tamaño máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR \_ CLUSTERLOG \_ SUPERA \_ MAXSIZE**
</dt> <dd> <dl> <dt>

5031 (0x13A7)
</dt> <dt>



El registro del clúster supera su tamaño máximo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR \_ CLUSTERLOG \_ CHKPOINT \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

5032 (0x13A8)
</dt> <dt>



No se encontró ningún registro de punto de comprobación en el registro del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR \_ CLUSTERLOG \_ NOT \_ ENOUGH \_ SPACE**
</dt> <dd> <dl> <dt>

5033 (0x13A9)
</dt> <dt>



El espacio en disco mínimo necesario para el registro no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR \_ PROPIETARIO DE CUÓRUM \_ \_ ACTIVO**
</dt> <dd> <dl> <dt>

5034 (0x13AA)
</dt> <dt>



El nodo de clúster no pudo tomar el control del recurso de cuórum porque el recurso pertenece a otro nodo activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR \_ NETWORK \_ NOT \_ AVAILABLE**
</dt> <dd> <dl> <dt>

5035 (0x13AB)
</dt> <dt>



Una red de clúster no está disponible para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**NODO DE ERROR \_ \_ NO \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

5036 (0x13AC)
</dt> <dt>



Un nodo de clúster no está disponible para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR \_ TODOS LOS NODOS NO ESTÁN \_ \_ \_ DISPONIBLES**
</dt> <dd> <dl> <dt>

5037 (0x13AD)
</dt> <dt>



Todos los nodos del clúster deben estar en ejecución para realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR \_ EN EL RECURSO \_**
</dt> <dd> <dl> <dt>

5038 (0x13AE)
</dt> <dt>



error en un recurso de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR \_ CLUSTER INVALID NODE \_ (NODO NO VÁLIDO DEL CLÚSTER DE \_ ERRORES)**
</dt> <dd> <dl> <dt>

5039 (0x13AF)
</dt> <dt>



El nodo de clúster no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**EL NODO \_ DE CLÚSTER DE ERRORES \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

5040 (0x13B0)
</dt> <dt>



El nodo de clúster ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR \_ DE COMBINACIÓN DE CLÚSTER EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5041 (0x13B1)
</dt> <dt>



Un nodo está en proceso de unirse al clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL NODO DE \_ \_ \_ CLÚSTER**
</dt> <dd> <dl> <dt>

5042 (0x13B2)
</dt> <dt>



No se encontró el nodo del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL NODO LOCAL DEL \_ \_ \_ \_ CLÚSTER**
</dt> <dd> <dl> <dt>

5043 (0x13B3)
</dt> <dt>



No se encontró la información del nodo local del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR \_ CLUSTER \_ NETWORK \_ EXISTS**
</dt> <dd> <dl> <dt>

5044 (0x13B4)
</dt> <dt>



La red del clúster ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA RED DEL \_ \_ \_ CLÚSTER**
</dt> <dd> <dl> <dt>

5045 (0x13B5)
</dt> <dt>



No se encontró la red del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR \_ CLUSTER \_ NETINTERFACE \_ EXISTS**
</dt> <dd> <dl> <dt>

5046 (0x13B6)
</dt> <dt>



La interfaz de red del clúster ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR \_ CLUSTER \_ NETINTERFACE \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

5047 (0x13B7)
</dt> <dt>



No se encontró la interfaz de red del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**SOLICITUD DE \_ CLÚSTER DE ERROR NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

5048 (0x13B8)
</dt> <dt>



La solicitud de clúster no es válida para este objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR \_ CLUSTER INVALID NETWORK PROVIDER (PROVEEDOR DE RED NO VÁLIDO DEL CLÚSTER DE \_ \_ \_ ERRORES)**
</dt> <dd> <dl> <dt>

5049 (0x13B9)
</dt> <dt>



El proveedor de red del clúster no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR \_ CLUSTER \_ NODE \_ DOWN**
</dt> <dd> <dl> <dt>

5050 (0x13BA)
</dt> <dt>



El nodo del clúster está abajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR CLUSTER NODE UNREACHABLE (NODO \_ DE CLÚSTER DE ERRORES \_ \_ INACCESIBLE)**
</dt> <dd> <dl> <dt>

5051 (0x13BB)
</dt> <dt>



No se puede acceder al nodo de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR \_ CLUSTER \_ NODE \_ NOT \_ MEMBER**
</dt> <dd> <dl> <dt>

5052 (0x13BC)
</dt> <dt>



El nodo de clúster no es miembro del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR LA \_ COMBINACIÓN DEL CLÚSTER NO ESTÁ EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5053 (0x13BD)
</dt> <dt>



Una operación de combinación de clúster no está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR \_ CLUSTER \_ INVALID \_ NETWORK**
</dt> <dd> <dl> <dt>

5054 (0x13BE)
</dt> <dt>



La red del clúster no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**NODO DE \_ CLÚSTER \_ DE ERROR \_ ACTIVO**
</dt> <dd> <dl> <dt>

5056 (0x13C0)
</dt> <dt>



El nodo del clúster está activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**\_IPADDR DEL CLÚSTER DE ERRORES EN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

5057 (0x13C1)
</dt> <dt>



La dirección IP del clúster ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**NODO DE \_ CLÚSTER DE ERRORES NO EN \_ \_ \_ PAUSA**
</dt> <dd> <dl> <dt>

5058 (0x13C2)
</dt> <dt>



El nodo del clúster no está en pausa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**CLÚSTER DE ERRORES \_ \_ SIN CONTEXTO DE \_ \_ SEGURIDAD**
</dt> <dd> <dl> <dt>

5059 (0x13C3)
</dt> <dt>



No hay ningún contexto de seguridad de clúster disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR \_ CLUSTER \_ NETWORK \_ NOT \_ INTERNAL**
</dt> <dd> <dl> <dt>

5060 (0x13C4)
</dt> <dt>



La red del clúster no está configurada para la comunicación interna del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**NODO \_ DE CLÚSTER DE ERRORES YA \_ \_ \_ ACTIVO**
</dt> <dd> <dl> <dt>

5061 (0x13C5)
</dt> <dt>



El nodo de clúster ya está activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR \_ CLUSTER \_ NODE \_ ALREADY \_ DOWN**
</dt> <dd> <dl> <dt>

5062 (0x13C6)
</dt> <dt>



El nodo del clúster ya está sin servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**RED DE \_ CLÚSTER DE ERRORES YA EN \_ \_ \_ LÍNEA**
</dt> <dd> <dl> <dt>

5063 (0x13C7)
</dt> <dt>



La red del clúster ya está en línea.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**RED DE \_ CLÚSTER DE ERRORES YA SIN \_ \_ \_ CONEXIÓN**
</dt> <dd> <dl> <dt>

5064 (0x13C8)
</dt> <dt>



La red del clúster ya está sin conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**NODO \_ DE CLÚSTER DE ERRORES YA \_ \_ \_ MIEMBRO**
</dt> <dd> <dl> <dt>

5065 (0x13C9)
</dt> <dt>



El nodo de clúster ya es miembro del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**CLÚSTER DE \_ ERRORES \_ ÚLTIMA RED \_ \_ INTERNA**
</dt> <dd> <dl> <dt>

5066 (0x13CA)
</dt> <dt>



La red del clúster es la única configurada para la comunicación interna del clúster entre dos o más nodos de clúster activos. La funcionalidad de comunicación interna no se puede quitar de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**LA RED \_ DE CLÚSTER DE ERRORES TIENE \_ \_ \_ DEPENDIENTES**
</dt> <dd> <dl> <dt>

5067 (0x13CB)
</dt> <dt>



Uno o varios recursos de clúster dependen de la red para proporcionar servicio a los clientes. La funcionalidad de acceso de cliente no se puede quitar de la red.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR \_ OPERACIÓN NO VÁLIDA EN \_ \_ QUORUM \_**
</dt> <dd> <dl> <dt>

5068 (0x13CC)
</dt> <dt>



Esta operación no se puede realizar en el recurso de clúster, ya que es el recurso de cuórum. No puede desconectar el recurso de cuórum ni modificar su lista de posibles propietarios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**DEPENDENCIA DE \_ ERROR \_ NO \_ PERMITIDA**
</dt> <dd> <dl> <dt>

5069 (0x13CD)
</dt> <dt>



No se permite que el recurso de cuórum de clúster tenga dependencias.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**NODO DE \_ CLÚSTER DE ERRORES EN \_ \_ PAUSA**
</dt> <dd> <dl> <dt>

5070 (0x13CE)
</dt> <dt>



El nodo de clúster está en pausa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR \_ NODE \_ CANT \_ HOST \_ RESOURCE**
</dt> <dd> <dl> <dt>

5071 (0x13CF)
</dt> <dt>



El recurso de clúster no se puede en línea. El nodo propietario no puede ejecutar este recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**NODO DE \_ CLÚSTER DE ERRORES NO \_ \_ \_ LISTO**
</dt> <dd> <dl> <dt>

5072 (0x13D0)
</dt> <dt>



El nodo de clúster no está listo para realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR \_ CLUSTER \_ NODE \_ SHUTTING \_ DOWN**
</dt> <dd> <dl> <dt>

5073 (0x13D1)
</dt> <dt>



El nodo del clúster se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR \_ CLUSTER \_ JOIN \_ ABORTED**
</dt> <dd> <dl> <dt>

5074 (0x13D2)
</dt> <dt>



Se anuló la operación de combinación de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**VERSIONES \_ INCOMPATIBLES \_ DEL CLÚSTER DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5075 (0x13D3)
</dt> <dt>



Error en la operación de unión al clúster debido a versiones de software incompatibles entre el nodo de unión y su patrocinador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR \_ CLUSTER \_ MAXNUM \_ OF \_ RESOURCES \_ EXCEEDED**
</dt> <dd> <dl> <dt>

5076 (0x13D4)
</dt> <dt>



Este recurso no se puede crear porque el clúster ha alcanzado el límite en el número de recursos que puede supervisar.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR \_ CLUSTER \_ SYSTEM \_ CONFIG \_ CHANGED**
</dt> <dd> <dl> <dt>

5077 (0x13D5)
</dt> <dt>



La configuración del sistema cambió durante la operación de combinación o formulario del clúster. Se anuló la operación de combinación o formulario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**NO SE \_ ENCONTRÓ EL TIPO DE RECURSO DE CLÚSTER DE \_ \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5078 (0x13D6)
</dt> <dt>



No se encontró el tipo de recurso especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR \_ CLUSTER \_ RESTYPE \_ NOT \_ SUPPORTED**
</dt> <dd> <dl> <dt>

5079 (0x13D7)
</dt> <dt>



El nodo especificado no admite un recurso de este tipo. Esto puede deberse a incoherencias de la versión o a la ausencia del archivo DLL de recursos en este nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR \_ CLUSTER \_ RESNAME \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

5080 (0x13D8)
</dt> <dt>



Este archivo DLL de recursos no admite el nombre de recurso especificado. Esto puede deberse a un nombre no correcto (o cambiado) proporcionado al archivo DLL de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**CLÚSTER DE \_ ERRORES \_ SIN \_ PAQUETES RPC \_ \_ REGISTRADOS**
</dt> <dd> <dl> <dt>

5081 (0x13D9)
</dt> <dt>



No se pudo registrar ningún paquete de autenticación con el servidor RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR \_ CLUSTER \_ OWNER \_ NOT \_ IN \_ PREFLIST**
</dt> <dd> <dl> <dt>

5082 (0x13DA)
</dt> <dt>



No puede poner el grupo en línea porque el propietario del grupo no está en la lista preferida del grupo. Para cambiar el nodo propietario del grupo, mueva el grupo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR \_ CLUSTER \_ DATABASE \_ SEQMISMATCH**
</dt> <dd> <dl> <dt>

5083 (0x13DB)
</dt> <dt>



Error en la operación de combinación porque el número de secuencia de la base de datos del clúster ha cambiado o no es compatible con el nodo locker. Esto puede ocurrir durante una operación de combinación si la base de datos del clúster cambiaba durante la combinación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ESTADO \_ NO VÁLIDO DE RESMON DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5084 (0x13DC)
</dt> <dt>



El monitor de recursos no permitirá que se realice la operación de error mientras el recurso está en su estado actual. Esto puede ocurrir si el recurso está en un estado pendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR \_ CLUSTER \_ NO \_ LOCKER \_**
</dt> <dd> <dl> <dt>

5085 (0x13DD)
</dt> <dt>



Un código que no es de Locker recibió una solicitud para reservar el bloqueo para realizar actualizaciones globales.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**DISCO \_ DE CUÓRUM DE ERROR NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

5086 (0x13DE)
</dt> <dt>



El servicio de clúster no pudo encontrar el disco de cuórum.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR \_ DATABASE \_ BACKUP \_ CORRUPT**
</dt> <dd> <dl> <dt>

5087 (0x13DF)
</dt> <dt>



Es posible que la base de datos del clúster de la que se ha copiado la copia de seguridad esté dañada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**EL \_ NODO DE CLÚSTER DE ERRORES YA TIENE LA RAÍZ \_ \_ \_ \_ DFS \_**
</dt> <dd> <dl> <dt>

5088 (0x13E0)
</dt> <dt>



Ya existe una raíz DFS en este nodo de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR \_ RESOURCE \_ PROPERTY \_ UNCHANGEABLE**
</dt> <dd> <dl> <dt>

5089 (0x13E1)
</dt> <dt>



Error al intentar modificar una propiedad de recurso porque entra en conflicto con otra propiedad existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ESTADO NO \_ VÁLIDO DE PERTENENCIA AL CLÚSTER DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5890 (0x1702)
</dt> <dt>



Se intentó realizar una operación que no es compatible con el estado de pertenencia actual del nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR \_ CLUSTER \_ QUORUMLOG \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

5891 (0x1703)
</dt> <dt>



El recurso de cuórum no contiene el registro de cuórum.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR \_ CLUSTER \_ MEMBERSHIP \_ HALT**
</dt> <dd> <dl> <dt>

5892 (0x1704)
</dt> <dt>



El motor de pertenencia solicitó el cierre del servicio de clúster en este nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR \_ CLUSTER \_ INSTANCE \_ ID \_ MISMATCH**
</dt> <dd> <dl> <dt>

5893 (0x1705)
</dt> <dt>



Error en la operación de combinación porque el identificador de instancia del clúster del nodo de unión no coincide con el identificador de instancia del clúster del nodo patrocinador.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR \_ CLUSTER \_ NETWORK \_ NOT \_ FOUND \_ FOR \_ IP**
</dt> <dd> <dl> <dt>

5894 (0x1706)
</dt> <dt>



No se encontró una red de clúster correspondiente para la dirección IP especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR \_ CLUSTER \_ PROPERTY \_ DATA \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

5895 (0x1707)
</dt> <dt>



El tipo de datos real de la propiedad no coincide con el tipo de datos esperado de la propiedad.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR \_ CLUSTER \_ EVICT \_ WITHOUT \_ CLEANUP**
</dt> <dd> <dl> <dt>

5896 (0x1708)
</dt> <dt>



El nodo del clúster se expulsó correctamente del clúster, pero el nodo no se ha limpiado. Para determinar qué pasos de limpieza no se realizaron correctamente y cómo recuperarlo, consulte el registro de eventos de la aplicación clústeres de conmutación por error Visor de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR \_ CLUSTER \_ PARAMETER \_ MISMATCH**
</dt> <dd> <dl> <dt>

5897 (0x1709)
</dt> <dt>



Dos o más valores de parámetro especificados para las propiedades de un recurso están en conflicto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**EL \_ NODO DE ERROR NO SE PUEDE \_ \_ \_ AGRUPAR EN CLÚSTERES**
</dt> <dd> <dl> <dt>

5898 (0x170A)
</dt> <dt>



Este equipo no se puede convertir en miembro de un clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR \_ CLUSTER \_ WRONG \_ OS \_ VERSION**
</dt> <dd> <dl> <dt>

5899 (0x170B)
</dt> <dt>



Este equipo no se puede convertir en miembro de un clúster porque no tiene instalada la versión Windows correcta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR \_ CLUSTER \_ CANT \_ CREATE \_ DUP \_ CLUSTER \_ NAME**
</dt> <dd> <dl> <dt>

5900 (0x170C)
</dt> <dt>



No se puede crear un clúster con el nombre de clúster especificado porque ese nombre de clúster ya está en uso. Especifique un nombre diferente para el clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR \_ CLUSCFG \_ YA \_ CONFIRMADO**
</dt> <dd> <dl> <dt>

5901 (0x170D)
</dt> <dt>



La acción de configuración del clúster ya se ha confirmado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR \_ CLUSCFG \_ ROLLBACK \_ FAILED**
</dt> <dd> <dl> <dt>

5902 (0x170E)
</dt> <dt>



No se pudo revertir la acción de configuración del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR \_ CLUSCFG \_ SYSTEM \_ DISK \_ DRIVE \_ LETTER \_ CONFLICT**
</dt> <dd> <dl> <dt>

5903 (0x170F)
</dt> <dt>



La letra de unidad asignada a un disco del sistema en un nodo entraba en conflicto con la letra de unidad asignada a un disco en otro nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**VERSIÓN ANTERIOR \_ DEL \_ CLÚSTER DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5904 (0x1710)
</dt> <dt>



Uno o varios nodos del clúster ejecutan una versión de Windows que no admite esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR \_ CLUSTER \_ UNTCHED \_ COMPUTER \_ ACCT \_ NAME**
</dt> <dd> <dl> <dt>

5905 (0x1711)
</dt> <dt>



El nombre de la cuenta de equipo correspondiente no coincide con el nombre de red de este recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**CLÚSTER DE \_ ERRORES \_ SIN \_ ADAPTADORES DE \_ RED**
</dt> <dd> <dl> <dt>

5906 (0x1712)
</dt> <dt>



No hay adaptadores de red disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**CLÚSTER \_ DE ERRORES \_ DUDOSO**
</dt> <dd> <dl> <dt>

5907 (0x1713)
</dt> <dt>



El nodo del clúster se ha dudoso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**MOVIMIENTO DEL \_ GRUPO \_ DE CLÚSTERES DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5908 (0x1714)
</dt> <dt>



El grupo no puede aceptar la solicitud porque se está moviendo a otro nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ TYPE \_ BUSY**
</dt> <dd> <dl> <dt>

5909 (0x1715)
</dt> <dt>



El tipo de recurso no puede aceptar la solicitud porque está demasiado ocupado realizando otra operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**TIEMPO DE \_ ESPERA DE LA LLAMADA DE RECURSO DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5910 (0x1716)
</dt> <dt>



Se ha producido un tiempo de espera de la llamada a la DLL del recurso de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR \_ DIRECCIÓN \_ \_ IPV6 DE CLÚSTER NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

5911 (0x1717)
</dt> <dt>



La dirección no es válida para un recurso de dirección IPv6. Se requiere una dirección IPv6 global y debe coincidir con una red de clúster. No se permiten direcciones de compatibilidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR \_ CLUSTER \_ INTERNAL \_ INVALID \_ FUNCTION**
</dt> <dd> <dl> <dt>

5912 (0x1718)
</dt> <dt>



Error interno del clúster. Se intentó llamar a una función no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**PARÁMETRO \_ DE CLÚSTER DE ERRORES FUERA DE \_ \_ \_ \_ LÍMITES**
</dt> <dd> <dl> <dt>

5913 (0x1719)
</dt> <dt>



Un valor de parámetro está fuera del intervalo aceptable.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR \_ CLUSTER \_ PARTIAL \_ SEND**
</dt> <dd> <dl> <dt>

5914 (0x171A)
</dt> <dt>



Error de red al enviar datos a otro nodo del clúster. El número de bytes transmitidos fue menor que el requerido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR \_ CLUSTER \_ REGISTRY \_ INVALID \_ FUNCTION**
</dt> <dd> <dl> <dt>

5915 (0x171B)
</dt> <dt>



Se intentó realizar una operación de registro de clúster no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**TERMINACIÓN DE \_ CADENA NO VÁLIDA DEL CLÚSTER DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5916 (0x171C)
</dt> <dt>



Una cadena de entrada de caracteres no termina correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**FORMATO DE \_ CADENA NO VÁLIDO DEL CLÚSTER DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5917 (0x171D)
</dt> <dt>



Una cadena de entrada de caracteres no tiene un formato válido para los datos que representa.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**TRANSACCIÓN DE \_ BASE DE DATOS DE CLÚSTER DE ERRORES EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5918 (0x171E)
</dt> <dt>



Error interno del clúster. Se intentó realizar una transacción de base de datos de clúster mientras una transacción ya estaba en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR LA \_ TRANSACCIÓN DE \_ BASE DE DATOS DEL CLÚSTER NO ESTÁ EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5919 (0x171F)
</dt> <dt>



Error interno del clúster. Se intentó confirmar una transacción de base de datos de clúster mientras no había ninguna transacción en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**DATOS NULL \_ DEL \_ CLÚSTER DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5920 (0x1720)
</dt> <dt>



Error interno del clúster. Los datos no se inicializaron correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**LECTURA \_ PARCIAL DEL CLÚSTER DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5921 (0x1721)
</dt> <dt>



Error al leer desde un flujo de datos. Se devolvió un número inesperado de bytes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ESCRITURA \_ PARCIAL DEL CLÚSTER DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5922 (0x1722)
</dt> <dt>



Error al escribir en un flujo de datos. No se pudo escribir el número necesario de bytes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR \_ CLUSTER \_ CANT \_ DESERIALIZE \_ DATA**
</dt> <dd> <dl> <dt>

5923 (0x1723)
</dt> <dt>



Error al deserializar un flujo de datos del clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR \_ DEPENDENT \_ RESOURCE \_ PROPERTY \_ CONFLICT**
</dt> <dd> <dl> <dt>

5924 (0x1724)
</dt> <dt>



Uno o varios valores de propiedad para este recurso están en conflicto con uno o varios valores de propiedad asociados a sus recursos dependientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR \_ CLUSTER \_ NO \_ QUORUM**
</dt> <dd> <dl> <dt>

5925 (0x1725)
</dt> <dt>



No había un cuórum de nodos de clúster para formar un clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR \_ CLUSTER \_ INVALID \_ IPV6 \_ NETWORK**
</dt> <dd> <dl> <dt>

5926 (0x1726)
</dt> <dt>



La red del clúster no es válida para un recurso de dirección IPv6 o no coincide con la dirección configurada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR \_ CLUSTER \_ INVALID \_ IPV6 \_ TUNNEL \_ NETWORK**
</dt> <dd> <dl> <dt>

5927 (0x1727)
</dt> <dt>



La red del clúster no es válida para un recurso de Tunnel IPv6. Compruebe la configuración del recurso de dirección IP del que depende el recurso Tunnel IPv6.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**CUÓRUM \_ DE ERROR NO PERMITIDO EN ESTE \_ \_ \_ \_ \_ GRUPO**
</dt> <dd> <dl> <dt>

5928 (0x1728)
</dt> <dt>



El recurso de cuórum no puede residir en el grupo Storage disponibilidad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ÁRBOL DE \_ \_ DEPENDENCIAS DE \_ ERROR DEMASIADO \_ COMPLEJO**
</dt> <dd> <dl> <dt>

5929 (0x1729)
</dt> <dt>



Las dependencias de este recurso están anidadas demasiado profundamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**EXCEPCIÓN \_ DE ERROR EN LA LLAMADA DE \_ \_ \_ RECURSO**
</dt> <dd> <dl> <dt>

5930 (0x172A)
</dt> <dt>



La llamada a la DLL de recursos produjo una excepción no controlada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR DE \_ INICIALIZACIÓN \_ DE RHS \_ DEL CLÚSTER DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5931 (0x172B)
</dt> <dt>



No se pudo inicializar el proceso RHS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**CLÚSTER \_ DE ERRORES NO \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

5932 (0x172C)
</dt> <dt>



La característica Clústeres de conmutación por error no está instalada en este nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**LOS \_ RECURSOS DEL CLÚSTER DE ERRORES DEBEN ESTAR EN LÍNEA EN EL MISMO \_ \_ \_ \_ \_ \_ \_ \_ NODO**
</dt> <dd> <dl> <dt>

5933 (0x172D)
</dt> <dt>



Los recursos deben estar en línea en el mismo nodo para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR \_ CLUSTER \_ MAX \_ NODES \_ IN \_ CLUSTER**
</dt> <dd> <dl> <dt>

5934 (0x172E)
</dt> <dt>



No se puede agregar un nuevo nodo, ya que este clúster ya está en su número máximo de nodos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**CLÚSTER \_ DE ERRORES \_ \_ DEMASIADOS \_ NODOS**
</dt> <dd> <dl> <dt>

5935 (0x172F)
</dt> <dt>



Este clúster no se puede crear porque el número especificado de nodos supera el límite máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**OBJETO \_ DE CLÚSTER DE ERRORES YA \_ \_ \_ USADO**
</dt> <dd> <dl> <dt>

5936 (0x1730)
</dt> <dt>



Error al intentar usar el nombre de clúster especificado porque ya existe en el dominio un objeto de equipo habilitado con el nombre especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR \_ NO SE ENCONTRARON GRUPOS DE \_ \_ NÚCLEOS**
</dt> <dd> <dl> <dt>

5937 (0x1731)
</dt> <dt>



Este clúster no se puede destruir. Tiene grupos de aplicaciones no principales que se deben eliminar antes de que se pueda destruir el clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**CONFLICTO DE \_ RECURSOS DEL RECURSO COMPARTIDO DE ARCHIVOS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5938 (0x1732)
</dt> <dt>



El recurso compartido de archivos asociado al recurso testigo de recurso compartido de archivos no se puede hospedar en este clúster ni en ninguno de sus nodos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR \_ CLUSTER \_ EVICT \_ INVALID \_ REQUEST**
</dt> <dd> <dl> <dt>

5939 (0x1733)
</dt> <dt>



La expulsión de este nodo no es válida en este momento. Debido a los requisitos de cuórum, la expulsión del nodo provocará el cierre del clúster. Si es el último nodo del clúster, debe usarse el comando destroy cluster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**RECURSO \_ \_ SINGLETON DEL CLÚSTER DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5940 (0x1734)
</dt> <dt>



Solo se permite una instancia de este tipo de recurso en el clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**RECURSO \_ \_ SINGLETON DEL GRUPO \_ DE CLÚSTERES DE \_ ERRORES**
</dt> <dd> <dl> <dt>

5941 (0x1735)
</dt> <dt>



Solo se permite una instancia de este tipo de recurso por grupo de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR DEL \_ PROVEEDOR DE RECURSOS DE \_ \_ \_ CLÚSTER**
</dt> <dd> <dl> <dt>

5942 (0x1736)
</dt> <dt>



El recurso no pudo estar en línea debido al error de uno o varios recursos del proveedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR DE \_ CONFIGURACIÓN DE RECURSOS DE \_ \_ \_ CLÚSTER**
</dt> <dd> <dl> <dt>

5943 (0x1737)
</dt> <dt>



El recurso ha indicado que no puede estar en línea en ningún nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**GRUPO DE \_ \_ CLÚSTERES DE ERRORES \_ OCUPADO**
</dt> <dd> <dl> <dt>

5944 (0x1738)
</dt> <dt>



La operación actual no se puede realizar en este grupo en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR \_ CLUSTER \_ NOT \_ SHARED \_ VOLUME**
</dt> <dd> <dl> <dt>

5945 (0x1739)
</dt> <dt>



El directorio o archivo no se encuentra en un volumen compartido de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**DESCRIPTOR DE \_ SEGURIDAD NO VÁLIDO DEL CLÚSTER DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5946 (0x173A)
</dt> <dt>



El descriptor de seguridad no cumple los requisitos de un clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR CLUSTER SHARED VOLUMES IN USE (VOLÚMENES \_ \_ \_ COMPARTIDOS DE CLÚSTER \_ DE ERRORES EN \_ USO)**
</dt> <dd> <dl> <dt>

5947 (0x173B)
</dt> <dt>



Hay uno o varios recursos de volúmenes compartidos configurados en el clúster. Esos recursos deben moverse al almacenamiento disponible para que la operación se pueda realizar correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR \_ CLUSTER \_ USE \_ SHARED \_ VOLUMES \_ API**
</dt> <dd> <dl> <dt>

5948 (0x173C)
</dt> <dt>



Este grupo o recurso no se puede manipular directamente. Use las API de volumen compartido para realizar la operación deseada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**COPIA DE \_ SEGURIDAD DEL CLÚSTER DE ERRORES EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5949 (0x173D)
</dt> <dt>



La copia de seguridad está en curso. Espere a que finalice la copia de seguridad antes de volver a intentar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR \_ RUTA DE ACCESO QUE NO ES \_ \_ CSV**
</dt> <dd> <dl> <dt>

5950 (0x173E)
</dt> <dt>



La ruta de acceso no pertenece a un volumen compartido de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR \_ VOLUMEN CSV NO \_ \_ \_ LOCAL**
</dt> <dd> <dl> <dt>

5951 (0x173F)
</dt> <dt>



El volumen compartido del clúster no se monta localmente en este nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR \_ CLUSTER \_ WATCHDOG \_ TERMINATING**
</dt> <dd> <dl> <dt>

5952 (0x1740)
</dt> <dt>



El watchdog del clúster está finalizando.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ VETOED \_ MOVE \_ INCOMPATIBLE \_ NODES**
</dt> <dd> <dl> <dt>

5953 (0x1741)
</dt> <dt>



Un recurso vetó un movimiento entre dos nodos porque no son compatibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**PESO DE \_ NODO NO VÁLIDO DEL CLÚSTER DE \_ \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

5954 (0x1742)
</dt> <dt>



La solicitud no es válida porque no se puede cambiar el peso del nodo mientras el clúster está en modo de cuórum de solo disco, o porque cambiar el peso del nodo infringiría los requisitos mínimos de cuórum de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ VETOED \_ CALL**
</dt> <dd> <dl> <dt>

5955 (0x1743)
</dt> <dt>



El recurso vetó la llamada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**FALTA \_ DE RECURSOS DEL SISTEMA RESMON DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

5956 (0x1744)
</dt> <dt>



El recurso no se pudo iniciar ni ejecutar porque no pudo reservar suficientes recursos del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ VETOED \_ MOVE \_ NOT \_ ENOUGH \_ RESOURCES \_ ON \_ DESTINATION**
</dt> <dd> <dl> <dt>

5957 (0x1745)
</dt> <dt>



Un recurso vetó un movimiento entre dos nodos porque el destino no tiene recursos suficientes para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ VETOED \_ MOVE \_ NOT \_ ENOUGH \_ RESOURCES \_ ON \_ SOURCE**
</dt> <dd> <dl> <dt>

5958 (0x1746)
</dt> <dt>



Un recurso vetó un movimiento entre dos nodos porque el origen no tiene recursos suficientes para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**GRUPO \_ DE \_ CLÚSTERES DE ERRORES EN \_ COLA**
</dt> <dd> <dl> <dt>

5959 (0x1747)
</dt> <dt>



La operación solicitada no se puede completar porque el grupo está en cola para una operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ LOCKED \_ STATUS**
</dt> <dd> <dl> <dt>

5960 (0x1748)
</dt> <dt>



La operación solicitada no se puede completar porque un recurso tiene el estado bloqueado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR \_ CLUSTER \_ SHARED \_ VOLUME \_ FAILOVER \_ NOT \_ ALLOWED**
</dt> <dd> <dl> <dt>

5961 (0x1749)
</dt> <dt>



El recurso no puede moverse a otro nodo porque un volumen compartido de clúster vetó la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**PURGA DEL \_ NODO DEL CLÚSTER DE ERRORES EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

5962 (0x174A)
</dt> <dt>



Ya hay una purga de nodos en curso.

Este valor también se **denominaBA ERROR \_ CLUSTER NODE \_ \_ ESTADESODO \_ EN \_ CURSO**


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**DISCO \_ DE CLÚSTER DE ERROR NO \_ \_ \_ CONECTADO**
</dt> <dd> <dl> <dt>

5963 (0x174B)
</dt> <dt>



El almacenamiento en clúster no está conectado al nodo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**DISCO DE ERROR \_ \_ NO COMPATIBLE CON \_ CSV \_**
</dt> <dd> <dl> <dt>

5964 (0x174C)
</dt> <dt>



El disco no está configurado de forma que se pueda usar con CSV. Los discos CSV deben tener al menos una partición con formato NTFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**RECURSO DE \_ ERROR NO EN EL ALMACENAMIENTO \_ \_ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

5965 (0x174D)
</dt> <dt>



El recurso debe formar parte del grupo Storage disponible para completar esta acción.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR \_ CLUSTER \_ SHARED \_ VOLUME \_ REDIRECTED**
</dt> <dd> <dl> <dt>

5966 (0x174E)
</dt> <dt>



Error en la operación de CSVFS, ya que el volumen está en modo redirigido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR \_ CLUSTER \_ SHARED \_ VOLUME \_ NOT \_ REDIRECTED**
</dt> <dd> <dl> <dt>

5967 (0x174F)
</dt> <dt>



Error en la operación de CSVFS, ya que el volumen no está en modo redirigido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**EL CLÚSTER \_ DE ERRORES NO PUEDE DEVOLVER \_ \_ \_ PROPIEDADES**
</dt> <dd> <dl> <dt>

5968 (0x1750)
</dt> <dt>



Las propiedades del clúster no se pueden devolver en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**EL RECURSO \_ DE CLÚSTER DE ERRORES CONTIENE UN ÁREA DE \_ \_ \_ \_ \_ DIFERENCIAS NO ADMITIDA PARA \_ \_ VOLÚMENES \_ COMPARTIDOS**
</dt> <dd> <dl> <dt>

5969 (0x1751)
</dt> <dt>



El recurso de disco en clúster contiene el área de diferencias de instantáneas de software que no se admiten para volúmenes compartidos de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**EL RECURSO \_ DE CLÚSTER DE ERRORES ESTÁ EN MODO DE \_ \_ \_ \_ \_ MANTENIMIENTO**
</dt> <dd> <dl> <dt>

5970 (0x1752)
</dt> <dt>



La operación no se puede completar porque el recurso está en modo de mantenimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR \_ CLUSTER \_ AFFINITY \_ CONFLICT**
</dt> <dd> <dl> <dt>

5971 (0x1753)
</dt> <dt>



La operación no se puede completar debido a conflictos de afinidad de clúster.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR \_ CLUSTER \_ RESOURCE \_ IS \_ REPLICA \_ VIRTUAL \_ MACHINE**
</dt> <dd> <dl> <dt>

5972 (0x1754)
</dt> <dt>



La operación no se puede completar porque el recurso es una máquina virtual de réplica.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




