---
title: Valores devueltos de BITS
description: El archivo Bitsmsg.h contiene las siguientes constantes de valor devuelto.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS de errores
- errores bits , códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c6795572a2f81324e287c385a78e22e0b195dbbc3af061585fc847c464a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173834"
---
# <a name="bits-return-values"></a>Valores devueltos de BITS

El archivo Bitsmsg.h contiene las siguientes constantes de valor devuelto. Las constantes representan los valores devueltos que BITS genera y los valores devueltos HTTP que bits captura. Todos los demás valores devueltos que puede recibir son COM, RPC o valores devueltos Windows convertidos (BITS usa la macro [HRESULT \_ FROM \_ WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para convertir los valores devueltos de Windows en valores HRESULT).

Tenga en cuenta que el archivo Bitsmsg.h contiene valores devueltos adicionales que no se enumeran a continuación.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG \_ S PARTIAL COMPLETE \_ \_ (0x00200017)
</dt> <dd>

Subconjunto de los archivos del trabajo transferidos correctamente antes de llamar al método [**IBackgroundCopyJob::Complete.**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) Se eliminaron aquellas que no se completaron.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S NO PUEDE ELIMINAR ARCHIVOS \_ \_ \_ \_ (0x0020001A)
</dt> <dd>

No se pueden eliminar todos los archivos temporales asociados al trabajo.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ INVALIDADO POR POLICY \_ \_ (0x00200055)
</dt> <dd>

La preferencia de configuración se ha guardado correctamente, pero no se usará porque una configuración directiva de grupo configuración invalida la preferencia.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E NO ENCONTRADO \_ \_ (0x80200001)
</dt> <dd>

No se encontró el trabajo solicitado.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG \_ E ESTADO NO VÁLIDO \_ \_ (0x80200002)
</dt> <dd>

La acción solicitada no se permite en el estado de trabajo actual.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ EMPTY (0x80200003)
</dt> <dd>

El trabajo debe contener uno o varios archivos para poder reanudar el trabajo.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>ARCHIVO \_ BG E NO DISPONIBLE \_ \_ \_ (0x80200004)
</dt> <dd>

La información del archivo no está disponible porque el error no está asociado a un archivo local o remoto.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>PROTOCOLO BG \_ E \_ NO DISPONIBLE \_ \_ (0x80200005)
</dt> <dd>

La información del protocolo no está disponible porque el error no está asociado al protocolo de transferencia especificado.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG \_ E DESTINATION LOCKED \_ \_ (0x8020000D)
</dt> <dd>

El volumen del sistema de archivos de destino, especificado en el nombre de archivo local, está bloqueado.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>CAMBIO \_ DE VOLUMEN BG E \_ \_ (0x8020000E)
</dt> <dd>

El volumen de destino, especificado en el nombre de archivo local, ha cambiado. Por ejemplo, el disquete original se ha reemplazado por otro disquete.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>INFORMACIÓN \_ DE ERROR BG E NO DISPONIBLE \_ \_ \_ (0x8020000F)
</dt> <dd>

La información de error solo está disponible cuando el estado del trabajo es BG \_ JOB \_ STATE \_ ERROR. La información de error no está disponible después de que BITS comience a transferir los datos del trabajo o el cliente salga.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ NETWORK \_ DISCONNECTED (0x80200010)
</dt> <dd>

El adaptador de red está inactivo o desconectado. Todos los trabajos se colocan en el estado BG \_ JOB \_ STATE TRANSIENT \_ \_ ERROR.

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG \_ E MISSING FILE SIZE \_ \_ \_ (0X80200011)
</dt> <dd>

El servidor no devolución del tamaño del archivo. BITS solo transfiere contenido estático y requiere que el servidor HTTP devuelva el encabezado Content-Length. Se produce un error en la solicitud de transferencia si la dirección URL apunta al contenido dinámico.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG \_ E COMPATIBILIDAD HTTP INSUFICIENTE \_ \_ \_ (0x80200012)
</dt> <dd>

El servidor no admite el protocolo HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG \_ E INSUFFICIENT RANGE SUPPORT \_ \_ \_ (0x80200013)
</dt> <dd>

El servidor no admite el encabezado Content-Range. Normalmente, recibe este error al intentar descargar contenido dinámico. También puede recibir este error si un proxy intermedio quita el encabezado Content-Range o Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E REMOTE NO SE ADMITE \_ \_ \_ (0x80200014)
</dt> <dd>

No se admite el uso remoto de BITS. Para obtener más información, vea [Usuarios y conexiones de red.](users-and-network-connections.md)

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>ASIGNACIÓN DE DIFERENCIAS DE NUEVO PROPIETARIO DE BG \_ E \_ \_ \_ \_ (0x80200015)
</dt> <dd>

La asignación de unidades de red para el archivo local es diferente para el propietario actual que para el propietario anterior.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E NEW OWNER NO FILE ACCESS \_ \_ \_ \_ \_ (0X80200016)
</dt> <dd>

El nuevo propietario no tiene permisos suficientes para los archivos de trabajo temporales.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG \_ E PROXY LIST TOO LARGE \_ \_ \_ \_ (0x80200018)
</dt> <dd>

La lista de proxy HTTP es demasiado larga. La lista no debe superar los 32 KB.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG \_ E PROXY BYPASS LIST TOO LARGE \_ \_ \_ \_ \_ (0x80200019)
</dt> <dd>

La lista de omisión del proxy HTTP es demasiado larga. La lista no debe superar los 32 KB.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ \_ \_ DEMASIADOS ARCHIVOS (0x8020001C)
</dt> <dd>

No puede agregar más de un archivo a un trabajo de carga.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>ARCHIVO LOCAL BG \_ E \_ CAMBIADO \_ \_ (0x8020001D)
</dt> <dd>

El contenido del archivo local cambió después de que se iniciara el proceso de transferencia. El contenido del archivo local no puede cambiar después de que el proceso de transferencia comience en un trabajo de carga o de respuesta.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E TOO LARGE \_ \_ (0x80200020)
</dt> <dd>

El tamaño del archivo de carga supera el tamaño máximo permitido de carga especificado en el servidor.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG \_ E STRING TOO LONG \_ \_ \_ (0x80200021)
</dt> <dd>

La cadena especificada es demasiado larga.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>ERROR DE COINCIDENCIA DEL PROTOCOLO DEL SERVIDOR CLIENTE BG \_ E \_ \_ \_ \_ (0x80200022)
</dt> <dd>

El cliente y el servidor no pudieron negociar un protocolo para usarlo para el trabajo de carga.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG \_ E SERVER EXECUTE ENABLED \_ \_ \_ (0x80200023)
</dt> <dd>

Los permisos de scripting o ejecución están habilitados en el directorio virtual de IIS asociado al trabajo. Para cargar archivos en el directorio virtual, deshabilite los permisos de scripting y ejecución en el directorio virtual.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E USERNAME TOO LARGE \_ \_ \_ (0X80200025)
</dt> <dd>

El nombre de usuario no puede superar los 300 caracteres.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG \_ E PASSWORD TOO LARGE \_ \_ \_ (0x80200026)
</dt> <dd>

La contraseña no puede superar los 65535 caracteres.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>DESTINO \_ DE AUTENTICACIÓN NO VÁLIDO BG E \_ \_ \_ (0x80200027)
</dt> <dd>

El destino de autenticación especificado no es válido.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>ESQUEMA DE AUTENTICACIÓN NO VÁLIDO DE BG \_ E \_ \_ \_ (0x80200028)
</dt> <dd>

El esquema de autenticación especificado no es válido.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG \_ E INTERVALO NO VÁLIDO \_ \_ (0x8020002B)
</dt> <dd>

El intervalo de bytes especificado no es válido. El intervalo de bytes debe existir dentro del archivo remoto especificado.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>RANGOS \_ BG E \_ \_ SUPERPUESTOS (0x8020002C)
</dt> <dd>

La lista de intervalos de bytes contiene intervalos superpuestos o duplicados, que no se admiten.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E BLOCKED BY POLICY \_ \_ \_ (0x8020003E)
</dt> <dd>

directiva de grupo configuración impide que los trabajos en segundo plano se ejecuten en este momento. Para más información, consulte la [directiva MaxInternetBandwidth.](group-policies.md)

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG \_ E INVALID PROXY INFO \_ \_ \_ (0x8020003F)
</dt> <dd>

Error en tiempo de ejecución que indica que la lista de proxy o la lista de omisión de proxy que especificó mediante el método [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) no es válida.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG \_ E CREDENCIALES NO \_ \_ VÁLIDAS (0x80200040)
</dt> <dd>

El formato de las credenciales de seguridad proporcionadas no es válido.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG \_ E RECORD DELETED \_ \_ (0x80200042)
</dt> <dd>

Se ha eliminado el registro de caché. El intento de actualizarlo se ha abandonado.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_ERROR BG E \_ UPNP \_ (0x80200045)
</dt> <dd>

Se ha producido Plug and Play universal (UPnP). Compruebe el dispositivo de puerta de enlace de Internet.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E \_ PEERCACHING DESHABILITADO \_ (0x80200047)
</dt> <dd>

El almacenamiento en caché del mismo nivel está deshabilitado.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)
</dt> <dd>

