---
description: Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.
MS-HAID: vspixengine.Hresult
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración HRESULT
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
ms.openlocfilehash: 3d5419feb0acb5967132fbb804a9bbc11bfa4248
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537329"
---
# <a name="span-idvspixenginehresultspanhresult-enumeration"></a><span id="vspixengine.hresult"></span>Enumeración HRESULT

Valores HRESULT personalizados para la interfaz de captura de diagnóstico de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="PIX_S_OK"></span><span id="pix_s_ok"></span>**PIX \_ S \_ correcto**  
HRESULT común que indica que la operación se realizó correctamente según lo esperado.

<span id="PIX_S_FALSE"></span><span id="pix_s_false"></span>**PIX \_ S \_ false**  
HRESULT común que indica que la operación se realizó correctamente, pero de forma diferente a lo esperado.

<span id="PIX_ERROR_FILE_NOT_FOUND"></span><span id="pix_error_file_not_found"></span>**\_ \_ \_ no \_ se encontró el archivo de error PIX**  
Un valor HRESULT personalizado que \_ \_ no se encontró el archivo de error transmite \_ .

<span id="PIX_ERROR_BAD_ENVIRONMENT"></span><span id="pix_error_bad_environment"></span>**ERROR de PIX en el \_ \_ \_ entorno incorrecto**  
Un valor HRESULT personalizado que transmite un ERROR de \_ \_ entorno incorrecto.

<span id="PIX_ERROR_BAD_FORMAT"></span><span id="pix_error_bad_format"></span>**\_error de \_ PIX \_ formato incorrecto**  
Un valor HRESULT personalizado que transmite el formato de ERROR no es \_ correcto \_ .

<span id="PIX_ERROR_SHARING_VIOLATION"></span><span id="pix_error_sharing_violation"></span>**infracción de \_ \_ uso compartido de errores de PIX \_**  
Un valor HRESULT personalizado que transmite \_ infracción de uso compartido de errores \_ .

<span id="PIX_ERROR_DISK_FULL"></span><span id="pix_error_disk_full"></span>**ERROR de PIX en el \_ \_ disco \_ lleno**  
Un valor HRESULT personalizado que transmite el disco de ERROR \_ \_ completo.

<span id="PIX_ERROR_MORE_DATA"></span><span id="pix_error_more_data"></span>**ERROR de PIX \_ : \_ más \_ datos**  
Un valor HRESULT personalizado que transmite errores \_ más \_ datos.

<span id="PIX_E_MISSING_DEBUG_KITS_POLICY"></span><span id="pix_e_missing_debug_kits_policy"></span>**\_no se \_ encuentra \_ la \_ Directiva del kit de depuración \_**  
Un valor HRESULT personalizado que indica que falta la Directiva del kit de depuración.

<span id="PIX_E_INVALID_VERSION"></span><span id="pix_e_invalid_version"></span>**PIX \_ E \_ versión no válida \_**  
Un valor HRESULT personalizado que indica que se está usando una versión no válida.

<span id="PIX_E_USING_DCOMP"></span><span id="pix_e_using_dcomp"></span>**PIX \_ E \_ mediante \_ DCOMP**  
Un HRESULT personalizado que indica que DirectComposition está en uso (no se admite la captura de DirectComposition).

<span id="PIX_E_USING_DIRECTWRITE"></span><span id="pix_e_using_directwrite"></span>**PIX \_ E \_ con \_ DIRECTWRITE**  
Un valor HRESULT personalizado que indica que se está usando DirectWrite (no se admite la captura de DirectWrite).

<span id="PIX_E_USING_D3D9"></span><span id="pix_e_using_d3d9"></span>**PIX \_ E \_ mediante \_ D3D9**  
Un HRESULT personalizado que indica que Direct3D9 está en uso (la captura de Direct3D9 no se admite en Windows 10).

<span id="PIX_E_CANT_CREATE_SHADER"></span><span id="pix_e_cant_create_shader"></span>**PIX \_ E no se \_ \_ crean \_ sombreador**  
Un valor HRESULT personalizado que indica que no se puede crear un sombreador especificado.

