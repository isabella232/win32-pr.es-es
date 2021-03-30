---
title: Valores devueltos de BITS
description: El archivo Bitsmsg. h contiene las siguientes constantes de valor devuelto.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BITS de errores
- BITS de errores, códigos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995501"
---
# <a name="bits-return-values"></a>Valores devueltos de BITS

El archivo Bitsmsg. h contiene las siguientes constantes de valor devuelto. Las constantes representan los valores devueltos que genera BITS y los valores devueltos de HTTP que BITS captura. Todos los demás valores devueltos que puede recibir son COM, RPC o valores devueltos de Windows convertidos (BITS usa el [valor HRESULT de la macro \_ \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) para convertir los valores devueltos de Windows en valores HRESULT).

Tenga en cuenta que el archivo Bitsmsg. h contiene valores devueltos adicionales que no se enumeran a continuación.

<dl> <dt>

<span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>Total de BG \_ S \_ parcial \_ (0x00200017)
</dt> <dd>

Un subconjunto de los archivos del trabajo transferidos correctamente antes de que se llamara al método [**IBackgroundCopyJob:: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Se eliminaron los que no se completaron.

</dd> <dt>

<span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG \_ S \_ no \_ puede \_ eliminar \_ archivos (0x0020001A)
</dt> <dd>

No se pueden eliminar todos los archivos temporales asociados al trabajo.

</dd> <dt>

<span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ S \_ invalidada \_ por la \_ Directiva (0x00200055)
</dt> <dd>

La preferencia de configuración se ha guardado correctamente, pero no se usará la preferencia porque un valor de directiva de grupo configurado invalida la preferencia.

</dd> <dt>

<span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ no \_ encontrado (0x80200001)
</dt> <dd>

No se encontró el trabajo solicitado.

</dd> <dt>

<span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>\_ \_ Estado no válido de BG E \_ (0x80200002)
</dt> <dd>

La acción solicitada no se permite en el estado de trabajo actual.

</dd> <dt>

<span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)
</dt> <dd>

El trabajo debe contener uno o más archivos para poder reanudar el trabajo.

</dd> <dt>

<span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>Archivo de BG \_ E \_ \_ no \_ disponible (0x80200004)
</dt> <dd>

La información del archivo no está disponible porque el error no está asociado a un archivo local o remoto.

</dd> <dt>

<span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocolo BG \_ E \_ no \_ disponible (0x80200005)
</dt> <dd>

La información del Protocolo no está disponible porque el error no está asociado con el protocolo de transferencia especificado.

</dd> <dt>

<span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>Destino de BG \_ E \_ \_ bloqueado (0x8020000D)
</dt> <dd>

El volumen del sistema de archivos de destino, especificado en el nombre de archivo local, está bloqueado.

</dd> <dt>

<span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>Volumen de BG \_ E \_ \_ cambiado (0x8020000E)
</dt> <dd>

Ha cambiado el volumen de destino especificado en el nombre de archivo local. Por ejemplo, el disquete original se ha reemplazado por un disquete diferente.

</dd> <dt>

<span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>Información de error de BG \_ E \_ \_ \_ no disponible (0x8020000F)
</dt> <dd>

La información del error solo está disponible cuando el estado del trabajo es \_ error de estado del trabajo de BG \_ \_ . La información del error no está disponible después de que BITS empiece a transferir los datos del trabajo o se cierre el cliente.

</dd> <dt>

<span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>\_Red BG \_ E \_ desconectada (0x80200010)
</dt> <dd>

El adaptador de red está inactivo o está desconectado. Todos los trabajos se colocan en el \_ \_ Estado de error transitorio de estado de trabajo de BG \_ \_ .

</dd> <dt>

<span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>\_ \_ Falta el tamaño de archivo de BG E \_ \_ (0x80200011)
</dt> <dd>

El servidor no devolvió el tamaño del archivo. BITS solo transfiere contenido estático y requiere que el servidor HTTP devuelva el encabezado Content-Length. Se produce un error en la solicitud de transferencia si la dirección URL señala a contenido dinámico.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ Compatibilidad con http insuficiente en BG E \_ \_ (0x80200012)
</dt> <dd>

El servidor no admite el protocolo HTTP/1.1.

</dd> <dt>

<span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>\_ \_ Compatibilidad con el intervalo insuficiente de BG E \_ \_ (0x80200013)
</dt> <dd>

El servidor no admite el encabezado Content-Range. Normalmente, recibirá este error al intentar descargar contenido dinámico. También puede recibir este error si un proxy intermedio está quitando el encabezado Content-Range o Content-Length.

</dd> <dt>

<span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ no \_ compatible (0x80200014)
</dt> <dd>

No se admite el uso remoto de BITS. Para obtener más información, consulte [usuarios y conexiones de red](users-and-network-connections.md).

