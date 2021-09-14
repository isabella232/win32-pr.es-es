---
description: Describe los códigos de error 8200-8999 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: f16fdfa3-b080-47ee-a7dd-241fe2d24278
title: Códigos de error del sistema (8200-8999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 7500ae4c178999de8052b0858089604652dc5237
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164581"
---
# <a name="system-error-codes-8200-8999"></a>Códigos de error del sistema (8200-8999)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema para los errores 8200 a 8999. La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_DS_NOT_INSTALLED"></span><span id="error_ds_not_installed"></span>**ERROR \_ DS \_ NOT \_ INSTALLED**
</dt> <dd> <dl> <dt>

8200 (0x2008)
</dt> <dt>



Error al instalar el servicio de directorio. Para más información, consulte el registro de eventos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MEMBERSHIP_EVALUATED_LOCALLY"></span><span id="error_ds_membership_evaluated_locally"></span>**ERROR \_ DS \_ MEMBERSHIP \_ EVALUATED \_ LOCALLY**
</dt> <dd> <dl> <dt>

8201 (0x2009)
</dt> <dt>



El servicio de directorio evaluó las pertenencias a grupos localmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_ATTRIBUTE_OR_VALUE"></span><span id="error_ds_no_attribute_or_value"></span>**ERROR \_ DS \_ SIN ATRIBUTO NI \_ \_ \_ VALOR**
</dt> <dd> <dl> <dt>

8202 (0x200A)
</dt> <dt>



El atributo o valor del servicio de directorio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ATTRIBUTE_SYNTAX"></span><span id="error_ds_invalid_attribute_syntax"></span>**ERROR \_ DS \_ SINTAXIS DE \_ ATRIBUTO NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8203 (0x200B)
</dt> <dt>



La sintaxis de atributo especificada para el servicio de directorio no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_TYPE_UNDEFINED"></span><span id="error_ds_attribute_type_undefined"></span>**ERROR \_ DS \_ ATTRIBUTE \_ TYPE \_ UNDEFINED**
</dt> <dd> <dl> <dt>

8204 (0x200C)
</dt> <dt>



El tipo de atributo especificado para el servicio de directorio no está definido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OR_VALUE_EXISTS"></span><span id="error_ds_attribute_or_value_exists"></span>**ERROR \_ DS \_ ATTRIBUTE \_ OR \_ VALUE \_ EXISTS**
</dt> <dd> <dl> <dt>

8205 (0x200D)
</dt> <dt>



El atributo o valor del servicio de directorio especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUSY"></span><span id="error_ds_busy"></span>**ERROR \_ DS \_ BUSY**
</dt> <dd> <dl> <dt>

8206 (0x200E)
</dt> <dt>



El servicio de directorio está ocupado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE"></span><span id="error_ds_unavailable"></span>**ERROR \_ DS \_ NO DISPONIBLE**
</dt> <dd> <dl> <dt>

8207 (0x200F)
</dt> <dt>



El servicio de directorio no está disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RIDS_ALLOCATED"></span><span id="error_ds_no_rids_allocated"></span>**ERROR \_ DS \_ NO \_ RIDS \_ ALLOCATED**
</dt> <dd> <dl> <dt>

8208 (0x2010)
</dt> <dt>



El servicio de directorios no puede asignar un identificador relativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MORE_RIDS"></span><span id="error_ds_no_more_rids"></span>**ERROR \_ DS \_ NO \_ MORE \_ RIDS**
</dt> <dd> <dl> <dt>

8209 (0x2011)
</dt> <dt>



El servicio de directorio ha agotado el grupo de identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCORRECT_ROLE_OWNER"></span><span id="error_ds_incorrect_role_owner"></span>**ERROR \_ DS \_ PROPIETARIO DE ROL \_ \_ INCORRECTO**
</dt> <dd> <dl> <dt>

8210 (0x2012)
</dt> <dt>



No se pudo realizar la operación solicitada porque el servicio de directorio no es el maestro para ese tipo de operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_INIT_ERROR"></span><span id="error_ds_ridmgr_init_error"></span>**ERROR \_ DS \_ RIDMGR \_ INIT \_ ERROR**
</dt> <dd> <dl> <dt>

8211 (0x2013)
</dt> <dt>



El servicio de directorio no pudo inicializar el subsistema que asigna identificadores relativos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_VIOLATION"></span><span id="error_ds_obj_class_violation"></span>**ERROR \_ DS \_ OBJ \_ CLASS \_ VIOLATION**
</dt> <dd> <dl> <dt>

8212 (0x2014)
</dt> <dt>



La operación solicitada no satisface una o varias restricciones asociadas a la clase del objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_NON_LEAF"></span><span id="error_ds_cant_on_non_leaf"></span>**ERROR \_ DS \_ CANT \_ ON \_ NON \_ LEAF**
</dt> <dd> <dl> <dt>

8213 (0x2015)
</dt> <dt>



El servicio de directorio solo puede realizar la operación solicitada en un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ON_RDN"></span><span id="error_ds_cant_on_rdn"></span>**ERROR \_ DS \_ CANT \_ ON \_ RDN**
</dt> <dd> <dl> <dt>

8214 (0x2016)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada en el atributo RDN de un objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_OBJ_CLASS"></span><span id="error_ds_cant_mod_obj_class"></span>**ERROR \_ DS \_ CANT \_ MOD \_ OBJ \_ (CLASE)**
</dt> <dd> <dl> <dt>

8215 (0x2017)
</dt> <dt>



El servicio de directorio detectó un intento de modificar la clase de objeto de un objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOM_MOVE_ERROR"></span><span id="error_ds_cross_dom_move_error"></span>**ERROR \_ DS \_ CROSS \_ DOM \_ MOVE \_ ERROR**
</dt> <dd> <dl> <dt>

8216 (0x2018)
</dt> <dt>



No se pudo realizar la operación de movimiento entre dominios solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_NOT_AVAILABLE"></span><span id="error_ds_gc_not_available"></span>**ERROR \_ DS \_ GC \_ NOT \_ AVAILABLE**
</dt> <dd> <dl> <dt>

8217 (0x2019)
</dt> <dt>



No se puede ponerse en contacto con el servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHARED_POLICY"></span><span id="error_shared_policy"></span>**ERROR \_ SHARED \_ POLICY**
</dt> <dd> <dl> <dt>

8218 (0x201A)
</dt> <dt>



El objeto de directiva se comparte y solo se puede modificar en la raíz.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_OBJECT_NOT_FOUND"></span><span id="error_policy_object_not_found"></span>**NO SE \_ ENCONTRÓ EL OBJETO DE DIRECTIVA DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8219 (0x201B)
</dt> <dt>



El objeto de directiva no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_POLICY_ONLY_IN_DS"></span><span id="error_policy_only_in_ds"></span>**DIRECTIVA \_ DE ERRORES SOLO EN \_ \_ \_ DS**
</dt> <dd> <dl> <dt>

8220 (0x201C)
</dt> <dt>



La información de directiva solicitada solo está en el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROMOTION_ACTIVE"></span><span id="error_promotion_active"></span>**PROMOCIÓN \_ DE ERRORES \_ ACTIVA**
</dt> <dd> <dl> <dt>

8221 (0x201D)
</dt> <dt>



Una promoción de controlador de dominio está activa actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PROMOTION_ACTIVE"></span><span id="error_no_promotion_active"></span>**ERROR \_ NO \_ PROMOTION \_ ACTIVE**
</dt> <dd> <dl> <dt>

8222 (0x201E)
</dt> <dt>



Una promoción de controlador de dominio no está activa actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OPERATIONS_ERROR"></span><span id="error_ds_operations_error"></span>**ERROR \_ DS \_ OPERATIONS \_ ERROR**
</dt> <dd> <dl> <dt>

8224 (0x2020)
</dt> <dt>



Se produjo un error de operaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PROTOCOL_ERROR"></span><span id="error_ds_protocol_error"></span>**ERROR \_ DS \_ PROTOCOL \_ ERROR**
</dt> <dd> <dl> <dt>

8225 (0x2021)
</dt> <dt>



Se ha producido un error de protocolo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TIMELIMIT_EXCEEDED"></span><span id="error_ds_timelimit_exceeded"></span>**ERROR \_ DS \_ TIMELIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8226 (0x2022)
</dt> <dt>



Se superó el límite de tiempo para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SIZELIMIT_EXCEEDED"></span><span id="error_ds_sizelimit_exceeded"></span>**ERROR \_ DS \_ SIZELIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8227 (0x2023)
</dt> <dt>



Se superó el límite de tamaño de esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADMIN_LIMIT_EXCEEDED"></span><span id="error_ds_admin_limit_exceeded"></span>**ERROR \_ DS \_ ADMIN \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8228 (0x2024)
</dt> <dt>



Se superó el límite administrativo para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_FALSE"></span><span id="error_ds_compare_false"></span>**ERROR \_ DS \_ COMPARE \_ FALSE**
</dt> <dd> <dl> <dt>

8229 (0x2025)
</dt> <dt>



La respuesta de comparación era false.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COMPARE_TRUE"></span><span id="error_ds_compare_true"></span>**ERROR \_ DS \_ COMPARE \_ TRUE**
</dt> <dd> <dl> <dt>

8230 (0x2026)
</dt> <dt>



La respuesta de comparación era verdadera.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_METHOD_NOT_SUPPORTED"></span><span id="error_ds_auth_method_not_supported"></span>**ERROR \_ NO SE ADMITE EL MÉTODO DE \_ \_ AUTENTICACIÓN \_ DE \_ DS**
</dt> <dd> <dl> <dt>

8231 (0x2027)
</dt> <dt>



El servidor no admite el método de autenticación solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRONG_AUTH_REQUIRED"></span><span id="error_ds_strong_auth_required"></span>**ERROR \_ DS \_ STRONG \_ AUTH \_ REQUIRED**
</dt> <dd> <dl> <dt>

8232 (0x2028)
</dt> <dt>



Se requiere un método de autenticación más seguro para este servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_AUTH"></span><span id="error_ds_inappropriate_auth"></span>**ERROR \_ DS \_ \_ AUTH INADECUADO**
</dt> <dd> <dl> <dt>

8233 (0x2029)
</dt> <dt>



Autenticación inapropiada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTH_UNKNOWN"></span><span id="error_ds_auth_unknown"></span>**ERROR \_ DS \_ AUTH \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8234 (0x202A)
</dt> <dt>



Se desconoce el mecanismo de autenticación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL"></span><span id="error_ds_referral"></span>**REFERENCIA \_ DE DS \_ DE ERROR**
</dt> <dd> <dl> <dt>

8235 (0x202B)
</dt> <dt>



El servidor ha devuelto una referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNAVAILABLE_CRIT_EXTENSION"></span><span id="error_ds_unavailable_crit_extension"></span>**ERROR \_ DS \_ NO DISPONIBLE EXTENSIÓN \_ CRIT \_**
</dt> <dd> <dl> <dt>

8236 (0x202C)
</dt> <dt>



El servidor no admite la extensión crítica solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIDENTIALITY_REQUIRED"></span><span id="error_ds_confidentiality_required"></span>**ERROR \_ DS \_ CONFIDENTIALITY \_ REQUIRED**
</dt> <dd> <dl> <dt>

8237 (0x202D)
</dt> <dt>



Esta solicitud requiere una conexión segura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INAPPROPRIATE_MATCHING"></span><span id="error_ds_inappropriate_matching"></span>**ERROR \_ DS \_ COINCIDENCIA \_ INAPROPIADA**
</dt> <dd> <dl> <dt>

8238 (0x202E)
</dt> <dt>



Coincidencia inapropiada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRAINT_VIOLATION"></span><span id="error_ds_constraint_violation"></span>**ERROR \_ DS \_ CONSTRAINT \_ VIOLATION**
</dt> <dd> <dl> <dt>

8239 (0x202F)
</dt> <dt>



Se produjo una infracción de restricción.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SUCH_OBJECT"></span><span id="error_ds_no_such_object"></span>**ERROR \_ DS \_ NO \_ SUCH \_ OBJECT**
</dt> <dd> <dl> <dt>

8240 (0x2030)
</dt> <dt>



No existe tal objeto en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_PROBLEM"></span><span id="error_ds_alias_problem"></span>**ERROR \_ DS \_ ALIAS \_ PROBLEM**
</dt> <dd> <dl> <dt>

8241 (0x2031)
</dt> <dt>



Hay un problema de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DN_SYNTAX"></span><span id="error_ds_invalid_dn_syntax"></span>**ERROR \_ DS \_ INVALID \_ DN \_ SYNTAX**
</dt> <dd> <dl> <dt>

8242 (0x2032)
</dt> <dt>



Se ha especificado una sintaxis dn no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_IS_LEAF"></span><span id="error_ds_is_leaf"></span>**ERROR \_ DS \_ IS \_ LEAF**
</dt> <dd> <dl> <dt>

8243 (0x2033)
</dt> <dt>



El objeto es un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_DEREF_PROBLEM"></span><span id="error_ds_alias_deref_problem"></span>**ERROR \_ DS \_ ALIAS \_ DEREF \_ PROBLEM**
</dt> <dd> <dl> <dt>

8244 (0x2034)
</dt> <dt>



Hay un problema de desreferenciación de alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNWILLING_TO_PERFORM"></span><span id="error_ds_unwilling_to_perform"></span>**ERROR \_ DS \_ NO ESTÁ DISPUESTO \_ A \_ REALIZAR**
</dt> <dd> <dl> <dt>

8245 (0x2035)
</dt> <dt>



El servidor no está dispuesto a procesar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOOP_DETECT"></span><span id="error_ds_loop_detect"></span>**ERROR \_ DS \_ LOOP \_ DETECT**
</dt> <dd> <dl> <dt>

8246 (0x2036)
</dt> <dt>



Se ha detectado un bucle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_VIOLATION"></span><span id="error_ds_naming_violation"></span>**ERROR \_ DS \_ NAMING \_ VIOLATION**
</dt> <dd> <dl> <dt>

8247 (0x2037)
</dt> <dt>



Hay una infracción de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_RESULTS_TOO_LARGE"></span><span id="error_ds_object_results_too_large"></span>**ERROR \_ DS \_ OBJECT RESULTS TOO LARGE (RESULTADOS DE OBJETOS DS DE ERROR \_ DEMASIADO \_ \_ GRANDES)**
</dt> <dd> <dl> <dt>

8248 (0x2038)
</dt> <dt>



El conjunto de resultados es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AFFECTS_MULTIPLE_DSAS"></span><span id="error_ds_affects_multiple_dsas"></span>**EL \_ ERROR DS \_ AFECTA A VARIAS \_ \_ DSAS**
</dt> <dd> <dl> <dt>

8249 (0x2039)
</dt> <dt>



La operación afecta a varios DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SERVER_DOWN"></span><span id="error_ds_server_down"></span>**ERROR \_ DS \_ SERVER \_ DOWN**
</dt> <dd> <dl> <dt>

8250 (0x203A)
</dt> <dt>



el servidor no es funcional.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_ERROR"></span><span id="error_ds_local_error"></span>**ERROR \_ DS \_ LOCAL \_ ERROR**
</dt> <dd> <dl> <dt>

8251 (0x203B)
</dt> <dt>



Se ha producido un error local.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ENCODING_ERROR"></span><span id="error_ds_encoding_error"></span>**ERROR \_ DS \_ ENCODING \_ ERROR**
</dt> <dd> <dl> <dt>

8252 (0x203C)
</dt> <dt>



Se ha producido un error de codificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DECODING_ERROR"></span><span id="error_ds_decoding_error"></span>**ERROR \_ DS \_ DECODING \_ ERROR**
</dt> <dd> <dl> <dt>

8253 (0x203D)
</dt> <dt>



Se ha producido un error de decodificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_UNKNOWN"></span><span id="error_ds_filter_unknown"></span>**ERROR \_ DS \_ FILTER \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8254 (0x203E)
</dt> <dt>



No se puede reconocer el filtro de búsqueda.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARAM_ERROR"></span><span id="error_ds_param_error"></span>**ERROR \_ DS \_ PARAM \_ ERROR**
</dt> <dd> <dl> <dt>

8255 (0x203F)
</dt> <dt>



Uno o varios parámetros no son ilegales.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED"></span><span id="error_ds_not_supported"></span>**ERROR \_ DS \_ NO \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

8256 (0x2040)
</dt> <dt>



No se admite el método especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RESULTS_RETURNED"></span><span id="error_ds_no_results_returned"></span>**ERROR \_ DS \_ NO SE \_ \_ DEVUELVEN RESULTADOS**
</dt> <dd> <dl> <dt>

8257 (0x2041)
</dt> <dt>



No se devolvieron resultados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONTROL_NOT_FOUND"></span><span id="error_ds_control_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL CONTROL DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8258 (0x2042)
</dt> <dt>



El servidor no admite el control especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLIENT_LOOP"></span><span id="error_ds_client_loop"></span>**ERROR \_ DS \_ CLIENT \_ LOOP**
</dt> <dd> <dl> <dt>

8259 (0x2043)
</dt> <dt>



El cliente detectó un bucle de referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFERRAL_LIMIT_EXCEEDED"></span><span id="error_ds_referral_limit_exceeded"></span>**ERROR \_ DS \_ REFERRAL \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8260 (0x2044)
</dt> <dt>



Se superó el límite de referencia preestablecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SORT_CONTROL_MISSING"></span><span id="error_ds_sort_control_missing"></span>**ERROR \_ DS \_ SORT \_ CONTROL \_ MISSING**
</dt> <dd> <dl> <dt>

8261 (0x2045)
</dt> <dt>



La búsqueda requiere un control SORT.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OFFSET_RANGE_ERROR"></span><span id="error_ds_offset_range_error"></span>**ERROR \_ DS \_ OFFSET \_ RANGE \_ ERROR**
</dt> <dd> <dl> <dt>

8262 (0x2046)
</dt> <dt>



Los resultados de la búsqueda superan el intervalo de desplazamiento especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RIDMGR_DISABLED"></span><span id="error_ds_ridmgr_disabled"></span>**ERROR \_ DS \_ RIDMGR \_ DESHABILITADO**
</dt> <dd> <dl> <dt>

8263 (0x2047)
</dt> <dt>



El servicio de directorio detectó que el subsistema que asigna identificadores relativos está deshabilitado. Esto puede ocurrir como un mecanismo de protección cuando el sistema determina que se ha agotado una parte significativa de los identificadores relativos (RID). Consulte los <https://go.microsoft.com/fwlink/p/?linkid=228610> pasos de diagnóstico recomendados y el procedimiento para volver a habilitar la creación de cuentas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_MUST_BE_NC"></span><span id="error_ds_root_must_be_nc"></span>**LA \_ RAÍZ DE DS DE ERROR \_ DEBE SER \_ \_ \_ NC**
</dt> <dd> <dl> <dt>

8301 (0x206D)
</dt> <dt>



El objeto raíz debe ser el responsable de un contexto de nomenclatura. El objeto raíz no puede tener un elemento primario con instancias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ADD_REPLICA_INHIBITED"></span><span id="error_ds_add_replica_inhibited"></span>**ERROR \_ DS \_ AGREGAR RÉPLICA \_ \_ INHIBIDA**
</dt> <dd> <dl> <dt>

8302 (0x206E)
</dt> <dt>



No se puede realizar la operación de agregar réplica. El contexto de nomenclatura debe poder escribirse para crear la réplica.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_IN_SCHEMA"></span><span id="error_ds_att_not_def_in_schema"></span>**ERROR \_ DS \_ ATT \_ NOT \_ DEF \_ IN \_ SCHEMA**
</dt> <dd> <dl> <dt>

8303 (0x206F)
</dt> <dt>



Se ha producido una referencia a un atributo que no está definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAX_OBJ_SIZE_EXCEEDED"></span><span id="error_ds_max_obj_size_exceeded"></span>**ERROR \_ DS \_ MAX \_ OBJ \_ SIZE \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8304 (0x2070)
</dt> <dt>



Se ha superado el tamaño máximo de un objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_STRING_NAME_EXISTS"></span><span id="error_ds_obj_string_name_exists"></span>**ERROR \_ DS \_ OBJ \_ STRING \_ NAME \_ EXISTS**
</dt> <dd> <dl> <dt>

8305 (0x2071)
</dt> <dt>



Se intentó agregar un objeto al directorio con un nombre que ya está en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_RDN_DEFINED_IN_SCHEMA"></span><span id="error_ds_no_rdn_defined_in_schema"></span>**ERROR \_ DS \_ NO \_ RDN DEFINIDO EN \_ \_ SCHEMA \_**
</dt> <dd> <dl> <dt>

8306 (0x2072)
</dt> <dt>



Se intentó agregar un objeto de una clase que no tiene un RDN definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RDN_DOESNT_MATCH_SCHEMA"></span><span id="error_ds_rdn_doesnt_match_schema"></span>**ERROR \_ DS \_ RDN \_ NO COINCIDE CON \_ EL \_ ESQUEMA**
</dt> <dd> <dl> <dt>

8307 (0x2073)
</dt> <dt>



Se intentó agregar un objeto mediante un RDN que no es el RDN definido en el esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REQUESTED_ATTS_FOUND"></span><span id="error_ds_no_requested_atts_found"></span>**ERROR \_ DS \_ NO SE ENCONTRÓ \_ NINGÚN \_ ATTS \_ SOLICITADO**
</dt> <dd> <dl> <dt>

8308 (0x2074)
</dt> <dt>



No se encontró ninguno de los atributos solicitados en los objetos .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_USER_BUFFER_TO_SMALL"></span><span id="error_ds_user_buffer_to_small"></span>**ERROR \_ DS \_ USER \_ BUFFER \_ TO \_ SMALL**
</dt> <dd> <dl> <dt>

8309 (0x2075)
</dt> <dt>



El búfer de usuario es demasiado pequeño.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_IS_NOT_ON_OBJ"></span><span id="error_ds_att_is_not_on_obj"></span>**ERROR \_ DS \_ ATT \_ IS \_ NOT \_ ON \_ OBJ**
</dt> <dd> <dl> <dt>

8310 (0x2076)
</dt> <dt>



El atributo especificado en la operación no está presente en el objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_MOD_OPERATION"></span><span id="error_ds_illegal_mod_operation"></span>**ERROR \_ DS \_ ILLEGAL \_ MOD \_ OPERATION**
</dt> <dd> <dl> <dt>

8311 (0x2077)
</dt> <dt>



Operación de modificación no ilegal. No se permite algún aspecto de la modificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_TOO_LARGE"></span><span id="error_ds_obj_too_large"></span>**ERROR \_ DS \_ OBJ \_ TOO \_ LARGE**
</dt> <dd> <dl> <dt>

8312 (0x2078)
</dt> <dt>



El objeto especificado es demasiado grande.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_INSTANCE_TYPE"></span><span id="error_ds_bad_instance_type"></span>**TIPO \_ DE INSTANCIA DE ERROR DS \_ \_ BAD \_**
</dt> <dd> <dl> <dt>

8313 (0x2079)
</dt> <dt>



El tipo de instancia especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MASTERDSA_REQUIRED"></span><span id="error_ds_masterdsa_required"></span>**ERROR \_ DS \_ MASTERDSA \_ REQUIRED**
</dt> <dd> <dl> <dt>

8314 (0x207A)
</dt> <dt>



La operación debe realizarse en un DSA maestro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_CLASS_REQUIRED"></span><span id="error_ds_object_class_required"></span>**SE \_ REQUIERE LA CLASE DE OBJETO DS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8315 (0x207B)
</dt> <dt>



Se debe especificar el atributo de clase de objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_REQUIRED_ATT"></span><span id="error_ds_missing_required_att"></span>**ERROR \_ DS \_ MISSING \_ REQUIRED \_ ATT**
</dt> <dd> <dl> <dt>

8316 (0x207C)
</dt> <dt>



Falta un atributo necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_NOT_DEF_FOR_CLASS"></span><span id="error_ds_att_not_def_for_class"></span>**ERROR \_ DS \_ ATT \_ NOT \_ DEF \_ FOR \_ CLASS**
</dt> <dd> <dl> <dt>

8317 (0x207D)
</dt> <dt>



Se intentó modificar un objeto para incluir un atributo que no es legal para su clase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_ALREADY_EXISTS"></span><span id="error_ds_att_already_exists"></span>**ERROR \_ DS \_ ATT \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

8318 (0x207E)
</dt> <dt>



El atributo especificado ya está presente en el objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_ATT_VALUES"></span><span id="error_ds_cant_add_att_values"></span>**ERROR \_ DS \_ CANT \_ ADD \_ ATT \_ VALUES**
</dt> <dd> <dl> <dt>

8320 (0x2080)
</dt> <dt>



El atributo especificado no está presente o no tiene ningún valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_VALUE_CONSTRAINT"></span><span id="error_ds_single_value_constraint"></span>**ERROR \_ DS \_ SINGLE \_ VALUE \_ CONSTRAINT**
</dt> <dd> <dl> <dt>

8321 (0x2081)
</dt> <dt>



Se especificaron varios valores para un atributo que solo puede tener un valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RANGE_CONSTRAINT"></span><span id="error_ds_range_constraint"></span>**ERROR \_ DS \_ RANGE \_ CONSTRAINT**
</dt> <dd> <dl> <dt>

8322 (0x2082)
</dt> <dt>



Un valor para el atributo no estaba en el intervalo de valores aceptable.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_VAL_ALREADY_EXISTS"></span><span id="error_ds_att_val_already_exists"></span>**ERROR \_ DS \_ ATT \_ VAL YA \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

8323 (0x2083)
</dt> <dt>



El valor especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT"></span><span id="error_ds_cant_rem_missing_att"></span>**ERROR \_ DS \_ CANT \_ REM \_ MISSING \_ ATT**
</dt> <dd> <dl> <dt>

8324 (0x2084)
</dt> <dt>



No se puede quitar el atributo porque no está presente en el objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REM_MISSING_ATT_VAL"></span><span id="error_ds_cant_rem_missing_att_val"></span>**ERROR \_ DS \_ CANT \_ REM \_ MISSING \_ ATT \_ VAL**
</dt> <dd> <dl> <dt>

8325 (0x2085)
</dt> <dt>



No se puede quitar el valor del atributo porque no está presente en el objeto .


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_CANT_BE_SUBREF"></span><span id="error_ds_root_cant_be_subref"></span>**ERROR \_ DS \_ ROOT \_ CANT \_ BE \_ SUBREF**
</dt> <dd> <dl> <dt>

8326 (0x2086)
</dt> <dt>



El objeto raíz especificado no puede ser una subreferencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINING"></span><span id="error_ds_no_chaining"></span>**ERROR \_ DS \_ NO \_ ENCADENAMIENTO**
</dt> <dd> <dl> <dt>

8327 (0x2087)
</dt> <dt>



No se permite el encadenamiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHAINED_EVAL"></span><span id="error_ds_no_chained_eval"></span>**ERROR \_ DS \_ NO \_ CHAINED \_ EVAL**
</dt> <dd> <dl> <dt>

8328 (0x2088)
</dt> <dt>



No se permite la evaluación encadenada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PARENT_OBJECT"></span><span id="error_ds_no_parent_object"></span>**ERROR \_ DS \_ NO \_ PARENT \_ OBJECT**
</dt> <dd> <dl> <dt>

8329 (0x2089)
</dt> <dt>



No se puede realizar la operación porque el principal del objeto no se ha instanciado o se ha eliminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PARENT_IS_AN_ALIAS"></span><span id="error_ds_parent_is_an_alias"></span>**EL \_ ELEMENTO PRIMARIO DS DE ERROR \_ ES UN \_ \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

8330 (0x208A)
</dt> <dt>



No se permite tener un elemento primario que sea un alias. Los alias son objetos hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MIX_MASTER_AND_REPS"></span><span id="error_ds_cant_mix_master_and_reps"></span>**ERROR \_ DS \_ CANT \_ MIX \_ MASTER \_ AND \_ REPS**
</dt> <dd> <dl> <dt>

8331 (0x208B)
</dt> <dt>



El objeto y el elemento primario deben ser del mismo tipo, ya sea maestros o ambas réplicas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CHILDREN_EXIST"></span><span id="error_ds_children_exist"></span>**ERROR \_ DS \_ CHILDREN \_ EXIST**
</dt> <dd> <dl> <dt>

8332 (0x208C)
</dt> <dt>



No se puede realizar la operación porque existen objetos secundarios. Esta operación solo se puede realizar en un objeto hoja.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_NOT_FOUND"></span><span id="error_ds_obj_not_found"></span>**ERROR \_ DS \_ OBJ \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

8333 (0x208D)
</dt> <dt>



No se encontró el objeto de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIASED_OBJ_MISSING"></span><span id="error_ds_aliased_obj_missing"></span>**ERROR \_ DS \_ ALIASED \_ OBJ \_ MISSING**
</dt> <dd> <dl> <dt>

8334 (0x208E)
</dt> <dt>



Falta el objeto con alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_NAME_SYNTAX"></span><span id="error_ds_bad_name_syntax"></span>**SINTAXIS \_ DE NOMBRE NO ES \_ \_ CORRECTA DE DS \_**
</dt> <dd> <dl> <dt>

8335 (0x208F)
</dt> <dt>



El nombre del objeto tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ALIAS_POINTS_TO_ALIAS"></span><span id="error_ds_alias_points_to_alias"></span>**EL ALIAS \_ DS \_ DE ERROR APUNTA \_ A \_ \_ ALIAS**
</dt> <dd> <dl> <dt>

8336 (0x2090)
</dt> <dt>



No se permite que un alias haga referencia a otro alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEREF_ALIAS"></span><span id="error_ds_cant_deref_alias"></span>**ERROR \_ DS \_ CANT \_ DEREF \_ ALIAS**
</dt> <dd> <dl> <dt>

8337 (0x2091)
</dt> <dt>



No se puede desreferenciar el alias.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_SCOPE"></span><span id="error_ds_out_of_scope"></span>**ERROR \_ DS \_ FUERA DEL \_ \_ ÁMBITO**
</dt> <dd> <dl> <dt>

8338 (0x2092)
</dt> <dt>



La operación está fuera del ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJECT_BEING_REMOVED"></span><span id="error_ds_object_being_removed"></span>**ERROR \_ DS \_ OBJECT \_ BEING \_ REMOVED**
</dt> <dd> <dl> <dt>

8339 (0x2093)
</dt> <dt>



La operación no puede continuar porque el objeto está en proceso de quitarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE_DSA_OBJ"></span><span id="error_ds_cant_delete_dsa_obj"></span>**ERROR \_ DS \_ CANT \_ DELETE \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8340 (0x2094)
</dt> <dt>



No se puede eliminar el objeto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GENERIC_ERROR"></span><span id="error_ds_generic_error"></span>**ERROR \_ DS \_ GENERIC \_ ERROR**
</dt> <dd> <dl> <dt>

8341 (0x2095)
</dt> <dt>



Se ha producido un error de servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DSA_MUST_BE_INT_MASTER"></span><span id="error_ds_dsa_must_be_int_master"></span>**ERROR \_ DS \_ DSA \_ DEBE SER INT \_ \_ \_ MASTER**
</dt> <dd> <dl> <dt>

8342 (0x2096)
</dt> <dt>



La operación solo se puede realizar en un objeto DSA maestro interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_NOT_DSA"></span><span id="error_ds_class_not_dsa"></span>**ERROR \_ DS \_ CLASS \_ NOT \_ DSA**
</dt> <dd> <dl> <dt>

8343 (0x2097)
</dt> <dt>



El objeto debe ser de la clase DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFF_ACCESS_RIGHTS"></span><span id="error_ds_insuff_access_rights"></span>**ERROR \_ DS \_ INSUFF \_ ACCESS \_ RIGHTS**
</dt> <dd> <dl> <dt>

8344 (0x2098)
</dt> <dt>



Derechos de acceso insuficientes para realizar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_SUPERIOR"></span><span id="error_ds_illegal_superior"></span>**ERROR \_ DS \_ ILLEGAL \_ SUPERIOR**
</dt> <dd> <dl> <dt>

8345 (0x2099)
</dt> <dt>



No se puede agregar el objeto porque el elemento primario no está en la lista de posibles superiores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATTRIBUTE_OWNED_BY_SAM"></span><span id="error_ds_attribute_owned_by_sam"></span>**ERROR \_ DS ATTRIBUTE OWNED BY SAM (ATRIBUTO DS \_ DE ERROR PROPIEDAD DE \_ \_ \_ SAM)**
</dt> <dd> <dl> <dt>

8346 (0x209A)
</dt> <dt>



No se permite el acceso al atributo porque es propiedad del Administrador de cuentas de seguridad (SAM).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_MANY_PARTS"></span><span id="error_ds_name_too_many_parts"></span>**ERROR \_ DS \_ NOMBRE \_ \_ DEMASIADAS \_ PARTES**
</dt> <dd> <dl> <dt>

8347 (0x209B)
</dt> <dt>



El nombre tiene demasiadas partes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TOO_LONG"></span><span id="error_ds_name_too_long"></span>**ERROR \_ DS \_ NAME \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

8348 (0x209C)
</dt> <dt>



El nombre es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_VALUE_TOO_LONG"></span><span id="error_ds_name_value_too_long"></span>**VALOR \_ DE NOMBRE DS DE ERROR \_ DEMASIADO \_ \_ \_ LARGO**
</dt> <dd> <dl> <dt>

8349 (0x209D)
</dt> <dt>



El valor de nombre es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_UNPARSEABLE"></span><span id="error_ds_name_unparseable"></span>**ERROR \_ DS \_ NAME \_ UNPARSEABLE**
</dt> <dd> <dl> <dt>

8350 (0x209E)
</dt> <dt>



El servicio de directorio encontró un error al analizar un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_TYPE_UNKNOWN"></span><span id="error_ds_name_type_unknown"></span>**ERROR \_ DS \_ NAME \_ TYPE \_ UNKNOWN**
</dt> <dd> <dl> <dt>

8351 (0x209F)
</dt> <dt>



El servicio de directorio no puede obtener el tipo de atributo de un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AN_OBJECT"></span><span id="error_ds_not_an_object"></span>**ERROR \_ DS \_ NO ES UN \_ \_ OBJETO**
</dt> <dd> <dl> <dt>

8352 (0x20A0)
</dt> <dt>



El nombre no identifica un objeto; el nombre identifica un fantasma.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_TOO_SHORT"></span><span id="error_ds_sec_desc_too_short"></span>**ERROR \_ DS \_ SEC \_ DESC \_ TOO \_ SHORT**
</dt> <dd> <dl> <dt>

8353 (0x20A1)
</dt> <dt>



El descriptor de seguridad es demasiado corto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEC_DESC_INVALID"></span><span id="error_ds_sec_desc_invalid"></span>**ERROR \_ DS \_ SEC \_ DESC \_ INVALID**
</dt> <dd> <dl> <dt>

8354 (0x20A2)
</dt> <dt>



El descriptor de seguridad no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_DELETED_NAME"></span><span id="error_ds_no_deleted_name"></span>**ERROR \_ DS \_ NO \_ DELETED \_ NAME**
</dt> <dd> <dl> <dt>

8355 (0x20A3)
</dt> <dt>



No se pudo crear el nombre para el objeto eliminado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBREF_MUST_HAVE_PARENT"></span><span id="error_ds_subref_must_have_parent"></span>**LA \_ \_ SUBREFERENCIA DS DE ERROR DEBE TENER UN ELEMENTO \_ \_ \_ PRIMARIO**
</dt> <dd> <dl> <dt>

8356 (0x20A4)
</dt> <dt>



Debe existir el elemento primario de una nueva subreferencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MUST_BE_NC"></span><span id="error_ds_ncname_must_be_nc"></span>**ERROR \_ DS \_ NCNAME \_ DEBE SER \_ \_ NC**
</dt> <dd> <dl> <dt>

8357 (0x20A5)
</dt> <dt>



El objeto debe ser un contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_SYSTEM_ONLY"></span><span id="error_ds_cant_add_system_only"></span>**ERROR \_ DS \_ CANT \_ ADD \_ SYSTEM \_ ONLY**
</dt> <dd> <dl> <dt>

8358 (0x20A6)
</dt> <dt>



No se permite agregar un atributo que sea propiedad del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CLASS_MUST_BE_CONCRETE"></span><span id="error_ds_class_must_be_concrete"></span>**LA \_ CLASE DS \_ DE ERROR DEBE SER \_ \_ \_ CONCRETA**
</dt> <dd> <dl> <dt>

8359 (0x20A7)
</dt> <dt>



La clase del objeto debe ser estructural; No se pueden crear instancias de una clase abstracta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_DMD"></span><span id="error_ds_invalid_dmd"></span>**ERROR \_ DS \_ INVALID \_ DMD**
</dt> <dd> <dl> <dt>

8360 (0x20A8)
</dt> <dt>



No se encontró el objeto de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_GUID_EXISTS"></span><span id="error_ds_obj_guid_exists"></span>**ERROR \_ DS \_ OBJ \_ GUID \_ EXISTS**
</dt> <dd> <dl> <dt>

8361 (0x20A9)
</dt> <dt>



Ya existe un objeto local con este GUID (activo o no activo).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_ON_BACKLINK"></span><span id="error_ds_not_on_backlink"></span>**ERROR \_ DS \_ NOT \_ ON \_ BACKLINK**
</dt> <dd> <dl> <dt>

8362 (0x20AA)
</dt> <dt>



La operación no se puede realizar en un vínculo hacia atrás.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CROSSREF_FOR_NC"></span><span id="error_ds_no_crossref_for_nc"></span>**ERROR \_ DS \_ NO \_ CROSSREF \_ FOR \_ NC**
</dt> <dd> <dl> <dt>

8363 (0x20AB)
</dt> <dt>



No se encontró la referencia cruzada para el contexto de nomenclatura especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SHUTTING_DOWN"></span><span id="error_ds_shutting_down"></span>**ERROR \_ DS \_ SHUTTING \_ DOWN**
</dt> <dd> <dl> <dt>

8364 (0x20AC)
</dt> <dt>



No se pudo realizar la operación porque el servicio de directorio se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_OPERATION"></span><span id="error_ds_unknown_operation"></span>**ERROR \_ DS \_ OPERACIÓN \_ DESCONOCIDA**
</dt> <dd> <dl> <dt>

8365 (0x20AD)
</dt> <dt>



La solicitud del servicio de directorio no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_ROLE_OWNER"></span><span id="error_ds_invalid_role_owner"></span>**ERROR \_ DS \_ PROPIETARIO DE ROL \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8366 (0x20AE)
</dt> <dt>



No se pudo leer el atributo de propietario del rol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_CONTACT_FSMO"></span><span id="error_ds_couldnt_contact_fsmo"></span>**ERROR \_ DS \_ COULDNT \_ CONTACT \_ FSMO**
</dt> <dd> <dl> <dt>

8367 (0x20AF)
</dt> <dt>



Error en la operación FSMO solicitada. No se puede poner en contacto con el titular de FSMO actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_NC_DN_RENAME"></span><span id="error_ds_cross_nc_dn_rename"></span>**ERROR \_ DS \_ CROSS \_ NC \_ DN \_ RENAME**
</dt> <dd> <dl> <dt>

8368 (0x20B0)
</dt> <dt>



No se permite la modificación de un DN en un contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_SYSTEM_ONLY"></span><span id="error_ds_cant_mod_system_only"></span>**ERROR \_ DS \_ CANT \_ MOD \_ SYSTEM \_ ONLY**
</dt> <dd> <dl> <dt>

8369 (0x20B1)
</dt> <dt>



El atributo no se puede modificar porque es propiedad del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICATOR_ONLY"></span><span id="error_ds_replicator_only"></span>**ERROR \_ SOLO \_ REPLICADOR DS \_**
</dt> <dd> <dl> <dt>

8370 (0x20B2)
</dt> <dt>



Solo el replicador puede realizar esta función.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_DEFINED"></span><span id="error_ds_obj_class_not_defined"></span>**ERROR \_ DS \_ OBJ \_ CLASS \_ NOT \_ DEFINED**
</dt> <dd> <dl> <dt>

8371 (0x20B3)
</dt> <dt>



La clase especificada no está definida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OBJ_CLASS_NOT_SUBCLASS"></span><span id="error_ds_obj_class_not_subclass"></span>**ERROR \_ DS \_ OBJ \_ CLASS \_ NOT \_ SUBCLASS**
</dt> <dd> <dl> <dt>

8372 (0x20B4)
</dt> <dt>



La clase especificada no es una subclase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_REFERENCE_INVALID"></span><span id="error_ds_name_reference_invalid"></span>**ERROR \_ DS \_ NAME \_ REFERENCE \_ INVALID**
</dt> <dd> <dl> <dt>

8373 (0x20B5)
</dt> <dt>



La referencia de nombre no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_EXISTS"></span><span id="error_ds_cross_ref_exists"></span>**ERROR \_ DS \_ CROSS \_ REF \_ EXISTS**
</dt> <dd> <dl> <dt>

8374 (0x20B6)
</dt> <dt>



Ya existe una referencia cruzada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEL_MASTER_CROSSREF"></span><span id="error_ds_cant_del_master_crossref"></span>**ERROR \_ DS \_ CANT \_ DEL \_ MASTER \_ CROSSREF**
</dt> <dd> <dl> <dt>

8375 (0x20B7)
</dt> <dt>



No se permite eliminar una referencia cruzada maestra.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUBTREE_NOTIFY_NOT_NC_HEAD"></span><span id="error_ds_subtree_notify_not_nc_head"></span>**ERROR \_ DS \_ SUBTREE \_ NOTIFY \_ NOT \_ NC \_ HEAD**
</dt> <dd> <dl> <dt>

8376 (0x20B8)
</dt> <dt>



Las notificaciones de subárbol solo se admiten en los jefes de NC.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOTIFY_FILTER_TOO_COMPLEX"></span><span id="error_ds_notify_filter_too_complex"></span>**ERROR \_ DS \_ NOTIFY \_ FILTER \_ TOO \_ COMPLEX**
</dt> <dd> <dl> <dt>

8377 (0x20B9)
</dt> <dt>



El filtro de notificación es demasiado complejo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_RDN"></span><span id="error_ds_dup_rdn"></span>**ERROR \_ DS \_ DUP \_ RDN**
</dt> <dd> <dl> <dt>

8378 (0x20BA)
</dt> <dt>



Error de actualización del esquema: RDN duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_OID"></span><span id="error_ds_dup_oid"></span>**ERROR \_ DS \_ DUP \_ OID**
</dt> <dd> <dl> <dt>

8379 (0x20BB)
</dt> <dt>



Error en la actualización del esquema: OID duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MAPI_ID"></span><span id="error_ds_dup_mapi_id"></span>**ERROR \_ DS \_ DUP \_ ID. DE LA MARCA DE IDENTIFICACIÓN DE LA CONTRASEÑA \_**
</dt> <dd> <dl> <dt>

8380 (0x20BC)
</dt> <dt>



Error en la actualización del esquema: identificador DE LAN duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_SCHEMA_ID_GUID"></span><span id="error_ds_dup_schema_id_guid"></span>**ERROR \_ DS \_ DUP \_ SCHEMA \_ ID \_ GUID**
</dt> <dd> <dl> <dt>

8381 (0x20BD)
</dt> <dt>



Error en la actualización del esquema: GUID de identificador de esquema duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LDAP_DISPLAY_NAME"></span><span id="error_ds_dup_ldap_display_name"></span>**ERROR \_ DS \_ DUP \_ LDAP \_ DISPLAY \_ NAME**
</dt> <dd> <dl> <dt>

8382 (0x20BE)
</dt> <dt>



Error en la actualización del esquema: nombre para mostrar ldap duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SEMANTIC_ATT_TEST"></span><span id="error_ds_semantic_att_test"></span>**ERROR \_ DS \_ SEMANTIC \_ ATT \_ TEST**
</dt> <dd> <dl> <dt>

8383 (0x20BF)
</dt> <dt>



Error en la actualización del esquema: intervalo menor que el intervalo superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SYNTAX_MISMATCH"></span><span id="error_ds_syntax_mismatch"></span>**ERROR \_ DS \_ SYNTAX \_ MISMATCH**
</dt> <dd> <dl> <dt>

8384 (0x20C0)
</dt> <dt>



Error en la actualización del esquema: no coincide la sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MUST_HAVE"></span><span id="error_ds_exists_in_must_have"></span>**EL \_ ERROR DS \_ EXISTE EN \_ DEBE \_ \_ TENER**
</dt> <dd> <dl> <dt>

8385 (0x20C1)
</dt> <dt>



Error de eliminación del esquema: el atributo se usa en must-contain.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_MAY_HAVE"></span><span id="error_ds_exists_in_may_have"></span>**EL \_ ERROR DS \_ EXISTE EN \_ PUEDE \_ \_ TENER**
</dt> <dd> <dl> <dt>

8386 (0x20C2)
</dt> <dt>



Error de eliminación del esquema: el atributo se usa en may-contain.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MAY_HAVE"></span><span id="error_ds_nonexistent_may_have"></span>**ERROR \_ QUE PUEDE TENER \_ DS \_ \_ INEXISTENTE**
</dt> <dd> <dl> <dt>

8387 (0x20C3)
</dt> <dt>



Error en la actualización del esquema: el atributo de may-contain no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_MUST_HAVE"></span><span id="error_ds_nonexistent_must_have"></span>**ERROR \_ QUE DS \_ INEXISTENTE \_ DEBE \_ TENER**
</dt> <dd> <dl> <dt>

8388 (0x20C4)
</dt> <dt>



Error en la actualización del esquema: el atributo en must-contain no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUX_CLS_TEST_FAIL"></span><span id="error_ds_aux_cls_test_fail"></span>**ERROR \_ DS \_ AUX \_ CLS \_ TEST \_ FAIL**
</dt> <dd> <dl> <dt>

8389 (0x20C5)
</dt> <dt>



Error de actualización de esquema: la clase de la lista de clases auxiliares no existe o no es una clase auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONEXISTENT_POSS_SUP"></span><span id="error_ds_nonexistent_poss_sup"></span>**ERROR \_ DS \_ NONEXISTENT \_ POSS \_ SUP**
</dt> <dd> <dl> <dt>

8390 (0x20C6)
</dt> <dt>



Error en la actualización del esquema: la clase en poss-superiors no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SUB_CLS_TEST_FAIL"></span><span id="error_ds_sub_cls_test_fail"></span>**ERROR \_ DS \_ SUB \_ CLS \_ TEST \_ FAIL**
</dt> <dd> <dl> <dt>

8391 (0x20C7)
</dt> <dt>



Error de actualización de esquema: la clase de la lista de subclases no existe o no cumple las reglas de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_RDN_ATT_ID_SYNTAX"></span><span id="error_ds_bad_rdn_att_id_syntax"></span>**ERROR \_ DS \_ BAD \_ RDN \_ ATT \_ ID \_ SYNTAX**
</dt> <dd> <dl> <dt>

8392 (0x20C8)
</dt> <dt>



Error en la actualización del esquema: Rdn-Att-Id tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_AUX_CLS"></span><span id="error_ds_exists_in_aux_cls"></span>**ERROR \_ DS \_ EXISTE EN \_ AUX \_ \_ CLS**
</dt> <dd> <dl> <dt>

8393 (0x20C9)
</dt> <dt>



Error de eliminación del esquema: la clase se usa como clase auxiliar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_SUB_CLS"></span><span id="error_ds_exists_in_sub_cls"></span>**ERROR \_ DS \_ EXISTE EN \_ SUB \_ \_ CLS**
</dt> <dd> <dl> <dt>

8394 (0x20CA)
</dt> <dt>



Error de eliminación del esquema: la clase se usa como subclase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_POSS_SUP"></span><span id="error_ds_exists_in_poss_sup"></span>**ERROR \_ DS \_ EXISTE EN \_ \_ POSS \_ SUP**
</dt> <dd> <dl> <dt>

8395 (0x20CB)
</dt> <dt>



Error de eliminación del esquema: la clase se usa como superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RECALCSCHEMA_FAILED"></span><span id="error_ds_recalcschema_failed"></span>**ERROR \_ DS \_ RECALCSCHEMA \_ FAILED**
</dt> <dd> <dl> <dt>

8396 (0x20CC)
</dt> <dt>



Error de actualización del esquema al volver a calcular la caché de validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_TREE_DELETE_NOT_FINISHED"></span><span id="error_ds_tree_delete_not_finished"></span>**ERROR \_ DS \_ TREE \_ DELETE \_ NOT \_ FINISHED**
</dt> <dd> <dl> <dt>

8397 (0x20CD)
</dt> <dt>



La eliminación del árbol no ha finalizado. La solicitud debe realizarse de nuevo para continuar eliminando el árbol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DELETE"></span><span id="error_ds_cant_delete"></span>**ERROR \_ DS \_ CANT \_ DELETE**
</dt> <dd> <dl> <dt>

8398 (0x20CE)
</dt> <dt>



No se pudo realizar la operación de eliminación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_ID"></span><span id="error_ds_att_schema_req_id"></span>**ERROR \_ DS \_ ATT \_ SCHEMA \_ REQ \_ ID**
</dt> <dd> <dl> <dt>

8399 (0x20CF)
</dt> <dt>



No se puede leer el identificador de clase governs para el registro de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_ATT_SCHEMA_SYNTAX"></span><span id="error_ds_bad_att_schema_syntax"></span>**ERROR \_ DS \_ BAD \_ ATT \_ SCHEMA \_ SYNTAX**
</dt> <dd> <dl> <dt>

8400 (0x20D0)
</dt> <dt>



El esquema de atributo tiene una sintaxis incorrecta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_ATT"></span><span id="error_ds_cant_cache_att"></span>**ERROR \_ DS \_ CANT \_ CACHE \_ ATT**
</dt> <dd> <dl> <dt>

8401 (0x20D1)
</dt> <dt>



El atributo no se pudo almacenar en caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CACHE_CLASS"></span><span id="error_ds_cant_cache_class"></span>**ERROR \_ DS \_ CANT \_ CACHE \_ (CLASE)**
</dt> <dd> <dl> <dt>

8402 (0x20D2)
</dt> <dt>



La clase no se pudo almacenar en caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_ATT_CACHE"></span><span id="error_ds_cant_remove_att_cache"></span>**ERROR \_ DS \_ CANT \_ REMOVE \_ ATT \_ CACHE**
</dt> <dd> <dl> <dt>

8403 (0x20D3)
</dt> <dt>



No se pudo quitar el atributo de la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REMOVE_CLASS_CACHE"></span><span id="error_ds_cant_remove_class_cache"></span>**ERROR \_ DS \_ CANT \_ REMOVE \_ CLASS \_ CACHE**
</dt> <dd> <dl> <dt>

8404 (0x20D4)
</dt> <dt>



No se pudo quitar la clase de la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_DN"></span><span id="error_ds_cant_retrieve_dn"></span>**ERROR \_ DS \_ CANT \_ RETRIEVE \_ DN**
</dt> <dd> <dl> <dt>

8405 (0x20D5)
</dt> <dt>



No se pudo leer el atributo de nombre distintivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_SUPREF"></span><span id="error_ds_missing_supref"></span>**ERROR \_ DS \_ MISSING \_ SUPREF**
</dt> <dd> <dl> <dt>

8406 (0x20D6)
</dt> <dt>



No se configuró ninguna referencia superior para el servicio de directorio. Por lo tanto, el servicio de directorio no puede emitir referencias a objetos fuera de este bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_INSTANCE"></span><span id="error_ds_cant_retrieve_instance"></span>**ERROR \_ DS \_ CANT \_ RETRIEVE \_ INSTANCE**
</dt> <dd> <dl> <dt>

8407 (0x20D7)
</dt> <dt>



No se pudo recuperar el atributo de tipo de instancia.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CODE_INCONSISTENCY"></span><span id="error_ds_code_inconsistency"></span>**INCOHERENCIA \_ DE CÓDIGO DS \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

8408 (0x20D8)
</dt> <dt>



Se ha producido un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DATABASE_ERROR"></span><span id="error_ds_database_error"></span>**ERROR \_ DS \_ DATABASE \_ ERROR**
</dt> <dd> <dl> <dt>

8409 (0x20D9)
</dt> <dt>



Se ha producido un error de base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GOVERNSID_MISSING"></span><span id="error_ds_governsid_missing"></span>**ERROR \_ DS \_ GOVERNSID \_ MISSING**
</dt> <dd> <dl> <dt>

8410 (0x20DA)
</dt> <dt>



Falta el atributo GOVERNSID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_EXPECTED_ATT"></span><span id="error_ds_missing_expected_att"></span>**ERROR \_ DS \_ MISSING \_ EXPECTED \_ ATT**
</dt> <dd> <dl> <dt>

8411 (0x20DB)
</dt> <dt>



Falta un atributo esperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NCNAME_MISSING_CR_REF"></span><span id="error_ds_ncname_missing_cr_ref"></span>**ERROR \_ DS \_ NCNAME \_ MISSING \_ CR \_ REF**
</dt> <dd> <dl> <dt>

8412 (0x20DC)
</dt> <dt>



Falta una referencia cruzada al contexto de nomenclatura especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_CHECKING_ERROR"></span><span id="error_ds_security_checking_error"></span>**ERROR \_ DS \_ SECURITY \_ CHECKING \_ ERROR**
</dt> <dd> <dl> <dt>

8413 (0x20DD)
</dt> <dt>



Se ha producido un error de comprobación de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_NOT_LOADED"></span><span id="error_ds_schema_not_loaded"></span>**ERROR \_ DS \_ SCHEMA \_ NOT \_ LOADED**
</dt> <dd> <dl> <dt>

8414 (0x20DE)
</dt> <dt>



El esquema no se carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_ALLOC_FAILED"></span><span id="error_ds_schema_alloc_failed"></span>**ERROR \_ DS \_ SCHEMA \_ ALLOC \_ FAILED**
</dt> <dd> <dl> <dt>

8415 (0x20DF)
</dt> <dt>



Error de asignación de esquema. Compruebe si la máquina se está quedando sin memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ATT_SCHEMA_REQ_SYNTAX"></span><span id="error_ds_att_schema_req_syntax"></span>**ERROR \_ DS \_ ATT \_ SCHEMA \_ REQ \_ SYNTAX**
</dt> <dd> <dl> <dt>

8416 (0x20E0)
</dt> <dt>



No se pudo obtener la sintaxis necesaria para el esquema de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GCVERIFY_ERROR"></span><span id="error_ds_gcverify_error"></span>**ERROR \_ DS \_ GCVERIFY \_ ERROR**
</dt> <dd> <dl> <dt>

8417 (0x20E1)
</dt> <dt>



Error en la comprobación del catálogo global. El catálogo global no está disponible o no admite la operación. Alguna parte del directorio no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_MISMATCH"></span><span id="error_ds_dra_schema_mismatch"></span>**ERROR \_ DS \_ DRA \_ SCHEMA \_ MISMATCH**
</dt> <dd> <dl> <dt>

8418 (0x20E2)
</dt> <dt>



Error en la operación de replicación debido a una falta de coincidencia de esquema entre los servidores implicados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DSA_OBJ"></span><span id="error_ds_cant_find_dsa_obj"></span>**ERROR \_ DS \_ CANT \_ FIND \_ DSA \_ OBJ**
</dt> <dd> <dl> <dt>

8419 (0x20E3)
</dt> <dt>



No se encontró el objeto DSA.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_EXPECTED_NC"></span><span id="error_ds_cant_find_expected_nc"></span>**ERROR \_ DS \_ CANT \_ FIND \_ EXPECTED \_ NC**
</dt> <dd> <dl> <dt>

8420 (0x20E4)
</dt> <dt>



No se encontró el contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_NC_IN_CACHE"></span><span id="error_ds_cant_find_nc_in_cache"></span>**ERROR \_ DS \_ CANT \_ FIND \_ NC \_ IN \_ CACHE**
</dt> <dd> <dl> <dt>

8421 (0x20E5)
</dt> <dt>



No se encontró el contexto de nomenclatura en la memoria caché.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_CHILD"></span><span id="error_ds_cant_retrieve_child"></span>**ERROR \_ DS \_ CANT \_ RETRIEVE \_ CHILD**
</dt> <dd> <dl> <dt>

8422 (0x20E6)
</dt> <dt>



No se pudo recuperar el objeto secundario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SECURITY_ILLEGAL_MODIFY"></span><span id="error_ds_security_illegal_modify"></span>**ERROR \_ DS \_ SECURITY \_ ILLEGAL \_ MODIFY**
</dt> <dd> <dl> <dt>

8423 (0x20E7)
</dt> <dt>



No se permitió la modificación por motivos de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_REPLACE_HIDDEN_REC"></span><span id="error_ds_cant_replace_hidden_rec"></span>**ERROR \_ DS \_ CANT \_ REPLACE \_ HIDDEN \_ REC**
</dt> <dd> <dl> <dt>

8424 (0x20E8)
</dt> <dt>



La operación no puede reemplazar el registro oculto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BAD_HIERARCHY_FILE"></span><span id="error_ds_bad_hierarchy_file"></span>**ARCHIVO \_ DE JERARQUÍA DE ERRORES DS \_ \_ \_**
</dt> <dd> <dl> <dt>

8425 (0x20E9)
</dt> <dt>



El archivo de jerarquía no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BUILD_HIERARCHY_TABLE_FAILED"></span><span id="error_ds_build_hierarchy_table_failed"></span>**ERROR \_ DS \_ BUILD \_ HIERARCHY \_ TABLE \_ FAILED**
</dt> <dd> <dl> <dt>

8426 (0x20EA)
</dt> <dt>



Error al intentar compilar la tabla de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONFIG_PARAM_MISSING"></span><span id="error_ds_config_param_missing"></span>**ERROR \_ DS \_ CONFIG \_ PARAM \_ MISSING**
</dt> <dd> <dl> <dt>

8427 (0x20EB)
</dt> <dt>



Falta el parámetro de configuración de directorio del registro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COUNTING_AB_INDICES_FAILED"></span><span id="error_ds_counting_ab_indices_failed"></span>**ERROR \_ DS \_ COUNTING \_ AB \_ INDICES \_ FAILED**
</dt> <dd> <dl> <dt>

8428 (0x20EC)
</dt> <dt>



Error al intentar contar los índices de la libreta de direcciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_MALLOC_FAILED"></span><span id="error_ds_hierarchy_table_malloc_failed"></span>**ERROR \_ DS \_ HIERARCHY \_ TABLE \_ MALLOC \_ FAILED**
</dt> <dd> <dl> <dt>

8429 (0x20ED)
</dt> <dt>



Error en la asignación de la tabla de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INTERNAL_FAILURE"></span><span id="error_ds_internal_failure"></span>**ERROR \_ DS \_ INTERNAL \_ FAILURE**
</dt> <dd> <dl> <dt>

8430 (0x20EE)
</dt> <dt>



El servicio de directorio encontró un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNKNOWN_ERROR"></span><span id="error_ds_unknown_error"></span>**ERROR \_ DS \_ UNKNOWN \_ ERROR**
</dt> <dd> <dl> <dt>

8431 (0x20EF)
</dt> <dt>



El servicio de directorio encontró un error desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROOT_REQUIRES_CLASS_TOP"></span><span id="error_ds_root_requires_class_top"></span>**ERROR \_ DS \_ ROOT \_ REQUIRES \_ CLASS \_ TOP**
</dt> <dd> <dl> <dt>

8432 (0x20F0)
</dt> <dt>



Un objeto raíz requiere una clase de "top".


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REFUSING_FSMO_ROLES"></span><span id="error_ds_refusing_fsmo_roles"></span>**ERROR \_ DS \_ AL RECHAZAR ROLES \_ FSMO \_**
</dt> <dd> <dl> <dt>

8433 (0x20F1)
</dt> <dt>



Este servidor de directorios se está cerrando y no puede tomar posesión de los nuevos roles de operación de maestro único flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_FSMO_SETTINGS"></span><span id="error_ds_missing_fsmo_settings"></span>**ERROR \_ DS \_ MISSING \_ FSMO \_ SETTINGS**
</dt> <dd> <dl> <dt>

8434 (0x20F2)
</dt> <dt>



Al servicio de directorio le falta información de configuración obligatoria y no puede determinar la propiedad de los roles de operación de un solo maestro flotante.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNABLE_TO_SURRENDER_ROLES"></span><span id="error_ds_unable_to_surrender_roles"></span>**ERROR \_ DS \_ NO SE PUEDEN \_ ENTREGAR \_ \_ ROLES**
</dt> <dd> <dl> <dt>

8435 (0x20F3)
</dt> <dt>



El servicio de directorio no pudo transferir la propiedad de uno o varios roles de operación de maestro único flotante a otros servidores.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_GENERIC"></span><span id="error_ds_dra_generic"></span>**ERROR \_ DS \_ DRA \_ GENERIC**
</dt> <dd> <dl> <dt>

8436 (0x20F4)
</dt> <dt>



Error en la operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INVALID_PARAMETER"></span><span id="error_ds_dra_invalid_parameter"></span>**ERROR \_ DS \_ DRA \_ INVALID \_ PARAMETER**
</dt> <dd> <dl> <dt>

8437 (0x20F5)
</dt> <dt>



Se especificó un parámetro no válido para esta operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BUSY"></span><span id="error_ds_dra_busy"></span>**ERROR \_ DS \_ DRA \_ BUSY**
</dt> <dd> <dl> <dt>

8438 (0x20F6)
</dt> <dt>



El servicio de directorio está demasiado ocupado para completar la operación de replicación en este momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_DN"></span><span id="error_ds_dra_bad_dn"></span>**ERROR \_ DS \_ DRA \_ BAD \_ DN**
</dt> <dd> <dl> <dt>

8439 (0x20F7)
</dt> <dt>



El nombre distintivo especificado para esta operación de replicación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_NC"></span><span id="error_ds_dra_bad_nc"></span>**ERROR \_ DS \_ DRA \_ BAD \_ NC**
</dt> <dd> <dl> <dt>

8440 (0x20F8)
</dt> <dt>



El contexto de nomenclatura especificado para esta operación de replicación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DN_EXISTS"></span><span id="error_ds_dra_dn_exists"></span>**ERROR \_ DS \_ DRA \_ DN \_ EXISTS**
</dt> <dd> <dl> <dt>

8441 (0x20F9)
</dt> <dt>



El nombre distintivo especificado para esta operación de replicación ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INTERNAL_ERROR"></span><span id="error_ds_dra_internal_error"></span>**ERROR \_ DS \_ DRA ERROR \_ \_ INTERNO**
</dt> <dd> <dl> <dt>

8442 (0x20FA)
</dt> <dt>



El sistema de replicación encontró un error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCONSISTENT_DIT"></span><span id="error_ds_dra_inconsistent_dit"></span>**ERROR \_ DS \_ DRA \_ INCONSISTENT \_ DIT**
</dt> <dd> <dl> <dt>

8443 (0x20FB)
</dt> <dt>



La operación de replicación encontró una incoherencia de base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CONNECTION_FAILED"></span><span id="error_ds_dra_connection_failed"></span>**ERROR \_ DS \_ DRA \_ CONNECTION \_ FAILED**
</dt> <dd> <dl> <dt>

8444 (0x20FC)
</dt> <dt>



No se pudo ponerse en contacto con el servidor especificado para esta operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_BAD_INSTANCE_TYPE"></span><span id="error_ds_dra_bad_instance_type"></span>**ERROR \_ DS \_ DRA \_ BAD \_ INSTANCE \_ TYPE**
</dt> <dd> <dl> <dt>

8445 (0x20FD)
</dt> <dt>



La operación de replicación encontró un objeto con un tipo de instancia no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_OF_MEM"></span><span id="error_ds_dra_out_of_mem"></span>**ERROR \_ DS \_ DRA \_ OUT \_ OF \_ MEM**
</dt> <dd> <dl> <dt>

8446 (0x20FE)
</dt> <dt>



La operación de replicación no pudo asignar memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MAIL_PROBLEM"></span><span id="error_ds_dra_mail_problem"></span>**ERROR \_ DS \_ DRA \_ MAIL \_ PROBLEM**
</dt> <dd> <dl> <dt>

8447 (0x20FF)
</dt> <dt>



La operación de replicación encontró un error con el sistema de correo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_ALREADY_EXISTS"></span><span id="error_ds_dra_ref_already_exists"></span>**ERROR \_ DS \_ DRA REF YA \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

8448 (0x2100)
</dt> <dt>



La información de referencia de replicación para el servidor de destino ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REF_NOT_FOUND"></span><span id="error_ds_dra_ref_not_found"></span>**ERROR \_ DS \_ DRA \_ REF \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

8449 (0x2101)
</dt> <dt>



La información de referencia de replicación para el servidor de destino no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_IS_REP_SOURCE"></span><span id="error_ds_dra_obj_is_rep_source"></span>**ERROR \_ DS \_ DRA \_ OBJ \_ IS \_ REP \_ SOURCE**
</dt> <dd> <dl> <dt>

8450 (0x2102)
</dt> <dt>



No se puede quitar el contexto de nomenclatura porque se replica en otro servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_DB_ERROR"></span><span id="error_ds_dra_db_error"></span>**ERROR \_ DS \_ DRA \_ DB \_ ERROR**
</dt> <dd> <dl> <dt>

8451 (0x2103)
</dt> <dt>



La operación de replicación encontró un error de base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NO_REPLICA"></span><span id="error_ds_dra_no_replica"></span>**ERROR \_ DS \_ DRA \_ NO \_ REPLICA**
</dt> <dd> <dl> <dt>

8452 (0x2104)
</dt> <dt>



El contexto de nomenclatura está en proceso de quitarse o no se replica desde el servidor especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ACCESS_DENIED"></span><span id="error_ds_dra_access_denied"></span>**ERROR \_ DS \_ DRA \_ ACCESS \_ DENIED**
</dt> <dd> <dl> <dt>

8453 (0x2105)
</dt> <dt>



Se denegó el acceso de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NOT_SUPPORTED"></span><span id="error_ds_dra_not_supported"></span>**ERROR \_ DS \_ DRA NO \_ \_ COMPATIBLE**
</dt> <dd> <dl> <dt>

8454 (0x2106)
</dt> <dt>



Esta versión del servicio de directorio no admite la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RPC_CANCELLED"></span><span id="error_ds_dra_rpc_cancelled"></span>**ERROR \_ DS \_ DRA \_ RPC \_ CANCELLED**
</dt> <dd> <dl> <dt>

8455 (0x2107)
</dt> <dt>



Se canceló la llamada al procedimiento remoto de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_DISABLED"></span><span id="error_ds_dra_source_disabled"></span>**ERROR \_ DS \_ DRA \_ SOURCE \_ DISABLED**
</dt> <dd> <dl> <dt>

8456 (0x2108)
</dt> <dt>



El servidor de origen está rechazando actualmente las solicitudes de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SINK_DISABLED"></span><span id="error_ds_dra_sink_disabled"></span>**ERROR \_ DS \_ DRA \_ SINK \_ DISABLED**
</dt> <dd> <dl> <dt>

8457 (0x2109)
</dt> <dt>



El servidor de destino está rechazando actualmente las solicitudes de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_NAME_COLLISION"></span><span id="error_ds_dra_name_collision"></span>**ERROR \_ DS \_ DRA \_ NAME \_ COLLISION**
</dt> <dd> <dl> <dt>

8458 (0x210A)
</dt> <dt>



Error en la operación de replicación debido a una colisión de nombres de objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_REINSTALLED"></span><span id="error_ds_dra_source_reinstalled"></span>**ERROR \_ DS \_ DRA SOURCE \_ \_ REINSTALADO**
</dt> <dd> <dl> <dt>

8459 (0x210B)
</dt> <dt>



Se ha reinstalado el origen de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_PARENT"></span><span id="error_ds_dra_missing_parent"></span>**ERROR \_ DS \_ DRA \_ MISSING \_ PARENT**
</dt> <dd> <dl> <dt>

8460 (0x210C)
</dt> <dt>



Error en la operación de replicación porque falta un objeto primario necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_PREEMPTED"></span><span id="error_ds_dra_preempted"></span>**ERROR \_ DS \_ DRA \_ PREEMPTED**
</dt> <dd> <dl> <dt>

8461 (0x210D)
</dt> <dt>



Se ha adelantado la operación de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_ABANDON_SYNC"></span><span id="error_ds_dra_abandon_sync"></span>**ERROR \_ DS \_ DRA \_ ABANDON \_ SYNC**
</dt> <dd> <dl> <dt>

8462 (0x210E)
</dt> <dt>



El intento de sincronización de replicación se abandonó debido a la falta de actualizaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SHUTDOWN"></span><span id="error_ds_dra_shutdown"></span>**ERROR \_ DS \_ DRA \_ SHUTDOWN**
</dt> <dd> <dl> <dt>

8463 (0x210F)
</dt> <dt>



La operación de replicación se finalizó porque el sistema se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_INCOMPATIBLE_PARTIAL_SET"></span><span id="error_ds_dra_incompatible_partial_set"></span>**ERROR \_ DS \_ DRA \_ INCOMPATIBLE \_ PARTIAL \_ SET**
</dt> <dd> <dl> <dt>

8464 (0x2110)
</dt> <dt>



Error en el intento de sincronización porque el controlador de dominio de destino está esperando actualmente para sincronizar nuevos atributos parciales desde el origen. Esta condición es normal si un cambio de esquema reciente modificó el conjunto de atributos parciales. El conjunto de atributos parciales de destino no es un subconjunto del conjunto de atributos parciales de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SOURCE_IS_PARTIAL_REPLICA"></span><span id="error_ds_dra_source_is_partial_replica"></span>**ERROR \_ DS \_ DRA \_ SOURCE \_ IS \_ PARTIAL \_ REPLICA**
</dt> <dd> <dl> <dt>

8465 (0x2111)
</dt> <dt>



Error en el intento de sincronización de replicación porque una réplica maestra intentó sincronizarse desde una réplica parcial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EXTN_CONNECTION_FAILED"></span><span id="error_ds_dra_extn_connection_failed"></span>**ERROR \_ DS \_ DRA \_ EXTN \_ CONNECTION \_ FAILED**
</dt> <dd> <dl> <dt>

8466 (0x2112)
</dt> <dt>



Se contactó con el servidor especificado para esta operación de replicación, pero ese servidor no pudo ponerse en contacto con un servidor adicional necesario para completar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_SCHEMA_MISMATCH"></span><span id="error_ds_install_schema_mismatch"></span>**ERROR \_ DS \_ INSTALL \_ SCHEMA \_ MISMATCH**
</dt> <dd> <dl> <dt>

8467 (0x2113)
</dt> <dt>



La versión del esquema del servicio de directorio del bosque de origen no es compatible con la versión del servicio de directorio en este equipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_LINK_ID"></span><span id="error_ds_dup_link_id"></span>**IDENTIFICADOR \_ DE VÍNCULO \_ DUP DE DS \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8468 (0x2114)
</dt> <dt>



Error en la actualización del esquema: ya existe un atributo con el mismo identificador de vínculo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_RESOLVING"></span><span id="error_ds_name_error_resolving"></span>**ERROR \_ DS \_ NAME \_ ERROR \_ RESOLVING**
</dt> <dd> <dl> <dt>

8469 (0x2115)
</dt> <dt>



Traducción de nombres: error de procesamiento genérico.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_FOUND"></span><span id="error_ds_name_error_not_found"></span>**ERROR \_ DS \_ NAME \_ ERROR \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

8470 (0x2116)
</dt> <dt>



Traducción de nombres: no se encontró el nombre o no se encontró el derecho suficiente para ver el nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NOT_UNIQUE"></span><span id="error_ds_name_error_not_unique"></span>**ERROR \_ DS \_ NAME \_ ERROR \_ NOT \_ UNIQUE**
</dt> <dd> <dl> <dt>

8471 (0x2117)
</dt> <dt>



Traducción de nombres: nombre de entrada asignado a más de un nombre de salida.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_MAPPING"></span><span id="error_ds_name_error_no_mapping"></span>**ERROR \_ DS \_ NAME \_ ERROR \_ NO \_ MAPPING**
</dt> <dd> <dl> <dt>

8472 (0x2118)
</dt> <dt>



Traducción de nombres: se encontró el nombre de entrada, pero no el formato de salida asociado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_DOMAIN_ONLY"></span><span id="error_ds_name_error_domain_only"></span>**SOLO \_ DOMINIO DE ERROR DE NOMBRE \_ \_ DS \_ \_**
</dt> <dd> <dl> <dt>

8473 (0x2119)
</dt> <dt>



Traducción de nombres: no se puede resolver completamente, solo se encontró el dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_NO_SYNTACTICAL_MAPPING"></span><span id="error_ds_name_error_no_syntactical_mapping"></span>**ERROR \_ DS \_ NAME \_ ERROR \_ NO \_ SYNTACTICAL \_ MAPPING**
</dt> <dd> <dl> <dt>

8474 (0x211A)
</dt> <dt>



Traducción de nombres: no se puede realizar una asignación puramente sintáctica en el cliente sin salir a la conexión.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CONSTRUCTED_ATT_MOD"></span><span id="error_ds_constructed_att_mod"></span>**ERROR \_ DS \_ CONSTRUIDO \_ ATT \_ MOD**
</dt> <dd> <dl> <dt>

8475 (0x211B)
</dt> <dt>



No se permite la modificación de un atributo construido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_OM_OBJ_CLASS"></span><span id="error_ds_wrong_om_obj_class"></span>**ERROR \_ DS \_ WRONG \_ OM \_ OBJ \_ CLASS**
</dt> <dd> <dl> <dt>

8476 (0x211C)
</dt> <dt>



La clase OM-Object especificada es incorrecta para un atributo con la sintaxis especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_REPL_PENDING"></span><span id="error_ds_dra_repl_pending"></span>**ERROR \_ DS \_ DRA \_ REPL \_ PENDING**
</dt> <dd> <dl> <dt>

8477 (0x211D)
</dt> <dt>



Se ha publicado la solicitud de replicación; esperando respuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DS_REQUIRED"></span><span id="error_ds_ds_required"></span>**ERROR \_ DS \_ DS \_ REQUIRED**
</dt> <dd> <dl> <dt>

8478 (0x211E)
</dt> <dt>



La operación solicitada requiere un servicio de directorio y no había ninguno disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_LDAP_DISPLAY_NAME"></span><span id="error_ds_invalid_ldap_display_name"></span>**ERROR \_ DS \_ NOMBRE PARA MOSTRAR LDAP NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8479 (0x211F)
</dt> <dt>



El nombre para mostrar LDAP de la clase o atributo contiene caracteres no ASCII.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_BASE_SEARCH"></span><span id="error_ds_non_base_search"></span>**ERROR \_ DS \_ NON \_ BASE \_ SEARCH**
</dt> <dd> <dl> <dt>

8480 (0x2120)
</dt> <dt>



La operación de búsqueda solicitada solo se admite para las búsquedas base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_ATTS"></span><span id="error_ds_cant_retrieve_atts"></span>**ERROR \_ DS \_ CANT \_ RETRIEVE \_ ATTS**
</dt> <dd> <dl> <dt>

8481 (0x2121)
</dt> <dt>



La búsqueda no pudo recuperar atributos de la base de datos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_BACKLINK_WITHOUT_LINK"></span><span id="error_ds_backlink_without_link"></span>**ERROR \_ DS \_ BACKLINK \_ WITHOUT \_ LINK**
</dt> <dd> <dl> <dt>

8482 (0x2122)
</dt> <dt>



La operación de actualización del esquema intentó agregar un atributo de vínculo hacia atrás que no tiene ningún vínculo hacia delante correspondiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EPOCH_MISMATCH"></span><span id="error_ds_epoch_mismatch"></span>**ERROR \_ DS \_ EPOCH \_ MISMATCH**
</dt> <dd> <dl> <dt>

8483 (0x2123)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden en el número de época del objeto. El origen o el destino no tienen la versión más reciente del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_NAME_MISMATCH"></span><span id="error_ds_src_name_mismatch"></span>**ERROR \_ DS \_ SRC \_ NAME \_ MISMATCH**
</dt> <dd> <dl> <dt>

8484 (0x2124)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden en el nombre actual del objeto. El origen o el destino no tienen la versión más reciente del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_NC_IDENTICAL"></span><span id="error_ds_src_and_dst_nc_identical"></span>**ERROR \_ DS \_ SRC \_ Y \_ DST NC \_ \_ IDÉNTICOS**
</dt> <dd> <dl> <dt>

8485 (0x2125)
</dt> <dt>



El origen y el destino de la operación de movimiento entre dominios son idénticos. El autor de la llamada debe usar la operación de movimiento local en lugar de la operación de movimiento entre dominios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_NC_MISMATCH"></span><span id="error_ds_dst_nc_mismatch"></span>**ERROR \_ DS \_ DST \_ NC \_ MISMATCH**
</dt> <dd> <dl> <dt>

8486 (0x2126)
</dt> <dt>



El origen y el destino de un traslado entre dominios no están de acuerdo con los contextos de nomenclatura del bosque. El origen o el destino no tienen la versión más reciente del contenedor Particiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_AUTHORITIVE_FOR_DST_NC"></span><span id="error_ds_not_authoritive_for_dst_nc"></span>**ERROR \_ DS \_ NOT \_ AUTHORITIVE \_ FOR \_ DST \_ NC**
</dt> <dd> <dl> <dt>

8487 (0x2127)
</dt> <dt>



El destino de un movimiento entre dominios no es autoritativo para el contexto de nomenclatura de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_GUID_MISMATCH"></span><span id="error_ds_src_guid_mismatch"></span>**ERROR \_ DS \_ SRC \_ GUID \_ MISMATCH**
</dt> <dd> <dl> <dt>

8488 (0x2128)
</dt> <dt>



El origen y el destino de un movimiento entre dominios no coinciden en la identidad del objeto de origen. El origen o el destino no tienen la versión más reciente del objeto de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_DELETED_OBJECT"></span><span id="error_ds_cant_move_deleted_object"></span>**ERROR \_ DS \_ CANT \_ MOVE \_ DELETED \_ OBJECT**
</dt> <dd> <dl> <dt>

8489 (0x2129)
</dt> <dt>



Ya se sabe que el servidor de destino elimina el objeto que se mueve entre dominios. El servidor de origen no tiene la versión más reciente del objeto de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_PDC_OPERATION_IN_PROGRESS"></span><span id="error_ds_pdc_operation_in_progress"></span>**ERROR \_ DS \_ PDC \_ OPERATION \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

8490 (0x212A)
</dt> <dt>



Otra operación que requiere acceso exclusivo al FSMO de PDC ya está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_DOMAIN_CLEANUP_REQD"></span><span id="error_ds_cross_domain_cleanup_reqd"></span>**ERROR \_ DS \_ CROSS \_ DOMAIN \_ CLEANUP \_ REQD**
</dt> <dd> <dl> <dt>

8491 (0x212B)
</dt> <dt>



Error en una operación de traslado entre dominios, de modo que existen dos versiones del objeto movido: una en los dominios de origen y destino. El objeto de destino debe quitarse para restaurar el sistema a un estado coherente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_XDOM_MOVE_OPERATION"></span><span id="error_ds_illegal_xdom_move_operation"></span>**ERROR \_ DS \_ ILLEGAL \_ XDOM \_ MOVE \_ OPERATION**
</dt> <dd> <dl> <dt>

8492 (0x212C)
</dt> <dt>



Es posible que este objeto no se mueva a través de los límites del dominio porque no se permite mover entre dominios para esta clase o porque el objeto tiene algunas características especiales, por ejemplo: cuenta de confianza o RID restringido, que impiden su traslado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_WITH_ACCT_GROUP_MEMBERSHPS"></span><span id="error_ds_cant_with_acct_group_membershps"></span>**ERROR \_ DS \_ CANT \_ WITH \_ ACCT \_ GROUP \_ MEMBERSHPS**
</dt> <dd> <dl> <dt>

8493 (0x212D)
</dt> <dt>



No se pueden mover objetos con pertenencias a través de los límites del dominio, ya que una vez movidos, esto infringiría las condiciones de pertenencia del grupo de cuentas. Quite el objeto de cualquier pertenencia a grupos de cuentas y vuelva a intentarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_MUST_HAVE_NC_PARENT"></span><span id="error_ds_nc_must_have_nc_parent"></span>**ERROR \_ DS \_ NC \_ MUST \_ HAVE \_ NC \_ PARENT**
</dt> <dd> <dl> <dt>

8494 (0x212E)
</dt> <dt>



Un jefe de contexto de nomenclatura debe ser el elemento secundario inmediato de otro responsable de contexto de nomenclatura, no de un nodo interior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE"></span><span id="error_ds_cr_impossible_to_validate"></span>**ERROR \_ DS \_ CR \_ IMPOSSIBLE \_ TO \_ VALIDATE**
</dt> <dd> <dl> <dt>

8495 (0x212F)
</dt> <dt>



El directorio no puede validar el nombre de contexto de nomenclatura propuesto porque no contiene una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto. Asegúrese de que el rol maestro de nomenclatura de dominio lo mantiene un servidor configurado como servidor de catálogo global y que el servidor está actualizado con sus asociados de replicación. (Solo se aplica a Windows maestros de nomenclatura de dominio 2000).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DST_DOMAIN_NOT_NATIVE"></span><span id="error_ds_dst_domain_not_native"></span>**ERROR \_ DS \_ DST \_ DOMAIN \_ NOT \_ NATIVE**
</dt> <dd> <dl> <dt>

8496 (0x2130)
</dt> <dt>



El dominio de destino debe estar en modo nativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MISSING_INFRASTRUCTURE_CONTAINER"></span><span id="error_ds_missing_infrastructure_container"></span>**ERROR \_ DS \_ MISSING \_ INFRASTRUCTURE \_ CONTAINER**
</dt> <dd> <dl> <dt>

8497 (0x2131)
</dt> <dt>



No se puede realizar la operación porque el servidor no tiene un contenedor de infraestructura en el dominio de interés.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_ACCOUNT_GROUP"></span><span id="error_ds_cant_move_account_group"></span>**ERROR \_ DS \_ CANT \_ MOVE \_ ACCOUNT \_ GROUP**
</dt> <dd> <dl> <dt>

8498 (0x2132)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de cuentas no vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_RESOURCE_GROUP"></span><span id="error_ds_cant_move_resource_group"></span>**ERROR \_ DS \_ CANT \_ MOVE \_ RESOURCE \_ GROUP**
</dt> <dd> <dl> <dt>

8499 (0x2133)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de recursos no vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG"></span><span id="error_ds_invalid_search_flag"></span>**ERROR \_ DS \_ MARCA DE BÚSQUEDA \_ NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

8500 (0x2134)
</dt> <dt>



Las marcas de búsqueda del atributo no son válidas. El bit ANR solo es válido en atributos de cadenas Unicode o Teletex.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_TREE_DELETE_ABOVE_NC"></span><span id="error_ds_no_tree_delete_above_nc"></span>**ERROR \_ DS \_ NO \_ TREE \_ DELETE \_ ABOVE \_ NC**
</dt> <dd> <dl> <dt>

8501 (0x2135)
</dt> <dt>



No se permiten eliminaciones de árbol a partir de un objeto que tenga un head nc como descendiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_LOCK_TREE_FOR_DELETE"></span><span id="error_ds_couldnt_lock_tree_for_delete"></span>**ERROR \_ DS \_ COULDNT \_ LOCK \_ TREE \_ FOR \_ DELETE**
</dt> <dd> <dl> <dt>

8502 (0x2136)
</dt> <dt>



El servicio de directorio no pudo bloquear un árbol como preparación para la eliminación de un árbol porque el árbol estaba en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_IDENTIFY_OBJECTS_FOR_TREE_DELETE"></span><span id="error_ds_couldnt_identify_objects_for_tree_delete"></span>**ERROR \_ DS \_ COULDNT \_ IDENTIFY \_ OBJECTS \_ FOR \_ TREE \_ DELETE**
</dt> <dd> <dl> <dt>

8503 (0x2137)
</dt> <dt>



El servicio de directorio no pudo identificar la lista de objetos que se deben eliminar al intentar la eliminación de un árbol.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE"></span><span id="error_ds_sam_init_failure"></span>**ERROR \_ DS \_ SAM \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8504 (0x2138)
</dt> <dt>



Error de inicialización del Administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x%2. Cierre este sistema y reinicie en Modo de restauración de servicios de directorio, compruebe el registro de eventos para obtener información más detallada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SENSITIVE_GROUP_VIOLATION"></span><span id="error_ds_sensitive_group_violation"></span>**ERROR \_ DS \_ SENSITIVE \_ GROUP \_ VIOLATION**
</dt> <dd> <dl> <dt>

8505 (0x2139)
</dt> <dt>



Solo un administrador puede modificar la lista de pertenencia de un grupo administrativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOD_PRIMARYGROUPID"></span><span id="error_ds_cant_mod_primarygroupid"></span>**ERROR \_ DS \_ CANT \_ MOD \_ PRIMARYGROUPID**
</dt> <dd> <dl> <dt>

8506 (0x213A)
</dt> <dt>



No se puede cambiar el identificador de grupo principal de una cuenta de controlador de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ILLEGAL_BASE_SCHEMA_MOD"></span><span id="error_ds_illegal_base_schema_mod"></span>**ERROR \_ DS \_ ILLEGAL \_ BASE \_ SCHEMA \_ MOD**
</dt> <dd> <dl> <dt>

8507 (0x213B)
</dt> <dt>



Se intenta modificar el esquema base.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NONSAFE_SCHEMA_CHANGE"></span><span id="error_ds_nonsafe_schema_change"></span>**ERROR \_ DS \_ NONSAFE \_ SCHEMA \_ CHANGE**
</dt> <dd> <dl> <dt>

8508 (0x213C)
</dt> <dt>



No se permite agregar un nuevo atributo obligatorio a una clase existente, eliminar un atributo obligatorio de una clase existente o agregar un atributo opcional a la clase especial Top que no sea un atributo backlink (directamente o a través de la herencia, por ejemplo, mediante la adición o eliminación de una clase auxiliar).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SCHEMA_UPDATE_DISALLOWED"></span><span id="error_ds_schema_update_disallowed"></span>**ERROR \_ NO SE PUEDE ACTUALIZAR EL ESQUEMA \_ \_ \_ DE DS**
</dt> <dd> <dl> <dt>

8509 (0x213D)
</dt> <dt>



No se permite la actualización del esquema en este controlador de dominio porque el controlador de dominio no es el propietario del rol FSMO del esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_UNDER_SCHEMA"></span><span id="error_ds_cant_create_under_schema"></span>**ERROR \_ DS \_ CANT \_ CREATE \_ UNDER \_ SCHEMA**
</dt> <dd> <dl> <dt>

8510 (0x213E)
</dt> <dt>



No se puede crear un objeto de esta clase en el contenedor de esquema. Solo puede crear objetos attribute-schema y class-schema en el contenedor de esquemas.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SRC_SCH_VERSION"></span><span id="error_ds_install_no_src_sch_version"></span>**ERROR \_ DS \_ INSTALL \_ NO \_ SRC \_ SCH \_ VERSION**
</dt> <dd> <dl> <dt>

8511 (0x213F)
</dt> <dt>



La instalación secundaria o de réplica no pudo obtener el atributo objectVersion en el contenedor de esquema en el controlador de dominio de origen. Falta el atributo en el contenedor de esquema o las credenciales proporcionadas no tienen permiso para leerlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSTALL_NO_SCH_VERSION_IN_INIFILE"></span><span id="error_ds_install_no_sch_version_in_inifile"></span>**ERROR \_ DS \_ INSTALL \_ NO \_ SCH \_ VERSION \_ IN \_ INIFILE**
</dt> <dd> <dl> <dt>

8512 (0x2140)
</dt> <dt>



La instalación de réplica o secundaria no pudo leer el atributo objectVersion en la sección SCHEMA del archivo schema.ini en el directorio system32.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_GROUP_TYPE"></span><span id="error_ds_invalid_group_type"></span>**ERROR \_ DS \_ TIPO DE GRUPO \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8513 (0x2141)
</dt> <dt>



El tipo de grupo especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_GLOBALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_globalgroup_in_mixeddomain"></span>**ERROR \_ DS \_ NO \_ NEST \_ GLOBALGROUP \_ IN \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8514 (0x2142)
</dt> <dt>



No puede anidar grupos globales en un dominio mixto si el grupo está habilitado para seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NEST_LOCALGROUP_IN_MIXEDDOMAIN"></span><span id="error_ds_no_nest_localgroup_in_mixeddomain"></span>**ERROR \_ DS \_ NO \_ NEST \_ LOCALGROUP \_ IN \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8515 (0x2143)
</dt> <dt>



No se pueden anidar grupos locales en un dominio mixto si el grupo está habilitado para seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_global_cant_have_local_member"></span>**ERROR \_ DS \_ GLOBAL \_ CANT \_ HAVE \_ LOCAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8516 (0x2144)
</dt> <dt>



Un grupo global no puede tener un grupo local como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_global_cant_have_universal_member"></span>**ERROR \_ DS \_ GLOBAL \_ CANT \_ HAVE \_ UNIVERSAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8517 (0x2145)
</dt> <dt>



Un grupo global no puede tener un grupo universal como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNIVERSAL_CANT_HAVE_LOCAL_MEMBER"></span><span id="error_ds_universal_cant_have_local_member"></span>**ERROR \_ DS \_ UNIVERSAL \_ CANT \_ HAVE \_ LOCAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8518 (0x2146)
</dt> <dt>



Un grupo universal no puede tener un grupo local como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GLOBAL_CANT_HAVE_CROSSDOMAIN_MEMBER"></span><span id="error_ds_global_cant_have_crossdomain_member"></span>**ERROR \_ DS \_ GLOBAL \_ CANT \_ HAVE \_ CROSSDOMAIN \_ MEMBER**
</dt> <dd> <dl> <dt>

8519 (0x2147)
</dt> <dt>



Un grupo global no puede tener un miembro entre dominios.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_CANT_HAVE_CROSSDOMAIN_LOCAL_MEMBER"></span><span id="error_ds_local_cant_have_crossdomain_local_member"></span>**ERROR \_ DS \_ LOCAL \_ CANT \_ HAVE \_ CROSSDOMAIN \_ LOCAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8520 (0x2148)
</dt> <dt>



Un grupo local no puede tener otro grupo local entre dominios como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HAVE_PRIMARY_MEMBERS"></span><span id="error_ds_have_primary_members"></span>**ERROR \_ DS \_ TIENEN MIEMBROS \_ PRINCIPALES \_**
</dt> <dd> <dl> <dt>

8521 (0x2149)
</dt> <dt>



Un grupo con miembros principales no puede cambiar a un grupo deshabilitado por seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_STRING_SD_CONVERSION_FAILED"></span><span id="error_ds_string_sd_conversion_failed"></span>**ERROR \_ DS \_ STRING \_ SD \_ CONVERSION \_ FAILED**
</dt> <dd> <dl> <dt>

8522 (0x214A)
</dt> <dt>



La carga de caché de esquema no pudo convertir la cadena predeterminada SD en un objeto de esquema de clase.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAMING_MASTER_GC"></span><span id="error_ds_naming_master_gc"></span>**ERROR \_ DS \_ NAMING \_ MASTER \_ GC**
</dt> <dd> <dl> <dt>

8523 (0x214B)
</dt> <dt>



Solo los DSA configurados para ser servidores de catálogo global deben tener el rol FSMO maestro de nomenclatura de dominios. (Solo se aplica a Windows 2000 servidores).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DNS_LOOKUP_FAILURE"></span><span id="error_ds_dns_lookup_failure"></span>**ERROR \_ DS \_ DNS \_ LOOKUP \_ FAILURE**
</dt> <dd> <dl> <dt>

8524 (0x214C)
</dt> <dt>



La operación DSA no puede continuar debido a un error de búsqueda dns.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_COULDNT_UPDATE_SPNS"></span><span id="error_ds_couldnt_update_spns"></span>**ERROR \_ DS \_ COULDNT \_ UPDATE \_ SPNS**
</dt> <dd> <dl> <dt>

8525 (0x214D)
</dt> <dt>



Al procesar un cambio en el nombre de host DNS de un objeto, los valores de Nombre de entidad de seguridad de servicio no se pudieron mantener sincronizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_RETRIEVE_SD"></span><span id="error_ds_cant_retrieve_sd"></span>**ERROR \_ DS \_ CANT \_ RETRIEVE \_ SD**
</dt> <dd> <dl> <dt>

8526 (0x214E)
</dt> <dt>



No se pudo leer el atributo Descriptor de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_KEY_NOT_UNIQUE"></span><span id="error_ds_key_not_unique"></span>**ERROR \_ DS \_ KEY \_ NOT \_ UNIQUE**
</dt> <dd> <dl> <dt>

8527 (0x214F)
</dt> <dt>



No se encontró el objeto solicitado, pero se encontró un objeto con esa clave.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WRONG_LINKED_ATT_SYNTAX"></span><span id="error_ds_wrong_linked_att_syntax"></span>**ERROR \_ DS \_ SINTAXIS \_ DE \_ ATT VINCULADA \_ INCORRECTA**
</dt> <dd> <dl> <dt>

8528 (0x2150)
</dt> <dt>



La sintaxis del atributo vinculado que se va a agregar es incorrecta. Los vínculos hacia delante solo pueden tener la sintaxis 2.5.5.1, 2.5.5.7 y 2.5.5.14, y los vínculos backlink solo pueden tener la sintaxis 2.5.5.1.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_PASSWORD"></span><span id="error_ds_sam_need_bootkey_password"></span>**ERROR \_ DS \_ SAM \_ NEED \_ BOOTKEY \_ PASSWORD**
</dt> <dd> <dl> <dt>

8529 (0x2151)
</dt> <dt>



El Administrador de cuentas de seguridad debe obtener la contraseña de arranque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_NEED_BOOTKEY_FLOPPY"></span><span id="error_ds_sam_need_bootkey_floppy"></span>**ERROR \_ DS \_ SAM \_ NEED \_ BOOTKEY \_ FLOPPY**
</dt> <dd> <dl> <dt>

8530 (0x2152)
</dt> <dt>



El Administrador de cuentas de seguridad debe obtener la clave de arranque del disquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_START"></span><span id="error_ds_cant_start"></span>**ERROR \_ DS \_ CANT \_ START**
</dt> <dd> <dl> <dt>

8531 (0x2153)
</dt> <dt>



No se puede iniciar el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE"></span><span id="error_ds_init_failure"></span>**ERROR \_ DS \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8532 (0x2154)
</dt> <dt>



No se pudo iniciar Servicios de directorio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_PKT_PRIVACY_ON_CONNECTION"></span><span id="error_ds_no_pkt_privacy_on_connection"></span>**ERROR \_ DS \_ NO \_ PKT \_ PRIVACY \_ ON \_ CONNECTION**
</dt> <dd> <dl> <dt>

8533 (0x2155)
</dt> <dt>



La conexión entre el cliente y el servidor requiere privacidad de paquetes o mejor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_DOMAIN_IN_FOREST"></span><span id="error_ds_source_domain_in_forest"></span>**DOMINIO \_ DE ORIGEN DE \_ DS DE ERROR EN EL \_ \_ \_ BOSQUE**
</dt> <dd> <dl> <dt>

8534 (0x2156)
</dt> <dt>



Es posible que el dominio de origen no esté en el mismo bosque que el destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_DOMAIN_NOT_IN_FOREST"></span><span id="error_ds_destination_domain_not_in_forest"></span>**ERROR \_ DS \_ DESTINATION \_ DOMAIN \_ NOT \_ IN \_ FOREST**
</dt> <dd> <dl> <dt>

8535 (0x2157)
</dt> <dt>



El dominio de destino debe estar en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DESTINATION_AUDITING_NOT_ENABLED"></span><span id="error_ds_destination_auditing_not_enabled"></span>**ERROR \_ DS \_ DESTINATION \_ AUDITING \_ NOT \_ ENABLED**
</dt> <dd> <dl> <dt>

8536 (0x2158)
</dt> <dt>



La operación requiere que se habilite la auditoría del dominio de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_FIND_DC_FOR_SRC_DOMAIN"></span><span id="error_ds_cant_find_dc_for_src_domain"></span>**ERROR \_ DS \_ CANT \_ FIND \_ DC \_ FOR \_ SRC \_ DOMAIN**
</dt> <dd> <dl> <dt>

8537 (0x2159)
</dt> <dt>



La operación no pudo encontrar un controlador de dominio para el dominio de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_OBJ_NOT_GROUP_OR_USER"></span><span id="error_ds_src_obj_not_group_or_user"></span>**ERROR \_ DS \_ SRC \_ OBJ \_ NOT \_ GROUP \_ OR \_ USER**
</dt> <dd> <dl> <dt>

8538 (0x215A)
</dt> <dt>



El objeto de origen debe ser un grupo o usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_SID_EXISTS_IN_FOREST"></span><span id="error_ds_src_sid_exists_in_forest"></span>**ERROR \_ DS \_ SRC \_ SID \_ EXISTS \_ IN \_ FOREST**
</dt> <dd> <dl> <dt>

8539 (0x215B)
</dt> <dt>



El SID del objeto de origen ya existe en el bosque de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_AND_DST_OBJECT_CLASS_MISMATCH"></span><span id="error_ds_src_and_dst_object_class_mismatch"></span>**ERROR \_ DS \_ SRC \_ Y \_ DST OBJECT CLASS \_ \_ \_ MISMATCH**
</dt> <dd> <dl> <dt>

8540 (0x215C)
</dt> <dt>



El objeto de origen y destino debe ser del mismo tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SAM_INIT_FAILURE"></span><span id="error_sam_init_failure"></span>**ERROR \_ SAM \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8541 (0x215D)
</dt> <dt>



Error de inicialización del Administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x%2. Haga clic en Aceptar para apagar el sistema y reiniciar en Caja fuerte modo. Compruebe el registro de eventos para obtener información detallada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_INFO_SHIP"></span><span id="error_ds_dra_schema_info_ship"></span>**ERROR \_ DS \_ DRA \_ SCHEMA \_ INFO \_ SHIP**
</dt> <dd> <dl> <dt>

8542 (0x215E)
</dt> <dt>



No se pudo incluir información de esquema en la solicitud de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SCHEMA_CONFLICT"></span><span id="error_ds_dra_schema_conflict"></span>**ERROR \_ DS \_ DRA \_ SCHEMA \_ CONFLICT**
</dt> <dd> <dl> <dt>

8543 (0x215F)
</dt> <dt>



No se pudo completar la operación de replicación debido a una incompatibilidad de esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_EARLIER_SCHEMA_CONFLICT"></span><span id="error_ds_dra_earlier_schema_conflict"></span>**ERROR \_ DS \_ DRA \_ EARLIER \_ SCHEMA \_ CONFLICT**
</dt> <dd> <dl> <dt>

8544 (0x2160)
</dt> <dt>



No se pudo completar la operación de replicación debido a una incompatibilidad de esquema anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OBJ_NC_MISMATCH"></span><span id="error_ds_dra_obj_nc_mismatch"></span>**ERROR \_ DS \_ DRA \_ OBJ \_ NC \_ MISMATCH**
</dt> <dd> <dl> <dt>

8545 (0x2161)
</dt> <dt>



No se pudo aplicar la actualización de replicación porque el origen o el destino aún no han recibido información sobre una operación de movimiento entre dominios reciente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NC_STILL_HAS_DSAS"></span><span id="error_ds_nc_still_has_dsas"></span>**ERROR \_ DS \_ NC TODAVÍA \_ TIENE \_ \_ DSAS**
</dt> <dd> <dl> <dt>

8546 (0x2162)
</dt> <dt>



No se pudo eliminar el dominio solicitado porque existen controladores de dominio que aún hospedan este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GC_REQUIRED"></span><span id="error_ds_gc_required"></span>**ERROR \_ DS \_ GC \_ REQUIRED**
</dt> <dd> <dl> <dt>

8547 (0x2163)
</dt> <dt>



La operación solicitada solo se puede realizar en un servidor de catálogo global.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOCAL_MEMBER_OF_LOCAL_ONLY"></span><span id="error_ds_local_member_of_local_only"></span>**ERROR \_ DS \_ MIEMBRO LOCAL SOLO DE \_ \_ \_ LOCAL \_**
</dt> <dd> <dl> <dt>

8548 (0x2164)
</dt> <dt>



Un grupo local solo puede ser miembro de otros grupos locales del mismo dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_FPO_IN_UNIVERSAL_GROUPS"></span><span id="error_ds_no_fpo_in_universal_groups"></span>**ERROR \_ DS \_ NO \_ FPO EN GRUPOS \_ \_ \_ UNIVERSALES**
</dt> <dd> <dl> <dt>

8549 (0x2165)
</dt> <dt>



Las entidades de seguridad externa no pueden ser miembros de grupos universales.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ADD_TO_GC"></span><span id="error_ds_cant_add_to_gc"></span>**ERROR \_ DS \_ CANT \_ ADD \_ TO \_ GC**
</dt> <dd> <dl> <dt>

8550 (0x2166)
</dt> <dt>



El atributo no se puede replicar en la GC por motivos de seguridad.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_CHECKPOINT_WITH_PDC"></span><span id="error_ds_no_checkpoint_with_pdc"></span>**ERROR \_ DS \_ NO \_ CHECKPOINT \_ WITH \_ PDC**
</dt> <dd> <dl> <dt>

8551 (0x2167)
</dt> <dt>



No se pudo realizar el punto de control con el PDC porque actualmente se están procesando demasiadas modificaciones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SOURCE_AUDITING_NOT_ENABLED"></span><span id="error_ds_source_auditing_not_enabled"></span>**ERROR \_ DS \_ SOURCE \_ AUDITING \_ NOT \_ ENABLED**
</dt> <dd> <dl> <dt>

8552 (0x2168)
</dt> <dt>



La operación requiere que se habilite la auditoría del dominio de origen.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_CREATE_IN_NONDOMAIN_NC"></span><span id="error_ds_cant_create_in_nondomain_nc"></span>**ERROR \_ DS \_ CANT \_ CREATE \_ IN \_ NONDOMAIN \_ NC**
</dt> <dd> <dl> <dt>

8553 (0x2169)
</dt> <dt>



Los objetos de entidad de seguridad solo se pueden crear dentro de contextos de nomenclatura de dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_NAME_FOR_SPN"></span><span id="error_ds_invalid_name_for_spn"></span>**ERROR \_ DS \_ NOMBRE NO VÁLIDO \_ PARA \_ \_ SPN**
</dt> <dd> <dl> <dt>

8554 (0x216A)
</dt> <dt>



No se pudo construir un nombre de entidad de seguridad de servicio (SPN) porque el nombre de host proporcionado no tiene el formato necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FILTER_USES_CONTRUCTED_ATTRS"></span><span id="error_ds_filter_uses_contructed_attrs"></span>**EL \_ FILTRO DS \_ DE ERROR \_ USA \_ \_ ATTRS CONTRUCTED**
</dt> <dd> <dl> <dt>

8555 (0x216B)
</dt> <dt>



Se pasó un filtro que usa atributos construidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNICODEPWD_NOT_IN_QUOTES"></span><span id="error_ds_unicodepwd_not_in_quotes"></span>**ERROR \_ DS \_ UNICODEPWD \_ NO ENTRE \_ \_ COMILLAS**
</dt> <dd> <dl> <dt>

8556 (0x216C)
</dt> <dt>



El valor del atributo unicodePwd debe incluirse entre comillas dobles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_QUOTA_EXCEEDED"></span><span id="error_ds_machine_account_quota_exceeded"></span>**ERROR \_ DS \_ MACHINE \_ ACCOUNT \_ QUOTA \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8557 (0x216D)
</dt> <dt>



No se pudo unir el equipo al dominio. Ha superado el número máximo de cuentas de equipo que puede crear en este dominio. Póngase en contacto con el administrador del sistema para restablecer o aumentar este límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MUST_BE_RUN_ON_DST_DC"></span><span id="error_ds_must_be_run_on_dst_dc"></span>**ERROR \_ DS \_ DEBE \_ \_ EJECUTARSE EN EL CONTROLADOR DE DOMINIO \_ DE \_ \_ DST**
</dt> <dd> <dl> <dt>

8558 (0x216E)
</dt> <dt>



Por motivos de seguridad, la operación debe ejecutarse en el controlador de dominio de destino.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SRC_DC_MUST_BE_SP4_OR_GREATER"></span><span id="error_ds_src_dc_must_be_sp4_or_greater"></span>**ERROR \_ DS \_ SRC \_ DC DEBE \_ \_ SER \_ SP4 O \_ \_ SUPERIOR**
</dt> <dd> <dl> <dt>

8559 (0x216F)
</dt> <dt>



Por motivos de seguridad, el controlador de dominio de origen debe ser NT4SP4 o superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_TREE_DELETE_CRITICAL_OBJ"></span><span id="error_ds_cant_tree_delete_critical_obj"></span>**ERROR \_ DS \_ CANT \_ TREE \_ DELETE \_ CRITICAL \_ OBJ**
</dt> <dd> <dl> <dt>

8560 (0x2170)
</dt> <dt>



Los objetos críticos del sistema de servicios de directorio no se pueden eliminar durante las operaciones de eliminación de árbol. Es posible que la eliminación del árbol se haya realizado parcialmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INIT_FAILURE_CONSOLE"></span><span id="error_ds_init_failure_console"></span>**ERROR \_ DS \_ INIT \_ FAILURE \_ CONSOLE**
</dt> <dd> <dl> <dt>

8561 (0x2171)
</dt> <dt>



No se pudo iniciar Servicios de directorio debido al siguiente error: %1. Estado de error: 0x%2. Haga clic en Aceptar para apagar el sistema. Puede usar la consola de recuperación para examinar el sistema más a fondo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SAM_INIT_FAILURE_CONSOLE"></span><span id="error_ds_sam_init_failure_console"></span>**ERROR \_ DS \_ SAM \_ INIT \_ FAILURE \_ CONSOLE**
</dt> <dd> <dl> <dt>

8562 (0x2172)
</dt> <dt>



Error de inicialización del Administrador de cuentas de seguridad debido al siguiente error: %1. Estado de error: 0x%2. Haga clic en Aceptar para apagar el sistema. Puede usar la consola de recuperación para examinar el sistema más a fondo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_HIGH"></span><span id="error_ds_forest_version_too_high"></span>**ERROR \_ DS \_ FOREST \_ VERSION \_ TOO \_ HIGH**
</dt> <dd> <dl> <dt>

8563 (0x2173)
</dt> <dt>



La versión del sistema operativo no es compatible con el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración. Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio de AD DS o agregar una instancia de AD LDS en este bosque de AD DS o en un conjunto de configuración AD LDS.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_HIGH"></span><span id="error_ds_domain_version_too_high"></span>**ERROR \_ DS \_ DOMAIN \_ VERSION \_ TOO \_ HIGH**
</dt> <dd> <dl> <dt>

8564 (0x2174)
</dt> <dt>



La versión del sistema operativo instalada no es compatible con el nivel funcional del dominio actual. Debe actualizar a una nueva versión del sistema operativo para que este servidor pueda convertirse en un controlador de dominio en este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FOREST_VERSION_TOO_LOW"></span><span id="error_ds_forest_version_too_low"></span>**ERROR \_ DS \_ FOREST \_ VERSION \_ TOO \_ LOW**
</dt> <dd> <dl> <dt>

8565 (0x2175)
</dt> <dt>



La versión del sistema operativo instalada en este servidor ya no admite el nivel funcional del bosque de AD DS actual o AD LDS nivel funcional del conjunto de configuración. Debe elevar el nivel funcional del bosque de AD DS o el nivel funcional del conjunto de configuración de AD LDS para que este servidor pueda convertirse en un controlador de dominio de AD DS o una instancia de AD LDS en este bosque o conjunto de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_VERSION_TOO_LOW"></span><span id="error_ds_domain_version_too_low"></span>**ERROR \_ DS \_ DOMAIN \_ VERSION \_ TOO \_ LOW**
</dt> <dd> <dl> <dt>

8566 (0x2176)
</dt> <dt>



La versión del sistema operativo instalada en este servidor ya no admite el nivel funcional de dominio actual. Debe aumentar el nivel funcional del dominio para que este servidor pueda convertirse en un controlador de dominio en este dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_VERSION"></span><span id="error_ds_incompatible_version"></span>**ERROR \_ DS \_ VERSIÓN INCOMPATIBLE \_**
</dt> <dd> <dl> <dt>

8567 (0x2177)
</dt> <dt>



La versión del sistema operativo instalada en este servidor no es compatible con el nivel funcional del dominio o bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_DSA_VERSION"></span><span id="error_ds_low_dsa_version"></span>**ERROR \_ DS \_ VERSIÓN BAJA DE \_ DSA \_**
</dt> <dd> <dl> <dt>

8568 (0x2178)
</dt> <dt>



El nivel funcional del dominio (o bosque) no se puede elevar al valor solicitado, porque hay uno o varios controladores de dominio en el dominio (o bosque) que están en un nivel funcional incompatible inferior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_BEHAVIOR_VERSION_IN_MIXEDDOMAIN"></span><span id="error_ds_no_behavior_version_in_mixeddomain"></span>**ERROR \_ DS \_ SIN VERSIÓN DE COMPORTAMIENTO EN \_ \_ \_ \_ MIXEDDOMAIN**
</dt> <dd> <dl> <dt>

8569 (0x2179)
</dt> <dt>



El nivel funcional del bosque no se puede elevar al valor solicitado, ya que uno o varios dominios todavía están en modo de dominio mixto. Todos los dominios del bosque deben estar en modo nativo para que pueda elevar el nivel funcional del bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_SUPPORTED_SORT_ORDER"></span><span id="error_ds_not_supported_sort_order"></span>**ERROR \_ DS \_ NO SE ADMITE EL CRITERIO DE \_ \_ \_ ORDENACIÓN**
</dt> <dd> <dl> <dt>

8570 (0x217A)
</dt> <dt>



No se admite el criterio de ordenación solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_NOT_UNIQUE"></span><span id="error_ds_name_not_unique"></span>**ERROR \_ DS \_ NAME \_ NOT \_ UNIQUE**
</dt> <dd> <dl> <dt>

8571 (0x217B)
</dt> <dt>



El nombre solicitado ya existe como identificador único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MACHINE_ACCOUNT_CREATED_PRENT4"></span><span id="error_ds_machine_account_created_prent4"></span>**ERROR \_ DS \_ MACHINE \_ ACCOUNT \_ CREATED \_ PRENT4**
</dt> <dd> <dl> <dt>

8572 (0x217C)
</dt> <dt>



La cuenta de equipo se creó antes de NT4. La cuenta debe volver a crearse.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OUT_OF_VERSION_STORE"></span><span id="error_ds_out_of_version_store"></span>**ERROR \_ DS \_ FUERA DEL ALMACÉN \_ DE \_ \_ VERSIONES**
</dt> <dd> <dl> <dt>

8573 (0x217D)
</dt> <dt>



La base de datos está fuera del almacén de versiones.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INCOMPATIBLE_CONTROLS_USED"></span><span id="error_ds_incompatible_controls_used"></span>**ERROR \_ DS \_ CONTROLES \_ INCOMPATIBLES \_ USADOS**
</dt> <dd> <dl> <dt>

8574 (0x217E)
</dt> <dt>



No se puede continuar la operación porque se usaron varios controles en conflicto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_REF_DOMAIN"></span><span id="error_ds_no_ref_domain"></span>**ERROR \_ DS \_ NO \_ REF \_ DOMAIN**
</dt> <dd> <dl> <dt>

8575 (0x217F)
</dt> <dt>



No se encuentra un dominio de referencia de descriptor de seguridad válido para esta partición.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_LINK_ID"></span><span id="error_ds_reserved_link_id"></span>**IDENTIFICADOR \_ DE VÍNCULO RESERVADO DE DS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8576 (0x2180)
</dt> <dt>



Error de actualización del esquema: el identificador de vínculo está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LINK_ID_NOT_AVAILABLE"></span><span id="error_ds_link_id_not_available"></span>**IDENTIFICADOR \_ DE VÍNCULO DS DE ERROR \_ NO \_ \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

8577 (0x2181)
</dt> <dt>



Error en la actualización del esquema: no hay identificadores de vínculo disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AG_CANT_HAVE_UNIVERSAL_MEMBER"></span><span id="error_ds_ag_cant_have_universal_member"></span>**ERROR \_ DS \_ AG \_ CANT \_ HAVE \_ UNIVERSAL \_ MEMBER**
</dt> <dd> <dl> <dt>

8578 (0x2182)
</dt> <dt>



Un grupo de cuentas no puede tener un grupo universal como miembro.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_INSTANCE_TYPE"></span><span id="error_ds_modifydn_disallowed_by_instance_type"></span>**ERROR \_ DS \_ MODIFYDN \_ NO PERMITIDO POR TIPO DE \_ \_ \_ INSTANCIA**
</dt> <dd> <dl> <dt>

8579 (0x2183)
</dt> <dt>



No se permiten operaciones de cambio de nombre o movimiento en los objetos de solo lectura o los objetos de contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_OBJECT_MOVE_IN_SCHEMA_NC"></span><span id="error_ds_no_object_move_in_schema_nc"></span>**ERROR \_ DS \_ NO SE MUEVE NINGÚN OBJETO EN EL NC DE \_ \_ \_ \_ \_ ESQUEMA**
</dt> <dd> <dl> <dt>

8580 (0x2184)
</dt> <dt>



No se permiten operaciones de movimiento en objetos en el contexto de nomenclatura del esquema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_DISALLOWED_BY_FLAG"></span><span id="error_ds_modifydn_disallowed_by_flag"></span>**ERROR \_ DS \_ MODIFYDN \_ DISALLOWED \_ BY \_ FLAG**
</dt> <dd> <dl> <dt>

8581 (0x2185)
</dt> <dt>



Se ha establecido una marca del sistema en el objeto y no permite mover ni cambiar el nombre del objeto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MODIFYDN_WRONG_GRANDPARENT"></span><span id="error_ds_modifydn_wrong_grandparent"></span>**ERROR \_ DS \_ MODIFYDN \_ WRONG \_ GRANDPARENT**
</dt> <dd> <dl> <dt>

8582 (0x2186)
</dt> <dt>



Este objeto no puede cambiar su contenedor primario principal. Los movimientos no están prohibidos en este objeto, pero están restringidos a los contenedores del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NAME_ERROR_TRUST_REFERRAL"></span><span id="error_ds_name_error_trust_referral"></span>**REFERENCIA DE \_ CONFIANZA DE ERRORES DE NOMBRE \_ DS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

8583 (0x2187)
</dt> <dt>



No se puede resolver completamente, se genera una referencia a otro bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_STANDARD_SERVER"></span><span id="error_not_supported_on_standard_server"></span>**ERROR \_ NO ADMITIDO EN EL SERVIDOR \_ \_ \_ \_ ESTÁNDAR**
</dt> <dd> <dl> <dt>

8584 (0x2188)
</dt> <dt>



La acción solicitada no se admite en el servidor estándar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_ACCESS_REMOTE_PART_OF_AD"></span><span id="error_ds_cant_access_remote_part_of_ad"></span>**ERROR DS CANT ACCESS REMOTE PART OF AD (ERROR \_ DS \_ NO PUEDE ACCEDER A LA PARTE REMOTA DE \_ \_ \_ \_ \_ AD)**
</dt> <dd> <dl> <dt>

8585 (0x2189)
</dt> <dt>



No se pudo acceder a una partición del servicio de directorio ubicado en un servidor remoto. Asegúrese de que al menos un servidor se está ejecutando para la partición en cuestión.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CR_IMPOSSIBLE_TO_VALIDATE_V2"></span><span id="error_ds_cr_impossible_to_validate_v2"></span>**ERROR \_ DS \_ CR \_ IMPOSSIBLE \_ TO \_ VALIDATE \_ V2**
</dt> <dd> <dl> <dt>

8586 (0x218A)
</dt> <dt>



El directorio no puede validar el nombre del contexto de nomenclatura propuesto (o partición) porque no contiene una réplica ni puede ponerse en contacto con una réplica del contexto de nomenclatura por encima del contexto de nomenclatura propuesto. Asegúrese de que el contexto de nomenclatura principal está registrado correctamente en DNS y que el maestro de nomenclatura de dominio puede acceder al menos a una réplica de este contexto de nomenclatura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_THREAD_LIMIT_EXCEEDED"></span><span id="error_ds_thread_limit_exceeded"></span>**ERROR \_ SE SUPERÓ EL \_ LÍMITE DE SUBPROCESOS \_ \_ DE DS**
</dt> <dd> <dl> <dt>

8587 (0x218B)
</dt> <dt>



Se superó el límite de subprocesos para esta solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NOT_CLOSEST"></span><span id="error_ds_not_closest"></span>**ERROR \_ DS \_ NOT \_ CLOSEST**
</dt> <dd> <dl> <dt>

8588 (0x218C)
</dt> <dt>



El servidor de catálogo global no está en el sitio más cercano.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_WITHOUT_SERVER_REF"></span><span id="error_ds_cant_derive_spn_without_server_ref"></span>**ERROR \_ DS \_ CANT \_ DERIVE \_ SPN \_ WITHOUT \_ SERVER \_ REF**
</dt> <dd> <dl> <dt>

8589 (0x218D)
</dt> <dt>



El DS no puede derivar un nombre de entidad de seguridad de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el objeto de servidor correspondiente de la base de datos DS local no tiene ningún atributo serverReference.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_SINGLE_USER_MODE_FAILED"></span><span id="error_ds_single_user_mode_failed"></span>**ERROR \_ DS \_ SINGLE \_ USER \_ MODE \_ FAILED**
</dt> <dd> <dl> <dt>

8590 (0x218E)
</dt> <dt>



El servicio de directorio no pudo entrar en modo de usuario único.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_SYNTAX_ERROR"></span><span id="error_ds_ntdscript_syntax_error"></span>**ERROR \_ DS \_ NTDSCRIPT \_ SYNTAX \_ ERROR**
</dt> <dd> <dl> <dt>

8591 (0x218F)
</dt> <dt>



El servicio de directorio no puede analizar el script debido a un error de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NTDSCRIPT_PROCESS_ERROR"></span><span id="error_ds_ntdscript_process_error"></span>**ERROR \_ DS \_ NTDSCRIPT \_ PROCESS \_ ERROR**
</dt> <dd> <dl> <dt>

8592 (0x2190)
</dt> <dt>



El servicio de directorio no puede procesar el script debido a un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DIFFERENT_REPL_EPOCHS"></span><span id="error_ds_different_repl_epochs"></span>**ERROR \_ DS \_ DIFFERENT \_ REPL \_ EPOCHS**
</dt> <dd> <dl> <dt>

8593 (0x2191)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada porque los servidores implicados son de diferentes épocas de replicación (que normalmente están relacionadas con un cambio de nombre de dominio que está en curso).


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRS_EXTENSIONS_CHANGED"></span><span id="error_ds_drs_extensions_changed"></span>**ERROR \_ DS \_ DRS \_ EXTENSIONS \_ CHANGED**
</dt> <dd> <dl> <dt>

8594 (0x2192)
</dt> <dt>



El enlace del servicio de directorio debe renegociarse debido a un cambio en la información de extensiones de servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPLICA_SET_CHANGE_NOT_ALLOWED_ON_DISABLED_CR"></span><span id="error_ds_replica_set_change_not_allowed_on_disabled_cr"></span>**ERROR \_ DS REPLICA SET CHANGE NOT ALLOWED ON DISABLED CR (ERROR DS \_ REPLICA SET CHANGE NOT ALLOWED ON DISABLED CR \_ \_ \_ \_ \_ )ERROR \_ DS REPLICA SET CHANGE NOT ALLOWED ON DISABLED \_ CR**
</dt> <dd> <dl> <dt>

8595 (0x2193)
</dt> <dt>



Operación no permitida en una referencia cruzada deshabilitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_MSDS_INTID"></span><span id="error_ds_no_msds_intid"></span>**ERROR \_ DS \_ NO \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8596 (0x2194)
</dt> <dt>



Error en la actualización del esquema: no hay valores disponibles para msDS-IntId.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUP_MSDS_INTID"></span><span id="error_ds_dup_msds_intid"></span>**ERROR \_ DS \_ DUP \_ MSDS \_ INTID**
</dt> <dd> <dl> <dt>

8597 (0x2195)
</dt> <dt>



Error en la actualización del esquema: msDS-INtId duplicado. Vuelva a intentar la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTS_IN_RDNATTID"></span><span id="error_ds_exists_in_rdnattid"></span>**ERROR \_ DS \_ EXISTE EN \_ \_ RDNATTID**
</dt> <dd> <dl> <dt>

8598 (0x2196)
</dt> <dt>



Error de eliminación del esquema: el atributo se usa en rDNAttID.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUTHORIZATION_FAILED"></span><span id="error_ds_authorization_failed"></span>**ERROR \_ ERROR AL AUTORIZACIÓN DE DS \_ \_**
</dt> <dd> <dl> <dt>

8599 (0x2197)
</dt> <dt>



El servicio de directorio no pudo autorizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SCRIPT"></span><span id="error_ds_invalid_script"></span>**ERROR \_ DS \_ SCRIPT NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8600 (0x2198)
</dt> <dt>



El servicio de directorio no puede procesar el script porque no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REMOTE_CROSSREF_OP_FAILED"></span><span id="error_ds_remote_crossref_op_failed"></span>**ERROR \_ DS \_ REMOTE \_ CROSSREF \_ OP \_ FAILED**
</dt> <dd> <dl> <dt>

8601 (0x2199)
</dt> <dt>



Error en la operación de creación remota de referencias cruzadas en el FSMO del maestro de nomenclatura de dominios. El error de la operación está en los datos extendidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CROSS_REF_BUSY"></span><span id="error_ds_cross_ref_busy"></span>**ERROR \_ DS \_ CROSS \_ REF \_ BUSY**
</dt> <dd> <dl> <dt>

8602 (0x219A)
</dt> <dt>



Una referencia cruzada se usa localmente con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DERIVE_SPN_FOR_DELETED_DOMAIN"></span><span id="error_ds_cant_derive_spn_for_deleted_domain"></span>**ERROR \_ DS \_ CANT \_ DERIVE \_ SPN \_ FOR \_ DELETED \_ DOMAIN**
</dt> <dd> <dl> <dt>

8603 (0x219B)
</dt> <dt>



El DS no puede derivar un nombre de entidad de seguridad de servicio (SPN) con el que autenticar mutuamente el servidor de destino porque el dominio del servidor se ha eliminado del bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_DEMOTE_WITH_WRITEABLE_NC"></span><span id="error_ds_cant_demote_with_writeable_nc"></span>**ERROR \_ DS \_ CANT \_ DEMOTE \_ WITH \_ WRITEABLE \_ NC**
</dt> <dd> <dl> <dt>

8604 (0x219C)
</dt> <dt>



Los NCs que se pueden escribir impiden que este controlador de dominio se desmoríba.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DUPLICATE_ID_FOUND"></span><span id="error_ds_duplicate_id_found"></span>**ERROR \_ DS \_ DUPLICATE \_ ID \_ FOUND**
</dt> <dd> <dl> <dt>

8605 (0x219D)
</dt> <dt>



El objeto solicitado tiene un identificador no único y no se puede recuperar.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INSUFFICIENT_ATTR_TO_CREATE_OBJECT"></span><span id="error_ds_insufficient_attr_to_create_object"></span>**ERROR \_ DS \_ INSUFFICIENT \_ ATTR \_ TO \_ CREATE \_ OBJECT**
</dt> <dd> <dl> <dt>

8606 (0x219E)
</dt> <dt>



Se han dado atributos insuficientes para crear un objeto . Es posible que este objeto no exista porque es posible que se haya eliminado y ya se haya recopilado la recolección de elementos no utilizados.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_GROUP_CONVERSION_ERROR"></span><span id="error_ds_group_conversion_error"></span>**ERROR \_ DS \_ GROUP \_ CONVERSION \_ ERROR**
</dt> <dd> <dl> <dt>

8607 (0x219F)
</dt> <dt>



El grupo no se puede convertir debido a restricciones de atributo en el tipo de grupo solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_BASIC_GROUP"></span><span id="error_ds_cant_move_app_basic_group"></span>**ERROR \_ DS \_ CANT \_ MOVE \_ APP \_ BASIC \_ GROUP**
</dt> <dd> <dl> <dt>

8608 (0x21A0)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de aplicaciones básicos no vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_CANT_MOVE_APP_QUERY_GROUP"></span><span id="error_ds_cant_move_app_query_group"></span>**ERROR \_ DS \_ CANT \_ MOVE \_ APP \_ QUERY \_ GROUP**
</dt> <dd> <dl> <dt>

8609 (0x21A1)
</dt> <dt>



No se permite el movimiento entre dominios de grupos de aplicaciones basados en consultas no vacíos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_ROLE_NOT_VERIFIED"></span><span id="error_ds_role_not_verified"></span>**ERROR \_ DS \_ ROLE \_ NOT \_ VERIFIED**
</dt> <dd> <dl> <dt>

8610 (0x21A2)
</dt> <dt>



No se pudo comprobar la propiedad del rol FSMO porque su partición de directorio no se ha replicado correctamente con al menos un asociado de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_WKO_CONTAINER_CANNOT_BE_SPECIAL"></span><span id="error_ds_wko_container_cannot_be_special"></span>**ERROR \_ DS \_ WKO \_ CONTAINER \_ CANNOT \_ BE \_ SPECIAL**
</dt> <dd> <dl> <dt>

8611 (0x21A3)
</dt> <dt>



El contenedor de destino para una redirección de un contenedor de objetos conocido no puede ser ya un contenedor especial.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_RENAME_IN_PROGRESS"></span><span id="error_ds_domain_rename_in_progress"></span>**ERROR \_ CAMBIO DE NOMBRE DE DOMINIO DE DS EN \_ \_ \_ \_ CURSO**
</dt> <dd> <dl> <dt>

8612 (0x21A4)
</dt> <dt>



El servicio de directorio no puede realizar la operación solicitada porque hay una operación de cambio de nombre de dominio en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_EXISTING_AD_CHILD_NC"></span><span id="error_ds_existing_ad_child_nc"></span>**ERROR \_ DS \_ EXISTING \_ AD \_ CHILD \_ NC**
</dt> <dd> <dl> <dt>

8613 (0x21A5)
</dt> <dt>



El servicio de directorio detectó una partición secundaria debajo del nombre de partición solicitado. La jerarquía de particiones debe crearse en un método de arriba abajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_REPL_LIFETIME_EXCEEDED"></span><span id="error_ds_repl_lifetime_exceeded"></span>**ERROR \_ DS \_ REPL \_ LIFETIME \_ EXCEEDED**
</dt> <dd> <dl> <dt>

8614 (0x21A6)
</dt> <dt>



El servicio de directorio no se puede replicar con este servidor porque el tiempo desde la última replicación con este servidor ha superado la duración de los objetos de desecho.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_IN_SYSTEM_CONTAINER"></span><span id="error_ds_disallowed_in_system_container"></span>**ERROR \_ DS \_ NO PERMITIDOS EN EL CONTENEDOR DEL \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

8615 (0x21A7)
</dt> <dt>



No se permite la operación solicitada en un objeto en el contenedor del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LDAP_SEND_QUEUE_FULL"></span><span id="error_ds_ldap_send_queue_full"></span>**ERROR \_ DS \_ LDAP \_ SEND \_ QUEUE \_ FULL**
</dt> <dd> <dl> <dt>

8616 (0x21A8)
</dt> <dt>



La cola de envío de red de servidores LDAP se ha rellenado porque el cliente no está procesando los resultados de sus solicitudes lo suficientemente rápido. No se procesarán más solicitudes hasta que el cliente se pondrá al día. Si el cliente no se pondrá al día, se desconectará.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_OUT_SCHEDULE_WINDOW"></span><span id="error_ds_dra_out_schedule_window"></span>**VENTANA \_ PROGRAMACIÓN \_ DE DRA OUT \_ \_ DE \_ ERROR DS**
</dt> <dd> <dl> <dt>

8617 (0x21A9)
</dt> <dt>



La replicación programada no tuvo lugar porque el sistema estaba demasiado ocupado para ejecutar la solicitud dentro de la ventana de programación. La cola de replicación está sobrecargada. Considere la posibilidad de reducir el número de asociados o reducir la frecuencia de replicación programada.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_POLICY_NOT_KNOWN"></span><span id="error_ds_policy_not_known"></span>**ERROR \_ NO SE CONOCE LA DIRECTIVA \_ \_ DE DS \_**
</dt> <dd> <dl> <dt>

8618 (0x21AA)
</dt> <dt>



En este momento, no se puede determinar si la directiva de replicación de rama está disponible en el controlador de dominio del centro. Vuelva a intentarlo más tarde para tener en cuenta las latencias de replicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SITE_SETTINGS_OBJECT"></span><span id="error_no_site_settings_object"></span>**ERROR \_ NO HAY OBJETO DE CONFIGURACIÓN DEL \_ \_ \_ SITIO**
</dt> <dd> <dl> <dt>

8619 (0x21AB)
</dt> <dt>



El objeto de configuración del sitio especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SECRETS"></span><span id="error_no_secrets"></span>**ERROR \_ SIN \_ SECRETOS**
</dt> <dd> <dl> <dt>

8620 (0x21AC)
</dt> <dt>



El almacén de cuentas local no contiene material secreto para la cuenta especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_WRITABLE_DC_FOUND"></span><span id="error_no_writable_dc_found"></span>**ERROR \_ NO SE ENCONTRÓ CONTROLADOR DE DOMINIO \_ \_ GRABABLE \_**
</dt> <dd> <dl> <dt>

8621 (0x21AD)
</dt> <dt>



No se encontró un controlador de dominio que se pueda escribir en el dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_SERVER_OBJECT"></span><span id="error_ds_no_server_object"></span>**ERROR \_ DS \_ NO \_ SERVER \_ OBJECT**
</dt> <dd> <dl> <dt>

8622 (0x21AE)
</dt> <dt>



El objeto de servidor para el controlador de dominio no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NO_NTDSA_OBJECT"></span><span id="error_ds_no_ntdsa_object"></span>**ERROR \_ DS \_ NO \_ NTDSA \_ OBJECT**
</dt> <dd> <dl> <dt>

8623 (0x21AF)
</dt> <dt>



El objeto Configuración NTDS para el controlador de dominio no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_NON_ASQ_SEARCH"></span><span id="error_ds_non_asq_search"></span>**ERROR \_ DS \_ NON \_ ASQ \_ SEARCH**
</dt> <dd> <dl> <dt>

8624 (0x21B0)
</dt> <dt>



La operación de búsqueda solicitada no se admite para las búsquedas de ASQ.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_AUDIT_FAILURE"></span><span id="error_ds_audit_failure"></span>**ERROR \_ DS \_ AUDIT \_ FAILURE**
</dt> <dd> <dl> <dt>

8625 (0x21B1)
</dt> <dt>



No se pudo generar un evento de auditoría necesario para la operación.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_SUBTREE"></span><span id="error_ds_invalid_search_flag_subtree"></span>**ERROR \_ \_ DS: \_ SUBÁRBOL DE MARCA DE BÚSQUEDA NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

8626 (0x21B2)
</dt> <dt>



Las marcas de búsqueda del atributo no son válidas. El bit de índice del subárbol solo es válido en atributos con un solo valor.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_INVALID_SEARCH_FLAG_TUPLE"></span><span id="error_ds_invalid_search_flag_tuple"></span>**ERROR \_ DS \_ INVALID \_ SEARCH \_ FLAG \_ TUPLE**
</dt> <dd> <dl> <dt>

8627 (0x21B3)
</dt> <dt>



Las marcas de búsqueda del atributo no son válidas. El bit de índice de tupla solo es válido en atributos de cadenas Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIERARCHY_TABLE_TOO_DEEP"></span><span id="error_ds_hierarchy_table_too_deep"></span>**ERROR \_ DS \_ HIERARCHY \_ TABLE \_ TOO \_ DEEP**
</dt> <dd> <dl> <dt>

8628 (0x21B4)
</dt> <dt>



Las libretas de direcciones están anidadas demasiado profundamente. No se pudo compilar la tabla de jerarquía.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_CORRUPT_UTD_VECTOR"></span><span id="error_ds_dra_corrupt_utd_vector"></span>**ERROR \_ DS \_ DRA \_ CORRUPT \_ UTD \_ VECTOR**
</dt> <dd> <dl> <dt>

8629 (0x21B5)
</dt> <dt>



El vector de ness actualizado especificado está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_SECRETS_DENIED"></span><span id="error_ds_dra_secrets_denied"></span>**ERROR \_ DS \_ DRA \_ SECRETS \_ DENIED**
</dt> <dd> <dl> <dt>

8630 (0x21B6)
</dt> <dt>



Se deniega la solicitud de replicación de secretos.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_RESERVED_MAPI_ID"></span><span id="error_ds_reserved_mapi_id"></span>**ERROR \_ DS \_ RESERVED \_ MAPI \_ ID**
</dt> <dd> <dl> <dt>

8631 (0x21B7)
</dt> <dt>



Error en la actualización del esquema: el identificador DE LAN está reservado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_MAPI_ID_NOT_AVAILABLE"></span><span id="error_ds_mapi_id_not_available"></span>**ERROR \_ DS \_ ID. DE MAPI \_ NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

8632 (0x21B8)
</dt> <dt>



Error en la actualización del esquema: no hay identificadores DE LAN disponibles.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_MISSING_KRBTGT_SECRET"></span><span id="error_ds_dra_missing_krbtgt_secret"></span>**ERROR \_ DS \_ DRA \_ MISSING \_ KRBTGT \_ SECRET**
</dt> <dd> <dl> <dt>

8633 (0x21B9)
</dt> <dt>



Error en la operación de replicación porque faltan los atributos necesarios del objeto krbtgt local.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DOMAIN_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_domain_name_exists_in_forest"></span>**ERROR \_ DS \_ DOMAIN \_ NAME \_ EXISTS \_ IN \_ FOREST**
</dt> <dd> <dl> <dt>

8634 (0x21BA)
</dt> <dt>



El nombre de dominio del dominio de confianza ya existe en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_FLAT_NAME_EXISTS_IN_FOREST"></span><span id="error_ds_flat_name_exists_in_forest"></span>**ERROR \_ DS \_ FLAT \_ NAME \_ EXISTS \_ IN \_ FOREST**
</dt> <dd> <dl> <dt>

8635 (0x21BB)
</dt> <dt>



El nombre plano del dominio de confianza ya existe en el bosque.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_USER_PRINCIPAL_NAME"></span><span id="error_invalid_user_principal_name"></span>**ERROR \_ NOMBRE PRINCIPAL DE USUARIO NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

8636 (0x21BC)
</dt> <dt>



El nombre principal de usuario (UPN) no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_MAPPED_GROUP_CANT_HAVE_MEMBERS"></span><span id="error_ds_oid_mapped_group_cant_have_members"></span>**ERROR \_ DS \_ OID \_ MAPPED \_ GROUP \_ CANT \_ HAVE \_ MEMBERS**
</dt> <dd> <dl> <dt>

8637 (0x21BD)
</dt> <dt>



Los grupos asignados por OID no pueden tener miembros.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_OID_NOT_FOUND"></span><span id="error_ds_oid_not_found"></span>**ERROR \_ DS \_ OID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

8638 (0x21BE)
</dt> <dt>



No se encuentra el OID especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DRA_RECYCLED_TARGET"></span><span id="error_ds_dra_recycled_target"></span>**ERROR \_ DS \_ DRA \_ RECYCLED \_ TARGET**
</dt> <dd> <dl> <dt>

8639 (0x21BF)
</dt> <dt>



Error en la operación de replicación porque se recicla el objeto de destino al que hace referencia un valor de vínculo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_DISALLOWED_NC_REDIRECT"></span><span id="error_ds_disallowed_nc_redirect"></span>**ERROR \_ DS \_ NO PERMITIDO REDIRECCIÓN \_ DE NC \_**
</dt> <dd> <dl> <dt>

8640 (0x21C0)
</dt> <dt>



Error en la operación de redireccionamiento porque el objeto de destino está en una NC diferente del controlador de dominio del controlador de dominio actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_ADLDS_FFL"></span><span id="error_ds_high_adlds_ffl"></span>**ERROR \_ DS \_ HIGH \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8641 (0x21C1)
</dt> <dt>



El nivel funcional del conjunto AD LDS configuración no se puede reducir al valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_HIGH_DSA_VERSION"></span><span id="error_ds_high_dsa_version"></span>**ERROR \_ DS \_ HIGH \_ DSA \_ VERSION**
</dt> <dd> <dl> <dt>

8642 (0x21C2)
</dt> <dt>



El nivel funcional del dominio (o bosque) no se puede reducir al valor solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_LOW_ADLDS_FFL"></span><span id="error_ds_low_adlds_ffl"></span>**ERROR \_ DS \_ LOW \_ ADLDS \_ FFL**
</dt> <dd> <dl> <dt>

8643 (0x21C3)
</dt> <dt>



El nivel funcional del conjunto de configuración AD LDS no se puede elevar al valor solicitado, porque hay una o varias instancias de ADLDS que se encuentran en un nivel funcional incompatible inferior.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_SID_SAME_AS_LOCAL_WORKSTATION"></span><span id="error_domain_sid_same_as_local_workstation"></span>**SID \_ DE DOMINIO DE ERROR IGUAL QUE LA ESTACIÓN DE TRABAJO \_ \_ \_ \_ \_ LOCAL**
</dt> <dd> <dl> <dt>

8644 (0x21C4)
</dt> <dt>



No se puede completar la unión al dominio porque el SID del dominio al que intentó unirse era idéntico al SID de esta máquina. Se trata de un síntoma de una instalación de sistema operativo clonada incorrectamente. Debe ejecutar sysprep en esta máquina para generar un nuevo SID de máquina. Consulte <https://go.microsoft.com/fwlink/p/?linkid=168895> para más información.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_UNDELETE_SAM_VALIDATION_FAILED"></span><span id="error_ds_undelete_sam_validation_failed"></span>**ERROR \_ DS \_ UNDELETE \_ SAM \_ VALIDATION \_ FAILED**
</dt> <dd> <dl> <dt>

8645 (0x21C5)
</dt> <dt>



Error en la operación de recuperación porque el nombre de cuenta sam o el nombre de cuenta sam adicional del objeto que se va a recuperar entra en conflicto con un objeto en directo existente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ACCOUNT_TYPE"></span><span id="error_incorrect_account_type"></span>**ERROR \_ TIPO DE CUENTA \_ \_ INCORRECTO**
</dt> <dd> <dl> <dt>

8646 (0x21C6)
</dt> <dt>



El sistema no es autoritativo para la cuenta especificada y, por tanto, no puede completar la operación. Vuelva a intentar la operación con el proveedor asociado a esta cuenta. Si se trata de un proveedor en línea, use el sitio en línea del proveedor.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 