<span id="PIX_E_USING_D2D"></span><span id="pix_e_using_d2d"></span>**PIX \_ E \_ mediante \_ D2D**  
Un HRESULT personalizado que indica que Direct2D está en uso (no se admite la captura de Direct2D).

<span id="PIX_E_NO_FRAMES"></span><span id="pix_e_no_frames"></span>**fotogramas de foto \_ E \_ no \_**  
Un valor HRESULT personalizado que indica que no se ha capturado ningún fotograma.

<span id="PIX_E_DISABLE_SPY"></span><span id="pix_e_disable_spy"></span>**PIX \_ E \_ deshabilitar \_ Spy**  

<span id="PIX_E_WIN8LOG_ON_WIN7"></span><span id="pix_e_win8log_on_win7"></span>**PIX \_ E \_ WIN8LOG \_ en \_ win7**  
Un HRESULT personalizado que indica que no se puede reproducir un vsglog de Windows 8 en Windows 7.

<span id="PIX_E_BUILD_SHADER_TRACE"></span><span id="pix_e_build_shader_trace"></span>**\_seguimiento del \_ \_ sombreador de \_ compilación de PIX**  
Un valor HRESULT personalizado que indica que se produjo un error al generar el seguimiento del sombreador.

<span id="PIX_E_NO_CS_DATA_VISUALIZATION"></span><span id="pix_e_no_cs_data_visualization"></span>**visualización de datos de PIX \_ E \_ no \_ CS \_ \_**  
Un HRESULT personalizado que indica que no hay ninguna visualización de datos del sombreador de cálculo.

<span id="PIX_E_MISMATCH_SDK"></span><span id="pix_e_mismatch_sdk"></span>**\_SDK de \_ no coincidencia \_ de PIX E**  
Un valor HRESULT personalizado que indica que hay una falta de coincidencia con el SDK actual.

<span id="PIX_E_POSSIBLE_MISMATCH_SDK"></span><span id="pix_e_possible_mismatch_sdk"></span>**\_SDK de \_ \_ coincidencia posible \_ de PIX E**  
Un valor HRESULT personalizado que indica que hay una posible falta de coincidencia con el SDK actual.

<span id="PIX_E_UNDETECTABLE_PIXEL"></span><span id="pix_e_undetectable_pixel"></span>**\_ \_ píxel indetectable de \_ PIX**  
Un valor HRESULT personalizado que indica que hay un píxel no detectable.

<span id="PIX_E_CANT_DEBUG_SHADER_USING_SYSTEM_VALUE_SEMANTICS"></span><span id="pix_e_cant_debug_shader_using_system_value_semantics"></span>**PIX E no se pudo \_ \_ \_ depurar \_ sombreador \_ mediante la semántica de \_ valores del sistema \_ \_**  
Un HRESULT personalizado que indica que sahder no se puede depurar utilizando la semántica del valor del sistema.

<span id="PIX_S_UPDATEAVAILABLE"></span><span id="pix_s_updateavailable"></span>**PIX \_ S \_ UPDATEAVAILABLE**  
Un valor HRESULT personalizado que indica que hay una actualización disponible.

<span id="PIX_DXGI_STATUS_NO_REDIRECTION"></span><span id="pix_dxgi_status_no_redirection"></span>**Estado de DXGI de PIX \_ \_ \_ sin \_ redireccionamiento**  
Un valor HRESULT personalizado que transmite el estado de DXGI \_ \_ no \_ redirección.

<span id="PIX_DXGI_STATUS_NO_DESKTOP_ACCESS"></span><span id="pix_dxgi_status_no_desktop_access"></span>**Estado de foto de PIX \_ \_ \_ no \_ \_ acceso al escritorio**  
Un valor HRESULT personalizado que transmite el estado de DXGI \_ \_ sin \_ \_ acceso al escritorio.