</dd> <dt>

<span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>\_Asignación de diferencias de nuevo propietario de BG E \_ \_ \_ \_ (0x80200015)
</dt> <dd>

La asignación de unidad de red para el archivo local es diferente para el propietario actual que para el propietario anterior.

</dd> <dt>

<span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ New \_ Owner \_ no \_ file \_ Access (0x80200016)
</dt> <dd>

El nuevo propietario no tiene permisos suficientes para los archivos de trabajo temporales.

</dd> <dt>

<span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>Lista de proxy de BG \_ E \_ \_ \_ demasiado \_ grande (0x80200018)
</dt> <dd>

La lista de proxy HTTP es demasiado larga. La lista no debe superar los 32 KB.

</dd> <dt>

<span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>Lista de omisión de proxy de BG \_ E \_ \_ \_ \_ demasiado \_ grande (0x80200019)
</dt> <dd>

La lista de omisión de proxy HTTP es demasiado larga. La lista no debe superar los 32 KB.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>Rebg \_ E \_ demasiados \_ \_ archivos (0x8020001C)
</dt> <dd>

No se puede agregar más de un archivo a un trabajo de carga.

</dd> <dt>

<span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_Cambio de archivo local de BG E \_ \_ \_ (0x8020001D)
</dt> <dd>

El contenido del archivo local cambió después del inicio del proceso de transferencia. El contenido del archivo local no puede cambiar después de que se inicie el proceso de transferencia en un trabajo de carga o de carga-respuesta.

</dd> <dt>

<span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ demasiado \_ grande (0x80200020)
</dt> <dd>

El tamaño del archivo de carga supera el tamaño de carga máximo permitido especificado en el servidor.

</dd> <dt>

<span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>Cadena de BG \_ E \_ \_ demasiado \_ larga (0x80200021)
</dt> <dd>

La cadena especificada es demasiado larga.

</dd> <dt>

<span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>Error \_ de \_ \_ coincidencia del protocolo del servidor cliente de BG E \_ \_ (0x80200022)
</dt> <dd>

El cliente y el servidor no pudieron negociar un protocolo para usarlo en el trabajo de carga.

</dd> <dt>

<span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>Ejecución de BG \_ E \_ Server \_ Execute \_ Enabled (0x80200023)
</dt> <dd>

Los permisos de ejecución o scripting están habilitados en el directorio virtual de IIS asociado al trabajo. Para cargar archivos en el directorio virtual, deshabilite los permisos de ejecución y scripting en el directorio virtual.

</dd> <dt>

<span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ nombreDeUsuario \_ demasiado \_ grande (0x80200025)
</dt> <dd>

El nombre de usuario no puede superar los 300 caracteres.

</dd> <dt>

<span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>La \_ contraseña de BG E \_ \_ es demasiado \_ grande (0x80200026)
</dt> <dd>

La contraseña no puede superar los 65535 caracteres.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>Destino de autenticación de BG \_ E \_ no válido \_ \_ (0x80200027)
</dt> <dd>

El destino de autenticación especificado no es válido.

</dd> <dt>

<span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>\_Esquema de \_ autenticación no válido de BG E \_ \_ (0x80200028)
</dt> <dd>

El esquema de autenticación especificado no es válido.

</dd> <dt>

<span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_ \_ Intervalo no válido de BG E \_ (0x8020002B)
</dt> <dd>

El intervalo de bytes especificado no es válido. El intervalo de bytes debe existir en el archivo remoto especificado.

</dd> <dt>

<span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>\_ \_ Intervalos superpuestos de BG E \_ (0x8020002C)
</dt> <dd>

La lista de intervalos de bytes contiene intervalos superpuestos o duplicados, que no se admiten.

</dd> <dt>

<span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloqueada \_ por la \_ Directiva (0x8020003E)
</dt> <dd>

Directiva de grupo configuración evita que los trabajos en segundo plano se ejecuten en este momento. Para obtener más información, consulte la directiva [MaxInternetBandwidth](group-policies.md) .

</dd> <dt>

<span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_Información de \_ proxy no válida de BG E \_ \_ (0x8020003F)
</dt> <dd>

Error en tiempo de ejecución que indica la lista de proxy o la lista de omisión de proxy que especificó mediante el método [**IBackgroundCopyJob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) no es válido.

</dd> <dt>

<span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>\_ \_ Credenciales no válidas de BG E \_ (0x80200040)
</dt> <dd>

El formato de las credenciales de seguridad proporcionadas no es válido.

</dd> <dt>

<span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>Se \_ eliminó el registro de BG E \_ \_ (0x80200042)
</dt> <dd>

Se ha eliminado el registro de caché. Se ha abandonado el intento de actualización.

</dd> <dt>

<span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>ERROR de desbg \_ E \_ UPnP \_ (0x80200045)
</dt> <dd>

