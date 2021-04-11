---
description: Describe los códigos de error 8200-8999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Códigos de error del sistema (8200-8999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274964"
---
# <a name="system-error-codes-8200-8999"></a>Códigos de error del sistema (8200-8999)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 8200 a 8999. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR \_ DS \_ no \_ instalado**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Error al instalar el servicio de directorio. Para obtener más información, vea el registro de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR de la \_ \_ pertenencia a DS \_ evaluada \_ localmente**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



El servicio de directorio evaluó las pertenencias a grupos localmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR \_ DS \_ ningún \_ atributo \_ o \_ valor**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



El atributo o valor de servicio de directorio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de atributo no válida de DS \_**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



La sintaxis de atributo especificada para el servicio de directorio no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR \_ de \_ tipo de atributo DS no \_ \_ definido**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



No se ha definido el tipo de atributo especificado para el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR \_ el \_ atributo \_ o \_ valor de DS \_ existe**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



El atributo o valor de servicio de directorio especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR de \_ DS \_ ocupado**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



El servicio de directorio está ocupado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR \_ DS \_ no disponible**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



El servicio de directorio no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR \_ DS \_ no \_ \_ asignado RID**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



El servicio de directorios no puede asignar un identificador relativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR \_ DS \_ no hay \_ más \_ RID**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



El servicio de directorio ha agotado el grupo de identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR en el \_ \_ propietario del rol incorrecto de DS \_ \_**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



No se pudo realizar la operación solicitada porque el servicio de directorio no es el maestro para ese tipo de operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**error \_ de \_ inicialización de RIDMGR de DS \_ \_**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



El servicio de directorio no pudo inicializar el subsistema que asigna identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR \_ de \_ \_ infracción de clase obj DS \_**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



La operación solicitada no cumplió una o más restricciones asociadas a la clase del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR \_ \_ de la peralte \_ de DS en \_ no \_ hoja**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



El servicio de directorio solo puede realizar la operación solicitada en un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR \_ de DS no se pudo \_ \_ en \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada en el atributo RDN de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR DS no se pudo \_ \_ mod ( \_ \_ \_ clase)**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



El servicio de directorio detectó un intento de modificar la clase de objeto de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**error \_ de \_ \_ movimiento entre Dom cruzado \_ de DS \_**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



No se pudo realizar la operación de movimiento entre dominios solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR \_ de \_ GC de DS \_ no \_ disponible**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



No se puede establecer contacto con el servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**\_Directiva compartida de errores \_**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



El objeto de Directiva se comparte y solo puede modificarse en la raíz.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**\_ \_ \_ no \_ se encontró el objeto de directiva de error**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



El objeto de Directiva no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**\_directiva \_ de error solo \_ en \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



La información de directiva solicitada solo está en el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**promoción de errores \_ \_ activa**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



La promoción del controlador de dominio está activa actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR: \_ no hay ninguna \_ promoción \_ activa**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



La promoción del controlador de dominio no está activa actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**error \_ de \_ operaciones de DS \_ error**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Se produjo un error de operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**error \_ de \_ Protocolo de DS \_ error**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Se ha producido un error de protocolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR de \_ DS \_ TIMELIMIT \_ superado**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



Se superó el límite de tiempo para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR de \_ DS \_ SIZELIMIT \_ superado**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



Se superó el límite de tamaño para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**se \_ \_ \_ superó el límite de administración de DS de error \_**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Se superó el límite administrativo para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR \_ de \_ comparación de DS \_ false**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



La respuesta de comparación era falsa.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR \_ de \_ comparación de DS \_ true**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



La respuesta de comparación era verdadera.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**\_no se \_ admite el \_ método de autenticación DS \_ de error \_**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



El servidor no admite el método de autenticación solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR \_ de \_ DS \_ autenticación segura \_ requerida**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Se requiere un método de autenticación más seguro para este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR \_ de \_ autenticación no adecuada de DS \_**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Autenticación inadecuada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR \_ de \_ autenticación DS \_ desconocida**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Se desconoce el mecanismo de autenticación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**\_referencia de DS de error \_**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



El servidor ha devuelto una referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR \_ DS \_ \_ extensión de crít no disponible \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



El servidor no admite la extensión crítica solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR \_ de \_ confidencialidad de DS \_ requerido**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Esta solicitud requiere una conexión segura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR \_ de \_ coincidencia incorrecta de DS \_**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Coincidencia inadecuada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR \_ de \_ infracción de restricción de DS \_**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Se ha producido una infracción de restricción.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR \_ DS \_ no \_ tal \_ objeto**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



No existe tal objeto en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**\_problema de \_ alias de DS de error \_**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Hay un problema de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR \_ DS \_ \_ Sintaxis DN no válida \_**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Se ha especificado una sintaxis DN no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**el ERROR de \_ DS \_ es \_ hoja**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



El objeto es un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**problema de alias de DS de ERROR \_ \_ \_ deref \_**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Hay un problema de desreferenciación de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR \_ \_ de DS que no \_ se \_ realizará**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



El servidor no va a procesar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR \_ de \_ detección de bucle DS \_**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Se ha detectado un bucle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR \_ de \_ infracción de nomenclatura de DS \_**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Existe una infracción de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**\_los resultados del objeto DS de error son \_ \_ \_ demasiado \_ grandes**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



El conjunto de resultados es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**el ERROR de \_ DS \_ afecta a \_ varios \_ DSA**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



La operación afecta a varios DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR en el \_ servidor de DS \_ \_**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



el servidor no es funcional.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**error de \_ DS \_ local \_ error**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Se ha producido un error local.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**error de \_ codificación de DS de error \_ \_**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Se ha producido un error de codificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**error \_ de \_ descodificación de DS \_**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Se ha producido un error de descodificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR \_ de \_ filtro de DS \_ desconocido**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



No se reconoce el filtro de búsqueda.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**error \_ de \_ parámetro DS de error \_**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Uno o más parámetros no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR \_ DS \_ no \_ compatible**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



No se admite el método especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR \_ DS \_ no \_ se \_ devolvió ningún resultado**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



No se devolvieron resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**\_ \_ \_ no \_ se encontró el control DS de error**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



El servidor no admite el control especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR \_ de \_ bucle de cliente DS \_**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



El cliente ha detectado un bucle de referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**se \_ \_ \_ superó el límite de referencia de DS \_**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



Se superó el límite de referencias preestablecidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR \_ \_ no se \_ encuentra el control de ordenación DS \_**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



La búsqueda requiere un control SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**error en el intervalo de desplazamiento de \_ DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Los resultados de la búsqueda superan el intervalo de desplazamiento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR de \_ DS \_ RIDMGR \_ deshabilitado**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



El servicio de directorio detectó que el subsistema que asigna identificadores relativos está deshabilitado. Esto puede ocurrir como un mecanismo de protección cuando el sistema determina que se ha agotado una parte importante de los identificadores relativos (RID). Consulte <https://go.microsoft.com/fwlink/p/?linkid=228610> para ver los pasos de diagnóstico recomendados y el procedimiento para volver a habilitar la creación de cuentas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**el ERROR de la \_ \_ raíz DS \_ debe \_ ser \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



El objeto raíz debe ser el encabezado de un contexto de nomenclatura. El objeto raíz no puede tener un elemento primario con instancias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR de la \_ réplica de adición de DS \_ \_ \_ desbloqueado**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



No se puede realizar la operación de agregar réplica. El contexto de nomenclatura debe ser grabable para poder crear la réplica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR \_ DS \_ ATT \_ no \_ Def \_ en el \_ esquema**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Se ha producido una referencia a un atributo que no está definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**se \_ \_ \_ \_ superó el tamaño máximo de obj de DS de error \_**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



Se ha superado el tamaño máximo de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR \_ DS \_ \_ el nombre de la cadena obj \_ \_ existe**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Se intentó agregar un objeto al directorio con un nombre que ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR \_ DS \_ no \_ se \_ ha definido ningún RDN \_ en el \_ esquema**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Se intentó agregar un objeto de una clase que no tiene un RDN definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**esquema de ERROR \_ DS no \_ \_ \_ coincidente de RDN \_**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Se intentó agregar un objeto con un RDN que no es el RDN definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR \_ DS \_ no \_ \_ \_ se ha solicitado ATTS**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



No se encontró ninguno de los atributos solicitados en los objetos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR \_ \_ \_ \_ de búfer de usuario de DS a \_ pequeño**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



El búfer del usuario es demasiado pequeño.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR \_ DS \_ ATT \_ \_ no está \_ en \_ obj**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



El atributo especificado en la operación no está presente en el objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR \_ DS \_ no válido de \_ operación de modificación \_**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Operación de modificación no válida. Algunos aspectos de la modificación no se permiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**el \_ obj DS de error \_ \_ es demasiado \_ grande**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



El objeto especificado es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**ERROR en el \_ \_ tipo de instancia incorrecta de DS \_ \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



El tipo de instancia especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR de \_ DS \_ MASTERDSA \_ requerido**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



La operación se debe realizar en un DSA maestro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**se \_ \_ requiere la \_ clase de objeto DS de error \_**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



Se debe especificar el atributo de clase de objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR \_ DS \_ falta \_ \_ ATT**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Falta un atributo requerido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR \_ DS \_ ATT \_ no \_ Def \_ para la \_ clase**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Se intentó modificar un objeto para incluir un atributo que no es válido para su clase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**el ERROR \_ DS \_ ATT \_ ya \_ existe**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



El atributo especificado ya está presente en el objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR DS no se pudo \_ \_ \_ agregar \_ valores de ATT \_**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



El atributo especificado no está presente o no tiene valores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR \_ de \_ \_ restricción de valor único de DS \_**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Se especificaron varios valores para un atributo que solo puede tener un valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**\_restricción de \_ intervalo de DS de error \_**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Un valor para el atributo no se encontraba en el intervalo aceptable de valores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**el ERROR \_ DS \_ ATT \_ Val \_ ya \_ existe**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



El valor especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR \_ DS \_ \_ no se \_ encuentra \_ la**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



No se puede quitar el atributo porque no está presente en el objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR \_ DS \_ \_ no se \_ encuentra \_ el \_ Val de ATT**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



No se puede quitar el valor de atributo porque no está presente en el objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR la \_ raíz de DS no \_ \_ \_ se puede \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



El objeto raíz especificado no puede ser un subref.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR \_ DS \_ sin \_ encadenamiento**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



No se permite el encadenamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR \_ DS \_ sin \_ cadena \_ eval**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



No se permite la evaluación encadenada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR \_ DS \_ ningún \_ \_ objeto primario**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



No se puede realizar la operación porque el principal del objeto no se ha instanciado o se ha eliminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**ERROR \_ DS \_ primario \_ es \_ un \_ alias**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



No se permite tener un elemento primario que sea un alias. Los alias son objetos hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR DS no se pudo \_ \_ \_ mezclar \_ Master \_ y \_ reps**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



El objeto y el elemento primario deben ser del mismo tipo, tanto maestros como ambas réplicas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR \_ DS los \_ elementos secundarios \_**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



No se puede realizar la operación porque existen objetos secundarios. Esta operación solo se puede realizar en un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**\_ \_ \_ no \_ se encontró el obj del DS de error**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



No se encontró el objeto de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**\_falta el \_ obj con alias de DS \_ \_**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Falta el objeto con alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de nombre incorrecto de DS \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



El nombre del objeto tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**el \_ alias \_ \_ de DS de error señala \_ a \_ alias**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



No se permite que un alias haga referencia a otro alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR DS no se pudo \_ \_ \_ deref \_ alias**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



No se puede desreferenciar el alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR \_ \_ de DS fuera \_ del \_ ámbito**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



La operación está fuera del ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR \_ al \_ quitar el objeto DS \_ \_**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



La operación no puede continuar porque el objeto está en proceso de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR DS no se pudo \_ \_ eliminar el \_ \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



No se puede eliminar el objeto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**error de \_ DS \_ genérico \_**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Error de servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR \_ DS \_ DSA \_ debe \_ ser \_ un \_ maestro int**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



La operación solo se puede realizar en un objeto DSA maestro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR \_ de \_ clase DS \_ no \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



El objeto debe ser de la clase DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**\_derechos de \_ acceso de INSUFF de DS \_ \_**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Derechos de acceso insuficientes para realizar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR \_ DS \_ no válido \_ superior**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



No se puede Agregar el objeto porque el elemento primario no está en la lista de posibles superiores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**\_atributo DS \_ \_ de error propiedad \_ de \_ Sam**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



No se permite el acceso al atributo porque el atributo es propiedad del administrador de cuentas de seguridad (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR \_ de \_ nombre de DS \_ demasiadas \_ \_ partes**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



El nombre tiene demasiadas partes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR \_ de \_ nombre de DS \_ demasiado \_ largo**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



El nombre es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**ERROR \_ : \_ el valor del nombre de DS \_ \_ es demasiado \_ largo**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



El valor del nombre es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR de \_ nombre de DS no \_ \_ analizable**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



El servicio de directorio encontró un error al analizar un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR \_ de \_ tipo de nombre de DS \_ \_ desconocido**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



El servicio de directorio no puede obtener el tipo de atributo de un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR \_ DS \_ no es \_ un \_ objeto**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



El nombre no identifica un objeto; el nombre identifica una ficticia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR \_ DS \_ seg. \_ desc. \_ \_**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



El descriptor de seguridad es demasiado corto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR \_ DS \_ s \_ DESC \_ no válido**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



El descriptor de seguridad no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR \_ DS \_ no se \_ eliminó \_ el nombre**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



No se pudo crear el nombre para el objeto eliminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**ERROR \_ DS \_ SUBREF \_ debe \_ tener un \_ elemento primario**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Debe existir el elemento primario de un nuevo subref.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR \_ DS \_ NCNAME \_ debe \_ ser \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



El objeto debe ser un contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR DS no se pudo \_ \_ \_ agregar \_ solo el sistema \_**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



No se permite agregar un atributo que sea propiedad del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**la \_ clase DS de error \_ \_ debe \_ ser \_ concreta**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



La clase del objeto debe ser estructural; no se puede crear una instancia de una clase abstracta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR \_ DS \_ no válido en el \_ DMD**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



No se encontró el objeto de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**\_existe el \_ \_ GUID obj de DS \_ de error**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Ya existe un objeto local con este GUID (inactivo o activo).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR \_ DS \_ no está \_ en \_ BACKLINK**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



La operación no se puede realizar en un vínculo de retroceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR \_ DS \_ no hay ningún \_ CROSSREF \_ para \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



No se encontró la referencia cruzada para el contexto de nomenclatura especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR \_ de \_ cierre de \_ DS**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



No se pudo realizar la operación porque el servicio de directorio se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR de \_ DS: \_ \_ operación desconocida**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



La solicitud de servicio de directorio no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR \_ del \_ \_ propietario del rol DS no válido \_**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



No se pudo leer el atributo del propietario del rol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR de \_ COULDNT de DS de \_ \_ contacto \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



Error en la operación FSMO solicitada. No se puede poner en contacto con el titular de FSMO actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR de \_ DS \_ Cross \_ NC \_ DN \_ Rename**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



No se permite la modificación de un DN en un contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR DS no se pudo \_ \_ \_ MODIF \_ \_ .**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



El atributo no se puede modificar porque es propiedad del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR \_ solo en el duplicador de DS \_ \_**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Solo el replicador puede realizar esta función.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR de la \_ \_ clase obj DS \_ \_ no \_ definida**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



La clase especificada no está definida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR \_ DS \_ \_ clase obj \_ no \_ subclase**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



La clase especificada no es una subclase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR de \_ referencia de nombre de DS \_ \_ \_ no válida**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



La referencia de nombre no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**\_existe una \_ \_ referencia cruzada de DS \_ de error**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Ya existe una referencia cruzada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR DS no se pudo \_ \_ \_ del \_ maestro \_ CROSSREF**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



No se permite eliminar una referencia cruzada maestra.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR \_ el \_ subárbol de DS no se pudo \_ notificar al \_ \_ \_ encabezado NC**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Las notificaciones de subárbol solo se admiten en encabezados de NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR de \_ filtro de notificación de DS \_ \_ \_ demasiado \_ complejo**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



El filtro de notificación es demasiado complejo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR \_ de \_ RDN DUP de DS \_**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



No se pudo actualizar el esquema: RDN duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**\_OID de \_ reduplicación DS de error \_**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



No se pudo actualizar el esquema: OID duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**\_ \_ \_ ID. de MAPI \_ DUP de error de DS**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Error al actualizar el esquema: identificador de MAPI duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**\_GUID de \_ \_ \_ ID. de esquema duplicado \_ de error de DS**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Error al actualizar el esquema: GUID de ID. de esquema duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR \_ en \_ \_ \_ el nombre para mostrar de LDAP DUP en DS \_**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Error al actualizar el esquema: nombre para mostrar LDAP duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR de \_ DS semántico de la \_ \_ prueba de ATT \_**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



No se pudo actualizar el esquema: intervalo menor que el intervalo superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR \_ de \_ coincidencia de sintaxis de DS \_**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Error al actualizar el esquema: no coincide la sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**el ERROR \_ DS \_ existe \_ en \_ debe \_ tener**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



No se pudo eliminar el esquema: el atributo se utiliza en debe contener.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**el ERROR \_ DS \_ existe \_ en \_ puede \_ tener**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



No se pudo eliminar el esquema: el atributo se usa en puede contener.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**el ERROR \_ DS \_ inexistente \_ puede \_ tener**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Error al actualizar el esquema: el atributo de puede contener no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**el ERROR \_ DS no \_ existente \_ debe \_ tener**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Error al actualizar el esquema: el atributo de debe contener no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR \_ de \_ \_ prueba de CLS de AUX \_ de DS \_**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Error al actualizar el esquema: la clase de la lista de clases auxiliares no existe o no es una clase auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR \_ de \_ \_ Poss SUP inexistente de DS \_**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



No se pudo actualizar el esquema: la clase en Poss no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR en la \_ \_ prueba de sub \_ CLS de \_ DS \_**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Error al actualizar el esquema: la clase en la lista de subclases no existe o no cumple las reglas de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR en la \_ \_ \_ Sintaxis de \_ \_ ID. de RDN RDN erróneo de DS \_**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



No se pudo actualizar el esquema: el ID. de RDN-ATT-ID tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**el ERROR \_ DS \_ existe \_ en \_ AUX \_ CLS**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



No se pudo eliminar el esquema: la clase se usa como clase auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**el \_ error \_ DS \_ existe \_ en \_ subcls**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



No se pudo eliminar el esquema: la clase se usa como subclase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**el ERROR \_ DS \_ existe en el \_ SUP de \_ Poss \_**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



No se pudo eliminar el esquema: se usa la clase como Poss superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR \_ de \_ RECALCSCHEMA de DS \_**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



No se pudo actualizar el esquema al recalcular la caché de validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR \_ al \_ eliminar el árbol de DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



No se ha terminado de eliminar el árbol. La solicitud se debe volver a realizar para continuar con la eliminación del árbol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR DS no se pudo \_ \_ \_ eliminar**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



No se pudo realizar la operación de eliminación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**\_ \_ \_ \_ ID. de solicitud de esquema DS ATT de error \_**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



No se puede leer el identificador de clase de control para el registro de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR \_ de \_ \_ Sintaxis de \_ esquema de ATT \_ de DS incorrecta**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



El esquema de atributo tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR de caché de ERROR de \_ DS \_ \_ \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



No se pudo almacenar en caché el atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR de la \_ \_ \_ \_ clase caché no se pudo DS**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



No se pudo almacenar en caché la clase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR DS no se pudo \_ \_ quitar la \_ \_ caché de ATT \_**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



No se pudo quitar el atributo de la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR DS no se pudo \_ \_ quitar la \_ \_ caché de clases \_**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



No se pudo quitar la clase de la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



No se pudo leer el atributo de nombre distintivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR de \_ DS \_ que falta \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



No se configuró ninguna referencia superior para el servicio de directorio. Por tanto, el servicio de directorio no puede emitir referencias a los objetos fuera de este bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR DS no se pudo \_ \_ recuperar la \_ \_ instancia**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



No se pudo recuperar el atributo de tipo de instancia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**ERROR \_ de \_ incoherencia de código DS \_**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**error \_ de \_ base de datos de DS \_**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Error de base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR \_ DS \_ GOVERNSID \_**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Falta el atributo GOVERNSID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR \_ DS \_ falta \_ \_ ATT esperado**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Falta un atributo esperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR \_ DS \_ \_ falta la \_ \_ referencia CR de NCNAME**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Falta una referencia cruzada en el contexto de nomenclatura especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**error \_ de \_ comprobación de seguridad de DS \_ \_**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Se ha producido un error de comprobación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**\_no se \_ cargó el esquema DS de \_ error \_**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



No se ha cargado el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR \_ de \_ asignación de esquema de DS \_ \_**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



No se pudo asignar el esquema. Compruebe si el equipo se está quedando sin memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR en la \_ Sintaxis de REQ de esquema de DS \_ ATT \_ \_ \_**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



No se pudo obtener la sintaxis necesaria para el esquema de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**error \_ \_ GCVERIFY DS \_ error**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



No se pudo comprobar el catálogo global. El catálogo global no está disponible o no es compatible con la operación. Parte del directorio no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de esquema \_ de DS Dra**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



No se pudo realizar la operación de replicación debido a un error de coincidencia de esquema entre los servidores implicados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR \_ DS no se \_ encuentra el \_ \_ DSA \_ obj**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



No se encontró el objeto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR \_ DS \_ no \_ se encuentra el \_ \_ NC esperado**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



No se encontró el contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR \_ DS no se \_ \_ encuentra \_ NC \_ en la \_ memoria caché**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



No se encontró el contexto de nomenclatura en la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR DS no se pudo \_ \_ recuperar el \_ \_ elemento secundario**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



No se pudo recuperar el objeto secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR \_ de \_ seguridad de DS \_ modificación no válida \_**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



No se permitió la modificación por motivos de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR DS no se pudo \_ \_ reemplazar el \_ \_ \_ rec oculto**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



La operación no puede reemplazar el registro oculto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ERROR en el \_ \_ archivo de jerarquía incorrecta de DS \_ \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



El archivo de jerarquía no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR en la \_ tabla de jerarquía de compilación de DS \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Error al tratar de generar la tabla de jerarquías.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR \_ \_ falta el \_ parámetro de configuración de DS \_**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Falta el parámetro de configuración de directorio en el registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR \_ DS \_ \_ al contar \_ índices AB \_ con errores**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Error al intentar contar los índices de la libreta de direcciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR en la \_ tabla de jerarquía de DS \_ \_ \_ MALLOC \_**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Error en la asignación de la tabla de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR \_ interno de DS \_ \_**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



El servicio de directorio encontró un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**error de \_ DS \_ desconocido \_**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



El servicio de directorio encontró un error desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**el ERROR de la \_ raíz de DS \_ requiere la \_ \_ clase \_ Top**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Un objeto raíz requiere una clase de ' Top '.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR de \_ DS al \_ rechazar los \_ \_ roles FSMO**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Este servidor de directorio se está cerrando y no puede tomar posesión de los nuevos roles de operación de maestro único flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR \_ DS \_ falta \_ la \_ configuración de FSMO**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Falta información de configuración obligatoria en el servicio de directorio y no puede determinar la propiedad de los roles de operación de un solo maestro flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR \_ DS \_ no se pueden ceder \_ \_ \_ roles**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



El servicio de directorio no pudo transferir la propiedad de uno o varios roles de operación de maestro único flotante a otros servidores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR de \_ DS \_ Dra \_ genérico**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



No se pudo realizar la operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR en el \_ \_ \_ parámetro no válido del Dra DS \_**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Se especificó un parámetro no válido para esta operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR de \_ DS \_ Dra \_ ocupado**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



El servicio de directorio está demasiado ocupado para completar la operación de replicación en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR \_ DS \_ Dra \_ \_ DN erróneo**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



El nombre distintivo especificado para esta operación de replicación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR de \_ DS no válido de DS \_ Dra \_ \_**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



El contexto de nomenclatura especificado para esta operación de replicación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR \_ \_ DN Dra \_ DN \_ existe**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



El nombre distintivo especificado para esta operación de replicación ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**error \_ \_ interno de Dra de DS \_ \_**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



El sistema de replicación encontró un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR en el \_ \_ \_ DIT Dra incoherente de DS \_**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



La operación de replicación encontró una incoherencia en la base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR en la \_ \_ \_ conexión \_ Dra de DS**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



No se pudo establecer contacto con el servidor especificado para esta operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR \_ de \_ \_ tipo de \_ instancia \_ incorrecta de Dra DS**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



La operación de replicación encontró un objeto con un tipo de instancia no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR \_ \_ de DS \_ Dra \_ de \_ memoria insuficiente**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



La operación de replicación no pudo asignar memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR \_ de \_ correo Dra de DS \_ \_**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



La operación de replicación encontró un error con el sistema de correo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**el ERROR \_ DS \_ Dra \_ ref \_ ya \_ existe**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



La información de referencia de replicación para el servidor de destino ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR \_ de \_ referencia Dra de DS \_ \_ no \_ encontrada**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



La información de referencia de replicación para el servidor de destino no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR \_ DS \_ Dra \_ obj \_ es \_ origen de REP \_**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



No se puede quitar el contexto de nomenclatura porque se replica en otro servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**error \_ DS \_ BD de Dra \_ \_ error**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



La operación de replicación encontró un error de base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR \_ DS \_ Dra \_ sin \_ réplica**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



El contexto de nomenclatura se está quitando o no se ha replicado desde el servidor especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR \_ de \_ acceso de Dra DS \_ \_ denegado**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Se denegó el acceso a la replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR \_ DS \_ Dra \_ no \_ compatible**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



La operación solicitada no es compatible con esta versión del servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR \_ de \_ RPC Dra de DS \_ \_ cancelado**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



Se canceló la llamada a procedimiento remoto de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**origen Dra de ERROR de \_ DS \_ \_ \_ deshabilitado**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



El servidor de origen está rechazando actualmente las solicitudes de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR \_ de \_ receptor Dra de DS \_ \_ deshabilitado**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



El servidor de destino está rechazando actualmente las solicitudes de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**\_conflicto de \_ nombres de Dra de DS \_ \_**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



No se pudo realizar la operación de replicación debido a una colisión de nombres de objetos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR \_ de \_ origen Dra de DS \_ \_ reinstalado**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



Se ha reinstalado el origen de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR \_ : \_ no se encuentra el \_ elemento primario de Dra DS \_**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



No se pudo realizar la operación de replicación porque falta un objeto primario necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR \_ de \_ Dra DS \_ cambiado**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



Se ha adelantado la operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR \_ DS: salir de la \_ \_ \_ sincronización**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



Se abandonó el intento de sincronización de la replicación debido a una falta de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR \_ de \_ cierre de Dra de DS \_**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



La operación de replicación finalizó porque el sistema se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR en el \_ \_ \_ \_ \_ conjunto parcial de Dra no compatible DS**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



No se pudo realizar el intento de sincronización porque el controlador de dominio de destino está esperando sincronizar nuevos atributos parciales desde el origen. Esta condición es normal si un cambio de esquema reciente modificó el conjunto de atributos parcial. El conjunto de atributos parciales de destino no es un subconjunto del conjunto de atributos parciales de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**el \_ origen Dra DS de error \_ \_ es una \_ \_ \_ réplica parcial**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



No se pudo realizar el intento de sincronización de replicación porque una réplica maestra intentó realizar la sincronización desde una réplica parcial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR \_ de \_ \_ conexión de EXTN Dra \_ de DS \_**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Se ha establecido contacto con el servidor especificado para esta operación de replicación, pero el servidor no pudo ponerse en contacto con un servidor adicional necesario para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de esquema de instalación de DS \_**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



La versión del esquema del servicio de directorio del bosque de origen no es compatible con la versión del servicio de directorio de este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**\_identificador de \_ \_ vínculo DUP de DS \_ de error**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



No se pudo actualizar el esquema: ya existe un atributo con el mismo identificador de vínculo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR \_ al \_ resolver el nombre de DS \_ error \_**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Traducción de nombres: error de procesamiento genérico.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**error \_ de \_ nombre de DS \_ \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Traducción de nombres: no se encontró el nombre o no es suficiente para ver el nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR \_ de \_ nombre de DS \_ error \_ no \_ único**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Traducción de nombres: nombre de entrada asignado a más de un nombre de salida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR \_ \_ el nombre de DS \_ error \_ no \_ asignación**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Traducción de nombres: se encontró el nombre de entrada, pero no el formato de salida asociado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**ERROR \_ nombre de DS \_ \_ error \_ \_ solo dominio**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Traducción de nombres: no se puede resolver completamente, solo se encontró el dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR \_ \_ el nombre de DS \_ error \_ no \_ \_ asignación sintáctica**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Traducción de nombres: no se puede realizar una asignación puramente sintáctica en el cliente sin pasar a la conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR de \_ DS construido en el \_ \_ \_ módulo**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



No se permite la modificación de un atributo construido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR \_ DS \_ \_ clase obj de OM incorrecta \_ \_**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



El objeto OM-Object-Class especificado no es correcto para un atributo con la sintaxis especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR \_ de \_ REPL de Dra de DS \_ \_ pendiente**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



Se ha publicado la solicitud de replicación; esperando respuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR \_ DS \_ DS \_ requerido**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



La operación solicitada requiere un servicio de directorio y no hay ninguna disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR \_ DS \_ \_ nombre para \_ Mostrar \_ LDAP no válido**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



El nombre LDAP para mostrar de la clase o el atributo contiene caracteres que no son ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR \_ de \_ \_ búsqueda no \_ base de DS**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



La operación de búsqueda solicitada solo se admite para las búsquedas base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ ATTS**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



La búsqueda no pudo recuperar los atributos de la base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR de \_ DS \_ BACKLINK \_ sin \_ vínculo**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



La operación de actualización del esquema intentó agregar un atributo de vínculo hacia atrás que no tiene un vínculo de avance correspondiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR \_ de \_ coincidencia de tiempo de DS \_**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden con el número de tiempo del objeto. El origen o el destino no tienen la versión más reciente del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de nombre de origen de DS \_**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden con el nombre actual del objeto. El origen o el destino no tienen la versión más reciente del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR \_ DS \_ src \_ y \_ DST \_ NC \_ idénticos**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



El origen y el destino de la operación de movimiento entre dominios son idénticos. El autor de la llamada debe usar la operación de movimiento local en lugar de la operación de movimiento entre dominios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR de \_ DS \_ DST \_ NC \_ no coincidente**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no están en acuerdo con los contextos de nomenclatura del bosque. El origen o el destino no tienen la versión más reciente del contenedor de particiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR \_ DS \_ no \_ AUTHORITIVE \_ para \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



El destino de un movimiento entre dominios no es autoritativo para el contexto de nomenclatura de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de GUID de src de DS \_**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden con la identidad del objeto de origen. El origen o el destino no tienen la versión más reciente del objeto de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ \_ objeto eliminado**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



El servidor de destino ya sabe que el objeto que se está moviendo entre dominios se ha eliminado. El servidor de origen no tiene la versión más reciente del objeto de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR \_ \_ en la \_ operación \_ de PDC de DS en \_ curso**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Otra operación que requiere acceso exclusivo al PDC FSMO ya está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR \_ de \_ limpieza entre dominios de DS \_ \_ \_ REQD**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



No se pudo realizar una operación de movimiento entre dominios, de modo que existen dos versiones del objeto movido: una en los dominios de origen y de destino. Es necesario quitar el objeto de destino para restaurar el sistema a un estado coherente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR de \_ DS \_ XDOM de \_ \_ operación de traslado \_ no válida**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Es posible que este objeto no se mueva entre los límites del dominio porque no se permiten los movimientos entre dominios para esta clase, o bien el objeto tiene algunas características especiales, por ejemplo: cuenta de confianza o RID restringida, que impiden su movimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR \_ DS \_ peralte \_ con el \_ grupo de acct \_ \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



No se pueden trasladar objetos con pertenencias a los límites del dominio como una vez movidos, lo que infringiría las condiciones de pertenencia del grupo de cuentas. Quite el objeto de cualquier pertenencia a grupos de cuentas e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**el \_ NC DS de error \_ \_ debe \_ tener el \_ \_ elemento primario NC**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Un encabezado de contexto de nomenclatura debe ser el elemento secundario inmediato de otro encabezado de contexto de nomenclatura, no de un nodo interior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR \_ DS \_ CR \_ imposible \_ \_ validar**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



El directorio no puede validar el nombre del contexto de nomenclatura propuesto porque no contiene una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto. Asegúrese de que el rol de maestro de nomenclatura de dominios está incluido en un servidor que está configurado como un servidor de catálogo global y que el servidor está actualizado con sus asociados de replicación. (Se aplica solo a los maestros de nomenclatura de dominios de Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR de \_ dominio de DST de DS \_ \_ \_ no \_ nativo**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



El dominio de destino debe estar en modo nativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR \_ DS \_ falta \_ el \_ contenedor de infraestructura**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



No se puede realizar la operación porque el servidor no tiene un contenedor de infraestructura en el dominio de interés.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ grupo de cuentas \_**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de cuentas que no estén vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR DS no se pudo \_ \_ quitar el \_ \_ grupo de recursos \_**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de recursos no vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR \_ de \_ \_ marca de búsqueda no válida DS \_**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Las marcas de búsqueda para el atributo no son válidas. El bit de ANR solo es válido en atributos de cadenas Unicode o teletexto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR \_ DS \_ no \_ se \_ eliminó el árbol \_ antes de \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



No se permiten las eliminaciones de árbol a partir de un objeto que tiene un encabezado NC como descendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR \_ DS \_ COULDNT \_ \_ árbol \_ de bloqueo para \_ eliminar**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



El servicio de directorio no pudo bloquear un árbol para preparar una eliminación de árbol porque el árbol estaba en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR \_ DS \_ COULDNT \_ identificar \_ objetos \_ para \_ la \_ eliminación de árbol**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



El servicio de directorio no pudo identificar la lista de objetos que se van a eliminar al intentar una eliminación de árbol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR de \_ DS de \_ \_ inicialización de Sam \_**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x %2. Apague este sistema y reinicie en Modo de restauración de servicios de directorio, compruebe el registro de eventos para obtener información más detallada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR \_ de \_ \_ infracción de grupo sensible a DS \_**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Solo un administrador puede modificar la lista de miembros de un grupo administrativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR DS no se pudo \_ \_ \_ mod \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



No se puede cambiar el identificador de grupo principal de una cuenta de controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR \_ de \_ \_ modificación de \_ esquema de base no válido de DS \_**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Se ha intentado modificar el esquema base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR \_ de \_ esquema no seguro de DS \_ \_**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



No se permite agregar un nuevo atributo obligatorio a una clase existente, eliminar un atributo obligatorio de una clase existente o agregar un atributo opcional a la clase especial superior que no es un atributo backlink (directamente o a través de la herencia, por ejemplo, mediante la adición o eliminación de una clase auxiliar).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR: no se \_ permite la actualización del esquema de DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



No se permite la actualización de esquemas en este controlador de dominio porque el controlador de dominio no es el propietario del rol FSMO del esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR DS no se pudo \_ \_ \_ crear \_ en el \_ esquema**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



No se puede crear un objeto de esta clase en el contenedor de esquemas. En el contenedor de esquemas solo se pueden crear objetos Attribute-Schema y Class-Schema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR \_ DS \_ \_ no instalar ninguna \_ versión de src \_ SCH \_**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



La instalación de la réplica o el elemento secundario no pudo obtener el atributo objectVersion en el contenedor de esquema en el controlador de dominio de origen. Falta el atributo en el contenedor de esquema o las credenciales proporcionadas no tienen permiso para leerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR \_ DS \_ instalar \_ no \_ \_ versión SCH \_ en \_ INIFILE**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



La instalación de la réplica o el elemento secundario no pudo leer el atributo objectVersion en la sección SCHEMA del archivo schema.ini en el directorio system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR \_ DS \_ \_ tipo de grupo no válido \_**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



El tipo de grupo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR \_ DS \_ no \_ anidado \_ GLOBALGROUP \_ en \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



No se pueden anidar grupos globales en un dominio mixto si el grupo tiene habilitada la seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR \_ DS \_ no \_ anidar el \_ LOCALGROUP \_ en \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



No se pueden anidar grupos locales en un dominio mixto si el grupo tiene habilitada la seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ \_ miembro local**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Un grupo global no puede tener un grupo local como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ \_ miembro universal**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Un grupo global no puede tener un grupo universal como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR \_ DS \_ universal \_ peralte \_ tiene \_ \_ miembro local**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Un grupo universal no puede tener un grupo local como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR \_ DS \_ global no se \_ \_ tiene \_ miembro de CROSSDOMAIN \_**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Un grupo global no puede tener un miembro entre dominios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR \_ DS \_ local no se tiene un \_ \_ \_ \_ miembro local de CROSSDOMAIN \_**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Un grupo local no puede tener otro grupo local entre dominios como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**el \_ error \_ DS \_ tiene \_ miembros principales**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Un grupo con miembros principales no puede cambiar a un grupo deshabilitado para la seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR en la \_ \_ \_ \_ conversión SD \_ de la cadena DS**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



La carga de la caché de esquema no pudo convertir el SD predeterminado de la cadena en un objeto de esquema de clase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR \_ DS de \_ nomenclatura del \_ \_ GC maestro**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Solo se debe permitir que los DSA configurados como servidores de catálogo global contengan el rol FSMO del maestro de nomenclatura de dominios. (Sólo se aplica a los servidores de Windows 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR \_ de \_ búsqueda de DNS de DS \_ \_**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



La operación DSA no puede continuar debido a un error de búsqueda DNS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**SPN de ERROR de \_ \_ COULDNT de \_ actualización de DS \_**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Al procesar un cambio en el nombre de host DNS de un objeto, los valores de nombre de entidad de seguridad de servicio no se pueden mantener sincronizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR DS no se pudo \_ \_ \_ recuperar \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



No se pudo leer el atributo de descriptor de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR de la \_ \_ clave DS no es \_ \_ única**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



No se encontró el objeto solicitado, pero se encontró un objeto con esa clave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR \_ de \_ DS \_ \_ Sintaxis de ATT vinculada incorrecta \_**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



La sintaxis del atributo vinculado que se va a agregar es incorrecta. Los vínculos hacia delante solo pueden tener la sintaxis 2.5.5.1, 2.5.5.7 y 2.5.5.14, y los vínculos posteriores solo pueden tener la sintaxis 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR \_ DS \_ Sam \_ necesito \_ BOOTKEY \_ contraseña**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



El administrador de cuentas de seguridad debe obtener la contraseña de arranque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR \_ DS \_ Sam \_ necesito \_ \_ disquete BOOTKEY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



El administrador de cuentas de seguridad debe obtener la clave de arranque desde el disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR DS no se pudo \_ \_ \_ iniciar**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



No se puede iniciar el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR \_ de \_ inicialización de DS \_**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



No se pudieron iniciar los servicios de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR \_ \_ de DS \_ sin \_ Privacidad \_ en la \_ conexión**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



La conexión entre el cliente y el servidor requiere privacidad del paquete o mejor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**ERROR \_ \_ \_ de dominio de origen DS \_ en el \_ bosque**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Es posible que el dominio de origen no esté en el mismo bosque que el destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR \_ el \_ \_ dominio de destino DS no está en el \_ \_ \_ bosque**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



El dominio de destino debe estar en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR de \_ Auditoría de destino de DS \_ \_ \_ no \_ habilitada**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



La operación requiere que esté habilitada la auditoría de dominio de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR \_ DS no se \_ encuentra el \_ \_ controlador \_ de dominio para el \_ \_ dominio src**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



La operación no pudo encontrar un DC para el dominio de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR \_ DS \_ src \_ obj \_ not \_ Group \_ or \_ User**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



El objeto de origen debe ser un grupo o un usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR \_ DS \_ src \_ SID \_ exist \_ in \_ Forest**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



El SID del objeto de origen ya existe en el bosque de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR \_ DS \_ src \_ y \_ la \_ clase de objeto DST \_ \_ no coinciden**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



El objeto de origen y el de destino deben ser del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR \_ Sam \_ init \_ error**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x %2. Haga clic en Aceptar para apagar el sistema y reiniciar en modo seguro. Compruebe el registro de eventos para obtener información detallada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR \_ de \_ \_ envío de \_ información de esquema \_ de DS Dra**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



No se pudo incluir la información de esquema en la solicitud de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**\_conflicto de esquema de DS Dra de error \_ \_ \_**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



No se pudo completar la operación de replicación debido a una incompatibilidad de esquemas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**\_conflicto de \_ \_ \_ esquemas Dra \_ anteriores de error de DS**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



No se pudo completar la operación de replicación debido a una incompatibilidad de esquema anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR de \_ DS. \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



No se pudo aplicar la actualización de replicación porque el origen o el destino no han recibido todavía información relacionada con una operación de movimiento entre dominios reciente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**el \_ NC DS de error \_ \_ sigue teniendo \_ \_ DSA**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



No se pudo eliminar el dominio solicitado porque existen controladores de dominio que todavía hospedan este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR \_ DS \_ GC \_ requerido**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



La operación solicitada solo se puede realizar en un servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR \_ DS \_ local \_ miembro \_ de \_ \_ solo local**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Un grupo local solo puede ser miembro de otros grupos locales del mismo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR \_ DS \_ no \_ FPO \_ en \_ grupos universales \_**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Las entidades de seguridad externas no pueden ser miembros de grupos universales.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR \_ DS \_ no \_ se pudo agregar \_ al \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



El atributo no se puede replicar en el GC por motivos de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR \_ DS \_ no \_ Checkpoint \_ con \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



No se pudo realizar el punto de control con el PDC porque actualmente se están procesando demasiadas modificaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR de \_ Auditoría de origen de DS \_ \_ \_ no \_ habilitada**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



La operación requiere que esté habilitada la auditoría de dominio de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR DS no se pudo \_ \_ \_ crear \_ en el NC del no \_ dominio \_**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Los objetos de entidad de seguridad solo se pueden crear dentro de los contextos de nomenclatura de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR \_ DS \_ nombre no válido \_ \_ para el \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



No se pudo construir un nombre principal de servicio (SPN) porque el nombre de host proporcionado no tiene el formato necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**el \_ filtro DS de error \_ \_ utiliza \_ construye \_ attrs**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Se pasó un filtro que utiliza atributos construidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR \_ DS \_ UNICODEPWD \_ no \_ entre \_ comillas**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



El valor del atributo unicodePwd debe ir entre comillas dobles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR al superar la cuota de la \_ cuenta del \_ equipo DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



No se pudo unir el equipo al dominio. Ha superado el número máximo de cuentas de equipo que se permite crear en este dominio. Póngase en contacto con el administrador del sistema para que este límite se restablezca o aumente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**el \_ error \_ DS \_ debe \_ ejecutarse \_ en el \_ controlador de dominio de DST \_**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Por motivos de seguridad, la operación se debe ejecutar en el controlador de dominio de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR \_ DS \_ src \_ DC \_ debe \_ ser \_ SP4 \_ o \_ superior**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Por motivos de seguridad, el controlador de dominio de origen debe ser NT4SP4 o superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR DS no se pudo \_ \_ eliminar el \_ árbol \_ \_ imprescindible \_**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



No se pueden eliminar objetos críticos del sistema de servicios de directorio durante las operaciones de eliminación de árboles. Es posible que se haya realizado parcialmente la eliminación de árboles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR en la consola de error de \_ DS \_ init \_ \_**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



No se pudieron iniciar los servicios de directorio debido al siguiente error: %1. Estado de error: 0x %2. Haga clic en Aceptar para cerrar el sistema. Puede usar la consola de recuperación para examinar el sistema más a fondo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR \_ DS \_ Sam \_ init \_ error \_ Console**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



No se pudo inicializar el administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x %2. Haga clic en Aceptar para cerrar el sistema. Puede usar la consola de recuperación para examinar el sistema más a fondo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR en la \_ \_ versión del bosque DS \_ \_ demasiado \_ alta**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



La versión del sistema operativo no es compatible con el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración. Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio de AD DS o agregar una instancia de AD LDS en este AD DS bosque o AD LDS conjunto de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR de \_ versión de dominio de DS \_ \_ \_ demasiado \_ alto**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



La versión del sistema operativo instalada es incompatible con el nivel funcional del dominio actual. Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio en este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR: la \_ \_ versión del bosque DS \_ \_ es demasiado \_ baja**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



La versión del sistema operativo instalado en este servidor ya no es compatible con el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración. Debe elevar el nivel funcional del bosque de AD DS o AD LDS nivel funcional del conjunto de configuración antes de que este servidor pueda convertirse en un controlador de dominio de AD DS o en una instancia de AD LDS en este bosque o conjunto de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR en la \_ versión de dominio de DS \_ \_ \_ demasiado \_ baja**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



La versión del sistema operativo instalado en este servidor ya no es compatible con el nivel funcional del dominio actual. Debe elevar el nivel funcional del dominio para que este servidor pueda convertirse en un controlador de dominio en este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR \_ de \_ versión de DS compatible \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



La versión del sistema operativo instalado en este servidor no es compatible con el nivel funcional del dominio o bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR \_ DS \_ \_ versión de DSA inferior \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



No se puede elevar el nivel funcional del dominio (o bosque) al valor solicitado porque existen uno o más controladores de dominio en el dominio (o bosque) que están en un nivel funcional inferior incompatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR \_ DS \_ \_ \_ versión de comportamiento no \_ en \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



No se puede elevar el nivel funcional del bosque al valor solicitado porque uno o varios dominios todavía están en modo de dominio mixto. Todos los dominios del bosque deben estar en modo nativo para elevar el nivel funcional del bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR \_ DS \_ no \_ compatible con el criterio de \_ ordenación \_**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



No se admite el criterio de ordenación solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR \_ de \_ nombre de DS \_ no \_ único**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



El nombre solicitado ya existe como identificador único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR en la \_ \_ cuenta de equipo DS \_ \_ creada \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



La cuenta de equipo se creó antes de NT4. Es necesario volver a crear la cuenta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR \_ \_ de DS \_ fuera \_ del \_ almacén de versiones**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



La base de datos está fuera del almacén de versiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR \_ en \_ \_ los controles \_ no compatibles de DS**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



No se puede continuar la operación porque se usaron varios controles conflictivos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR \_ DS \_ sin \_ dominio de referencia \_**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



No se encuentra un dominio de referencia de descriptor de seguridad válido para esta partición.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**\_ \_ \_ ID. de vínculo \_ reservado de DS de error**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Error al actualizar el esquema: el identificador del vínculo está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**ERROR \_ de \_ ID. de vínculo de DS \_ \_ no \_ disponible**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



No se pudo actualizar el esquema: no hay identificadores de vínculo disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR \_ DS \_ AG no se \_ \_ tiene \_ \_ miembro universal**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Un grupo de cuentas no puede tener un grupo universal como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR \_ \_ de MODIFYDN \_ de DS no \_ permitido \_ por \_ tipo de instancia**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



No se permiten las operaciones de cambio de nombre o movimiento en encabezados de contexto de nomenclatura o en objetos de solo lectura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR \_ DS \_ no \_ se \_ mueve ningún objeto en el \_ \_ esquema \_ NC**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



No se permiten las operaciones de movimiento en objetos en el contexto de nomenclatura de esquemas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR \_ \_ de DS MODIFYDN no \_ permitido \_ por la \_ marca**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Se ha establecido una marca de sistema en el objeto y no permite que el objeto se mueva o cambie de nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR de \_ DS \_ MODIFYDN de \_ \_ padre incorrecto**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Este objeto no tiene permiso para cambiar su contenedor principal. Los movimientos no están prohibidos en este objeto, pero están restringidos a contenedores relacionados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**ERROR \_ de \_ nombre de DS error de \_ \_ referencia de confianza \_**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



No se puede resolver por completo, se genera una referencia a otro bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR \_ no \_ admitido \_ en el \_ \_ servidor estándar**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



La acción solicitada no se admite en el servidor estándar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR \_ DS no se \_ \_ puede acceder a la \_ \_ parte remota \_ de \_ ad**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



No se pudo obtener acceso a una partición del servicio de directorio ubicada en un servidor remoto. Asegúrese de que se está ejecutando al menos un servidor para la partición en cuestión.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR \_ DS \_ CR \_ imposible \_ \_ validar \_ V2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



El directorio no puede validar el nombre de contexto de nomenclatura propuesto (o partición) porque no contiene una réplica ni puede ponerse en contacto con una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto. Asegúrese de que el contexto de nomenclatura principal esté registrado correctamente en DNS y de que el maestro de nombres de dominio pueda tener acceso al menos a una réplica de este contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**se \_ \_ \_ superó el límite de subprocesos de DS \_**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



Se superó el límite de subprocesos para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR \_ DS \_ no \_ más cercano**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



El servidor de catálogo global no está en el sitio más cercano.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR \_ DS \_ no se pudo \_ derivar \_ SPN \_ sin \_ referencia de servidor \_**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



El DS no puede derivar un nombre principal de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el objeto de servidor correspondiente en la base de datos de DS local no tiene ningún atributo serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR en el \_ \_ \_ modo de usuario único \_ de DS \_**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



El servicio de directorio no pudo entrar en el modo de usuario único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**error \_ de \_ Sintaxis de NTDSCRIPT de DS \_ \_**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



El servicio de directorio no puede analizar el script debido a un error de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**error \_ de \_ proceso NTDSCRIPT de DS \_ \_**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



El servicio de directorio no puede procesar el script debido a un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**\_tiempo de \_ \_ réplica diferente \_ de error de DS**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada porque los servidores implicados tienen tiempos de replicación diferentes (que suelen estar relacionados con un cambio de nombre de dominio que está en curso).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**se \_ \_ \_ cambiaron las extensiones de DS DRS \_**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



El enlace del servicio de directorio se debe volver a negociar debido a un cambio en la información de las extensiones del servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR \_ \_ \_ \_ de cambio de conjunto de réplicas DS \_ no \_ permitido \_ en \_ CR deshabilitado \_**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Operación no permitida en una referencia cruzada deshabilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR \_ DS \_ no \_ MSDS \_ INtId**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



No se pudo actualizar el esquema: no hay valores disponibles para msDS-IntId.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR \_ de \_ atributo DUP de DS \_ \_**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



No se pudo actualizar el esquema: se ha duplicado msDS-INtId. Vuelva a intentar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**el \_ DS \_ de error existe \_ en \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



No se pudo eliminar el esquema: el atributo se usa en rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR \_ de \_ autorización de DS \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



El servicio de directorio no pudo autorizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR \_ de \_ script DS no válido \_**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



El servicio de directorio no puede procesar el script porque no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR \_ de \_ OP remota de \_ CROSSREF de \_ DS \_**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



No se pudo realizar la operación de referencia cruzada de creación remota en el FSMO del maestro de nomenclatura de dominios. El error de la operación se encuentra en los datos extendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR en la \_ \_ \_ referencia \_ cruzada de DS**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Una referencia cruzada está en uso localmente con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR DS no se pudo \_ \_ \_ derivar \_ SPN \_ para el \_ \_ dominio eliminado**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



El DS no puede derivar un nombre principal de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el dominio del servidor se ha eliminado del bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR DS no se pudo \_ \_ \_ disminuir \_ de nivel con el \_ \_ NC grabable**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



Los NC grabable impiden que este controlador de dominio se degrade.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR \_ de \_ ID. de DS duplicado \_ \_ encontrado**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



El objeto solicitado tiene un identificador no único y no se puede recuperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR \_ DS \_ atributo insuficiente \_ \_ para \_ crear el \_ objeto**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Se asignaron atributos insuficientes para crear un objeto. Es posible que este objeto no exista porque puede que se haya eliminado y ya se haya recolectado el elemento no utilizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**error \_ de \_ conversión de grupo DS \_ de error \_**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



No se puede convertir el grupo debido a restricciones de atributo en el tipo de grupo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR DS no se pudo \_ \_ cambiar el \_ \_ \_ \_ grupo básico de la aplicación**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de aplicaciones básicas no vacías.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR DS no se pudo \_ \_ \_ migrar el \_ \_ grupo de consultas \_ de la aplicación**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de aplicaciones basados en consultas no vacías.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**\_no se \_ \_ ha \_ comprobado el rol DS de error**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



No se pudo comprobar la propiedad del rol FSMO porque su partición de directorio no se ha replicado correctamente con al menos un asociado de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**el \_ contenedor WKO de DS de error \_ \_ \_ no puede \_ ser \_ especial**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



El contenedor de destino para una redirección de un contenedor de objetos conocido no puede ser ya un contenedor especial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR \_ \_ \_ de cambio de nombre \_ de dominio de DS en \_ curso**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada porque hay una operación de cambio de nombre de dominio en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR \_ DS \_ \_ ad \_ Child \_ NC existente**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



El servicio de directorio detectó una partición secundaria debajo del nombre de partición solicitado. La jerarquía de particiones se debe crear en un método de arriba abajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR en la \_ duración de REPL de DS \_ \_ \_ superada**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



El servicio de directorio no se puede replicar con este servidor porque el tiempo transcurrido desde la última replicación con este servidor superó la duración del desecho.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR \_ de DS no \_ permitido \_ en \_ el \_ contenedor del sistema**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



La operación solicitada no se permite en un objeto en el contenedor del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR \_ \_ en la \_ cola de envío LDAP \_ DS \_**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



La cola de envío de red de servidores LDAP se ha rellenado porque el cliente no está procesando los resultados de sus solicitudes con la rapidez suficiente. No se procesarán más solicitudes hasta que el cliente se ponga al día. Si el cliente no se pone al día, se desconectará.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**ERROR de la \_ \_ \_ ventana de \_ programación Dra \_ de DS**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



No se pudo realizar la replicación programada porque el sistema estaba demasiado ocupado para ejecutar la solicitud en la ventana de programación. La cola de replicación está sobrecargada. Considere la posibilidad de reducir el número de asociados o disminuir la frecuencia de replicación programada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR \_ de \_ Directiva de DS \_ \_ desconocida**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



En este momento, no se puede determinar si la Directiva de replicación de la rama está disponible en el controlador de dominio del concentrador. Vuelva a intentarlo más tarde para tener en cuenta las latencias de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR: \_ no hay ningún \_ objeto de configuración de sitio \_ \_**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



No existe el objeto de configuración del sitio para el sitio especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR \_ sin \_ secretos**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



El almacén de cuentas local no contiene el material secreto de la cuenta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR \_ : \_ no \_ \_ se encontró un DC grabable**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



No se pudo encontrar un controlador de dominio grabable en el dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR \_ DS \_ no \_ hay \_ objeto de servidor**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



El objeto de servidor para el controlador de dominio no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR \_ DS \_ no \_ NTDSA \_ objeto**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



No existe el objeto de configuración NTDS para el controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR de \_ búsqueda de DS \_ no \_ ASQ \_**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



La operación de búsqueda solicitada no se admite para las búsquedas de ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR \_ de \_ Auditoría de DS \_**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



No se pudo generar un evento de auditoría necesario para la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR \_ DS \_ de \_ marca de búsqueda no válida \_ \_**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Las marcas de búsqueda para el atributo no son válidas. El bit de índice de subárbol solo es válido en atributos de valor único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR de la \_ tupla de marca de \_ búsqueda no válida de DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Las marcas de búsqueda para el atributo no son válidas. El bit de índice de tupla solo es válido en atributos de cadenas Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR en la \_ tabla de jerarquía de DS \_ \_ \_ demasiado \_ profunda**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Las libretas de direcciones tienen un anidamiento demasiado profundo. No se pudo generar la tabla de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR \_ DS \_ Dra \_ dañado \_ UTD \_ Vector**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



El vector de actualización especificado está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR de los \_ secretos de Dra de DS \_ \_ \_ denegados**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



Se denegó la solicitud de replicación de secretos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR \_ de \_ \_ ID. de MAPI reservado de DS \_**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



No se pudo actualizar el esquema: el identificador de MAPI está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR \_ de \_ ID. de MAPI de DS \_ \_ no \_ disponible**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



No se pudo actualizar el esquema: no hay identificadores de MAPI disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR \_ DS \_ Dra \_ falta \_ el \_ secreto de KRBTGT**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



No se pudo realizar la operación de replicación porque faltan los atributos necesarios del objeto krbtgt local.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR \_ \_ \_ el nombre \_ de dominio \_ de DS existe en el \_ bosque**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



El nombre de dominio del dominio de confianza ya existe en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR \_ DS \_ \_ el nombre plano \_ existe en el \_ \_ bosque**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



El nombre plano del dominio de confianza ya existe en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR \_ de \_ \_ nombre principal de usuario no válido \_**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



El nombre principal de usuario (UPN) no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR \_ DS \_ OID \_ el \_ grupo asignado no \_ \_ tiene \_ miembros**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



Los grupos asignados OID no pueden tener miembros.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR \_ DS \_ OID \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



No se encuentra el OID especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**\_destino de \_ Dra \_ reciclado de DS de error \_**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



No se pudo realizar la operación de replicación porque se recicla el objeto de destino al que hace referencia un valor de vínculo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR \_ DS no \_ permitido \_ \_ redirección de NC**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



No se pudo realizar la operación de redirección porque el objeto de destino está en un NC diferente del NC de dominio del controlador de dominio actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR de \_ DS de \_ alta calidad \_ \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



El nivel funcional del conjunto de configuración AD LDS no puede reducirse al valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR \_ de \_ DS \_ versión de DSA alta \_**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



El nivel funcional del dominio (o bosque) no puede reducirse al valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR \_ DS \_ Low-ad \_ \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



No se puede elevar el nivel funcional del conjunto de configuración AD LDS al valor solicitado porque existe una o más instancias de la instancia de este que se encuentran en un nivel funcional inferior incompatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**\_ \_ SID de dominio \_ de error igual \_ que la \_ estación de \_ trabajo local**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



No se puede completar la Unión al dominio porque el SID del dominio al que intentó unirse era idéntico al SID de esta máquina. Esto es un síntoma de una instalación de sistema operativo clonada incorrectamente. Debe ejecutar Sysprep en este equipo para poder generar un nuevo SID de equipo. Consulte <https://go.microsoft.com/fwlink/p/?linkid=168895> para más información.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR de \_ validación de DS de \_ eliminación de \_ Sam \_ \_**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



No se pudo realizar la operación de eliminación porque el nombre de cuenta SAM o el nombre de cuenta SAM adicional del objeto que se va a recuperar entra en conflicto con un objeto activo existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR \_ de \_ tipo de cuenta incorrecto \_**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



El sistema no es autoritativo para la cuenta especificada y, por lo tanto, no puede completar la operación. Vuelva a intentar la operación con el proveedor asociado a esta cuenta. Si se trata de un proveedor en línea, use el sitio en línea del proveedor.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