<span id="PIX_DXGI_STATUS_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_status_graphics_vidpn_source_in_use"></span>**\_ \_ \_ \_ \_ código fuente VIDPN \_ de gráficos de estado de \_ la foto**  
Un valor HRESULT personalizado que transmite \_ el \_ \_ \_ origen de VIDPN \_ de gráficos de estado de DXGI en \_ uso.

<span id="PIX_DXGI_STATUS_MODE_CHANGED"></span><span id="pix_dxgi_status_mode_changed"></span>**modo de estado de \_ DXGI \_ \_ \_ cambiado**  
Un valor HRESULT personalizado que cambió el modo de estado de transmite DXGI \_ \_ \_ .

<span id="PIX_DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_status_mode_change_in_progress"></span>**\_ \_ \_ cambio en el modo \_ de estado de DXGI de PIX \_ en \_ curso**  
Un valor HRESULT personalizado que \_ cambia el \_ modo \_ de estado de transmite DXGI \_ \_ .

<span id="PIX_DXGI_STATUS_UNOCCLUDED"></span><span id="pix_dxgi_status_unoccluded"></span>**\_UNOCCLUDED de \_ Estado de la foto de PIX \_**  
Un valor HRESULT personalizado que transmite \_ UNOCCLUDED de estado de DXGI \_ .

<span id="PIX_DXGI_STATUS_DDA_WAS_STILL_DRAWING"></span><span id="pix_dxgi_status_dda_was_still_drawing"></span>**error de la DDA de estado de la \_ \_ imagen de \_ \_ \_ \_ dibujo**  
Un valor HRESULT personalizado que transmite de estado de DXGI \_ \_ \_ \_ todavía estaba \_ dibujando.

<span id="PIX_E_NOTIMPL"></span><span id="pix_e_notimpl"></span>**PIX \_ E \_ NOTIMPL**  
Un valor HRESULT personalizado que transmite E \_ NOTIMPL.

<span id="PIX_E_NOINTERFACE"></span><span id="pix_e_nointerface"></span>**PIX \_ E \_ nointerface**  
Un valor HRESULT personalizado que transmite E \_ nointerface.

<span id="PIX_E_POINTER"></span><span id="pix_e_pointer"></span>**\_cursor PIX E \_**  
Un valor HRESULT personalizado que transmite \_ puntero E.

<span id="PIX_E_ABORT"></span><span id="pix_e_abort"></span>**PIX \_ E \_ Abort**  
Un valor HRESULT personalizado que transmite E \_ anula.

<span id="PIX_E_FAIL"></span><span id="pix_e_fail"></span>**PIX \_ E \_ FAIL**  
Un valor HRESULT personalizado que transmite E \_ produce un error.

<span id="PIX_E_UNEXPECTED"></span><span id="pix_e_unexpected"></span>**PIX \_ E \_ inesperado**  
Un valor HRESULT personalizado que transmite E \_ inesperado.

<span id="PIX_E_ACCESSDENIED"></span><span id="pix_e_accessdenied"></span>**PIX \_ E \_ ACCESSDENIED**  
Un valor HRESULT personalizado que transmite E \_ ACCESSDENIED.

<span id="PIX_E_HANDLE"></span><span id="pix_e_handle"></span>**identificador de PIX \_ \_**  
Un valor HRESULT personalizado que transmite \_ identificador E.

<span id="PIX_E_OUTOFMEMORY"></span><span id="pix_e_outofmemory"></span>**PIX \_ E \_ OUTOFMEMORY**  
Un valor HRESULT personalizado que transmite E \_ OUTOFMEMORY.

<span id="PIX_E_INVALIDARG"></span><span id="pix_e_invalidarg"></span>**PIX \_ E \_ INVALIDARG**  
Un valor HRESULT personalizado que transmite E \_ INVALIDARG.

<span id="PIX_XBOX_ERROR_DISK_FULL"></span><span id="pix_xbox_error_disk_full"></span>**disco de error de la \_ Xbox PIX \_ \_ \_ lleno**  
Un valor HRESULT personalizado que indica que el disco está lleno.

