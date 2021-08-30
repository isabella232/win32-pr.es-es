---
description: Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración Hresult
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 246FA53F-FF5B-44E1-BABB-F45AE0212687
api_name:
- Hresult
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ac0d209a4f3890d7a0a2a0aad7232f9d19abf4e2
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622501"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Enumeración Hresult

Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**OK de LA S de NO \_ \_ ESTÁ BIEN**  
HRESULT común que indica que la operación se ha hecho correctamente según lo previsto.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**FALSE DE NO ESTÁ \_ \_ EN LA FACTURACIÓN**  
HRESULT común que indica que la operación se ha hecho correctamente, pero de una manera diferente a la esperada.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**NO \_ SE ENCONTRÓ EL ARCHIVO DE ERROR DE NO SE \_ \_ \_ ENCUENTRA.**  
HRESULT personalizado que devuelve ERROR \_ FILE \_ NOT \_ FOUND.

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**ERROR DE ERROR DE ERROR \_ DE ERROR EN EL \_ \_ ENTORNO**  
HRESULT personalizado que devuelve ERROR \_ BAD \_ ENVIRONMENT.

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**FORMATO NO CORRECTO DE ERROR DE ERROR \_ \_ DE ERROR \_**  
HRESULT personalizado que devuelve ERROR \_ BAD \_ FORMAT.

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**INFRACCIÓN \_ DE USO COMPARTIDO DE \_ ERRORES DE PIXEL \_**  
HRESULT personalizado que devuelve ERROR \_ SHARING \_ VIOLATION.

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**DISCO DE ERROR DE ERROR DE ERROR \_ \_ \_ COMPLETO**  
HRESULT personalizado que devuelve ERROR \_ DISK \_ FULL.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**ERROR DE ERROR DE ERROR DE ERROR \_ \_ MÁS \_ DATOS**  
HRESULT personalizado que devuelve ERROR \_ MORE \_ DATA.

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**FALTA LA \_ DIRECTIVA DE KITS DE \_ \_ \_ DEPURACIÓN DE \_ PIXEL E**  
HRESULT personalizado que indica que falta la directiva de kits de depuración.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**VERSIÓN NO VÁLIDA DE PIXEL \_ E \_ \_**  
HRESULT personalizado que indica que se está utilizando una versión no válida.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIXEL \_ E \_ USING \_ DCOMP**  
HRESULT personalizado que indica que DirectComposition está en uso (no se admite la captura de DirectComposition).

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIXEL \_ E \_ CON \_ DIRECTWRITE**  
HRESULT personalizado que indica que DirectWrite está en uso (no se admite DirectWrite captura de datos).

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIXEL \_ E \_ CON \_ D3D9**  
HRESULT personalizado que indica que Direct3D9 está en uso (la captura de Direct3D9 no se admite en Windows 10).

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E \_ CANT \_ CREATE \_ SHADER**  
HRESULT personalizado que indica que no se puede crear un sombreador especificado.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIXEL \_ E \_ CON \_ D2D**  
HRESULT personalizado que indica que Direct2D está en uso (no se admite la captura de Direct2D).

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**NO HAY \_ \_ \_ FOTOGRAMAS DE PIXEL E**  
HRESULT personalizado que indica que no se han capturado fotogramas.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**DISABLE SPY DE LA \_ \_ E DE \_ SPY**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIXEL \_ E \_ WIN8LOG \_ EN \_ WIN7**  
HRESULT personalizado que indica que un Windows 8 vsglog no se puede reproducir en Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**SEGUIMIENTO DEL \_ \_ SOMBREADOR \_ DE COMPILACIÓN DE \_ PIXEL E**  
HRESULT personalizado que indica que se produjo un error al compilar el seguimiento del sombreador.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**VISUALIZACIÓN DE DATOS DE PIXEL \_ E \_ NO \_ CS \_ \_**  
HRESULT personalizado que indica que no hay ninguna visualización de datos del sombreador de proceso.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**SDK DE E \_ \_ MISMATCH de PIXEL \_**  
HRESULT personalizado que indica que hay un error de coincidencia con el SDK actual.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**SDK DE ERROR \_ \_ DE COINCIDENCIA POSIBLE \_ DE \_ VLAN E**  
HRESULT personalizado que indica que hay un posible error de coincidencia con el SDK actual.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**PIXEL INDETECTABLE DE PIXEL E DE PIXEL DE NO \_ \_ \_ DETECTABLE DE PIXEL**  
HRESULT personalizado que indica que hay un píxel indetectable.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX \_ E \_ CANT \_ DEBUG \_ SHADER \_ USING \_ SYSTEM \_ VALUE \_ SEMANTICS**  
HRESULT personalizado que indica que el sahder no se puede depurar mediante la semántica de valores del sistema.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**UPDATEAVAILABLE de PIXEL \_ S \_**  
HRESULT personalizado que indica que hay una actualización disponible.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**ESTADO DE DX \_ DXGI \_ SIN \_ \_ REDIRECCIONAMIENTO**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ NO \_ REDIRECTION.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**ESTADO DE DX \_ DXGI \_ SIN ACCESO DE \_ \_ \_ ESCRITORIO**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ NO DESKTOP \_ \_ ACCESS.

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**FUENTE \_ \_ VIDPN DE GRÁFICOS DE ESTADO \_ \_ DXGI \_ DE \_ \_ DXGI EN USO**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ GRAPHICS \_ VIDPN \_ SOURCE IN \_ \_ USE.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**CAMBIO \_ DEL MODO DE ESTADO \_ DXGI \_ \_ DE DXGI**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ MODE \_ CHANGED.

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**CAMBIO \_ DEL MODO DE ESTADO DXGI DE DXGI \_ \_ EN \_ \_ \_ CURSO**  
HRESULT personalizado que devuelve EL CAMBIO DE MODO DE ESTADO DE DXGI \_ \_ EN \_ \_ \_ CURSO.

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**ESTADO \_ DE DX DXGI NO \_ \_ FINALIZADO**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ UNOCCLUDED.

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**EL \_ DDA DE ESTADO DE DXGI DE DXGI \_ SIGUE \_ \_ \_ \_ DIBUJANDO**  
HRESULT personalizado que devuelve DXGI \_ STATUS \_ DDA \_ WAS STILL \_ \_ DRAWING.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**NOIMPL \_ DE \_ E DE PARATE DE NILO**  
HRESULT personalizado que devuelve E \_ NOTIMPL.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**INTERFACE \_ E \_ NOINTERFACE**  
HRESULT personalizado que devuelve E \_ NOINTERFACE.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**PUNTERO E \_ \_ DE ASÍNS**  
HRESULT personalizado que devuelve E \_ POINTER.

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**ABORT \_ E \_ DEULE DE PIXEL**  
HRESULT personalizado que devuelve E \_ ABORT.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**ERROR DE E DE PIXEL \_ \_**  
HRESULT personalizado que devuelve E \_ FAIL.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**NO SE \_ HA PRODUCIDO LA EXCEPCIÓN DE FIREWALL E \_**  
HRESULT personalizado que devuelve E \_ UNEXPECTED.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**\_ \_ ACCESSDENIED DE ASÍNS E**  
HRESULT personalizado que devuelve E \_ ACCESSDENIED.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**HANDLE \_ E de PIXEL \_**  
HRESULT personalizado que devuelve E \_ HANDLE.

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**\_OUTOFMEMORY DE PIXEL E \_**  
HRESULT personalizado que devuelve E \_ OUTOFMEMORY.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIXEL \_ E \_ INVALIDARG**  
HRESULT personalizado que devuelve E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**DISCO \_ DE ERROR DE XBOX DE XBOX \_ \_ \_ LLENO**  
HRESULT personalizado que indica que el disco está lleno.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**DIRECCIÓN WS E DE WU \_ \_ EN \_ \_ \_ USO**  
HRESULT personalizado que indica que la dirección ya está en uso.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**DIRECTIVA DE KITS QUE FALTAN EN EL \_ \_ WS E \_ \_ DE \_ WU**  
HRESULT personalizado que indica que la dirección no está disponible.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**NO \_ SE PUDO CARGAR EL MÓDULO DE SOFTWARE DE PIXEL \_**  
HRESULT personalizado que indica que no se pudo cargar un módulo de software necesario.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIXEL \_ TE \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**  
HRESULT personalizado que indica que el módulo de software usado no era el controlador WARP o REF.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIXEL \_ TE \_ CORRUPTEDFILE**  
HRESULT personalizado que indica que el archivo está dañado.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**FAILEDTOOPENFILE DE PIXEL \_ TE \_**  
HRESULT personalizado que indica que no se pudo abrir el archivo.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**FAX \_ TE \_ CALLFAILENILPLAYBACK**  
HRESULT personalizado que indica que se ha dado error en una llamada durante la reproducción.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIXEL \_ TE \_ UNKNOWNUUID**  
HRESULT personalizado que indica que se encontró un UUID desconocido; esto nunca debería ocurrir.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIXEL \_ TE \_ NOTCAPTUREFILEORCORRUPTED**  
HRESULT personalizado que indica que el archivo no es un archivo de captura o está dañado.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**ARCHIVO MÁS RECIENTE DE PIXEL \_ TE \_**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIXEL \_ TE \_ OLDERFILE**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**INVALIDMOMENT DE PIXEL \_ TE \_**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**CONTROLADOR BAD DE HAD \_ TE \_ \_**  
HRESULT personalizado que indica que el controlador es malo.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**ERROR DE NO \_ SE PUEDE ACCEDER A \_ \_ \_ DEPTHSTENCIL \_ EN LA \_ CPU**  
HRESULT personalizado que indica que la CPU intentó acceder al búfer de galería de símbolos de profundidad, lo que produjo un error.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**ERROR DE ERROR DE NO \_ SE PUEDE RESOLVER LA TEXTURA \_ \_ \_ MULTIMUESTREO \_**  
HRESULT personalizado que indica que se ha intentado resolver una textura con varias muestras, lo que da lugar a un error.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**ERROR \_ DE DXGI \_ LLAMADA NO \_ \_ VÁLIDA**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ INVALID \_ CALL.

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**ERROR \_ DE DX DXGI NO \_ \_ \_ ENCONTRADO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ NOT \_ FOUND.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**ERROR \_ DE DXGI DE DXGI \_ MÁS \_ \_ DATOS**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ MORE \_ DATA.

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**\_ERROR DE DXGI NO \_ \_ COMPATIBLE**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ UNSUPPORTED.

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**DISPOSITIVO \_ DE ERROR DXGI DE DXGI \_ \_ \_ ELIMINADO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ DEVICE \_ REMOVED.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**DISPOSITIVO \_ DE ERROR DXGI DE DXGI \_ CON \_ \_ ERRORES**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ DEVICE \_ HUNG.

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**ERROR DE DX \_ DXGI \_ \_ RESTABLECIMIENTO DEL \_ DISPOSITIVO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ DEVICE \_ RESET.

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**ERROR \_ DE DX DXGI TODAVÍA \_ \_ \_ \_ DIBUJABA**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ WAS STILL \_ \_ DRAWING.

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**ESTADÍSTICAS \_ DE FOTOGRAMAS DE ERROR DXGI DE DXGI \_ \_ \_ \_ DISJOINT**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ FRAME \_ STATISTICS \_ DISJOINT.

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**FUENTE \_ VIDPN DE GRÁFICOS DE ERROR DE DXGI DE \_ \_ \_ DXGI \_ EN \_ \_ USO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ GRAPHICS \_ VIDPN \_ SOURCE IN \_ \_ USE.

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**ERROR INTERNO DEL CONTROLADOR DXGI DE \_ \_ \_ \_ \_ DXGI**  
HRESULT personalizado que devuelve EL ERROR INTERNO DEL CONTROLADOR \_ DE \_ ERROR \_ \_ DXGI.

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**ERROR \_ DE DX DXGI \_ \_ NONEXCLUSIVE**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ NONEXCLUSIVE.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**ERROR \_ DE DX DXGI NO DISPONIBLE \_ \_ \_ \_ ACTUALMENTE**  
HRESULT personalizado que devuelve EL ERROR DXGI \_ \_ NO ESTÁ DISPONIBLE \_ \_ ACTUALMENTE.

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**ERROR \_ DE DXGI \_ CLIENTE REMOTO \_ \_ \_ DESCONECTADO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ REMOTE CLIENT \_ \_ DISCONNECTED.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**ERROR \_ DE DXGI \_ REMOTE \_ \_ OUTOFMEMORY**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ REMOTE \_ OUTOFMEMORY.

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**CAMBIO \_ DEL MODO DE ERROR DE DXGI DE DXGI EN \_ \_ \_ \_ \_ CURSO**  
HRESULT personalizado que devuelve EL CAMBIO DE MODO DE ERROR DE DXGI \_ \_ EN \_ \_ \_ CURSO.

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**PÉRDIDA \_ DE ACCESO DE ERROR DE DXGI \_ \_ \_ DE DXGI**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ ACCESS \_ LOST.

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**TIEMPO \_ DE ESPERA DE ERROR DE DXGI \_ \_ \_ DE DXGI**  
HRESULT personalizado que devuelve EL TIEMPO DE ESPERA DE \_ ERROR DE DXGI. \_ \_

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**SESIÓN \_ DE ERROR DE DXGI DE DXGI \_ \_ \_ DESCONECTADA**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ SESSION \_ DISCONNECTED.

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**ERROR \_ DE DXGI \_ RESTRICT TO OUTPUT \_ \_ \_ \_ STALE**  
HRESULT personalizado que devuelve EL ERROR DXGI \_ \_ RESTRICT TO OUTPUT \_ \_ \_ STALE.

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**ERROR DE DX \_ DXGI \_ NO PUEDE PROTEGER EL \_ \_ \_ CONTENIDO**  
HRESULT personalizado que devuelve EL ERROR DXGI \_ NO PUEDE PROTEGER EL \_ \_ \_ CONTENIDO.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**ACCESO \_ DE ERROR DE DXGI DE DXGI \_ \_ \_ DENEGADO**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ ACCESS \_ DENIED.

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**EL \_ NOMBRE DEL ERROR DE DXGI DE DXGI YA \_ \_ \_ \_ EXISTE**  
HRESULT personalizado que devuelve EL NOMBRE DE \_ ERROR \_ DXGI \_ YA \_ EXISTE.

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**FALTA \_ EL COMPONENTE DEL SDK DE ERROR DE DXGI \_ \_ \_ \_ DE DXGI**  
HRESULT personalizado que devuelve DXGI \_ ERROR \_ SDK COMPONENT \_ \_ MISSING.

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**DX \_ DXGI \_ DDI \_ ERR \_ WASSTFUNDING**  
HRESULT personalizado que devuelve DXGI \_ DDI \_ ERR \_ WASST ICMPDRAWING.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**ERROR \_ DE DX DXGI \_ DDI NO \_ \_ COMPATIBLE**  
HRESULT personalizado que devuelve DXGI \_ DDI \_ ERR \_ UNSUPPORTED.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**DX \_ DXGI \_ DDI \_ ERR \_ NONEXCLUSIVE**  
HRESULT personalizado que devuelve DXGI \_ DDI \_ ERR \_ NONEXCLUSIVE.

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**ERROR DE HAD \_ D3D10 \_ \_ \_ DEMASIADOS \_ OBJETOS DE ESTADO \_ \_ ÚNICOS**  
HRESULT personalizado que devuelve EL ERROR D3D10 \_ \_ \_ DEMASIADOS \_ OBJETOS DE ESTADO \_ \_ ÚNICOS.

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**ARCHIVO \_ DE ERROR D3D10 DE HAD \_ NO \_ \_ \_ ENCONTRADO**  
HRESULT personalizado que devuelve D3D10 \_ ERROR \_ FILE NOT \_ \_ FOUND.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**ERROR DE HAD \_ D3D11 \_ \_ \_ DEMASIADOS \_ OBJETOS DE ESTADO \_ \_ ÚNICOS**  
HRESULT personalizado que devuelve EL ERROR D3D11 \_ \_ \_ DEMASIADOS \_ OBJETOS DE ESTADO \_ \_ ÚNICOS.

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**ARCHIVO \_ DE ERROR D3D11 DE HAD \_ NO \_ \_ \_ ENCONTRADO**  
HRESULT personalizado que devuelve D3D11 \_ ERROR \_ FILE NOT \_ \_ FOUND.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**ERROR DE HAD \_ D3D11 \_ \_ \_ DEMASIADOS \_ OBJETOS DE VISTA \_ \_ ÚNICOS**  
HRESULT personalizado que devuelve EL ERROR D3D11 \_ \_ DEMASIADOS \_ OBJETOS DE VISTA \_ \_ \_ ÚNICOS.

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**ERROR DE HAD \_ D3D11 \_ MAPA DE CONTEXTO \_ DIFERIDO \_ SIN DESCARTE \_ \_ \_ \_ INICIAL**  
HRESULT personalizado que devuelve el ERROR D3D11 \_ MAPA \_ DE CONTEXTO \_ DIFERIDO SIN DESCARTE \_ \_ \_ \_ INICIAL.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**ERROR DE PIXEL \_ \_ LLAMADA A DRAW \_ \_ OCCLUDED**  
HRESULT personalizado que indica que una llamada a draw se ha ocluido completamente, lo que da lugar a un error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