El registro de caché está en uso y no se puede cambiar ni eliminar. Vuelva a intentarlo después de unos segundos.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ \_ DEMASIADOS TRABAJOS POR USUARIO \_ \_ \_ (0x80200049)
</dt> <dd>

El número de trabajos del usuario ha superado el límite de trabajos por usuario establecido por la configuración de directiva de grupo MaxJobsPerUser.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ \_ DEMASIADOS TRABAJOS POR MÁQUINA \_ \_ \_ (0x80200050)
</dt> <dd>

El número de trabajos del equipo ha superado el límite de trabajos por equipo establecido por la configuración de directiva de grupo MaxJobsPerMachine.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ \_ DEMASIADOS ARCHIVOS EN EL TRABAJO \_ \_ \_ (0X80200051)
</dt> <dd>

El número de archivos del trabajo ha superado el límite de archivos por trabajo establecido por la configuración de directiva de grupo MaxFilesPerJob.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E TOO MANY \_ \_ \_ RANGES IN FILE \_ \_ (0X80200052)
</dt> <dd>

El número de intervalos del archivo ha superado el límite por intervalo de archivos establecido por la configuración de directiva de grupo MaxRangesPerFile.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>ERROR DE VALIDACIÓN DE BG \_ E \_ \_ (0x80200053)
</dt> <dd>