<span id="PIX_WS_E_ADDRESS_IN_USE"></span><span id="pix_ws_e_address_in_use"></span>**\_Dirección WS \_ E \_ \_ de PIX en \_ uso**  
Un valor HRESULT personalizado que indica que la dirección ya está en uso.

<span id="PIX_WS_E_MISSING_KITS_POLICY"></span><span id="pix_ws_e_missing_kits_policy"></span>**\_Directiva de \_ \_ kits que faltan de \_ PIX WS E \_**  
Un valor HRESULT personalizado que indica que la dirección no está disponible.

<span id="PIX_TE_FAILEDTOLOADSOFTWAREMODULE"></span><span id="pix_te_failedtoloadsoftwaremodule"></span>**PIX \_ te \_ FAILEDTOLOADSOFTWAREMODULE**  
Un valor HRESULT personalizado que indica que no se pudo cargar un módulo de software necesario.

<span id="PIX_TE_USEDSOFTWAREMODULETHATWASNTWARPORREF"></span><span id="pix_te_usedsoftwaremodulethatwasntwarporref"></span>**PIX \_ te \_ USEDSOFTWAREMODULETHATWASNTWARPORREF**  
Un valor HRESULT personalizado que indica que el módulo de software usado no era el controlador de ALABEo o REF.

<span id="PIX_TE_CORRUPTEDFILE"></span><span id="pix_te_corruptedfile"></span>**PIX \_ te \_ CORRUPTEDFILE**  
Un valor HRESULT personalizado que indica que el archivo está dañado.

<span id="PIX_TE_FAILEDTOOPENFILE"></span><span id="pix_te_failedtoopenfile"></span>**PIX \_ te \_ FAILEDTOOPENFILE**  
Un valor HRESULT personalizado que indica que no se pudo abrir el archivo.

<span id="PIX_TE_CALLFAILEDONPLAYBACK"></span><span id="pix_te_callfailedonplayback"></span>**PIX \_ te \_ CALLFAILEDONPLAYBACK**  
Un HRESULT personalizado que indica que se produjo un error en una llamada durante la reproducción.

<span id="PIX_TE_UNKNOWNUUID"></span><span id="pix_te_unknownuuid"></span>**PIX \_ te \_ UNKNOWNUUID**  
HRESULT personalizado que indica que se encontró un UUID desconocido; nunca se debe producir.

<span id="PIX_TE_NOTCAPTUREFILEORCORRUPTED"></span><span id="pix_te_notcapturefileorcorrupted"></span>**PIX \_ te \_ NOTCAPTUREFILEORCORRUPTED**  
Un valor HRESULT personalizado que indica que el archivo no es un archivo de captura o está dañado.

<span id="PIX_TE_NEWERFILE"></span><span id="pix_te_newerfile"></span>**PIX \_ te \_ NEWERFILE**  

<span id="PIX_TE_OLDERFILE"></span><span id="pix_te_olderfile"></span>**PIX \_ te \_ OLDERFILE**  

<span id="PIX_TE_INVALIDMOMENT"></span><span id="pix_te_invalidmoment"></span>**PIX \_ te \_ INVALIDMOMENT**  

<span id="PIX_TE_BAD_DRIVER"></span><span id="pix_te_bad_driver"></span>**\_ \_ controlador incorrecto de \_ PIX**  
Un valor HRESULT personalizado que indica que el controlador es incorrecto.

<span id="PIX_ERROR_CANT_ACCESS_DEPTHSTENCIL_IN_CPU"></span><span id="pix_error_cant_access_depthstencil_in_cpu"></span>**ERROR de PIX no se \_ \_ \_ puede acceder a \_ DEPTHSTENCIL \_ en la \_ CPU**  
Un HRESULT personalizado que indica que la CPU intentó tener acceso al búfer de la galería de símbolos de profundidad, lo que produce un error.

