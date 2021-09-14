---
description: Describe los códigos de error 9000-11999 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Códigos de error del sistema (9000-11999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164573"
---
# <a name="system-error-codes-9000-11999"></a>Códigos de error del sistema (9000-11999)

> [!NOTE]
> Esta información está pensada para desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema (errores 9000 a 11999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**ERROR \_ DE \_ DNS: ERROR DE FORMATO RCODE \_ \_**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



El servidor DNS no puede interpretar el formato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**ERROR DE DNS \_ \_ RCODE \_ SERVER \_ FAILURE**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Error de servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**ERROR DE DNS \_ \_ RCODE \_ NAME \_ ERROR**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



El nombre DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**\_ERROR DE DNS \_ RCODE NO \_ \_ IMPLEMENTADO**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



La solicitud DNS no es compatible con el servidor de nombres.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**ERROR DE DNS \_ \_ RCODE \_ RECHAZADO**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Operación DNS rechazada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**\_ERROR DE DNS \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



El nombre DNS que no existe existe, existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**\_ERROR DE DNS \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



El conjunto rr. de DNS que no existe, existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**ERROR DE DNS \_ \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



El conjunto rr. de DNS que debería existir, no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**ERROR DE DNS \_ \_ RCODE \_ NOTAUTH**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



Servidor DNS no autoritativo para la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**ERROR DE DNS \_ \_ RCODE \_ NOTZONE**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



El nombre DNS de la actualización o la solicitud previa no está en la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**ERROR \_ DE \_ DNS RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



No se pudo comprobar la firma DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**ERROR \_ DE DNS \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Clave dns no es buena.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**ERROR \_ DE DNS \_ RCODE \_ BADTIME**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



La validez de la firma DNS ha expirado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**ERROR DE DNS \_ \_ KEYMASTER \_ REQUERIDO**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Solo el servidor DNS que actúa como maestro de claves para la zona puede realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**ERROR \_ DE DNS NO PERMITIDO EN LA ZONA \_ \_ \_ \_ \_ FIRMADA**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Esta operación no se permite en una zona que esté firmada o tenga claves de firma.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_ERROR DE DNS \_ NSEC3 \_ INCOMPATIBLE CON RSA \_ \_ \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



NSEC3 no es compatible con el algoritmo RSA-SHA-1. Elija otro algoritmo o use NSEC.

Este valor también se **denominaba DNS \_ ERROR INVALID \_ \_ NSEC3 \_ PARAMETERS**


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**ERROR \_ DE DNS NO HAY \_ \_ \_ SUFICIENTES \_ \_ DESCRIPTORES DE CLAVE DE FIRMA**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



La zona no tiene suficientes claves de firma. Debe haber al menos una clave de firma de claves (KSK) y al menos una clave de firma de zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**ALGORITMO \_ NO ADMITIDO DE ERROR \_ DE DNS \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



No se admite el algoritmo especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**ERROR DE DNS \_ TAMAÑO DE CLAVE NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



No se admite el tamaño de clave especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**CLAVE DE FIRMA DE ERROR DE DNS \_ \_ NO \_ \_ \_ ACCESIBLE**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Una o varias de las claves de firma de una zona no son accesibles para el servidor DNS. La firma de zona no estará operativa hasta que se resuelva este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**ERROR \_ DE DNS \_ KSP \_ NO ADMITE LA \_ \_ \_ PROTECCIÓN**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



El proveedor de almacenamiento de claves especificado no admite la protección de datos de DPAPI++. La firma de zona no estará operativa hasta que se resuelva este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**ERROR \_ DE DNS ERROR INESPERADO DE PROTECCIÓN DE \_ \_ \_ \_ DATOS**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Se encontró un error inesperado de DPAPI++. La firma de zona no estará operativa hasta que se resuelva este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**ERROR \_ DE DNS ERROR INESPERADO DE \_ \_ CNG \_**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Se encontró un error criptográfico inesperado. Es posible que la firma de zona no esté operativa hasta que se resuelva este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**ERROR DE DNS \_ VERSIÓN DESCONOCIDA DEL PARÁMETRO DE \_ \_ \_ \_ FIRMA**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



El servidor DNS encontró una clave de firma con una versión desconocida. La firma de zona no estará operativa hasta que se resuelva este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**ERROR \_ DE DNS \_ KSP \_ NO \_ ACCESIBLE**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



El servidor DNS no puede abrir el proveedor de servicios de claves especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**\_ERROR DE DNS \_ \_ DEMASIADOS \_ SKD**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



El servidor DNS no puede aceptar más claves de firma con el algoritmo y el valor de marca de KSK especificados para esta zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**ERROR DE DNS \_ \_ PERÍODO DE \_ SUVERSIÓN NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



El período de suversión especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**ERROR DE DNS \_ \_ DESPLAZAMIENTO INICIAL NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



El desplazamiento de suversión inicial especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**SUVERSIÓN DE ERRORES DE DNS \_ \_ EN \_ \_ CURSO**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



La clave de firma especificada ya está en proceso de revertir las claves.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**CLAVE \_ EN ESPERA DE ERROR DNS NO \_ \_ \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



La clave de firma especificada no tiene una clave en espera para revocar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_ERROR DE DNS NO PERMITIDO EN \_ \_ \_ \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Esta operación no se permite en una clave de firma de zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_ERROR DE DNS NO PERMITIDO EN \_ \_ \_ \_ \_ SKD ACTIVO**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Esta operación no se permite en una clave de firma activa.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**SUVERSIÓN DE ERRORES DE DNS \_ \_ YA ESTÁ EN \_ \_ COLA**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



La clave de firma especificada ya está en cola para su suversión.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_ERROR DE DNS NO PERMITIDO EN LA ZONA SIN \_ \_ \_ \_ \_ SIGNO**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Esta operación no se permite en una zona sin signo.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**ERROR DE DNS \_ \_ BAD \_ KEYMASTER**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



Esta operación no se pudo completar porque el servidor DNS que aparece como el maestro de claves actual para esta zona está fuera de servicio o está mal configurado. Resuelva el problema en el maestro de claves actual para esta zona o use otro servidor DNS para aprovechar el rol maestro de claves.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**ERROR DE DNS \_ PERÍODO DE VALIDEZ DE FIRMA NO \_ \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



El período de validez de la firma especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**RECUENTO \_ DE \_ \_ ITERACIONES DE NSEC3 NO VÁLIDO DE ERROR \_ \_ DNS**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



El recuento de iteraciones NSEC3 especificado es mayor que el permitido por la longitud de clave mínima usada en la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**DNS \_ ERROR \_ DNSSEC \_ IS \_ DISABLED**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



Esta operación no se pudo completar porque el servidor DNS se ha configurado con características DNSSEC deshabilitadas. Habilite DNSSEC en el servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**ERROR DE DNS \_ \_ XML NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



Esta operación no se pudo completar porque la secuencia XML recibida está vacía o no es válida sintácticamente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**\_ERROR DE DNS NO HAY \_ \_ \_ DELIMITADORES DE CONFIANZA \_ VÁLIDOS**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Esta operación se completó, pero no se agregaron anclajes de confianza porque todos los delimitadores de confianza recibidos no eran válidos, no se admiten, expiraban o no se convertían en válidos en menos de 30 días.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**SUVERSIÓN DE ERRORES DE DNS \_ \_ NO SE PUEDE \_ \_ PASAR**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



La clave de firma especificada no está esperando la actualización del DS parental.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**DNS \_ ERROR \_ NSEC3 \_ NAME \_ COLLISION**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



Se detectó una colisión de hash durante la firma de NSEC3. Especifique otro valor de sal proporcionado por el usuario o use un valor salt generado aleatoriamente e intente firmar de nuevo la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_ERROR DE DNS \_ NSEC INCOMPATIBLE CON \_ \_ \_ NSEC3 \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC no es compatible con el algoritmo NSEC3-RSA-SHA-1. Elija un algoritmo diferente o use NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**INFORMACIÓN DE DNS \_ \_ SIN \_ REGISTROS**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



No se ha encontrado ningún registro para la consulta DNS especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**ERROR \_ DE \_ DNS: PAQUETE NO ESTÁ \_ BIEN**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Paquete DNS no bueno.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**\_ERROR DE DNS NO \_ \_ PACKET**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



Ningún paquete DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**ERROR DE DNS \_ \_ RCODE**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Error de DNS, compruebe rcode.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**ERROR DE DNS \_ \_ PAQUETE NO \_ SEGURO**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Paquete DNS no seguro.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**SOLICITUD \_ DNS \_ PENDIENTE**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



La solicitud de consulta DNS está pendiente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**TIPO DE ERROR DE DNS \_ \_ NO \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Tipo DNS no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**\_ERROR DE DNS DIRECCIÓN IP NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Dirección IP no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**ERROR \_ DE \_ DNS: PROPIEDAD NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Propiedad no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**\_ERROR DE DNS \_ \_ INTÉNTELO DE NUEVO MÁS \_ TARDE**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Vuelva a intentar la operación DNS más adelante.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**\_ERROR DE DNS NO \_ \_ ÚNICO**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



El registro para el nombre y el tipo especificados no es único.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**ERROR DE DNS \_ \_ NOMBRE NO \_ RFC \_**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



El nombre DNS no cumple las especificaciones de RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**FQDN \_ DE \_ ESTADO DNS**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



El nombre DNS es un nombre DNS completo.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**NOMBRE \_ DE PUNTOS DE ESTADO \_ \_ DNS**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



El nombre DNS está punteado (varias etiquetas).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**NOMBRE \_ DE UNA SOLA PARTE DEL ESTADO \_ \_ \_ DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



El nombre DNS es un nombre de una sola parte.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**ERROR DE DNS \_ \_ NOMBRE NO VÁLIDO \_ \_ CHAR**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



El nombre DNS contiene un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**NOMBRE \_ NUMÉRICO DEL ERROR DE \_ \_ DNS**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



El nombre DNS es completamente numérico.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**ERROR \_ DE DNS NO PERMITIDO EN EL SERVIDOR \_ \_ \_ \_ \_ RAÍZ**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



La operación solicitada no se permite en un servidor raíz DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**ERROR \_ DE DNS NO PERMITIDO EN \_ \_ \_ \_ DELEGACIÓN**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



No se pudo crear el registro porque esta parte del espacio de nombres DNS se ha delegado a otro servidor.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**ERROR \_ DE DNS NO ENCUENTRA \_ \_ \_ \_ SUGERENCIAS RAÍZ**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



El servidor DNS no pudo encontrar un conjunto de sugerencias raíz.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**SUGERENCIAS \_ RAÍZ \_ \_ INCOHERENTES DE ERROR \_ DE DNS**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



El servidor DNS encontró sugerencias raíz, pero no eran coherentes en todos los adaptadores.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**VALOR \_ DWORD DE ERROR DE DNS \_ \_ DEMASIADO \_ \_ PEQUEÑO**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



El valor especificado es demasiado pequeño para este parámetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**VALOR \_ \_ DWORD DE ERROR DNS \_ DEMASIADO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



El valor especificado es demasiado grande para este parámetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**CARGA EN \_ SEGUNDO PLANO DE ERROR DE \_ \_ DNS**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Esta operación no se permite mientras el servidor DNS carga zonas en segundo plano. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**ERROR \_ DE DNS NO PERMITIDO EN \_ \_ \_ \_ RODC**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



La operación solicitada no se permite en en un servidor DNS que se ejecuta en un controlador de dominio de solo lectura.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**ERROR \_ DE DNS NO PERMITIDO EN \_ \_ \_ \_ DNAME**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



No se permite que existan datos debajo de un registro DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**DELEGACIÓN DE ERRORES DE DNS \_ \_ \_ REQUERIDA**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Esta operación requiere la delegación de credenciales.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**ERROR DE DNS \_ TABLA DE DIRECTIVAS NO \_ \_ \_ VÁLIDAS**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



La tabla de directivas de resolución de nombres está dañada. Se producirá un error en la resolución DNS hasta que se corrigió. Póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**LA \_ ZONA DE ERROR DNS NO \_ \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



La zona DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**ERROR DE DNS \_ \_ SIN INFORMACIÓN DE \_ \_ ZONA**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



La información de zona DNS no está disponible.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**ERROR DE DNS \_ OPERACIÓN DE ZONA NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Operación no válida para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**ERROR \_ DE CONFIGURACIÓN DE ZONA DE ERROR DE \_ \_ \_ DNS**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Configuración de zona DNS no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**LA \_ ZONA DE ERROR DNS NO TIENE NINGÚN REGISTRO \_ \_ \_ \_ SOA \_**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



La zona DNS no tiene ningún registro de inicio de autoridad (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**LA \_ ZONA DE ERROR DNS NO TIENE REGISTROS \_ \_ \_ \_ NS \_**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



La zona DNS no tiene ningún registro de servidor de nombres (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**ZONA \_ DE ERROR DNS \_ \_ BLOQUEADA**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



La zona DNS está bloqueada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**ERROR AL \_ CREAR LA ZONA DE ERROR \_ \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



Error al crear la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**ZONA \_ DE ERROR DNS YA \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



La zona DNS ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**YA \_ EXISTE LA ZONA AUTOMÁTICA DE ERROR \_ \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



La zona automática dns ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**ERROR DE DNS \_ TIPO DE ZONA NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Tipo de zona DNS no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**DNS \_ ERROR SECONDARY REQUIRES MASTER IP (DNS ERROR SECUNDARIO REQUIERE DIRECCIÓN IP \_ \_ \_ \_ MAESTRA)**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



La zona DNS secundaria requiere una dirección IP maestra.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**ZONA \_ DE ERROR DNS NO \_ \_ \_ SECUNDARIA**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Zona DNS no secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**ERROR \_ DE DNS NECESITA DIRECCIONES \_ \_ \_ SECUNDARIAS**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



Necesita una dirección IP secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**ERROR \_ DE \_ DNS: ERROR DE \_ INIT \_**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Error de inicialización de WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**ERROR \_ DE DNS NECESITA SERVIDORES \_ \_ WINS \_**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Necesita servidores WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**ERROR \_ DE DNS \_ NBSTAT \_ INIT \_ FAILED**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Error en la llamada de inicialización de NBTSTAT.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**\_ERROR DE DNS \_ SOA DELETE \_ \_ INVALID**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Eliminación no válida del inicio de autoridad (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**EL \_ \_ REENVIADOR DE ERRORES DE DNS \_ \_ YA EXISTE**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Ya existe una zona de reenvío condicional para ese nombre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**LA ZONA DE ERROR DE DNS \_ REQUIERE UNA DIRECCIÓN IP \_ \_ \_ \_ MAESTRA**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Esta zona debe configurarse con una o varias direcciones IP del servidor DNS maestro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**LA ZONA DE ERROR DE DNS \_ \_ ESTÁ \_ \_ APAGADA**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



No se puede realizar la operación porque esta zona está apagada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**ZONA \_ DE ERROR DNS BLOQUEADA PARA \_ \_ \_ \_ FIRMA**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



Esta operación no se puede realizar porque la zona se está firmando actualmente. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**EL ERROR DE DNS \_ \_ PRINCIPAL REQUIERE \_ \_ DATAFILE**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



La zona DNS principal requiere un archivo de datos.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**ERROR DE DNS \_ NOMBRE DE ARCHIVO DE DATOS NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Nombre de archivo de datos no válido para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**ERROR DE DNS \_ \_ DATAFILE \_ OPEN \_ FAILURE**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



No se pudo abrir el archivo de datos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**ERROR \_ DE ESCRITURA \_ REESCRIBIDA DEL ARCHIVO DE ERROR \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



No se pudo escribir el archivo de datos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**ANÁLISIS DE ARCHIVOS DE DATOS DE ERROR \_ \_ DE DNS \_**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Error al leer el archivo de datos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**EL REGISTRO DE ERRORES DE DNS \_ \_ NO \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



El registro DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**FORMATO \_ DE REGISTRO DE ERRORES DE \_ \_ DNS**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Error de formato de registro DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**ERROR DE \_ DNS ERROR AL CREAR EL \_ \_ \_ NODO**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Error de creación de nodos en DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**TIPO \_ DE REGISTRO DESCONOCIDO DE ERROR \_ \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Tipo de registro DNS desconocido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**TIEMPO \_ DE ESPERA DEL REGISTRO DE ERRORES \_ \_ DE \_ DNS**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



Se ha pasado el tiempo de espera del registro DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**NOMBRE \_ DE ERROR DNS NO ESTÁ EN LA \_ \_ \_ \_ ZONA**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



Nombre que no está en la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**ERROR DE DNS \_ \_ BUCLE \_ CNAME**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Se detectó un bucle CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**EL \_ NODO DE ERROR DNS ES \_ \_ \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



Node es un registro DNS CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**COLISIÓN \_ DE CNAME DE ERROR \_ DE \_ DNS**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Ya existe un registro CNAME para un nombre determinado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**REGISTRO \_ DE ERRORES DNS SOLO EN LA RAÍZ DE \_ \_ \_ \_ \_ ZONA**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Registre solo en la raíz de la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**EL REGISTRO DE ERRORES DE DNS \_ \_ YA \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



El registro DNS ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**DATOS \_ SECUNDARIOS DE ERROR DE \_ \_ DNS**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Error de datos de la zona DNS secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**ERROR DE DNS \_ NO CREAR DATOS DE \_ \_ \_ CACHÉ \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



No se pudieron crear datos de caché DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**EL \_ NOMBRE DEL ERROR DNS NO \_ \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



El nombre DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**ERROR \_ DE CREACIÓN DE PTR DE ADVERTENCIA \_ \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



No se pudo crear el registro de puntero (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**DOMINIO DE ADVERTENCIA DE DNS \_ \_ \_ ELIMINADO**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



Se ha eliminado el dominio DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**\_ERROR DE DNS \_ DS NO \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



El servicio de directorio no está disponible.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**DNS \_ ERROR \_ DS \_ ZONE \_ ALREADY \_ EXISTS**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



La zona DNS ya existe en el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**DNS \_ ERROR \_ NO \_ BOOTFILE \_ IF \_ DS \_ ZONE**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



El servidor DNS no crea ni lee el archivo de arranque para la zona DNS integrada del servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**EL \_ NODO DE ERROR DNS ES \_ \_ \_ DNAME**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



Node es un registro DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**COLISIÓN \_ DE DNAME DE ERROR \_ \_ DE DNS**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Ya existe un registro DNAME para un nombre determinado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**BUCLE \_ DE ALIAS DE ERROR DE \_ \_ DNS**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



Se ha detectado un bucle de alias con registros CNAME o DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**AXFR DE INFORMACIÓN DE DNS \_ \_ \_ COMPLETADO**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



AXFR de DNS (transferencia de zona) completado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**ERROR DE DNS \_ \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



Error de transferencia de zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**DNS \_ INFO \_ ADDED \_ LOCAL \_ WINS**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Se ha agregado el servidor WINS local.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**ESTADO DNS \_ \_ NECESARIO \_**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



La llamada de actualización segura debe continuar con la solicitud de actualización.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**\_ERROR DE DNS NO \_ \_ TCPIP**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



El protocolo de red TCP/IP no está instalado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**\_ERROR DNS NO HAY SERVIDORES \_ \_ \_ DNS**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



No hay servidores DNS configurados para el sistema local.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**EL DP DE ERROR DE DNS \_ \_ NO \_ \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



La partición de directorio especificada no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**EL DP DE ERROR DE DNS \_ \_ YA \_ \_ EXISTE**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



La partición de directorio especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**ERROR DE DNS \_ \_ DP NO \_ \_ INSCRITO**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Este servidor DNS no está inscrito en la partición de directorio especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**DP DE ERROR DE DNS \_ \_ YA DADO DE \_ \_ ALTA**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Este servidor DNS ya está dado de alta en la partición de directorio especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**ERROR DE DNS \_ \_ DP NO \_ \_ DISPONIBLE**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



La partición de directorio no está disponible en este momento. Espere unos minutos y vuelva a intentarlo.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**ERROR DE DNS \_ \_ DP \_ FSMO \_ ERROR**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



Error en la operación porque no se pudo alcanzar el rol FSMO maestro de nomenclatura de dominio. El controlador de dominio que mantiene el rol FSMO del maestro de nomenclatura de dominio está sin servicio o no puede dar servicio a la solicitud o no está ejecutando Windows Server 2003 o posterior.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Una llamada a WSACancelBlockingCall interrumpió una operación de bloqueo.


</dt> </dl> </dd> <dt>

<span id="WSAEBADF"></span><span id="wsaebadf"></span>**WSAEBADF**
</dt> <dd> <dl> <dt>

10009 (0x2719)
</dt> <dt>



El identificador de archivo proporcionado no es válido.


</dt> </dl> </dd> <dt>

<span id="WSAEACCES"></span><span id="wsaeacces"></span>**WSAEACCES**
</dt> <dd> <dl> <dt>

10013 (0x271D)
</dt> <dt>



Se intentó acceder a un socket de una manera prohibida por sus permisos de acceso.


</dt> </dl> </dd> <dt>

<span id="WSAEFAULT"></span><span id="wsaefault"></span>**WSAEFAULT**
</dt> <dd> <dl> <dt>

10014 (0x271E)
</dt> <dt>



El sistema detectó una dirección de puntero no válida al intentar usar un argumento de puntero en una llamada.


</dt> </dl> </dd> <dt>

<span id="WSAEINVAL"></span><span id="wsaeinval"></span>**WSAEINVAL**
</dt> <dd> <dl> <dt>

10022 (0x2726)
</dt> <dt>



Se proporcionó un argumento no válido.


</dt> </dl> </dd> <dt>

<span id="WSAEMFILE"></span><span id="wsaemfile"></span>**WSAEMFILE**
</dt> <dd> <dl> <dt>

10024 (0x2728)
</dt> <dt>



Demasiados sockets abiertos.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



No se pudo completar inmediatamente una operación de socket sin bloqueo.


</dt> </dl> </dd> <dt>

<span id="WSAEINPROGRESS"></span><span id="wsaeinprogress"></span>**WSAEINPROGRESS**
</dt> <dd> <dl> <dt>

10036 (0x2734)
</dt> <dt>



Se está ejecutando una operación de bloqueo actualmente.


</dt> </dl> </dd> <dt>

<span id="WSAEALREADY"></span><span id="wsaealready"></span>**WSAEALREADY**
</dt> <dd> <dl> <dt>

10037 (0x2735)
</dt> <dt>



Se ha intentado una operación en un socket que no es de bloqueo y que ya tenía una operación en marcha.


</dt> </dl> </dd> <dt>

<span id="WSAENOTSOCK"></span><span id="wsaenotsock"></span>**WSAENOTSOCK**
</dt> <dd> <dl> <dt>

10038 (0x2736)
</dt> <dt>



Se intentó realizar una operación en algo que no es un socket.


</dt> </dl> </dd> <dt>

<span id="WSAEDESTADDRREQ"></span><span id="wsaedestaddrreq"></span>**WSAEDESTADDRREQ**
</dt> <dd> <dl> <dt>

10039 (0x2737)
</dt> <dt>



Se omitió una dirección necesaria de una operación en un socket.


</dt> </dl> </dd> <dt>

<span id="WSAEMSGSIZE"></span><span id="wsaemsgsize"></span>**WSAEMSGSIZE**
</dt> <dd> <dl> <dt>

10040 (0x2738)
</dt> <dt>



Un mensaje enviado en un socket de datagrama es más largo que el búfer de mensajes interno o que algún otro límite de la red, o bien el búfer usado para recibir un datagrama es más pequeño que el datagrama.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTOTYPE"></span><span id="wsaeprototype"></span>**WSAEPROTOTYPE**
</dt> <dd> <dl> <dt>

10041 (0x2739)
</dt> <dt>



Se especificó un protocolo en la llamada de función de socket que no admite la semántica del tipo de socket solicitado.


</dt> </dl> </dd> <dt>

<span id="WSAENOPROTOOPT"></span><span id="wsaenoprotoopt"></span>**WSAENOPROTOOPT**
</dt> <dd> <dl> <dt>

10042 (0x273A)
</dt> <dt>



Se especificó una opción o un nivel desconocidos, no válidos o no admitidos en una llamada a getsockopt o setsockopt.


</dt> </dl> </dd> <dt>

<span id="WSAEPROTONOSUPPORT"></span><span id="wsaeprotonosupport"></span>**WSAEPROTONOSUPPORT**
</dt> <dd> <dl> <dt>

10043 (0x273B)
</dt> <dt>



El protocolo solicitado no se ha configurado en el sistema o no existe ninguna implementación para él.


</dt> </dl> </dd> <dt>

<span id="WSAESOCKTNOSUPPORT"></span><span id="wsaesocktnosupport"></span>**WSAESOCKTNOSUPPORT**
</dt> <dd> <dl> <dt>

10044 (0x273C)
</dt> <dt>



Esta familia de direcciones no es compatible con el tipo de socket especificado.


</dt> </dl> </dd> <dt>

<span id="WSAEOPNOTSUPP"></span><span id="wsaeopnotsupp"></span>**WSAEOPNOTSUPP**
</dt> <dd> <dl> <dt>

10045 (0x273D)
</dt> <dt>



La operación intentada no se admite para el tipo de objeto al que se hace referencia.


</dt> </dl> </dd> <dt>

<span id="WSAEPFNOSUPPORT"></span><span id="wsaepfnosupport"></span>**WSAEPFNOSUPPORT**
</dt> <dd> <dl> <dt>

10046 (0x273E)
</dt> <dt>



La familia de protocolos no se ha configurado en el sistema o no existe ninguna implementación para ella.


</dt> </dl> </dd> <dt>

<span id="WSAEAFNOSUPPORT"></span><span id="wsaeafnosupport"></span>**WSAEAFNOSUPPORT**
</dt> <dd> <dl> <dt>

10047 (0x273F)
</dt> <dt>



Se usó una dirección incompatible con el protocolo solicitado.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRINUSE"></span><span id="wsaeaddrinuse"></span>**WSAEADDRINUSE**
</dt> <dd> <dl> <dt>

10048 (0x2740)
</dt> <dt>



Only one usage of each socket address (protocol/network address/port) is normally permitted.


</dt> </dl> </dd> <dt>

<span id="WSAEADDRNOTAVAIL"></span><span id="wsaeaddrnotavail"></span>**WSAEADDRNOTAVAIL**
</dt> <dd> <dl> <dt>

10049 (0x2741)
</dt> <dt>



La dirección solicitada no es válida en su contexto.


</dt> </dl> </dd> <dt>

<span id="WSAENETDOWN"></span><span id="wsaenetdown"></span>**WSAENETDOWN**
</dt> <dd> <dl> <dt>

10050 (0x2742)
</dt> <dt>



Una operación de socket encontró una red inactiva.


</dt> </dl> </dd> <dt>

<span id="WSAENETUNREACH"></span><span id="wsaenetunreach"></span>**WSAENETUNREACH**
</dt> <dd> <dl> <dt>

10051 (0x2743)
</dt> <dt>



Se intentó realizar una operación de socket en una red inaccesible.


</dt> </dl> </dd> <dt>

<span id="WSAENETRESET"></span><span id="wsaenetreset"></span>**WSAENETRESET**
</dt> <dd> <dl> <dt>

10052 (0x2744)
</dt> <dt>



La conexión se ha roto debido a que la actividad de mantenimiento activo detectó un error mientras la operación estaba en curso.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECOBORTED**
</dt> <dd> <dl> <dt>

10053 (0x2745)
</dt> <dt>



El software del equipo host anuló una conexión establecida.


</dt> </dl> </dd> <dt>

<span id="WSAECONNRESET"></span><span id="wsaeconnreset"></span>**WSAECONNRESET**
</dt> <dd> <dl> <dt>

10054 (0x2746)
</dt> <dt>



El host remoto forzó el cierre de la conexión existente.


</dt> </dl> </dd> <dt>

<span id="WSAENOBUFS"></span><span id="wsaenobufs"></span>**WSAENOBUFS**
</dt> <dd> <dl> <dt>

10055 (0x2747)
</dt> <dt>



No se pudo realizar una operación en un socket porque el sistema no tenía suficiente espacio en búfer o porque una cola estaba llena.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Se realizó una solicitud de conexión en un socket ya conectado.


</dt> </dl> </dd> <dt>

<span id="WSAENOTCONN"></span><span id="wsaenotconn"></span>**WSAENOTCONN**
</dt> <dd> <dl> <dt>

10057 (0x2749)
</dt> <dt>



No se permitió una solicitud de envío o recepción de datos debido a que el socket no está conectado y no se especificó ninguna dirección al realizar el envío en un socket de datagrama mediante una llamada sendto.


</dt> </dl> </dd> <dt>

<span id="WSAESHUTDOWN"></span><span id="wsaeshutdown"></span>**WSAESHUTDOWN**
</dt> <dd> <dl> <dt>

10058 (0x274A)
</dt> <dt>



No se ha permitido la solicitud para enviar o recibir datos porque el socket ya se había apagado en esa dirección con una llamada de apagado previa.


</dt> </dl> </dd> <dt>

<span id="WSAETOOMANYREFS"></span><span id="wsaetoomanyrefs"></span>**WSAETOOMANYREFS**
</dt> <dd> <dl> <dt>

10059 (0x274B)
</dt> <dt>



Demasiadas referencias a algún objeto de kernel.


</dt> </dl> </dd> <dt>

<span id="WSAETIMEDOUT"></span><span id="wsaetimedout"></span>**WSAETIMEDOUT**
</dt> <dd> <dl> <dt>

10060 (0x274C)
</dt> <dt>



Error en un intento de conexión porque la parte conectada no respondió correctamente después de un período de tiempo o se ha establecido un error en la conexión porque el host conectado no ha podido responder.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



No se pudo realizar ninguna conexión porque la máquina de destino la rechazó activamente.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



No se puede traducir el nombre.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



El nombre o componente de nombre era demasiado largo.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



Error en una operación de socket porque el host de destino estaba fuera de servicio.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTUNREACH"></span><span id="wsaehostunreach"></span>**WSAEHOSTUNREACH**
</dt> <dd> <dl> <dt>

10065 (0x2751)
</dt> <dt>



Se intentó realizar una operación de socket a un host inalcanzable.


</dt> </dl> </dd> <dt>

<span id="WSAENOTEMPTY"></span><span id="wsaenotempty"></span>**WSAENOTEMPTY**
</dt> <dd> <dl> <dt>

10066 (0x2752)
</dt> <dt>



No se puede quitar un directorio que no esté vacío.


</dt> </dl> </dd> <dt>

<span id="WSAEPROCLIM"></span><span id="wsaeproclim"></span>**WSAEPROCLIM**
</dt> <dd> <dl> <dt>

10067 (0x2753)
</dt> <dt>



Una implementación Windows Sockets puede tener un límite en el número de aplicaciones que pueden usarla simultáneamente.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSDÚPLEXERS**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Se ha quedo sin cuota.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Se ha quedo sin cuota de disco.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



La referencia del identificador de archivo ya no está disponible.


</dt> </dl> </dd> <dt>

<span id="WSAEREMOTE"></span><span id="wsaeremote"></span>**WSAEREMOTE**
</dt> <dd> <dl> <dt>

10071 (0x2757)
</dt> <dt>



El elemento no está disponible localmente.


</dt> </dl> </dd> <dt>

<span id="WSASYSNOTREADY"></span><span id="wsasysnotready"></span>**WSASYSNOTREADY**
</dt> <dd> <dl> <dt>

10091 (0x276B)
</dt> <dt>



WSAStartup no puede funcionar en este momento porque el sistema subyacente que usa para proporcionar servicios de red no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



No Windows la versión de Sockets solicitada.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



La aplicación no ha llamado a WSAStartup o WSAStartup ha dado error.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Devuelto por WSARecv o WSARecvFrom para indicar que la parte remota ha iniciado una secuencia de apagado estable.


</dt> </dl> </dd> <dt>

<span id="WSAENOMORE"></span><span id="wsaenomore"></span>**WSAENOMORE**
</dt> <dd> <dl> <dt>

10102 (0x2776)
</dt> <dt>



WSALookupServiceNext no puede devolver más resultados.


</dt> </dl> </dd> <dt>

<span id="WSAECANCELLED"></span><span id="wsaecancelled"></span>**WSAECANCELLED**
</dt> <dd> <dl> <dt>

10103 (0x2777)
</dt> <dt>



Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando. La llamada se ha cancelado.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROCTABLE"></span><span id="wsaeinvalidproctable"></span>**WSAEINVALIDPROCTABLE**
</dt> <dd> <dl> <dt>

10104 (0x2778)
</dt> <dt>



La tabla de llamadas a procedimientos no es válida.


</dt> </dl> </dd> <dt>

<span id="WSAEINVALIDPROVIDER"></span><span id="wsaeinvalidprovider"></span>**WSAEINVALIDPROVIDER**
</dt> <dd> <dl> <dt>

10105 (0x2779)
</dt> <dt>



El proveedor de servicios solicitado no es válido.


</dt> </dl> </dd> <dt>

<span id="WSAEPROVIDERFAILEDINIT"></span><span id="wsaeproviderfailedinit"></span>**WSAEPROVIDERFAILEDINIT**
</dt> <dd> <dl> <dt>

10106 (0x277A)
</dt> <dt>



No se pudo cargar ni inicializar el proveedor de servicios solicitado.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Error en una llamada del sistema.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**WSASERVICE \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



No se conoce este servicio. El servicio no se encuentra en el espacio de nombres especificado.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**WSATYPE \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



No se encontró la clase especificada.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ NO \_ MORE**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



WSALookupServiceNext no puede devolver más resultados.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ CANCELLED**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando. La llamada se ha cancelado.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Error en una consulta de base de datos porque se rechazó activamente.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**WSAHOST \_ NO \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



Se desconoce el host.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY \_ AGAIN**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Éste es normalmente un error temporal durante la resolución de nombres de host y significa que el servidor local no recibió una respuesta de un servidor autorizado.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**RECUPERACIÓN DE WSANO \_**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



Se produjo un error no recuperable durante una búsqueda de base de datos.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**DATOS DE \_ WSANO**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



El nombre solicitado es válido, pero no se encontró ningún dato del tipo solicitado.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**RECEPTORES \_ DE QOS WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



Ha llegado al menos una reserva.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**REMITENTES \_ DE QOS DE WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



Ha llegado al menos una ruta de acceso.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**WSA \_ QOS \_ NO \_ SENDERS**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



No hay remitentes.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**WSA \_ QOS \_ SIN \_ RECEPTORES**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



No hay receptores.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**SOLICITUD DE \_ QOS DE WSA \_ \_ CONFIRMADA**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



Se ha confirmado la reserva.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**ERROR DE ADMISIÓN \_ DE QOS \_ WSA \_**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Error debido a la falta de recursos.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**ERROR DE DIRECTIVA DE QOS DE \_ WSA \_ \_**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Rechazado por motivos administrativos: credenciales no válidas.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**ESTILO DE \_ CALIDAD DE SERVICIO DE WSA \_ \_**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Estilo desconocido o en conflicto.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**WSA \_ QOS \_ BAD \_ OBJECT**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Problema con alguna parte del búfer filterspec o providerspecific en general.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**ERROR DE \_ CTRL DE TRÁFICO DE QOS \_ WSA \_ \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Problema con alguna parte de flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**ERROR GENÉRICO \_ DE QOS DE WSA \_ \_**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Error general de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**WSA \_ QOS \_ ESERVICETYPE**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



Se encontró un tipo de servicio no válido o no reconocido en flowspec.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de QOS de WSA \_**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



Se encontró un valor flowspec no válido o incoherente en la estructura qos.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**WSA \_ QOS \_ EPROVSPECBUF**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Búfer específico del proveedor de QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**WSA \_ QOS \_ EFILTERSTYLE**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



Se usó un estilo de filtro QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**WSA \_ QOS \_ EFILTERTYPE**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



Se usó un tipo de filtro QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**WSA \_ QOS \_ EFILTERCOUNT**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



Se especificó un número incorrecto de FILTROS DE QOS EN FLOWDESCRIPTOR.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**WSA \_ QOS \_ EOBJLENGTH**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



Se especificó un objeto con un campo ObjectLength no válido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**WSA \_ QOS \_ EFLOWCOUNT**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



Se especificó un número incorrecto de descriptores de flujo en la estructura qos.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**WSA \_ QOS \_ EUNNPSOBJ**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



Se encontró un objeto desconocido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**WSA \_ QOS \_ EPOLICYOBJ**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



Se encontró un objeto de directiva no válido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de QOS \_ WSA**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



Se encontró un descriptor de flujo qos no válido en la lista de descriptores de flujo.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**WSA \_ QOS \_ EPSFLOWSPEC**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



Se encontró una clase flowspec no válida o incoherente en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**WSA \_ QOS \_ EPSFILTERSPEC**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



Se encontró un FILTERSPEC no válido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**WSA \_ QOS \_ ESDMODEOBJ**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



Se encontró un objeto de modo de descarte de forma no válido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**WSA \_ QOS \_ ESHAPERATEOBJ**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



Se encontró un objeto de velocidad de modelado no válido en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**WSA \_ QOS \_ RESERVED \_ PETYPE**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Se encontró un elemento de directiva reservada en el búfer específico del proveedor de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**NO SE ENCUENTRA \_ \_ EL HOST SEGURO \_ DE \_ WSA**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



Este host no se conoce de forma segura.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**ERROR DE DIRECTIVA \_ DE NOMBRE DE WSA IPSEC \_ \_ \_**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



No se pudo agregar la directiva IPSEC basada en nombres.


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

 

 