La aplicación solicitó datos de un sitio web, pero la respuesta no fue válida. Para más información, use Visor de eventos para ver el registro operativo de \\ Microsoft \\ Windows \\ \\ bits-client.

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG \_ E \_ MAXDOWNLOAD TIMEOUT \_ (0x80200054)
</dt> <dd>

Bits ha pasado el tiempo de espera al descargar el trabajo. La descarga no se ha completado dentro del tiempo de descarga máximo establecido en el trabajo o en la configuración de directiva de grupo MaxDownloadTime.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>ERROR \_ \_ HTTP \_ \_ 400 DE BG E (0x80190190)
</dt> <dd>

El servidor no pudo procesar la solicitud de transferencia porque la sintaxis del nombre de archivo remoto no es válida.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>ERROR \_ \_ HTTP \_ \_ 401 de BG E (0x80190191)
</dt> <dd>

El usuario no tiene permiso para acceder al archivo remoto. El recurso solicitado requiere autenticación de usuarios.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>ERROR \_ \_ HTTP \_ 404 DE BG E \_ (0x80190194)
</dt> <dd>

La dirección URL solicitada no existe en el servidor.

En IIS 7, este error puede indicar

-   Las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.
-   Que el tamaño de carga supera el límite máximo de carga (para obtener más información, vea la propiedad de extensión DE IIS [**BITSMaximumUploadSize).**](bits-iis-extension-properties.md)

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>ERROR HTTP DE BG \_ E \_ \_ \_ 407 (0x80190197)
</dt> <dd>

El usuario no tiene permiso para acceder al proxy. El proxy requiere autenticación de usuario.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>ERROR \_ \_ HTTP \_ \_ 414 DE BG E (0x8019019E)
</dt> <dd>

El servidor no puede procesar la solicitud de transferencia. El identificador uniforme de recursos (URI) en el nombre de archivo remoto es más largo de lo que el servidor puede interpretar.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>ERROR \_ \_ HTTP \_ \_ 501 de BG E (0x801901F5)
</dt> <dd>

El servidor no admite la funcionalidad necesaria para satisfacer la solicitud. En IIS 6, este error indica que las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>ERROR \_ \_ HTTP \_ \_ 503 de BG E (0x801901F7)
</dt> <dd>

El servicio está sobrecargado temporalmente y no puede procesar la solicitud. Reanude el trabajo más adelante.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>ERROR HTTP DE BG \_ E \_ \_ \_ 504 (0x801901F8)
</dt> <dd>

Se ha producido un tiempo de espera de la solicitud de transferencia mientras se esperaba una puerta de enlace. Reanude el trabajo más adelante.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>ERROR HTTP DE BG \_ E \_ \_ \_ 505 (0x801901F9)
</dt> <dd>

El servidor no admite la versión del protocolo HTTP especificada en el nombre de archivo remoto.

</dd> </dl>

El archivo de encabezado Bitsmsg.h contiene valores devueltos HTTP adicionales no enumerados anteriormente que BITS usa internamente. Para obtener información sobre estos y otros valores devueltos HTTP que puede recibir, vea la especificación RFC 2616 del Grupo de tareas de ingeniería de Internet en [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 