<span id="PIX_ERROR_CANT_RESOLVE_MULTISAMPLED_TEXTURE"></span><span id="pix_error_cant_resolve_multisampled_texture"></span>**ERROR de PIX no se resuelve la textura de múltiples \_ \_ \_ \_ muestras \_**  
Un valor HRESULT personalizado que indica que se ha intentado resolver una textura con varias muestras, lo que produce un error.

<span id="PIX_DXGI_ERROR_INVALID_CALL"></span><span id="pix_dxgi_error_invalid_call"></span>**\_error de \_ la \_ llamada no válida \_**  
Un valor HRESULT personalizado que transmite \_ DXGI \_ no pudo \_ llamar a.

<span id="PIX_DXGI_ERROR_NOT_FOUND"></span><span id="pix_dxgi_error_not_found"></span>**\_error de \_ fotostat de PIX \_ no \_ encontrado**  
Un valor HRESULT personalizado que \_ \_ no \_ se encontró transmite DXGI.

<span id="PIX_DXGI_ERROR_MORE_DATA"></span><span id="pix_dxgi_error_more_data"></span>**\_ \_ \_ más datos de error de DXGI de PIX \_**  
Un valor HRESULT personalizado que transmite DXGI tiene \_ \_ más \_ datos.

<span id="PIX_DXGI_ERROR_UNSUPPORTED"></span><span id="pix_dxgi_error_unsupported"></span>**ERROR de la DXGI de PIX \_ \_ \_ no compatible**  
Un valor HRESULT personalizado que \_ no es \_ compatible con transmite DXGI.

<span id="PIX_DXGI_ERROR_DEVICE_REMOVED"></span><span id="pix_dxgi_error_device_removed"></span>**se \_ \_ \_ quitó el dispositivo de error de de PIX \_**  
Un valor HRESULT personalizado que el dispositivo de error de transmite DXGI \_ \_ \_ quitó.

<span id="PIX_DXGI_ERROR_DEVICE_HUNG"></span><span id="pix_dxgi_error_device_hung"></span>**\_error de \_ dispositivo de error de DXGI de PIX \_ \_**  
Un valor HRESULT personalizado que el dispositivo de error de transmite DXGI ha dejado de estar \_ \_ \_ bloqueado.

<span id="PIX_DXGI_ERROR_DEVICE_RESET"></span><span id="pix_dxgi_error_device_reset"></span>**\_restablecimiento del \_ dispositivo de error de DXGI de PIX \_ \_**  
Un valor HRESULT personalizado que transmite el dispositivo de error de DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_WAS_STILL_DRAWING"></span><span id="pix_dxgi_error_was_still_drawing"></span>**el \_ error de DXGI de PIX \_ \_ todavía se está \_ \_ dibujando**  
Un valor HRESULT personalizado que el error de transmite DXGI \_ \_ \_ todavía estaba \_ dibujando.

<span id="PIX_DXGI_ERROR_FRAME_STATISTICS_DISJOINT"></span><span id="pix_dxgi_error_frame_statistics_disjoint"></span>**\_estadísticas de \_ \_ fotogramas de error de fotogramas de \_ \_ PIX**  
HRESULT personalizado que transmite las \_ estadísticas de \_ fotogramas de errores de DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_GRAPHICS_VIDPN_SOURCE_IN_USE"></span><span id="pix_dxgi_error_graphics_vidpn_source_in_use"></span>**\_ \_ \_ gráficos de errores de fotográficos \_ VIDPN \_ de PIX \_ en \_ uso**  
Un valor HRESULT personalizado que transmite \_ el \_ \_ \_ origen de VIDPN \_ de gráficos de error de DXGI en \_ uso.

<span id="PIX_DXGI_ERROR_DRIVER_INTERNAL_ERROR"></span><span id="pix_dxgi_error_driver_internal_error"></span>**\_ \_ \_ error interno del controlador de errores \_ de \_ PIX de PIX**  
Un valor HRESULT personalizado que transmite error interno del controlador de errores de DXGI \_ \_ \_ \_ .