Se ha producido un error de Plug and Play universal (UPnP). Compruebe el dispositivo de puerta de enlace a Internet.

</dd> <dt>

<span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>Deshabilitación de la caché de BG \_ E \_ \_ (0x80200047)
</dt> <dd>

El almacenamiento en caché del mismo nivel está deshabilitado.

</dd> <dt>

<span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)
</dt> <dd>

El registro de caché está en uso y no se puede cambiar ni eliminar. Vuelva a intentarlo después de unos segundos.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ demasiados \_ \_ trabajos \_ por \_ usuario (0x80200049)
</dt> <dd>

El número de trabajos para el usuario ha superado el límite de trabajos por usuario establecido por el valor de MaxJobsPerUser directiva de grupo.

</dd> <dt>

<span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ demasiados \_ \_ trabajos \_ por \_ equipo (0x80200050)
</dt> <dd>

El recuento de trabajos del equipo ha superado el límite de trabajos por equipo establecido por el valor de MaxJobsPerMachine directiva de grupo.

</dd> <dt>

<span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ demasiados \_ \_ archivos \_ en el \_ trabajo (0x80200051)
</dt> <dd>

El número de archivos del trabajo ha superado el límite de archivos por trabajo establecido por el valor de MaxFilesPerJob directiva de grupo.

</dd> <dt>

<span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ demasiados \_ \_ intervalos \_ en el \_ archivo (0x80200052)
</dt> <dd>

El recuento de intervalos del archivo ha superado el límite por intervalo de archivos establecido por el valor de MaxRangesPerFile directiva de grupo.

</dd> <dt>

<span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>Error de validación de BG \_ E \_ \_ (0x80200053)
</dt> <dd>

La aplicación solicitó datos de un sitio web, pero la respuesta no era válida. Para obtener más información, use Visor de eventos para ver los registros de aplicación \\ Microsoft \\ Windows \\ bits- \\ registro operativo del cliente.

</dd> <dt>

<span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>Tiempo de espera de BG \_ E \_ MAXDOWNLOAD \_ (0x80200054)
</dt> <dd>

BITS agotó el tiempo de espera de descarga del trabajo. La descarga no se completó en el tiempo de descarga máximo establecido en el trabajo o en la configuración del directiva de grupo de MaxDownloadTime.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Error http de BG E \_ \_ \_ 400 (0x80190190)
</dt> <dd>

El servidor no pudo procesar la solicitud de transferencia porque la sintaxis del nombre de archivo remoto no es válida.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Error http de BG E \_ \_ \_ 401 (0x80190191)
</dt> <dd>

El usuario no tiene permiso para obtener acceso al archivo remoto. El recurso solicitado requiere autenticación de usuarios.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Error http de BG E \_ \_ \_ 404 (0x80190194)
</dt> <dd>

La dirección URL solicitada no existe en el servidor.

En IIS 7, este error puede indicar

-   Las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.
-   Que el tamaño de carga supere el límite máximo de carga (para obtener más información, consulte la propiedad extensión IIS de [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).

</dd> <dt>

<span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Error http de BG E \_ \_ \_ 407 (0x80190197)
</dt> <dd>

El usuario no tiene permiso para obtener acceso al proxy. El proxy requiere autenticación de usuario.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Error http de BG E \_ \_ \_ 414 (0x8019019E)
</dt> <dd>

El servidor no puede procesar la solicitud de transferencia. El identificador uniforme de recursos (URI) en el nombre de archivo remoto es más largo que el que el servidor puede interpretar.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Error http de BG E \_ \_ \_ 501 (0x801901F5)
</dt> <dd>

El servidor no admite la funcionalidad necesaria para completar la solicitud. En IIS 6, este error indica que las cargas de BITS no están habilitadas en el directorio virtual (vdir) del servidor.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Error http de BG E \_ \_ \_ 503 (0x801901F7)
</dt> <dd>

El servicio está sobrecargado temporalmente y no puede procesar la solicitud. Reanude el trabajo más tarde.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Error http de BG E \_ \_ \_ 504 (0x801901F8)
</dt> <dd>

Se agotó el tiempo de espera de la solicitud de transferencia mientras se esperaba una puerta de enlace. Reanude el trabajo más tarde.

</dd> <dt>

<span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Error http de BG E \_ \_ \_ 505 (0x801901F9)
</dt> <dd>

El servidor no admite la versión del protocolo HTTP especificada en el nombre de archivo remoto.

</dd> </dl>

El archivo de encabezado Bitsmsg. h contiene valores devueltos HTTP adicionales que no se enumeran antes que BITS usa internamente. Para obtener información sobre estos y otros valores devueltos de HTTP que puede recibir, consulte la especificación RFC 2616 de Internet Engineering Task Force en [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .

 

 