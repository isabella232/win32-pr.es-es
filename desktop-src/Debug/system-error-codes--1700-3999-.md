---
description: Describe los códigos de error 1700-3999 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 7e57c087-53e4-443d-9227-21d9eb3cc71f
title: Códigos de error del sistema (1700-3999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 707425f7714c84d92bf5bc001f57c1677183b9edbd9170236d1c629bc0aaf121
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405606"
---
# <a name="system-error-codes-1700-3999"></a>Códigos de error del sistema (1700-3999)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema para los errores 1700 a 3999. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="RPC_S_INVALID_STRING_BINDING"></span><span id="rpc_s_invalid_string_binding"></span>**RPC \_ S \_ INVALID \_ STRING \_ BINDING**
</dt> <dd> <dl> <dt>

1700 (0x6A4)
</dt> <dt>



El enlace de cadena no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_WRONG_KIND_OF_BINDING"></span><span id="rpc_s_wrong_kind_of_binding"></span>**RPC \_ ES UN TIPO INCORRECTO DE \_ \_ \_ \_ ENLACE**
</dt> <dd> <dl> <dt>

1701 (0x6A5)
</dt> <dt>



El identificador de enlace no es el tipo correcto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BINDING"></span><span id="rpc_s_invalid_binding"></span>**ENLACE \_ RPC S NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1702 (0x6A6)
</dt> <dt>



El identificador de enlace no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_SUPPORTED"></span><span id="rpc_s_protseq_not_supported"></span>**RPC \_ S \_ PROTSEQ \_ NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

1703 (0x6A7)
</dt> <dt>



No se admite la secuencia del protocolo RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_RPC_PROTSEQ"></span><span id="rpc_s_invalid_rpc_protseq"></span>**RPC \_ S \_ INVALID \_ RPC \_ PROTSEQ**
</dt> <dd> <dl> <dt>

1704 (0x6A8)
</dt> <dt>



La secuencia del protocolo RPC no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_STRING_UUID"></span><span id="rpc_s_invalid_string_uuid"></span>**UUID \_ DE CADENA NO VÁLIDA \_ \_ \_ DE RPC S**
</dt> <dd> <dl> <dt>

1705 (0x6A9)
</dt> <dt>



El identificador único universal (UUID) de cadena no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ENDPOINT_FORMAT"></span><span id="rpc_s_invalid_endpoint_format"></span>**FORMATO DE \_ PUNTO DE CONEXIÓN NO \_ \_ VÁLIDO DE \_ RPC**
</dt> <dd> <dl> <dt>

1706 (0x6AA)
</dt> <dt>



El formato del punto de conexión no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NET_ADDR"></span><span id="rpc_s_invalid_net_addr"></span>**RPC \_ S \_ INVALID \_ NET \_ ADDR**
</dt> <dd> <dl> <dt>

1707 (0x6AB)
</dt> <dt>



La dirección de red no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENDPOINT_FOUND"></span><span id="rpc_s_no_endpoint_found"></span>**RPC \_ S NO SE ENCONTRÓ NINGÚN PUNTO DE \_ \_ \_ CONEXIÓN**
</dt> <dd> <dl> <dt>

1708 (0x6AC)
</dt> <dt>



No se encontró ningún punto de conexión.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TIMEOUT"></span><span id="rpc_s_invalid_timeout"></span>**TIEMPO DE \_ ESPERA DE RPC S NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1709 (0x6AD)
</dt> <dt>



El valor de tiempo de espera no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OBJECT_NOT_FOUND"></span><span id="rpc_s_object_not_found"></span>**NO SE ENCONTRÓ EL OBJETO RPC \_ \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1710 (0x6AE)
</dt> <dt>



No se encontró el identificador único universal (UUID) del objeto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_REGISTERED"></span><span id="rpc_s_already_registered"></span>**RPC \_ S \_ YA \_ REGISTRADOS**
</dt> <dd> <dl> <dt>

1711 (0x6AF)
</dt> <dt>



El identificador único universal (UUID) del objeto ya se ha registrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_TYPE_ALREADY_REGISTERED"></span><span id="rpc_s_type_already_registered"></span>**TIPO \_ RPC S YA \_ \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

1712 (0x6B0)
</dt> <dt>



El identificador único universal (UUID) de tipo ya se ha registrado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ALREADY_LISTENING"></span><span id="rpc_s_already_listening"></span>**RPC \_ S QUE YA \_ \_ ESCUCHA**
</dt> <dd> <dl> <dt>

1713 (0x6B1)
</dt> <dt>



El servidor RPC ya está escuchando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS_REGISTERED"></span><span id="rpc_s_no_protseqs_registered"></span>**RPC \_ S \_ SIN \_ PROTSEQS \_ REGISTRADOS**
</dt> <dd> <dl> <dt>

1714 (0x6B2)
</dt> <dt>



No se ha registrado ninguna secuencia de protocolo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_LISTENING"></span><span id="rpc_s_not_listening"></span>**RPC \_ S \_ NOT \_ LISTENING**
</dt> <dd> <dl> <dt>

1715 (0x6B3)
</dt> <dt>



El servidor RPC no escucha.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_MGR_TYPE"></span><span id="rpc_s_unknown_mgr_type"></span>**TIPO \_ DE \_ \_ MGR DESCONOCIDO DE \_ RPC**
</dt> <dd> <dl> <dt>

1716 (0x6B4)
</dt> <dt>



El tipo de administrador es desconocido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_IF"></span><span id="rpc_s_unknown_if"></span>**RPC \_ S \_ UNKNOWN \_ IF**
</dt> <dd> <dl> <dt>

1717 (0x6B5)
</dt> <dt>



La interfaz es desconocida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_BINDINGS"></span><span id="rpc_s_no_bindings"></span>**RPC \_ S \_ SIN \_ ENLACES**
</dt> <dd> <dl> <dt>

1718 (0x6B6)
</dt> <dt>



No hay enlaces.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PROTSEQS"></span><span id="rpc_s_no_protseqs"></span>**RPC \_ S \_ NO \_ PROTSEQS**
</dt> <dd> <dl> <dt>

1719 (0x6B7)
</dt> <dt>



No hay secuencias de protocolo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANT_CREATE_ENDPOINT"></span><span id="rpc_s_cant_create_endpoint"></span>**RPC \_ S \_ CANT \_ CREATE \_ ENDPOINT**
</dt> <dd> <dl> <dt>

1720 (0x6B8)
</dt> <dt>



No se puede crear el punto de conexión.


</dt> </dl> </dd> <dt>

<span id="RPC_S_OUT_OF_RESOURCES"></span><span id="rpc_s_out_of_resources"></span>**RPC \_ S FUERA DE \_ \_ \_ RECURSOS**
</dt> <dd> <dl> <dt>

1721 (0x6B9)
</dt> <dt>



No hay suficientes recursos disponibles para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_UNAVAILABLE"></span><span id="rpc_s_server_unavailable"></span>**SERVIDOR \_ RPC S NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

1722 (0x6BA)
</dt> <dt>



El servidor RPC no está disponible.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SERVER_TOO_BUSY"></span><span id="rpc_s_server_too_busy"></span>**SERVIDOR RPC \_ S \_ DEMASIADO \_ \_ OCUPADO**
</dt> <dd> <dl> <dt>

1723 (0x6BB)
</dt> <dt>



El servidor RPC está demasiado ocupado para completar esta operación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NETWORK_OPTIONS"></span><span id="rpc_s_invalid_network_options"></span>**OPCIONES \_ DE RED NO \_ VÁLIDAS \_ DE \_ RPC S**
</dt> <dd> <dl> <dt>

1724 (0x6BC)
</dt> <dt>



Las opciones de red no son válidas.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CALL_ACTIVE"></span><span id="rpc_s_no_call_active"></span>**RPC \_ S \_ NO \_ CALL \_ ACTIVE**
</dt> <dd> <dl> <dt>

1725 (0x6BD)
</dt> <dt>



No hay llamadas a procedimientos remotos activas en este subproceso.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED"></span><span id="rpc_s_call_failed"></span>**ERROR EN LA LLAMADA DE RPC \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1726 (0x6BE)
</dt> <dt>



Error en la llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_FAILED_DNE"></span><span id="rpc_s_call_failed_dne"></span>**ERROR \_ EN LA LLAMADA RPC S A \_ \_ \_ DNE**
</dt> <dd> <dl> <dt>

1727 (0x6BF)
</dt> <dt>



Error en la llamada a procedimiento remoto y no se ejecutó.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTOCOL_ERROR"></span><span id="rpc_s_protocol_error"></span>**ERROR \_ DE PROTOCOLO RPC S \_ \_**
</dt> <dd> <dl> <dt>

1728 (0x6C0)
</dt> <dt>



Se produjo un error de protocolo de llamada a procedimiento remoto (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROXY_ACCESS_DENIED"></span><span id="rpc_s_proxy_access_denied"></span>**ACCESO DE PROXY DE RPC \_ S \_ \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

1729 (0x6C1)
</dt> <dt>



Se deniega el acceso al proxy HTTP.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TRANS_SYN"></span><span id="rpc_s_unsupported_trans_syn"></span>**RPC \_ S \_ UNSUPPORTED \_ TRANS \_ SYN**
</dt> <dd> <dl> <dt>

1730 (0x6C2)
</dt> <dt>



El servidor RPC no admite la sintaxis de transferencia.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_TYPE"></span><span id="rpc_s_unsupported_type"></span>**RPC \_ S \_ UNSUPPORTED \_ TYPE**
</dt> <dd> <dl> <dt>

1732 (0x6C4)
</dt> <dt>



No se admite el tipo de identificador único universal (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_TAG"></span><span id="rpc_s_invalid_tag"></span>**RPC \_ S \_ INVALID \_ TAG**
</dt> <dd> <dl> <dt>

1733 (0x6C5)
</dt> <dt>



La etiqueta no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_BOUND"></span><span id="rpc_s_invalid_bound"></span>**RPC \_ S ENLAZADO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1734 (0x6C6)
</dt> <dt>



Los límites de la matriz no son válidos.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_ENTRY_NAME"></span><span id="rpc_s_no_entry_name"></span>**RPC \_ S SIN NOMBRE DE \_ \_ \_ ENTRADA**
</dt> <dd> <dl> <dt>

1735 (0x6C7)
</dt> <dt>



El enlace no contiene un nombre de entrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAME_SYNTAX"></span><span id="rpc_s_invalid_name_syntax"></span>**SINTAXIS \_ DE NOMBRE NO VÁLIDO \_ \_ DE \_ RPC S**
</dt> <dd> <dl> <dt>

1736 (0x6C8)
</dt> <dt>



La sintaxis de nombre no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_NAME_SYNTAX"></span><span id="rpc_s_unsupported_name_syntax"></span>**SINTAXIS \_ DE NOMBRES NO \_ \_ ADMITIDOS DE \_ RPC**
</dt> <dd> <dl> <dt>

1737 (0x6C9)
</dt> <dt>



No se admite la sintaxis de nombre.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_NO_ADDRESS"></span><span id="rpc_s_uuid_no_address"></span>**UUID \_ DE RPC S SIN \_ \_ \_ DIRECCIÓN**
</dt> <dd> <dl> <dt>

1739 (0x6CB)
</dt> <dt>



No hay ninguna dirección de red disponible para construir un identificador único universal (UUID).


</dt> </dl> </dd> <dt>

<span id="RPC_S_DUPLICATE_ENDPOINT"></span><span id="rpc_s_duplicate_endpoint"></span>**PUNTO DE CONEXIÓN DUPLICADO DE RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1740 (0x6CC)
</dt> <dt>



El punto de conexión es un duplicado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_TYPE"></span><span id="rpc_s_unknown_authn_type"></span>**TIPO \_ DE \_ \_ AUTENTICACIÓN DESCONOCIDO DE \_ RPC**
</dt> <dd> <dl> <dt>

1741 (0x6CD)
</dt> <dt>



El tipo de autenticación es desconocido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_MAX_CALLS_TOO_SMALL"></span><span id="rpc_s_max_calls_too_small"></span>**RPC \_ S \_ MAX \_ CALLS \_ TOO \_ SMALL**
</dt> <dd> <dl> <dt>

1742 (0x6CE)
</dt> <dt>



El número máximo de llamadas es demasiado pequeño.


</dt> </dl> </dd> <dt>

<span id="RPC_S_STRING_TOO_LONG"></span><span id="rpc_s_string_too_long"></span>**RPC \_ S \_ STRING \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

1743 (0x6CF)
</dt> <dt>



La cadena es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROTSEQ_NOT_FOUND"></span><span id="rpc_s_protseq_not_found"></span>**RPC \_ S \_ PROTSEQ \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1744 (0x6D0)
</dt> <dt>



No se encontró la secuencia del protocolo RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROCNUM_OUT_OF_RANGE"></span><span id="rpc_s_procnum_out_of_range"></span>**RPC \_ S \_ PROCNUM FUERA DEL \_ \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

1745 (0x6D1)
</dt> <dt>



El número de procedimiento está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_HAS_NO_AUTH"></span><span id="rpc_s_binding_has_no_auth"></span>**EL \_ ENLACE RPC S NO TIENE \_ \_ \_ \_ AUTENTICACIÓN**
</dt> <dd> <dl> <dt>

1746 (0x6D2)
</dt> <dt>



El enlace no contiene ninguna información de autenticación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_SERVICE"></span><span id="rpc_s_unknown_authn_service"></span>**SERVICIO \_ DE \_ \_ AUTENTICACIÓN DESCONOCIDO DE \_ RPC**
</dt> <dd> <dl> <dt>

1747 (0x6D3)
</dt> <dt>



Se desconoce el servicio de autenticación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHN_LEVEL"></span><span id="rpc_s_unknown_authn_level"></span>**NIVEL \_ DE \_ AUTENTICACIÓN DESCONOCIDO \_ DE \_ RPC**
</dt> <dd> <dl> <dt>

1748 (0x6D4)
</dt> <dt>



Se desconoce el nivel de autenticación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_AUTH_IDENTITY"></span><span id="rpc_s_invalid_auth_identity"></span>**IDENTIDAD \_ DE \_ AUTENTICACIÓN NO VÁLIDA \_ DE \_ RPC S**
</dt> <dd> <dl> <dt>

1749 (0x6D5)
</dt> <dt>



El contexto de seguridad no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNKNOWN_AUTHZ_SERVICE"></span><span id="rpc_s_unknown_authz_service"></span>**SERVICIO \_ \_ \_ AUTHZ DESCONOCIDO DE RPC \_**
</dt> <dd> <dl> <dt>

1750 (0x6D6)
</dt> <dt>



Se desconoce el servicio de autorización.


</dt> </dl> </dd> <dt>

<span id="EPT_S_INVALID_ENTRY"></span><span id="ept_s_invalid_entry"></span>**ENTRADA NO VÁLIDA DE EPT \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1751 (0x6D7)
</dt> <dt>



La entrada no es válida.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_PERFORM_OP"></span><span id="ept_s_cant_perform_op"></span>**EPT \_ S \_ CANT \_ PERFORM \_ OP**
</dt> <dd> <dl> <dt>

1752 (0x6D8)
</dt> <dt>



El punto de conexión del servidor no puede realizar la operación.


</dt> </dl> </dd> <dt>

<span id="EPT_S_NOT_REGISTERED"></span><span id="ept_s_not_registered"></span>**EPT \_ S \_ NO \_ REGISTRADO**
</dt> <dd> <dl> <dt>

1753 (0x6D9)
</dt> <dt>



no hay más puntos de conexión disponibles desde el asignador de puntos de conexión.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOTHING_TO_EXPORT"></span><span id="rpc_s_nothing_to_export"></span>**RPC \_ S \_ NOTHING \_ TO \_ EXPORT**
</dt> <dd> <dl> <dt>

1754 (0x6DA)
</dt> <dt>



No se ha exportado ninguna interfaz.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INCOMPLETE_NAME"></span><span id="rpc_s_incomplete_name"></span>**NOMBRE INCOMPLETO DE RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1755 (0x6DB)
</dt> <dt>



El nombre de la entrada está incompleto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_VERS_OPTION"></span><span id="rpc_s_invalid_vers_option"></span>**RPC \_ S \_ INVALID \_ VERS \_ OPTION**
</dt> <dd> <dl> <dt>

1756 (0x6DC)
</dt> <dt>



La opción de versión no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_MEMBERS"></span><span id="rpc_s_no_more_members"></span>**RPC \_ S NO MÁS \_ \_ \_ MIEMBROS**
</dt> <dd> <dl> <dt>

1757 (0x6DD)
</dt> <dt>



No hay más miembros.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_UNEXPORTED"></span><span id="rpc_s_not_all_objs_unexported"></span>**RPC \_ S \_ NOT \_ ALL \_ OBJS \_ UNEXPORTED**
</dt> <dd> <dl> <dt>

1758 (0x6DE)
</dt> <dt>



No hay nada que desaportar.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_FOUND"></span><span id="rpc_s_interface_not_found"></span>**NO \_ SE ENCONTRÓ LA INTERFAZ RPC \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1759 (0x6DF)
</dt> <dt>



No se encontró la interfaz.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_ALREADY_EXISTS"></span><span id="rpc_s_entry_already_exists"></span>**LA \_ ENTRADA RPC S YA \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

1760 (0x6E0)
</dt> <dt>



La entrada ya existe.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_NOT_FOUND"></span><span id="rpc_s_entry_not_found"></span>**NO \_ SE ENCONTRÓ LA ENTRADA RPC \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1761 (0x6E1)
</dt> <dt>



No se encuentra la entrada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NAME_SERVICE_UNAVAILABLE"></span><span id="rpc_s_name_service_unavailable"></span>**SERVICIO DE NOMBRES DE RPC \_ \_ S NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

1762 (0x6E2)
</dt> <dt>



El servicio de nombres no está disponible.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_NAF_ID"></span><span id="rpc_s_invalid_naf_id"></span>**IDENTIFICADOR \_ \_ NAF NO VÁLIDO de RPC \_ \_ S**
</dt> <dd> <dl> <dt>

1763 (0x6E3)
</dt> <dt>



La familia de direcciones de red no es válida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CANNOT_SUPPORT"></span><span id="rpc_s_cannot_support"></span>**RPC \_ S \_ NO ADMITE \_**
</dt> <dd> <dl> <dt>

1764 (0x6E4)
</dt> <dt>



No se admite la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_CONTEXT_AVAILABLE"></span><span id="rpc_s_no_context_available"></span>**RPC \_ S SIN CONTEXTO \_ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

1765 (0x6E5)
</dt> <dt>



No hay ningún contexto de seguridad disponible para permitir la suplantación.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERNAL_ERROR"></span><span id="rpc_s_internal_error"></span>**ERROR INTERNO DE RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1766 (0x6E6)
</dt> <dt>



Error interno en una llamada a procedimiento remoto (RPC).


</dt> </dl> </dd> <dt>

<span id="RPC_S_ZERO_DIVIDE"></span><span id="rpc_s_zero_divide"></span>**RPC \_ S \_ ZERO \_ DIVIDE**
</dt> <dd> <dl> <dt>

1767 (0x6E7)
</dt> <dt>



El servidor RPC intentó una división de enteros por cero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ADDRESS_ERROR"></span><span id="rpc_s_address_error"></span>**ERROR DE DIRECCIÓN DE RPC \_ S \_ \_**
</dt> <dd> <dl> <dt>

1768 (0x6E8)
</dt> <dt>



Error de direccionamiento en el servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_DIV_ZERO"></span><span id="rpc_s_fp_div_zero"></span>**RPC \_ S \_ FP \_ DIV \_ ZERO**
</dt> <dd> <dl> <dt>

1769 (0x6E9)
</dt> <dt>



Una operación de punto flotante en el servidor RPC produjo una división por cero.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_UNDERFLOW"></span><span id="rpc_s_fp_underflow"></span>**FLUJO \_ INFERIOR DE FP \_ \_ de RPC S**
</dt> <dd> <dl> <dt>

1770 (0x6EA)
</dt> <dt>



Se produjo un subdesbordmiento de punto flotante en el servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_FP_OVERFLOW"></span><span id="rpc_s_fp_overflow"></span>**RPC \_ S \_ FP \_ OVERFLOW**
</dt> <dd> <dl> <dt>

1771 (0x6EB)
</dt> <dt>



Se produjo un desbordamiento de punto flotante en el servidor RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NO_MORE_ENTRIES"></span><span id="rpc_x_no_more_entries"></span>**RPC \_ X \_ NO \_ MORE \_ ENTRIES**
</dt> <dd> <dl> <dt>

1772 (0x6EC)
</dt> <dt>



Se ha agotado la lista de servidores RPC disponibles para el enlace de identificadores automáticos.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_OPEN_FAIL"></span><span id="rpc_x_ss_char_trans_open_fail"></span>**ERROR AL ABRIR RPC \_ X \_ SS \_ CHAR \_ TRANS \_ \_**
</dt> <dd> <dl> <dt>

1773 (0x6ED)
</dt> <dt>



No se puede abrir el archivo de tabla de traducción de caracteres.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CHAR_TRANS_SHORT_FILE"></span><span id="rpc_x_ss_char_trans_short_file"></span>**ARCHIVO \_ CORTO RPC X \_ SS CHAR \_ \_ TRANS \_ \_**
</dt> <dd> <dl> <dt>

1774 (0x6EE)
</dt> <dt>



El archivo que contiene la tabla de traducción de caracteres tiene menos de 512 bytes.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_IN_NULL_CONTEXT"></span><span id="rpc_x_ss_in_null_context"></span>**RPC \_ X \_ SS EN CONTEXTO \_ \_ \_ NULL**
</dt> <dd> <dl> <dt>

1775 (0x6EF)
</dt> <dt>



Se pasó un identificador de contexto null desde el cliente al host durante una llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CONTEXT_DAMAGED"></span><span id="rpc_x_ss_context_damaged"></span>**CONTEXTO \_ DE RPC X \_ SS \_ \_ DAÑADO**
</dt> <dd> <dl> <dt>

1777 (0x6F1)
</dt> <dt>



El identificador de contexto cambió durante una llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_HANDLES_MISMATCH"></span><span id="rpc_x_ss_handles_mismatch"></span>**ERROR \_ DE COINCIDENCIA DE \_ \_ IDENTIFICADORES DE RPC X SS \_**
</dt> <dd> <dl> <dt>

1778 (0x6F2)
</dt> <dt>



Los identificadores de enlace pasados a una llamada a procedimiento remoto no coinciden.


</dt> </dl> </dd> <dt>

<span id="RPC_X_SS_CANNOT_GET_CALL_HANDLE"></span><span id="rpc_x_ss_cannot_get_call_handle"></span>**RPC \_ X \_ SS NO PUEDE OBTENER EL \_ IDENTIFICADOR DE \_ \_ \_ LLAMADA**
</dt> <dd> <dl> <dt>

1779 (0x6F3)
</dt> <dt>



El código auxiliar no puede obtener el identificador de llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_X_NULL_REF_POINTER"></span><span id="rpc_x_null_ref_pointer"></span>**PUNTERO RPC \_ X \_ NULL \_ REF \_**
</dt> <dd> <dl> <dt>

1780 (0x6F4)
</dt> <dt>



Se pasó un puntero de referencia null al código auxiliar.


</dt> </dl> </dd> <dt>

<span id="RPC_X_ENUM_VALUE_OUT_OF_RANGE"></span><span id="rpc_x_enum_value_out_of_range"></span>**VALOR DE ENUMERACIÓN RPC \_ X \_ FUERA DEL \_ \_ \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

1781 (0x6F5)
</dt> <dt>



El valor de la enumeración está fuera del intervalo.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BYTE_COUNT_TOO_SMALL"></span><span id="rpc_x_byte_count_too_small"></span>**RECUENTO \_ DE BYTES RPC X DEMASIADO \_ \_ \_ \_ PEQUEÑO**
</dt> <dd> <dl> <dt>

1782 (0x6F6)
</dt> <dt>



El recuento de bytes es demasiado pequeño.


</dt> </dl> </dd> <dt>

<span id="RPC_X_BAD_STUB_DATA"></span><span id="rpc_x_bad_stub_data"></span>**DATOS \_ DE CÓDIGO AUXILIAR NO CIFRADO \_ \_ RPC X \_**
</dt> <dd> <dl> <dt>

1783 (0x6F7)
</dt> <dt>



El código auxiliar recibió datos no recibidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_BUFFER"></span><span id="error_invalid_user_buffer"></span>**ERROR \_ BÚFER DE USUARIO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1784 (0x6F8)
</dt> <dt>



El búfer de usuario proporcionado no es válido para la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_MEDIA"></span><span id="error_unrecognized_media"></span>**MEDIOS \_ NO RECONOCIDOS DE \_ ERROR**
</dt> <dd> <dl> <dt>

1785 (0x6F9)
</dt> <dt>



No se reconocen los medios de disco. Es posible que no tenga formato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_LSA_SECRET"></span><span id="error_no_trust_lsa_secret"></span>**ERROR \_ NO \_ TRUST \_ LSA \_ SECRET**
</dt> <dd> <dl> <dt>

1786 (0x6FA)
</dt> <dt>



La estación de trabajo no tiene un secreto de confianza.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRUST_SAM_ACCOUNT"></span><span id="error_no_trust_sam_account"></span>**ERROR \_ NO \_ TRUST \_ SAM \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1787 (0x6FB)
</dt> <dt>



La base de datos de seguridad del servidor no tiene una cuenta de equipo para esta relación de confianza de estación de trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_DOMAIN_FAILURE"></span><span id="error_trusted_domain_failure"></span>**ERROR DE \_ DOMINIO \_ DE \_ CONFIANZA**
</dt> <dd> <dl> <dt>

1788 (0x6FC)
</dt> <dt>



Error en la relación de confianza entre el dominio principal y el dominio en el que se confía.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUSTED_RELATIONSHIP_FAILURE"></span><span id="error_trusted_relationship_failure"></span>**ERROR ERROR \_ DE \_ RELACIÓN DE \_ CONFIANZA**
</dt> <dd> <dl> <dt>

1789 (0x6FD)
</dt> <dt>



Error en la relación de confianza entre esta estación de trabajo y el dominio principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRUST_FAILURE"></span><span id="error_trust_failure"></span>**ERROR DE \_ CONFIANZA \_**
</dt> <dd> <dl> <dt>

1790 (0x6FE)
</dt> <dt>



Error de inicio de sesión de red.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_IN_PROGRESS"></span><span id="rpc_s_call_in_progress"></span>**LLAMADA \_ RPC S EN \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

1791 (0x6FF)
</dt> <dt>



Ya hay una llamada a procedimiento remoto en curso para este subproceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETLOGON_NOT_STARTED"></span><span id="error_netlogon_not_started"></span>**ERROR \_ NETLOGON \_ NOT \_ STARTED**
</dt> <dd> <dl> <dt>

1792 (0x700)
</dt> <dt>



Se intentó iniciar sesión, pero no se inició el servicio de inicio de sesión de red.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_EXPIRED"></span><span id="error_account_expired"></span>**CUENTA DE ERROR \_ \_ EXPIRADA**
</dt> <dd> <dl> <dt>

1793 (0x701)
</dt> <dt>



La cuenta del usuario ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_REDIRECTOR_HAS_OPEN_HANDLES"></span><span id="error_redirector_has_open_handles"></span>**EL \_ REDIRECTOR DE ERRORES \_ TIENE \_ IDENTIFICADORES \_ ABIERTOS**
</dt> <dd> <dl> <dt>

1794 (0x702)
</dt> <dt>



El redirector está en uso y no se puede descargar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_ALREADY_INSTALLED"></span><span id="error_printer_driver_already_installed"></span>**ERROR \_ CONTROLADOR DE IMPRESORA YA \_ \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

1795 (0x703)
</dt> <dt>



El controlador de impresora especificado ya está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PORT"></span><span id="error_unknown_port"></span>**ERROR \_ PUERTO \_ DESCONOCIDO**
</dt> <dd> <dl> <dt>

1796 (0x704)
</dt> <dt>



Se desconoce el puerto especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTER_DRIVER"></span><span id="error_unknown_printer_driver"></span>**ERROR \_ CONTROLADOR DE IMPRESORA \_ \_ DESCONOCIDO**
</dt> <dd> <dl> <dt>

1797 (0x705)
</dt> <dt>



Se desconoce el controlador de impresora.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINTPROCESSOR"></span><span id="error_unknown_printprocessor"></span>**ERROR \_ UNKNOWN \_ PRINTPROCESSOR**
</dt> <dd> <dl> <dt>

1798 (0x706)
</dt> <dt>



Se desconoce el procesador de impresión.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SEPARATOR_FILE"></span><span id="error_invalid_separator_file"></span>**ERROR \_ ARCHIVO SEPARADOR NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1799 (0x707)
</dt> <dt>



El archivo separador especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRIORITY"></span><span id="error_invalid_priority"></span>**ERROR \_ INVALID \_ PRIORITY**
</dt> <dd> <dl> <dt>

1800 (0x708)
</dt> <dt>



La prioridad especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_NAME"></span><span id="error_invalid_printer_name"></span>**ERROR \_ NOMBRE DE IMPRESORA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1801 (0x709)
</dt> <dt>



El nombre de la impresora no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_ALREADY_EXISTS"></span><span id="error_printer_already_exists"></span>**YA EXISTE \_ \_ LA IMPRESORA DE \_ ERRORES**
</dt> <dd> <dl> <dt>

1802 (0x70A)
</dt> <dt>



La impresora ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_COMMAND"></span><span id="error_invalid_printer_command"></span>**ERROR \_ COMANDO DE IMPRESORA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1803 (0x70B)
</dt> <dt>



El comando de impresora no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DATATYPE"></span><span id="error_invalid_datatype"></span>**ERROR \_ TIPO DE DATOS NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1804 (0x70C)
</dt> <dt>



El tipo de datos especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ENVIRONMENT"></span><span id="error_invalid_environment"></span>**ERROR \_ ENTORNO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1805 (0x70D)
</dt> <dt>



El entorno especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_MORE_BINDINGS"></span><span id="rpc_s_no_more_bindings"></span>**RPC \_ S \_ NO \_ MORE \_ BINDINGS**
</dt> <dd> <dl> <dt>

1806 (0x70E)
</dt> <dt>



No hay más enlaces.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_INTERDOMAIN_TRUST_ACCOUNT"></span><span id="error_nologon_interdomain_trust_account"></span>**ERROR \_ NOLOGON \_ INTERDOMAIN \_ TRUST \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1807 (0x70F)
</dt> <dt>



La cuenta usada es una cuenta de confianza entre dominios. Use la cuenta de usuario global o la cuenta de usuario local para acceder a este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_WORKSTATION_TRUST_ACCOUNT"></span><span id="error_nologon_workstation_trust_account"></span>**ERROR \_ NOLOGON \_ WORKSTATION \_ TRUST \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1808 (0x710)
</dt> <dt>



La cuenta usada es una cuenta de equipo. Use la cuenta de usuario global o la cuenta de usuario local para acceder a este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOLOGON_SERVER_TRUST_ACCOUNT"></span><span id="error_nologon_server_trust_account"></span>**ERROR \_ NOLOGON \_ SERVER \_ TRUST \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1809 (0x711)
</dt> <dt>



La cuenta usada es una cuenta de confianza del servidor. Use la cuenta de usuario global o la cuenta de usuario local para acceder a este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_TRUST_INCONSISTENT"></span><span id="error_domain_trust_inconsistent"></span>**ERROR CONFIANZA \_ DE \_ DOMINIO \_ INCOHERENTE**
</dt> <dd> <dl> <dt>

1810 (0x712)
</dt> <dt>



El nombre o el identificador de seguridad (SID) del dominio especificado es incoherente con la información de confianza de ese dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_HAS_OPEN_HANDLES"></span><span id="error_server_has_open_handles"></span>**EL \_ SERVIDOR DE ERRORES TIENE \_ \_ IDENTIFICADORES \_ ABIERTOS**
</dt> <dd> <dl> <dt>

1811 (0x713)
</dt> <dt>



El servidor está en uso y no se puede descargar.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_DATA_NOT_FOUND"></span><span id="error_resource_data_not_found"></span>**NO SE \_ ENCONTRARON DATOS DE RECURSOS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1812 (0x714)
</dt> <dt>



El archivo de imagen especificado no contenía una sección de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_resource_type_not_found"></span>**TIPO \_ DE RECURSO DE ERROR NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1813 (0x715)
</dt> <dt>



No se encuentra el tipo de recurso especificado en el archivo de imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_NAME_NOT_FOUND"></span><span id="error_resource_name_not_found"></span>**ERROR \_ NOMBRE DE RECURSO NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

1814 (0x716)
</dt> <dt>



No se encuentra el nombre de recurso especificado en el archivo de imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_LANG_NOT_FOUND"></span><span id="error_resource_lang_not_found"></span>**ERROR \_ RESOURCE \_ LANG \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

1815 (0x717)
</dt> <dt>



No se encuentra el identificador de idioma de recurso especificado en el archivo de imagen.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_QUOTA"></span><span id="error_not_enough_quota"></span>**ERROR \_ NO HAY SUFICIENTE \_ \_ CUOTA**
</dt> <dd> <dl> <dt>

1816 (0x718)
</dt> <dt>



Cuota insuficiente para procesar este comando.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_INTERFACES"></span><span id="rpc_s_no_interfaces"></span>**RPC \_ S \_ SIN \_ INTERFACES**
</dt> <dd> <dl> <dt>

1817 (0x719)
</dt> <dt>



No se ha registrado ninguna interfaz.


</dt> </dl> </dd> <dt>

<span id="RPC_S_CALL_CANCELLED"></span><span id="rpc_s_call_cancelled"></span>**LLAMADA \_ RPC S \_ \_ CANCELADA**
</dt> <dd> <dl> <dt>

1818 (0x71A)
</dt> <dt>



Se canceló la llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_BINDING_INCOMPLETE"></span><span id="rpc_s_binding_incomplete"></span>**ENLACE \_ RPC S \_ \_ INCOMPLETO**
</dt> <dd> <dl> <dt>

1819 (0x71B)
</dt> <dt>



El identificador de enlace no contiene toda la información necesaria.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COMM_FAILURE"></span><span id="rpc_s_comm_failure"></span>**ERROR \_ DE \_ COMM DE RPC \_**
</dt> <dd> <dl> <dt>

1820 (0x71C)
</dt> <dt>



Se produjo un error de comunicaciones durante una llamada a procedimiento remoto.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UNSUPPORTED_AUTHN_LEVEL"></span><span id="rpc_s_unsupported_authn_level"></span>**NIVEL \_ DE AUTENTICACIÓN NO \_ \_ ADMITIDO DE \_ RPC**
</dt> <dd> <dl> <dt>

1821 (0x71D)
</dt> <dt>



No se admite el nivel de autenticación solicitado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NO_PRINC_NAME"></span><span id="rpc_s_no_princ_name"></span>**RPC \_ S SIN NOMBRE DE \_ \_ PRINC \_**
</dt> <dd> <dl> <dt>

1822 (0x71E)
</dt> <dt>



No se ha registrado ningún nombre principal.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_RPC_ERROR"></span><span id="rpc_s_not_rpc_error"></span>**RPC \_ S \_ NOT \_ RPC \_ ERROR**
</dt> <dd> <dl> <dt>

1823 (0x71F)
</dt> <dt>



El error especificado no es válido Windows código de error RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_S_UUID_LOCAL_ONLY"></span><span id="rpc_s_uuid_local_only"></span>**RPC \_ S \_ UUID \_ LOCAL \_ ONLY**
</dt> <dd> <dl> <dt>

1824 (0x720)
</dt> <dt>



Se ha asignado un UUID que solo es válido en este equipo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEC_PKG_ERROR"></span><span id="rpc_s_sec_pkg_error"></span>**ERROR DE RPC \_ S \_ SEC \_ PKG \_**
</dt> <dd> <dl> <dt>

1825 (0x721)
</dt> <dt>



Error específico del paquete de seguridad.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_CANCELLED"></span><span id="rpc_s_not_cancelled"></span>**RPC \_ S \_ NO \_ CANCELADOS**
</dt> <dd> <dl> <dt>

1826 (0x722)
</dt> <dt>



El subproceso no se cancela.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_ES_ACTION"></span><span id="rpc_x_invalid_es_action"></span>**RPC \_ X ACCIÓN DE ES NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1827 (0x723)
</dt> <dt>



Operación no válida en el identificador de codificación/decoding.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_ES_VERSION"></span><span id="rpc_x_wrong_es_version"></span>**RPC \_ X VERSIÓN INCORRECTA DE \_ \_ ES \_**
</dt> <dd> <dl> <dt>

1828 (0x724)
</dt> <dt>



Versión incompatible del paquete de serialización.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_STUB_VERSION"></span><span id="rpc_x_wrong_stub_version"></span>**VERSIÓN \_ DE CÓDIGO AUXILIAR RPC X \_ \_ \_ INCORRECTA**
</dt> <dd> <dl> <dt>

1829 (0x725)
</dt> <dt>



Versión incompatible del código auxiliar rpc.


</dt> </dl> </dd> <dt>

<span id="RPC_X_INVALID_PIPE_OBJECT"></span><span id="rpc_x_invalid_pipe_object"></span>**OBJETO DE \_ CANALIZACIÓN RPC X NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1830 (0x726)
</dt> <dt>



El objeto de canalización RPC no es válido o está dañado.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_ORDER"></span><span id="rpc_x_wrong_pipe_order"></span>**RPC \_ X ORDEN DE CANALIZACIÓN \_ \_ \_ INCORRECTO**
</dt> <dd> <dl> <dt>

1831 (0x727)
</dt> <dt>



Se intentó realizar una operación no válida en un objeto de canalización RPC.


</dt> </dl> </dd> <dt>

<span id="RPC_X_WRONG_PIPE_VERSION"></span><span id="rpc_x_wrong_pipe_version"></span>**RPC \_ X VERSIÓN DE CANALIZACIÓN \_ \_ \_ INCORRECTA**
</dt> <dd> <dl> <dt>

1832 (0x728)
</dt> <dt>



Versión de canalización RPC no admitida.


</dt> </dl> </dd> <dt>

<span id="RPC_S_COOKIE_AUTH_FAILED"></span><span id="rpc_s_cookie_auth_failed"></span>**ERROR \_ EN LA \_ AUTENTICACIÓN DE COOKIES \_ DE \_ RPC S**
</dt> <dd> <dl> <dt>

1833 (0x729)
</dt> <dt>



El servidor proxy HTTP rechazó la conexión porque se ha generado un error en la autenticación de cookies.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GROUP_MEMBER_NOT_FOUND"></span><span id="rpc_s_group_member_not_found"></span>**NO SE ENCONTRÓ EL MIEMBRO DEL GRUPO RPC \_ \_ \_ \_ \_ S**
</dt> <dd> <dl> <dt>

1898 (0x76A)
</dt> <dt>



No se encontró el miembro del grupo.


</dt> </dl> </dd> <dt>

<span id="EPT_S_CANT_CREATE"></span><span id="ept_s_cant_create"></span>**EPT \_ S \_ CANT \_ CREATE**
</dt> <dd> <dl> <dt>

1899 (0x76B)
</dt> <dt>



No se pudo crear la entrada de la base de datos del asignador de puntos de conexión.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_OBJECT"></span><span id="rpc_s_invalid_object"></span>**RPC \_ S \_ INVALID \_ OBJECT**
</dt> <dd> <dl> <dt>

1900 (0x76C)
</dt> <dt>



El identificador único universal (UUID) del objeto es el UUID nulo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TIME"></span><span id="error_invalid_time"></span>**ERROR \_ HORA NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

1901 (0x76D)
</dt> <dt>



La hora especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_NAME"></span><span id="error_invalid_form_name"></span>**ERROR \_ NOMBRE DE FORMULARIO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1902 (0x76E)
</dt> <dt>



El nombre del formulario especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FORM_SIZE"></span><span id="error_invalid_form_size"></span>**ERROR \_ TAMAÑO DE FORMULARIO NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1903 (0x76F)
</dt> <dt>



El tamaño de formulario especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WAITING"></span><span id="error_already_waiting"></span>**ERROR \_ YA \_ EN ESPERA**
</dt> <dd> <dl> <dt>

1904 (0x770)
</dt> <dt>



El identificador de impresora especificado ya está esperando.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DELETED"></span><span id="error_printer_deleted"></span>**ERROR \_ IMPRESORA \_ ELIMINADA**
</dt> <dd> <dl> <dt>

1905 (0x771)
</dt> <dt>



Se ha eliminado la impresora especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_STATE"></span><span id="error_invalid_printer_state"></span>**ERROR \_ ESTADO DE IMPRESORA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1906 (0x772)
</dt> <dt>



El estado de la impresora no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_MUST_CHANGE"></span><span id="error_password_must_change"></span>**ERROR \_ LA CONTRASEÑA DEBE \_ \_ CAMBIAR**
</dt> <dd> <dl> <dt>

1907 (0x773)
</dt> <dt>



La contraseña del usuario debe cambiarse antes de iniciar sesión.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_NOT_FOUND"></span><span id="error_domain_controller_not_found"></span>**NO SE \_ ENCONTRÓ EL CONTROLADOR DE DOMINIO DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1908 (0x774)
</dt> <dt>



No se encontró el controlador de dominio para este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCOUNT_LOCKED_OUT"></span><span id="error_account_locked_out"></span>**CUENTA DE ERROR \_ \_ BLOQUEADA \_**
</dt> <dd> <dl> <dt>

1909 (0x775)
</dt> <dt>



La cuenta a la que se hace referencia está bloqueada actualmente y es posible que no haya iniciado sesión en .


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OXID"></span><span id="or_invalid_oxid"></span>**O \_ INVALIDAD \_**
</dt> <dd> <dl> <dt>

1910 (0x776)
</dt> <dt>



No se encontró el exportador de objetos especificado.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_OID"></span><span id="or_invalid_oid"></span>**O \_ \_ OID NO VÁLIDO**
</dt> <dd> <dl> <dt>

1911 (0x777)
</dt> <dt>



No se encontró el objeto especificado.


</dt> </dl> </dd> <dt>

<span id="OR_INVALID_SET"></span><span id="or_invalid_set"></span>**O CONJUNTO \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

1912 (0x778)
</dt> <dt>



No se encontró el conjunto de solucionador de objetos especificado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_SEND_INCOMPLETE"></span><span id="rpc_s_send_incomplete"></span>**RPC \_ S \_ SEND \_ INCOMPLETE**
</dt> <dd> <dl> <dt>

1913 (0x779)
</dt> <dt>



Algunos datos permanecen para enviarse en el búfer de solicitudes.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_HANDLE"></span><span id="rpc_s_invalid_async_handle"></span>**IDENTIFICADOR \_ \_ ASINCRÓNICO NO VÁLIDO \_ DE \_ RPC**
</dt> <dd> <dl> <dt>

1914 (0x77A)
</dt> <dt>



Identificador de llamada a procedimiento remoto asincrónico no válido.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INVALID_ASYNC_CALL"></span><span id="rpc_s_invalid_async_call"></span>**RPC \_ S \_ INVALID \_ ASYNC \_ CALL**
</dt> <dd> <dl> <dt>

1915 (0x77B)
</dt> <dt>



Identificador de llamada RPC asincrónica no válido para esta operación.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_CLOSED"></span><span id="rpc_x_pipe_closed"></span>**RPC \_ X \_ PIPE \_ CLOSED**
</dt> <dd> <dl> <dt>

1916 (0x77C)
</dt> <dt>



El objeto de canalización RPC ya se ha cerrado.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_DISCIPLINE_ERROR"></span><span id="rpc_x_pipe_discipline_error"></span>**ERROR DE \_ LA \_ MATERIA DE \_ CANALIZACIÓN \_ RPC X**
</dt> <dd> <dl> <dt>

1917 (0x77D)
</dt> <dt>



La llamada RPC se completó antes de procesar todas las canalizaciones.


</dt> </dl> </dd> <dt>

<span id="RPC_X_PIPE_EMPTY"></span><span id="rpc_x_pipe_empty"></span>**CANALIZACIÓN \_ RPC X \_ \_ VACÍA**
</dt> <dd> <dl> <dt>

1918 (0x77E)
</dt> <dt>



No hay más datos disponibles en la canalización RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITENAME"></span><span id="error_no_sitename"></span>**ERROR \_ NO \_ SITENAME**
</dt> <dd> <dl> <dt>

1919 (0x77F)
</dt> <dt>



No hay ningún nombre de sitio disponible para esta máquina.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ACCESS_FILE"></span><span id="error_cant_access_file"></span>**ERROR \_ NO SE PUEDE ACCEDER AL \_ \_ ARCHIVO**
</dt> <dd> <dl> <dt>

1920 (0x780)
</dt> <dt>



El sistema no puede acceder al archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RESOLVE_FILENAME"></span><span id="error_cant_resolve_filename"></span>**ERROR \_ NO SE PUEDE RESOLVER EL NOMBRE DE \_ \_ ARCHIVO**
</dt> <dd> <dl> <dt>

1921 (0x781)
</dt> <dt>



El sistema no puede resolver el nombre del archivo.


</dt> </dl> </dd> <dt>

<span id="RPC_S_ENTRY_TYPE_MISMATCH"></span><span id="rpc_s_entry_type_mismatch"></span>**ERROR DE \_ COINCIDENCIA DEL TIPO DE \_ \_ ENTRADA DE \_ RPC S**
</dt> <dd> <dl> <dt>

1922 (0x782)
</dt> <dt>



La entrada no es del tipo esperado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_NOT_ALL_OBJS_EXPORTED"></span><span id="rpc_s_not_all_objs_exported"></span>**RPC \_ S NO TODOS LOS \_ \_ \_ OBJ \_ EXPORTADOS**
</dt> <dd> <dl> <dt>

1923 (0x783)
</dt> <dt>



No todos los UUID de objeto se podrían exportar a la entrada especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_INTERFACE_NOT_EXPORTED"></span><span id="rpc_s_interface_not_exported"></span>**INTERFAZ \_ RPC S NO \_ \_ \_ EXPORTADA**
</dt> <dd> <dl> <dt>

1924 (0x784)
</dt> <dt>



No se pudo exportar la interfaz a la entrada especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PROFILE_NOT_ADDED"></span><span id="rpc_s_profile_not_added"></span>**PERFIL DE RPC \_ \_ S NO \_ \_ AGREGADO**
</dt> <dd> <dl> <dt>

1925 (0x785)
</dt> <dt>



No se pudo agregar la entrada de perfil especificada.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_ADDED"></span><span id="rpc_s_prf_elt_not_added"></span>**RPC \_ S \_ PRF \_ ELT \_ NOT \_ ADDED**
</dt> <dd> <dl> <dt>

1926 (0x786)
</dt> <dt>



No se pudo agregar el elemento de perfil especificado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_PRF_ELT_NOT_REMOVED"></span><span id="rpc_s_prf_elt_not_removed"></span>**RPC \_ S \_ PRF \_ ELT \_ NOT \_ REMOVED**
</dt> <dd> <dl> <dt>

1927 (0x787)
</dt> <dt>



No se pudo quitar el elemento de perfil especificado.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_ADDED"></span><span id="rpc_s_grp_elt_not_added"></span>**RPC \_ S \_ GRP \_ ELT \_ NOT \_ ADDED**
</dt> <dd> <dl> <dt>

1928 (0x788)
</dt> <dt>



No se pudo agregar el elemento group.


</dt> </dl> </dd> <dt>

<span id="RPC_S_GRP_ELT_NOT_REMOVED"></span><span id="rpc_s_grp_elt_not_removed"></span>**RPC \_ S \_ GRP \_ ELT \_ NOT \_ REMOVED**
</dt> <dd> <dl> <dt>

1929 (0x789)
</dt> <dt>



No se pudo quitar el elemento group.


</dt> </dl> </dd> <dt>

<span id="ERROR_KM_DRIVER_BLOCKED"></span><span id="error_km_driver_blocked"></span>**ERROR \_ KM \_ DRIVER \_ BLOCKED**
</dt> <dd> <dl> <dt>

1930 (0x78A)
</dt> <dt>



El controlador de impresora no es compatible con una directiva habilitada en el equipo que bloquea los controladores NT 4.0.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTEXT_EXPIRED"></span><span id="error_context_expired"></span>**CONTEXTO DE ERROR \_ \_ EXPIRADO**
</dt> <dd> <dl> <dt>

1931 (0x78B)
</dt> <dt>



El contexto ha expirado y ya no se puede usar.


</dt> </dl> </dd> <dt>

<span id="ERROR_PER_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_per_user_trust_quota_exceeded"></span>**ERROR POR \_ CUOTA DE CONFIANZA DE USUARIO \_ \_ \_ \_ SUPERADA**
</dt> <dd> <dl> <dt>

1932 (0x78C)
</dt> <dt>



Se ha superado la cuota de creación de confianza delegada del usuario actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALL_USER_TRUST_QUOTA_EXCEEDED"></span><span id="error_all_user_trust_quota_exceeded"></span>**ERROR SE \_ \_ SUPERÓ \_ LA CUOTA DE CONFIANZA DE TODOS LOS \_ \_ USUARIOS**
</dt> <dd> <dl> <dt>

1933 (0x78D)
</dt> <dt>



Se ha superado la cuota total de creación de confianza delegada.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_DELETE_TRUST_QUOTA_EXCEEDED"></span><span id="error_user_delete_trust_quota_exceeded"></span>**ERROR EL \_ USUARIO ELIMINA LA CUOTA DE CONFIANZA \_ \_ \_ \_ SUPERADA**
</dt> <dd> <dl> <dt>

1934 (0x78E)
</dt> <dt>



Se ha superado la cuota de eliminación de confianza delegada del usuario actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUTHENTICATION_FIREWALL_FAILED"></span><span id="error_authentication_firewall_failed"></span>**ERROR DE \_ FIREWALL DE \_ \_ AUTENTICACIÓN**
</dt> <dd> <dl> <dt>

1935 (0x78F)
</dt> <dt>



El equipo en el que inicia sesión está protegido por un firewall de autenticación. La cuenta especificada no puede autenticarse en el equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_PRINT_CONNECTIONS_BLOCKED"></span><span id="error_remote_print_connections_blocked"></span>**ERROR \_ CONEXIONES \_ DE IMPRESIÓN REMOTA \_ \_ BLOQUEADAS**
</dt> <dd> <dl> <dt>

1936 (0x790)
</dt> <dt>



Las conexiones remotas al colador de impresión están bloqueadas por una directiva establecida en el equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NTLM_BLOCKED"></span><span id="error_ntlm_blocked"></span>**ERROR \_ NTLM \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

1937 (0x791)
</dt> <dt>



Error de autenticación porque se ha deshabilitado la autenticación NTLM.


</dt> </dl> </dd> <dt>

<span id="ERROR_PASSWORD_CHANGE_REQUIRED"></span><span id="error_password_change_required"></span>**SE REQUIERE \_ UN CAMBIO DE CONTRASEÑA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

1938 (0x792)
</dt> <dt>



Error de inicio de sesión: la directiva de EAS requiere que el usuario cambie su contraseña antes de que se pueda realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PIXEL_FORMAT"></span><span id="error_invalid_pixel_format"></span>**ERROR \_ FORMATO DE PÍXEL NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2000 (0x7D0)
</dt> <dt>



El formato de píxel no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DRIVER"></span><span id="error_bad_driver"></span>**ERROR: \_ CONTROLADOR \_ NO ESTÁ BIEN**
</dt> <dd> <dl> <dt>

2001 (0x7D1)
</dt> <dt>



El controlador especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_WINDOW_STYLE"></span><span id="error_invalid_window_style"></span>**ERROR \_ ESTILO DE VENTANA NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2002 (0x7D2)
</dt> <dt>



El atributo de clase o estilo de ventana no es válido para esta operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_METAFILE_NOT_SUPPORTED"></span><span id="error_metafile_not_supported"></span>**ERROR \_ \_ METARCHIVO NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

2003 (0x7D3)
</dt> <dt>



No se admite la operación de metarchivo solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSFORM_NOT_SUPPORTED"></span><span id="error_transform_not_supported"></span>**NO SE \_ ADMITE LA TRANSFORMACIÓN DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

2004 (0x7D4)
</dt> <dt>



No se admite la operación de transformación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIPPING_NOT_SUPPORTED"></span><span id="error_clipping_not_supported"></span>**NO SE \_ ADMITE EL RECORTE DE \_ \_ ERRORES**
</dt> <dd> <dl> <dt>

2005 (0x7D5)
</dt> <dt>



No se admite la operación de recorte solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>**ERROR \_ \_ CMM NO VÁLIDO**
</dt> <dd> <dl> <dt>

2010 (0x7DA)
</dt> <dt>



El módulo de administración de colores especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>**ERROR \_ PERFIL NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2011 (0x7DB)
</dt> <dt>



El perfil de color especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>**NO \_ SE ENCONTRÓ LA ETIQUETA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

2012 (0x7DC)
</dt> <dt>



No se encontró la etiqueta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>**ETIQUETA \_ DE ERROR NO \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

2013 (0x7DD)
</dt> <dt>



No hay una etiqueta obligatoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>**ERROR \_ DUPLICATE \_ TAG**
</dt> <dd> <dl> <dt>

2014 (0x7DE)
</dt> <dt>



La etiqueta especificada ya está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>**PERFIL \_ DE ERROR NO ASOCIADO AL \_ \_ \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

2015 (0x7DF)
</dt> <dt>



El perfil de color especificado no está asociado al dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND"></span><span id="error_profile_not_found"></span>**NO SE \_ ENCONTRÓ EL PERFIL DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

2016 (0x7E0)
</dt> <dt>



No se encontró el perfil de color especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>**ERROR \_ ESPACIO DE COLORES NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2017 (0x7E1)
</dt> <dt>



El espacio de colores especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>**ERROR \_ ICM \_ HABILITADO \_**
</dt> <dd> <dl> <dt>

2018 (0x7E2)
</dt> <dt>



Image Color Management no está habilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>**ERROR \_ AL ELIMINAR ICM \_ \_ XFORM**
</dt> <dd> <dl> <dt>

2019 (0x7E3)
</dt> <dt>



Se produjo un error al eliminar la transformación de color.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSFORM"></span><span id="error_invalid_transform"></span>**ERROR \_ INVALID \_ TRANSFORM**
</dt> <dd> <dl> <dt>

2020 (0x7E4)
</dt> <dt>



La transformación de color especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_COLORSPACE_MISMATCH"></span><span id="error_colorspace_mismatch"></span>**ERROR \_ COLORSPACE \_ MISMATCH**
</dt> <dd> <dl> <dt>

2021 (0x7E5)
</dt> <dt>



La transformación especificada no coincide con el espacio de colores del mapa de bits.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COLORINDEX"></span><span id="error_invalid_colorindex"></span>**ERROR \_ \_ COLORINDEX NO VÁLIDO**
</dt> <dd> <dl> <dt>

2022 (0x7E6)
</dt> <dt>



El índice de color con nombre especificado no está presente en el perfil.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILE_DOES_NOT_MATCH_DEVICE"></span><span id="error_profile_does_not_match_device"></span>**EL PERFIL \_ DE ERROR NO COINCIDE CON EL \_ \_ \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

2023 (0x7E7)
</dt> <dt>



El perfil especificado está pensado para un dispositivo de un tipo diferente al dispositivo especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD"></span><span id="error_connected_other_password"></span>**ERROR \_ CONECTADO OTRA \_ \_ CONTRASEÑA**
</dt> <dd> <dl> <dt>

2108 (0x83C)
</dt> <dt>



La conexión de red se realizó correctamente, pero se tuvo que solicitar al usuario una contraseña que no sea la especificada originalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTED_OTHER_PASSWORD_DEFAULT"></span><span id="error_connected_other_password_default"></span>**ERROR \_ CONECTADO OTRA CONTRASEÑA \_ \_ \_ PREDETERMINADA**
</dt> <dd> <dl> <dt>

2109 (0x83D)
</dt> <dt>



La conexión de red se realizó correctamente con las credenciales predeterminadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USERNAME"></span><span id="error_bad_username"></span>**ERROR \_ NOMBRE DE USUARIO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

2202 (0x89A)
</dt> <dt>



El nombre de usuario especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONNECTED"></span><span id="error_not_connected"></span>**ERROR \_ NO \_ CONECTADO**
</dt> <dd> <dl> <dt>

2250 (0x8CA)
</dt> <dt>



Esta conexión de red no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPEN_FILES"></span><span id="error_open_files"></span>**ERROR \_ AL ABRIR \_ ARCHIVOS**
</dt> <dd> <dl> <dt>

2401 (0x961)
</dt> <dt>



Esta conexión de red tiene archivos abiertos o solicitudes pendientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVE_CONNECTIONS"></span><span id="error_active_connections"></span>**ERROR \_ CONEXIONES \_ ACTIVAS**
</dt> <dd> <dl> <dt>

2402 (0x962)
</dt> <dt>



Las conexiones activas siguen existiendo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_IN_USE"></span><span id="error_device_in_use"></span>**ERROR \_ DEL DISPOSITIVO EN \_ \_ USO**
</dt> <dd> <dl> <dt>

2404 (0x964)
</dt> <dt>



El dispositivo está en uso por un proceso activo y no se puede desconectar.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNKNOWN_PRINT_MONITOR"></span><span id="error_unknown_print_monitor"></span>**ERROR \_ MONITOR DE IMPRESIÓN \_ \_ DESCONOCIDO**
</dt> <dd> <dl> <dt>

3000 (0xBB8)
</dt> <dt>



Se desconoce el monitor de impresión especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_IN_USE"></span><span id="error_printer_driver_in_use"></span>**ERROR \_ CONTROLADOR DE IMPRESORA EN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

3001 (0xBB9)
</dt> <dt>



El controlador de impresora especificado está actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPOOL_FILE_NOT_FOUND"></span><span id="error_spool_file_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL ARCHIVO \_ \_ SPOOL \_**
</dt> <dd> <dl> <dt>

3002 (0xBBA)
</dt> <dt>



No se encontró el archivo de cola.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_STARTDOC"></span><span id="error_spl_no_startdoc"></span>**ERROR \_ SPL \_ NO \_ STARTDOC**
</dt> <dd> <dl> <dt>

3003 (0xBBB)
</dt> <dt>



No se emitió una llamada a StartDocPrinter.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPL_NO_ADDJOB"></span><span id="error_spl_no_addjob"></span>**ERROR \_ SPL \_ NO \_ ADDJOB**
</dt> <dd> <dl> <dt>

3004 (0xBBC)
</dt> <dt>



No se emitió una llamada a AddJob.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_PROCESSOR_ALREADY_INSTALLED"></span><span id="error_print_processor_already_installed"></span>**ERROR \_ EL PROCESADOR DE IMPRESIÓN YA ESTÁ \_ \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

3005 (0xBBD)
</dt> <dt>



El procesador de impresión especificado ya está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_ALREADY_INSTALLED"></span><span id="error_print_monitor_already_installed"></span>**ERROR PRINT MONITOR ALREADY INSTALLED (MONITOR DE \_ IMPRESIÓN DE ERRORES YA \_ \_ \_ INSTALADO)**
</dt> <dd> <dl> <dt>

3006 (0xBBE)
</dt> <dt>



El monitor de impresión especificado ya se ha instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINT_MONITOR"></span><span id="error_invalid_print_monitor"></span>**ERROR \_ MONITOR DE IMPRESIÓN NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

3007 (0xBBF)
</dt> <dt>



El monitor de impresión especificado no tiene las funciones necesarias.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_MONITOR_IN_USE"></span><span id="error_print_monitor_in_use"></span>**ERROR \_ DEL MONITOR DE IMPRESIÓN EN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

3008 (0xBC0)
</dt> <dt>



El monitor de impresión especificado está actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_HAS_JOBS_QUEUED"></span><span id="error_printer_has_jobs_queued"></span>**ERROR \_ LA IMPRESORA TIENE TRABAJOS EN \_ \_ \_ COLA**
</dt> <dd> <dl> <dt>

3009 (0xBC1)
</dt> <dt>



No se permite la operación solicitada cuando hay trabajos en cola en la impresora.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_REBOOT_REQUIRED"></span><span id="error_success_reboot_required"></span>**ERROR NECESARIO \_ \_ PARA REINICIAR \_ CORRECTAMENTE**
</dt> <dd> <dl> <dt>

3010 (0xBC2)
</dt> <dt>



La operación solicitada se ha realizado correctamente. Los cambios no serán efectivos hasta que se reinicie el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SUCCESS_RESTART_REQUIRED"></span><span id="error_success_restart_required"></span>**ERROR \_ NECESARIO PARA REINICIAR \_ \_ CORRECTAMENTE**
</dt> <dd> <dl> <dt>

3011 (0xBC3)
</dt> <dt>



La operación solicitada se ha realizado correctamente. Los cambios no serán efectivos hasta que se reinicie el servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_FOUND"></span><span id="error_printer_not_found"></span>**NO SE \_ ENCONTRÓ LA IMPRESORA DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

3012 (0xBC4)
</dt> <dt>



No se encontraron impresoras.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_WARNED"></span><span id="error_printer_driver_warned"></span>**ERROR \_ EL CONTROLADOR DE IMPRESORA HA SIDO \_ \_ AMONESTÓ**
</dt> <dd> <dl> <dt>

3013 (0xBC5)
</dt> <dt>



Se sabe que el controlador de impresora no es confiable.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_BLOCKED"></span><span id="error_printer_driver_blocked"></span>**ERROR CONTROLADOR \_ DE \_ IMPRESORA \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

3014 (0xBC6)
</dt> <dt>



Se sabe que el controlador de impresora daña el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_PACKAGE_IN_USE"></span><span id="error_printer_driver_package_in_use"></span>**ERROR \_ DEL PAQUETE DEL CONTROLADOR DE IMPRESORA EN \_ \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

3015 (0xBC7)
</dt> <dt>



El paquete de controladores de impresora especificado está actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORE_DRIVER_PACKAGE_NOT_FOUND"></span><span id="error_core_driver_package_not_found"></span>**ERROR \_ CORE \_ DRIVER \_ PACKAGE \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

3016 (0xBC8)
</dt> <dt>



No se puede encontrar un paquete de controladores principal requerido por el paquete de controladores de impresora.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_REQUIRED"></span><span id="error_fail_reboot_required"></span>**ERROR AL \_ \_ REINICIAR NECESARIO \_**
</dt> <dd> <dl> <dt>

3017 (0xBC9)
</dt> <dt>



Error en la operación solicitada. Se requiere un reinicio del sistema para revertir los cambios realizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAIL_REBOOT_INITIATED"></span><span id="error_fail_reboot_initiated"></span>**ERROR \_ AL \_ REINICIAR \_ INICIADO**
</dt> <dd> <dl> <dt>

3018 (0xBCA)
</dt> <dt>



Error en la operación solicitada. Se ha iniciado un reinicio del sistema para revertir los cambios realizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_DRIVER_DOWNLOAD_NEEDED"></span><span id="error_printer_driver_download_needed"></span>**ERROR NECESARIO \_ PARA DESCARGAR EL CONTROLADOR DE \_ \_ \_ IMPRESORA**
</dt> <dd> <dl> <dt>

3019 (0xBCB)
</dt> <dt>



El controlador de impresora especificado no se encontró en el sistema y debe descargarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINT_JOB_RESTART_REQUIRED"></span><span id="error_print_job_restart_required"></span>**ERROR SE \_ REQUIERE REINICIAR EL TRABAJO DE \_ \_ \_ IMPRESIÓN**
</dt> <dd> <dl> <dt>

3020 (0xBCC)
</dt> <dt>



No se pudo imprimir el trabajo de impresión solicitado. Una actualización del sistema de impresión requiere que se vuelva a enviar el trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PRINTER_DRIVER_MANIFEST"></span><span id="error_invalid_printer_driver_manifest"></span>**ERROR \_ MANIFIESTO DE CONTROLADOR DE IMPRESORA NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

3021 (0xBCD)
</dt> <dt>



El controlador de impresora no contiene un manifiesto válido o demasiados manifiestos.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRINTER_NOT_SHAREABLE"></span><span id="error_printer_not_shareable"></span>**ERROR LA \_ IMPRESORA NO SE PUEDE \_ \_ COMPARTIR**
</dt> <dd> <dl> <dt>

3022 (0xBCE)
</dt> <dt>



No se puede compartir la impresora especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_PAUSED"></span><span id="error_request_paused"></span>**SOLICITUD \_ DE ERROR EN \_ PAUSA**
</dt> <dd> <dl> <dt>

3050 (0xBEA)
</dt> <dt>



La operación se ha pausado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_REISSUE_AS_CACHED"></span><span id="error_io_reissue_as_cached"></span>**ERROR \_ \_ E/S SE VUELVAN A EMITIR \_ COMO ALMACENADOS EN \_ CACHÉ**
</dt> <dd> <dl> <dt>

3950 (0xF6E)
</dt> <dt>



Vuelva a emitir la operación dada como una operación de E/S almacenada en caché.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