<span id="PIX_DXGI_ERROR_NONEXCLUSIVE"></span><span id="pix_dxgi_error_nonexclusive"></span>**ERROR de DXGI de PIX no \_ \_ \_ exclusivo**  
Un valor HRESULT personalizado que transmite DXGI no es \_ \_ exclusivo.

<span id="PIX_DXGI_ERROR_NOT_CURRENTLY_AVAILABLE"></span><span id="pix_dxgi_error_not_currently_available"></span>**ERROR de DXGI de PIX \_ \_ \_ no \_ \_ disponible actualmente**  
Un valor HRESULT personalizado que transmite \_ DXGI \_ no \_ tiene \_ disponible actualmente.

<span id="PIX_DXGI_ERROR_REMOTE_CLIENT_DISCONNECTED"></span><span id="pix_dxgi_error_remote_client_disconnected"></span>**mensaje de error de DXGI de PIX \_ \_ \_ \_ \_ desconectado**  
Un valor HRESULT personalizado que transmite de error de DXGI \_ \_ \_ \_ desconectó el cliente.

<span id="PIX_DXGI_ERROR_REMOTE_OUTOFMEMORY"></span><span id="pix_dxgi_error_remote_outofmemory"></span>**\_error de \_ \_ OUTOFMEMORY remoto \_ de la de PIX**  
Un valor HRESULT personalizado que transmite de error de DXGI \_ \_ \_ OUTOFMEMORY remoto.

<span id="PIX_DXGI_ERROR_MODE_CHANGE_IN_PROGRESS"></span><span id="pix_dxgi_error_mode_change_in_progress"></span>**\_ \_ \_ cambio en el modo \_ de error de DXGI \_ de \_ PIX**  
Un valor HRESULT personalizado que \_ \_ \_ cambia \_ en curso el modo de error de \_ transmite DXGI.

<span id="PIX_DXGI_ERROR_ACCESS_LOST"></span><span id="pix_dxgi_error_access_lost"></span>**\_error de \_ \_ acceso \_ de la DXGI de PIX**  
Un valor HRESULT personalizado que ha perdido el acceso de error de transmite DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_WAIT_TIMEOUT"></span><span id="pix_dxgi_error_wait_timeout"></span>**\_tiempo de \_ espera de error \_ \_ de**  
Un valor HRESULT personalizado que transmite el tiempo de espera de error de DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_SESSION_DISCONNECTED"></span><span id="pix_dxgi_error_session_disconnected"></span>**sesión de errores de DXGI de PIX \_ \_ \_ \_ desconectada**  
Un valor HRESULT personalizado que desconectó la sesión de error de transmite DXGI \_ \_ \_ .

<span id="PIX_DXGI_ERROR_RESTRICT_TO_OUTPUT_STALE"></span><span id="pix_dxgi_error_restrict_to_output_stale"></span>**\_ \_ error de DXGI \_ de PIX restringido \_ a \_ salida \_ obsoleta**  
Un valor HRESULT personalizado que transmite \_ error \_ de DXGI restringido \_ a la \_ salida \_ obsoleta.

<span id="PIX_DXGI_ERROR_CANNOT_PROTECT_CONTENT"></span><span id="pix_dxgi_error_cannot_protect_content"></span>**el \_ error de DXGI de PIX \_ \_ no puede \_ proteger el \_ contenido**  
Un valor HRESULT personalizado que transmite \_ error de DXGI \_ no puede \_ proteger el \_ contenido.

<span id="PIX_DXGI_ERROR_ACCESS_DENIED"></span><span id="pix_dxgi_error_access_denied"></span>**\_error de \_ \_ acceso \_ denegado de DXGI de PIX**  
Un valor HRESULT personalizado que \_ denegó transmite error de acceso de DXGI \_ \_ .

<span id="PIX_DXGI_ERROR_NAME_ALREADY_EXISTS"></span><span id="pix_dxgi_error_name_already_exists"></span>**\_ \_ \_ \_ ya existe un nombre de error de la DXGI de PIX \_**  
Ya existe un HRESULT personalizado que transmite nombre de error de DXGI \_ \_ \_ \_ .

<span id="PIX_DXGI_ERROR_SDK_COMPONENT_MISSING"></span><span id="pix_dxgi_error_sdk_component_missing"></span>**\_falta el \_ componente del SDK de errores \_ \_ de PIX \_**  
Un valor HRESULT personalizado que no transmite el \_ componente SDK de error de DXGI \_ \_ \_ .

<span id="PIX_DXGI_DDI_ERR_WASSTILLDRAWING"></span><span id="pix_dxgi_ddi_err_wasstilldrawing"></span>**\_error de \_ DDI \_ \_ WASSTILLDRAWING de PIX**  
Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err \_ WASSTILLDRAWING.

<span id="PIX_DXGI_DDI_ERR_UNSUPPORTED"></span><span id="pix_dxgi_ddi_err_unsupported"></span>**error de DDI de foto de PIX \_ \_ \_ \_ no compatible**  
Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err no era \_ compatible.

<span id="PIX_DXGI_DDI_ERR_NONEXCLUSIVE"></span><span id="pix_dxgi_ddi_err_nonexclusive"></span>**\_error de \_ DDI \_ de \_ modo de foto de PIX**  
Un valor HRESULT personalizado que transmite DXGI \_ DDI \_ Err no \_ exclusivo.

<span id="PIX_D3D10_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d10_error_too_many_unique_state_objects"></span>**PIX \_ D3D10 \_ error \_ demasiados \_ \_ \_ objetos de estado único \_**  
Un valor HRESULT personalizado que transmite D3D10 \_ error \_ demasiado \_ numerosos objetos de \_ \_ Estado único \_ .

<span id="PIX_D3D10_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d10_error_file_not_found"></span>**\_ \_ \_ \_ No se encontró el archivo \_ de error D3D10 PIX**  
Un valor HRESULT personalizado que \_ \_ \_ no \_ se encontró en el archivo de error de transmite D3D10.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_STATE_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_state_objects"></span>**PIX \_ D3D11 \_ error \_ demasiados \_ \_ \_ objetos de estado único \_**  
Un valor HRESULT personalizado que transmite D3D11 \_ error \_ demasiado \_ numerosos objetos de \_ \_ Estado único \_ .

<span id="PIX_D3D11_ERROR_FILE_NOT_FOUND"></span><span id="pix_d3d11_error_file_not_found"></span>**\_ \_ \_ \_ No se encontró el archivo \_ de error D3D11 PIX**  
Un valor HRESULT personalizado que \_ \_ \_ no \_ se encontró en el archivo de error de transmite D3D11.

<span id="PIX_D3D11_ERROR_TOO_MANY_UNIQUE_VIEW_OBJECTS"></span><span id="pix_d3d11_error_too_many_unique_view_objects"></span>**PIX \_ D3D11 \_ error \_ demasiados \_ \_ \_ objetos de vista únicos \_**  
Un valor HRESULT personalizado que transmite D3D11 \_ error \_ demasiado \_ numerosos objetos de \_ \_ vista únicos \_ .

<span id="PIX_D3D11_ERROR_DEFERRED_CONTEXT_MAP_WITHOUT_INITIAL_DISCARD"></span><span id="pix_d3d11_error_deferred_context_map_without_initial_discard"></span>**ERROR de D3D11 de PIX en la \_ \_ asignación de \_ \_ contexto \_ \_ sin \_ \_ descartar inicial**  
Un valor HRESULT personalizado que transmite D3D11 \_ error \_ diferido de asignación de \_ contexto \_ \_ sin \_ \_ descartar inicial.

<span id="PIX_ERROR_OCCLUDED_DRAW_CALL"></span><span id="pix_error_occluded_draw_call"></span>**ERROR de PIX \_ \_ ocluidos \_ \_ llamada a Draw**  
Un HRESULT personalizado que indica que una llamada a Draw fue completamente ocluidos, lo que produjo un error.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



