---
description: Describe los códigos de error 9000-11999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 27fe3fee-4ae3-43f1-a1f2-91c935e9851b
title: Códigos de error del sistema (9000-11999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 01eb071962d8d0f5beb801067ce1d72adc796bad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807435"
---
# <a name="system-error-codes-9000-11999"></a>Códigos de error del sistema (9000-11999)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 9000 a 11999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="DNS_ERROR_RCODE_FORMAT_ERROR"></span><span id="dns_error_rcode_format_error"></span>**\_error de \_ formato de RCODE de error de DNS \_ \_**
</dt> <dd> <dl> <dt>

9001 (0x2329)
</dt> <dt>



El servidor DNS no puede interpretar el formato.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_SERVER_FAILURE"></span><span id="dns_error_rcode_server_failure"></span>**error de DNS del \_ \_ \_ servidor RCODE \_**
</dt> <dd> <dl> <dt>

9002 (0x232A)
</dt> <dt>



Error de servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NAME_ERROR"></span><span id="dns_error_rcode_name_error"></span>**error \_ de \_ nombre de RCODE de error de \_ DNS \_**
</dt> <dd> <dl> <dt>

9003 (0x232B)
</dt> <dt>



El nombre DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOT_IMPLEMENTED"></span><span id="dns_error_rcode_not_implemented"></span>**ERROR de DNS \_ \_ RCODE \_ no \_ implementado**
</dt> <dd> <dl> <dt>

9004 (0x232C)
</dt> <dt>



La solicitud DNS no es compatible con el servidor de nombres.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_REFUSED"></span><span id="dns_error_rcode_refused"></span>**RCODE de error de DNS \_ \_ \_ rechazado**
</dt> <dd> <dl> <dt>

9005 (0x232D)
</dt> <dt>



Operación DNS rechazada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXDOMAIN"></span><span id="dns_error_rcode_yxdomain"></span>**ERROR de DNS \_ \_ RCODE \_ YXDOMAIN**
</dt> <dd> <dl> <dt>

9006 (0x232E)
</dt> <dt>



Existe un nombre DNS que no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_YXRRSET"></span><span id="dns_error_rcode_yxrrset"></span>**ERROR de DNS \_ \_ RCODE \_ YXRRSET**
</dt> <dd> <dl> <dt>

9007 (0x232F)
</dt> <dt>



El conjunto de RR DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NXRRSET"></span><span id="dns_error_rcode_nxrrset"></span>**ERROR de DNS \_ \_ RCODE \_ NXRRSET**
</dt> <dd> <dl> <dt>

9008 (0x2330)
</dt> <dt>



El valor de RR de DNS establecido debe existir, no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTAUTH"></span><span id="dns_error_rcode_notauth"></span>**ERROR de DNS \_ \_ RCODE \_ NOTAUTH**
</dt> <dd> <dl> <dt>

9009 (0x2331)
</dt> <dt>



El servidor DNS no es autoritativo para la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_NOTZONE"></span><span id="dns_error_rcode_notzone"></span>**ERROR de DNS \_ \_ RCODE \_ NOTZONE**
</dt> <dd> <dl> <dt>

9010 (0x2332)
</dt> <dt>



El nombre DNS de la actualización o prereq no está en la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADSIG"></span><span id="dns_error_rcode_badsig"></span>**ERROR de DNS \_ \_ RCODE \_ BADSIG**
</dt> <dd> <dl> <dt>

9016 (0x2338)
</dt> <dt>



No se pudo comprobar la firma DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADKEY"></span><span id="dns_error_rcode_badkey"></span>**ERROR de DNS \_ \_ RCODE \_ BADKEY**
</dt> <dd> <dl> <dt>

9017 (0x2339)
</dt> <dt>



Clave incorrecta de DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE_BADTIME"></span><span id="dns_error_rcode_badtime"></span>**ERROR de DNS \_ \_ RCODE \_ BADTIME**
</dt> <dd> <dl> <dt>

9018 (0x233A)
</dt> <dt>



Expiró la validez de la firma DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KEYMASTER_REQUIRED"></span><span id="dns_error_keymaster_required"></span>**Maestro de error de DNS \_ \_ \_ requerido**
</dt> <dd> <dl> <dt>

9101 (0x238D)
</dt> <dt>



Solo el servidor DNS que actúa como maestro de claves para la zona puede realizar esta operación.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_SIGNED_ZONE"></span><span id="dns_error_not_allowed_on_signed_zone"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ zona firmada \_**
</dt> <dd> <dl> <dt>

9102 (0x238E)
</dt> <dt>



Esta operación no se permite en una zona firmada o con claves de firma.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_INCOMPATIBLE_WITH_RSA_SHA1"></span><span id="dns_error_nsec3_incompatible_with_rsa_sha1"></span>**\_Error \_ de DNS NSEC3 \_ incompatible \_ con \_ RSA \_ SHA1**
</dt> <dd> <dl> <dt>

9103 (0x238F)
</dt> <dt>



NSEC3 no es compatible con el algoritmo RSA-SHA-1. Elija un algoritmo diferente o use NSEC.

Este valor también se denominaba **DNS \_ error de \_ \_ NSEC3 \_ parámetros no válidos** .


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ENOUGH_SIGNING_KEY_DESCRIPTORS"></span><span id="dns_error_not_enough_signing_key_descriptors"></span>**ERROR de DNS \_ \_ no \_ hay suficientes \_ \_ descriptores de clave de firma \_**
</dt> <dd> <dl> <dt>

9104 (0x2390)
</dt> <dt>



La zona no tiene suficientes claves de firma. Debe haber al menos una clave de firma de clave (KSK) y al menos una clave de firma de zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSUPPORTED_ALGORITHM"></span><span id="dns_error_unsupported_algorithm"></span>**algoritmo de error de DNS \_ \_ no admitido \_**
</dt> <dd> <dl> <dt>

9105 (0x2391)
</dt> <dt>



No se admite el algoritmo especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_KEY_SIZE"></span><span id="dns_error_invalid_key_size"></span>**ERROR de DNS \_ \_ tamaño de clave no válido \_ \_**
</dt> <dd> <dl> <dt>

9106 (0x2392)
</dt> <dt>



No se admite el tamaño de clave especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SIGNING_KEY_NOT_ACCESSIBLE"></span><span id="dns_error_signing_key_not_accessible"></span>**clave de firma de error de DNS \_ \_ \_ \_ no \_ accesible**
</dt> <dd> <dl> <dt>

9107 (0x2393)
</dt> <dt>



Una o varias de las claves de firma para una zona no son accesibles para el servidor DNS. La firma de zona no estará operativa hasta que se solucione este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_DOES_NOT_SUPPORT_PROTECTION"></span><span id="dns_error_ksp_does_not_support_protection"></span>**el \_ KSP error de DNS no \_ admite la \_ \_ \_ \_ protección**
</dt> <dd> <dl> <dt>

9108 (0x2394)
</dt> <dt>



El proveedor de almacenamiento de claves especificado no admite la protección de datos de DPAPI + +. La firma de zona no estará operativa hasta que se solucione este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_DATA_PROTECTION_ERROR"></span><span id="dns_error_unexpected_data_protection_error"></span>**error \_ de \_ \_ protección de datos inesperado de error \_ de DNS \_**
</dt> <dd> <dl> <dt>

9109 (0x2395)
</dt> <dt>



Se encontró un error de DPAPI + + inesperado. La firma de zona no estará operativa hasta que se solucione este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNEXPECTED_CNG_ERROR"></span><span id="dns_error_unexpected_cng_error"></span>**error de error de \_ \_ CNG inesperado de DNS \_ \_**
</dt> <dd> <dl> <dt>

9110 (0x2396)
</dt> <dt>



Se encontró un error de cifrado inesperado. Es posible que la firma de zona no esté operativa hasta que se solucione este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_SIGNING_PARAMETER_VERSION"></span><span id="dns_error_unknown_signing_parameter_version"></span>**ERROR de DNS \_ \_ versión de \_ parámetro de firma desconocida \_ \_**
</dt> <dd> <dl> <dt>

9111 (0x2397)
</dt> <dt>



El servidor DNS encontró una clave de firma con una versión desconocida. La firma de zona no estará operativa hasta que se solucione este error.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_KSP_NOT_ACCESSIBLE"></span><span id="dns_error_ksp_not_accessible"></span>**\_KSP error de DNS \_ \_ no \_ accesible**
</dt> <dd> <dl> <dt>

9112 (0x2398)
</dt> <dt>



El servidor DNS no puede abrir el proveedor de servicios de claves especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TOO_MANY_SKDS"></span><span id="dns_error_too_many_skds"></span>**ERROR de DNS \_ \_ demasiados \_ \_ SKDS**
</dt> <dd> <dl> <dt>

9113 (0x2399)
</dt> <dt>



El servidor DNS no puede aceptar más claves de firma con el algoritmo especificado y el valor de la marca de KSK para esta zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ROLLOVER_PERIOD"></span><span id="dns_error_invalid_rollover_period"></span>**ERROR de DNS \_ \_ período de sustitución no válido \_ \_**
</dt> <dd> <dl> <dt>

9114 (0x239A)
</dt> <dt>



El período de sustitución especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_INITIAL_ROLLOVER_OFFSET"></span><span id="dns_error_invalid_initial_rollover_offset"></span>**ERROR de DNS \_ \_ \_ desplazamiento de sustitución inicial no válido \_ \_**
</dt> <dd> <dl> <dt>

9115 (0x239B)
</dt> <dt>



El desplazamiento de sustitución inicial especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_IN_PROGRESS"></span><span id="dns_error_rollover_in_progress"></span>**\_ \_ sustitución de errores \_ de DNS en \_ curso**
</dt> <dd> <dl> <dt>

9116 (0x239C)
</dt> <dt>



La clave de firma especificada ya está en proceso de revertir las claves.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_STANDBY_KEY_NOT_PRESENT"></span><span id="dns_error_standby_key_not_present"></span>**ERROR de DNS en \_ \_ espera de \_ clave \_ no \_ presente**
</dt> <dd> <dl> <dt>

9117 (0x239D)
</dt> <dt>



La clave de firma especificada no tiene una clave de espera para revocar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ZSK"></span><span id="dns_error_not_allowed_on_zsk"></span>**\_error \_ de DNS no \_ permitido \_ en \_ ZSK**
</dt> <dd> <dl> <dt>

9118 (0x239E)
</dt> <dt>



Esta operación no se permite en una clave de firma de zona (ZSK).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ACTIVE_SKD"></span><span id="dns_error_not_allowed_on_active_skd"></span>**\_error \_ de DNS no \_ permitido en el \_ \_ \_ SKD activo**
</dt> <dd> <dl> <dt>

9119 (0x239F)
</dt> <dt>



Esta operación no se permite en una clave de firma activa.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_ALREADY_QUEUED"></span><span id="dns_error_rollover_already_queued"></span>**sustitución de errores de DNS \_ \_ \_ ya \_ en cola**
</dt> <dd> <dl> <dt>

9120 (0x23A0)
</dt> <dt>



La clave de firma especificada ya está en cola para la sustitución.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_UNSIGNED_ZONE"></span><span id="dns_error_not_allowed_on_unsigned_zone"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ zona sin firmar \_**
</dt> <dd> <dl> <dt>

9121 (0x23A1)
</dt> <dt>



Esta operación no se permite en una zona sin firmar.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_KEYMASTER"></span><span id="dns_error_bad_keymaster"></span>**\_error de \_ DNS \_ maestro erróneo**
</dt> <dd> <dl> <dt>

9122 (0x23A2)
</dt> <dt>



No se pudo completar esta operación porque el servidor DNS que aparece como el maestro de claves actual para esta zona está inactivo o no está configurado correctamente. Resuelva el problema en el maestro de claves actual para esta zona o use otro servidor DNS para asumir el rol de maestro de claves.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_SIGNATURE_VALIDITY_PERIOD"></span><span id="dns_error_invalid_signature_validity_period"></span>**ERROR de DNS \_ \_ período de validez de firma no válido \_ \_ \_**
</dt> <dd> <dl> <dt>

9123 (0x23A3)
</dt> <dt>



El período de validez de la firma especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NSEC3_ITERATION_COUNT"></span><span id="dns_error_invalid_nsec3_iteration_count"></span>**\_Error de \_ DNS \_ \_ recuento de iteraciones de NSEC3 no válido \_**
</dt> <dd> <dl> <dt>

9124 (0x23A4)
</dt> <dt>



El número de iteraciones de NSEC3 especificado es mayor que el permitido por la longitud de clave mínima usada en la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNSSEC_IS_DISABLED"></span><span id="dns_error_dnssec_is_disabled"></span>**ERROR de DNS \_ \_ DNSSEC \_ \_ deshabilitado**
</dt> <dd> <dl> <dt>

9125 (0x23A5)
</dt> <dt>



No se pudo completar esta operación porque el servidor DNS se ha configurado con las características DNSSEC deshabilitadas. Habilite DNSSEC en el servidor DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_XML"></span><span id="dns_error_invalid_xml"></span>**ERROR de DNS \_ \_ XML no válido \_**
</dt> <dd> <dl> <dt>

9126 (0x23A6)
</dt> <dt>



No se pudo completar esta operación porque el flujo XML recibido está vacío o no es válido sintácticamente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_VALID_TRUST_ANCHORS"></span><span id="dns_error_no_valid_trust_anchors"></span>**ERROR de DNS \_ \_ sin \_ \_ anclajes de veracidad válidos \_**
</dt> <dd> <dl> <dt>

9127 (0x23A7)
</dt> <dt>



Esta operación se completó, pero no se agregaron anclajes de veracidad porque todos los anclajes de veracidad recibidos no eran válidos, no se admitían, expiraron o no eran válidos en menos de 30 días.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ROLLOVER_NOT_POKEABLE"></span><span id="dns_error_rollover_not_pokeable"></span>**sustitución de error de DNS \_ \_ \_ no se pudo escribir \_**
</dt> <dd> <dl> <dt>

9128 (0x23A8)
</dt> <dt>



La clave de firma especificada no está esperando la actualización del DS parental.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC3_NAME_COLLISION"></span><span id="dns_error_nsec3_name_collision"></span>**Colisión de nombre de error de DNS \_ \_ NSEC3 \_ \_**
</dt> <dd> <dl> <dt>

9129 (0x23A9)
</dt> <dt>



Colisión de hash detectada durante la firma de NSEC3. Especifique un valor Salt proporcionado por el usuario diferente o use un valor Salt generado aleatoriamente e intente volver a firmar la zona.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NSEC_INCOMPATIBLE_WITH_NSEC3_RSA_SHA1"></span><span id="dns_error_nsec_incompatible_with_nsec3_rsa_sha1"></span>**\_Error \_ de DNS NSEC \_ incompatible \_ con el \_ \_ RSA \_ SHA1 de NSEC3**
</dt> <dd> <dl> <dt>

9130 (0x23AA)
</dt> <dt>



NSEC no es compatible con el algoritmo NSEC3-RSA-SHA-1. Elija un algoritmo diferente o use NSEC3.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_NO_RECORDS"></span><span id="dns_info_no_records"></span>**\_ \_ no hay registros de información de DNS \_**
</dt> <dd> <dl> <dt>

9501 (0x251D)
</dt> <dt>



No se ha encontrado ningún registro para la consulta DNS especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BAD_PACKET"></span><span id="dns_error_bad_packet"></span>**ERROR de DNS en el \_ \_ \_ paquete incorrecto**
</dt> <dd> <dl> <dt>

9502 (0x251E)
</dt> <dt>



Paquete DNS incorrecto.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_PACKET"></span><span id="dns_error_no_packet"></span>**ERROR de DNS \_ \_ sin \_ paquete**
</dt> <dd> <dl> <dt>

9503 (0x251F)
</dt> <dt>



No hay ningún paquete DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RCODE"></span><span id="dns_error_rcode"></span>**\_RCODE de error de DNS \_**
</dt> <dd> <dl> <dt>

9504 (0x2520)
</dt> <dt>



Error de DNS, compruebe RCODE.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNSECURE_PACKET"></span><span id="dns_error_unsecure_packet"></span>**ERROR de DNS \_ : \_ paquete no seguro \_**
</dt> <dd> <dl> <dt>

9505 (0x2521)
</dt> <dt>



Paquete DNS no seguro.


</dt> </dl> </dd> <dt>

<span id="DNS_REQUEST_PENDING"></span><span id="dns_request_pending"></span>**solicitud de DNS \_ \_ pendiente**
</dt> <dd> <dl> <dt>

9506 (0x2522)
</dt> <dt>



La solicitud de consulta DNS está pendiente.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_TYPE"></span><span id="dns_error_invalid_type"></span>**tipo de error de DNS \_ \_ no válido \_**
</dt> <dd> <dl> <dt>

9551 (0x254F)
</dt> <dt>



Tipo de DNS no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_IP_ADDRESS"></span><span id="dns_error_invalid_ip_address"></span>**ERROR de DNS de \_ \_ \_ dirección IP no válida \_**
</dt> <dd> <dl> <dt>

9552 (0x2550)
</dt> <dt>



Dirección IP no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_PROPERTY"></span><span id="dns_error_invalid_property"></span>**\_propiedad error de DNS \_ no válida \_**
</dt> <dd> <dl> <dt>

9553 (0x2551)
</dt> <dt>



Propiedad no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_TRY_AGAIN_LATER"></span><span id="dns_error_try_again_later"></span>**ERROR de DNS \_ \_ inténtelo de \_ nuevo \_ más tarde**
</dt> <dd> <dl> <dt>

9554 (0x2552)
</dt> <dt>



Vuelva a intentar la operación DNS más tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_UNIQUE"></span><span id="dns_error_not_unique"></span>**ERROR de DNS \_ \_ no \_ único**
</dt> <dd> <dl> <dt>

9555 (0x2553)
</dt> <dt>



El registro para el nombre y el tipo especificados no es único.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NON_RFC_NAME"></span><span id="dns_error_non_rfc_name"></span>**ERROR de DNS \_ \_ no \_ \_ nombre RFC**
</dt> <dd> <dl> <dt>

9556 (0x2554)
</dt> <dt>



El nombre DNS no cumple las especificaciones RFC.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_FQDN"></span><span id="dns_status_fqdn"></span>**\_FQDN de estado de DNS \_**
</dt> <dd> <dl> <dt>

9557 (0x2555)
</dt> <dt>



Nombre DNS es un nombre DNS completo.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_DOTTED_NAME"></span><span id="dns_status_dotted_name"></span>**\_nombre con \_ puntos de estado de DNS \_**
</dt> <dd> <dl> <dt>

9558 (0x2556)
</dt> <dt>



El nombre DNS tiene puntos (varias etiquetas).


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_SINGLE_PART_NAME"></span><span id="dns_status_single_part_name"></span>**\_nombre de \_ una sola \_ parte \_ de estado de DNS**
</dt> <dd> <dl> <dt>

9559 (0x2557)
</dt> <dt>



El nombre DNS es un nombre de una sola parte.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_NAME_CHAR"></span><span id="dns_error_invalid_name_char"></span>**ERROR de DNS \_ \_ nombre no válido \_ \_ Char**
</dt> <dd> <dl> <dt>

9560 (0x2558)
</dt> <dt>



El nombre DNS contiene un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NUMERIC_NAME"></span><span id="dns_error_numeric_name"></span>**\_ \_ nombre numérico del error de DNS \_**
</dt> <dd> <dl> <dt>

9561 (0x2559)
</dt> <dt>



El nombre DNS es totalmente numérico.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_ROOT_SERVER"></span><span id="dns_error_not_allowed_on_root_server"></span>**\_error \_ de DNS no \_ permitido en el \_ \_ \_ servidor raíz**
</dt> <dd> <dl> <dt>

9562 (0x255A)
</dt> <dt>



La operación solicitada no se permite en un servidor raíz DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DELEGATION"></span><span id="dns_error_not_allowed_under_delegation"></span>**\_error \_ de DNS no \_ permitido en la \_ \_ delegación**
</dt> <dd> <dl> <dt>

9563 (0x255B)
</dt> <dt>



No se pudo crear el registro porque esta parte del espacio de nombres DNS se ha delegado en otro servidor.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CANNOT_FIND_ROOT_HINTS"></span><span id="dns_error_cannot_find_root_hints"></span>**ERROR de DNS \_ \_ no se \_ encuentran \_ sugerencias de raíz \_**
</dt> <dd> <dl> <dt>

9564 (0x255C)
</dt> <dt>



El servidor DNS no encontró un conjunto de sugerencias de raíz.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INCONSISTENT_ROOT_HINTS"></span><span id="dns_error_inconsistent_root_hints"></span>**ERROR de DNS \_ : \_ sugerencias de raíz incoherentes \_ \_**
</dt> <dd> <dl> <dt>

9565 (0x255D)
</dt> <dt>



El servidor DNS encontró sugerencias de raíz pero no eran coherentes en todos los adaptadores.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_SMALL"></span><span id="dns_error_dword_value_too_small"></span>**\_valor DWORD de error de DNS \_ \_ \_ demasiado \_ pequeño**
</dt> <dd> <dl> <dt>

9566 (0x255E)
</dt> <dt>



El valor especificado es demasiado pequeño para este parámetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DWORD_VALUE_TOO_LARGE"></span><span id="dns_error_dword_value_too_large"></span>**\_valor DWORD de error de DNS \_ \_ \_ demasiado \_ grande**
</dt> <dd> <dl> <dt>

9567 (0x255F)
</dt> <dt>



El valor especificado es demasiado grande para este parámetro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_BACKGROUND_LOADING"></span><span id="dns_error_background_loading"></span>**\_ \_ carga en segundo plano de error de DNS \_**
</dt> <dd> <dl> <dt>

9568 (0x2560)
</dt> <dt>



Esta operación no está permitida mientras el servidor DNS está cargando zonas en segundo plano. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_ON_RODC"></span><span id="dns_error_not_allowed_on_rodc"></span>**\_error \_ de DNS no \_ permitido \_ en \_ RODC**
</dt> <dd> <dl> <dt>

9569 (0x2561)
</dt> <dt>



La operación solicitada no se permite en un servidor DNS que se ejecuta en un controlador de dominio de solo lectura.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NOT_ALLOWED_UNDER_DNAME"></span><span id="dns_error_not_allowed_under_dname"></span>**\_error \_ de DNS no \_ permitido \_ en \_ dname**
</dt> <dd> <dl> <dt>

9570 (0x2562)
</dt> <dt>



No se permite la existencia de datos debajo de un registro DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DELEGATION_REQUIRED"></span><span id="dns_error_delegation_required"></span>**se \_ \_ requiere la delegación de error de DNS \_**
</dt> <dd> <dl> <dt>

9571 (0x2563)
</dt> <dt>



Esta operación requiere la delegación de credenciales.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_POLICY_TABLE"></span><span id="dns_error_invalid_policy_table"></span>**ERROR de DNS en la \_ \_ tabla de directivas no válida \_ \_**
</dt> <dd> <dl> <dt>

9572 (0x2564)
</dt> <dt>



La tabla de directivas de resolución de nombres está dañada. Se producirá un error en la resolución de DNS hasta que se corrija. Póngase en contacto con el administrador de red.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_DOES_NOT_EXIST"></span><span id="dns_error_zone_does_not_exist"></span>**\_ \_ \_ \_ no \_ existe la zona de errores de DNS**
</dt> <dd> <dl> <dt>

9601 (0x2581)
</dt> <dt>



La zona DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_ZONE_INFO"></span><span id="dns_error_no_zone_info"></span>**ERROR de DNS \_ \_ no hay \_ información de zona \_**
</dt> <dd> <dl> <dt>

9602 (0x2582)
</dt> <dt>



Información de zona DNS no disponible.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_OPERATION"></span><span id="dns_error_invalid_zone_operation"></span>**ERROR de DNS \_ \_ operación de zona no válida \_ \_**
</dt> <dd> <dl> <dt>

9603 (0x2583)
</dt> <dt>



Operación no válida para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CONFIGURATION_ERROR"></span><span id="dns_error_zone_configuration_error"></span>**\_error de \_ configuración de zona de error de DNS \_ \_**
</dt> <dd> <dl> <dt>

9604 (0x2584)
</dt> <dt>



Configuración de zona DNS no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_SOA_RECORD"></span><span id="dns_error_zone_has_no_soa_record"></span>**la \_ zona de errores de DNS \_ \_ \_ no tiene ningún \_ \_ registro SOA**
</dt> <dd> <dl> <dt>

9605 (0x2585)
</dt> <dt>



La zona DNS no tiene registro de inicio de autoridad (SOA).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_HAS_NO_NS_RECORDS"></span><span id="dns_error_zone_has_no_ns_records"></span>**la \_ zona de errores de DNS \_ \_ \_ no tiene \_ \_ registros NS**
</dt> <dd> <dl> <dt>

9606 (0x2586)
</dt> <dt>



La zona DNS no tiene un registro de servidor de nombres (NS).


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED"></span><span id="dns_error_zone_locked"></span>**zona de errores de DNS \_ \_ \_ bloqueada**
</dt> <dd> <dl> <dt>

9607 (0x2587)
</dt> <dt>



La zona DNS está bloqueada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_CREATION_FAILED"></span><span id="dns_error_zone_creation_failed"></span>**\_ \_ \_ \_ no se pudo crear la zona de errores de DNS**
</dt> <dd> <dl> <dt>

9608 (0x2588)
</dt> <dt>



No se pudo crear la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_ALREADY_EXISTS"></span><span id="dns_error_zone_already_exists"></span>**\_ \_ \_ ya existe una zona de errores de DNS \_**
</dt> <dd> <dl> <dt>

9609 (0x2589)
</dt> <dt>



La zona DNS ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AUTOZONE_ALREADY_EXISTS"></span><span id="dns_error_autozone_already_exists"></span>**ERROR de DNS \_ \_ AutoZone \_ ya \_ existe**
</dt> <dd> <dl> <dt>

9610 (0x258A)
</dt> <dt>



La zona automática DNS ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_ZONE_TYPE"></span><span id="dns_error_invalid_zone_type"></span>**ERROR de DNS \_ \_ tipo de zona no válida \_ \_**
</dt> <dd> <dl> <dt>

9611 (0x258B)
</dt> <dt>



Tipo de zona DNS no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_REQUIRES_MASTER_IP"></span><span id="dns_error_secondary_requires_master_ip"></span>**el \_ secundario de error de DNS \_ requiere una \_ \_ \_ dirección IP maestra**
</dt> <dd> <dl> <dt>

9612 (0x258C)
</dt> <dt>



La zona DNS secundaria requiere una dirección IP maestra.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_NOT_SECONDARY"></span><span id="dns_error_zone_not_secondary"></span>**zona de errores de DNS \_ \_ \_ no \_ secundaria**
</dt> <dd> <dl> <dt>

9613 (0x258D)
</dt> <dt>



Zona DNS no secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_SECONDARY_ADDRESSES"></span><span id="dns_error_need_secondary_addresses"></span>**los \_ errores de DNS \_ necesitan \_ direcciones secundarias \_**
</dt> <dd> <dl> <dt>

9614 (0x258E)
</dt> <dt>



Se necesita una dirección IP secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_WINS_INIT_FAILED"></span><span id="dns_error_wins_init_failed"></span>**\_ \_ \_ \_ no se pudo inicializar el error de DNS WINS init**
</dt> <dd> <dl> <dt>

9615 (0x258F)
</dt> <dt>



Error de inicialización de WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NEED_WINS_SERVERS"></span><span id="dns_error_need_wins_servers"></span>**\_los errores de DNS \_ necesitan \_ \_ servidores WINS**
</dt> <dd> <dl> <dt>

9616 (0x2590)
</dt> <dt>



Necesita servidores WINS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NBSTAT_INIT_FAILED"></span><span id="dns_error_nbstat_init_failed"></span>**error de DNS \_ \_ NBSTAT \_ init \_**
</dt> <dd> <dl> <dt>

9617 (0x2591)
</dt> <dt>



Error en la llamada de inicialización de NBTSTAT.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SOA_DELETE_INVALID"></span><span id="dns_error_soa_delete_invalid"></span>**ERROR de DNS \_ \_ SOA de \_ eliminación \_ no válida**
</dt> <dd> <dl> <dt>

9618 (0x2592)
</dt> <dt>



Eliminación de inicio de autoridad (SOA) no válida.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FORWARDER_ALREADY_EXISTS"></span><span id="dns_error_forwarder_already_exists"></span>**el \_ reenviador de errores de DNS \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

9619 (0x2593)
</dt> <dt>



Ya existe una zona de reenvío condicional para ese nombre.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_REQUIRES_MASTER_IP"></span><span id="dns_error_zone_requires_master_ip"></span>**la \_ zona de errores de DNS \_ requiere una \_ \_ \_ dirección IP maestra**
</dt> <dd> <dl> <dt>

9620 (0x2594)
</dt> <dt>



Esta zona debe estar configurada con una o más direcciones IP de servidor DNS maestro.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_IS_SHUTDOWN"></span><span id="dns_error_zone_is_shutdown"></span>**la \_ zona de errores de DNS \_ \_ está \_ apagada**
</dt> <dd> <dl> <dt>

9621 (0x2595)
</dt> <dt>



No se puede realizar la operación porque esta zona está apagada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ZONE_LOCKED_FOR_SIGNING"></span><span id="dns_error_zone_locked_for_signing"></span>**\_ \_ zona de errores \_ de DNS bloqueada \_ para \_ firmar**
</dt> <dd> <dl> <dt>

9622 (0x2596)
</dt> <dt>



No se puede realizar esta operación porque la zona se está firmando actualmente. Vuelva a intentarlo más tarde.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_PRIMARY_REQUIRES_DATAFILE"></span><span id="dns_error_primary_requires_datafile"></span>**el \_ error de DNS \_ principal \_ requiere un archivo de \_ archivos**
</dt> <dd> <dl> <dt>

9651 (0x25B3)
</dt> <dt>



La zona DNS principal requiere un archivo de archivos.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_INVALID_DATAFILE_NAME"></span><span id="dns_error_invalid_datafile_name"></span>**ERROR de DNS \_ \_ nombre de archivo de archivos no válido \_ \_**
</dt> <dd> <dl> <dt>

9652 (0x25B4)
</dt> <dt>



Nombre de archivo de la zona DNS no válido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_OPEN_FAILURE"></span><span id="dns_error_datafile_open_failure"></span>**error \_ de \_ apertura de archivo de archivo de errores de \_ DNS \_**
</dt> <dd> <dl> <dt>

9653 (0x25B5)
</dt> <dt>



No se pudo abrir el archivo de archivos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_FILE_WRITEBACK_FAILED"></span><span id="dns_error_file_writeback_failed"></span>**\_error de \_ \_ escritura diferida del archivo de error de DNS \_**
</dt> <dd> <dl> <dt>

9654 (0x25B6)
</dt> <dt>



No se pudo escribir el archivo de archivos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DATAFILE_PARSING"></span><span id="dns_error_datafile_parsing"></span>**\_análisis de \_ archivos de errores de DNS \_**
</dt> <dd> <dl> <dt>

9655 (0x25B7)
</dt> <dt>



Error al leer el archivo de archivos para la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_DOES_NOT_EXIST"></span><span id="dns_error_record_does_not_exist"></span>**el registro de errores de DNS no \_ \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9701 (0x25E5)
</dt> <dt>



El registro DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_FORMAT"></span><span id="dns_error_record_format"></span>**\_formato de \_ registro de errores de DNS \_**
</dt> <dd> <dl> <dt>

9702 (0x25E6)
</dt> <dt>



Error de formato de registro DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_CREATION_FAILED"></span><span id="dns_error_node_creation_failed"></span>**\_ \_ \_ \_ no se pudo crear el nodo de error de DNS**
</dt> <dd> <dl> <dt>

9703 (0x25E7)
</dt> <dt>



Error de creación de nodo en DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_UNKNOWN_RECORD_TYPE"></span><span id="dns_error_unknown_record_type"></span>**\_tipo de registro de error desconocido de DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9704 (0x25E8)
</dt> <dt>



Tipo de registro DNS desconocido.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_TIMED_OUT"></span><span id="dns_error_record_timed_out"></span>**se \_ \_ \_ agotó el tiempo de espera del registro de errores de DNS \_**
</dt> <dd> <dl> <dt>

9705 (0x25E9)
</dt> <dt>



El registro DNS agotó el tiempo de espera.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_NOT_IN_ZONE"></span><span id="dns_error_name_not_in_zone"></span>**\_ \_ nombre de error \_ de DNS no \_ en \_ zona**
</dt> <dd> <dl> <dt>

9706 (0x25EA)
</dt> <dt>



El nombre no está en la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_LOOP"></span><span id="dns_error_cname_loop"></span>**\_ \_ bucle CNAME de error de DNS \_**
</dt> <dd> <dl> <dt>

9707 (0x25EB)
</dt> <dt>



Se detectó un bucle CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_CNAME"></span><span id="dns_error_node_is_cname"></span>**el \_ nodo de error de DNS \_ \_ es \_ CNAME**
</dt> <dd> <dl> <dt>

9708 (0x25EC)
</dt> <dt>



El nodo es un registro DNS CNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_CNAME_COLLISION"></span><span id="dns_error_cname_collision"></span>**\_ \_ colisión CNAME de error de DNS \_**
</dt> <dd> <dl> <dt>

9709 (0x25ED)
</dt> <dt>



Ya existe un registro CNAME para el nombre especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ONLY_AT_ZONE_ROOT"></span><span id="dns_error_record_only_at_zone_root"></span>**\_ \_ registro de error \_ de DNS solo \_ en la raíz de la \_ zona \_**
</dt> <dd> <dl> <dt>

9710 (0x25EE)
</dt> <dt>



Registre solo en la raíz de la zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_RECORD_ALREADY_EXISTS"></span><span id="dns_error_record_already_exists"></span>**el \_ registro de errores de DNS \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

9711 (0x25EF)
</dt> <dt>



El registro DNS ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_SECONDARY_DATA"></span><span id="dns_error_secondary_data"></span>**\_ \_ datos secundarios de error de DNS \_**
</dt> <dd> <dl> <dt>

9712 (0x25F0)
</dt> <dt>



Error de datos de la zona DNS secundaria.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_CREATE_CACHE_DATA"></span><span id="dns_error_no_create_cache_data"></span>**ERROR de DNS \_ \_ no \_ crear \_ datos de caché \_**
</dt> <dd> <dl> <dt>

9713 (0x25F1)
</dt> <dt>



No se pudieron crear los datos de caché DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NAME_DOES_NOT_EXIST"></span><span id="dns_error_name_does_not_exist"></span>**\_ \_ \_ \_ no \_ existe el nombre de error de DNS**
</dt> <dd> <dl> <dt>

9714 (0x25F2)
</dt> <dt>



El nombre DNS no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_PTR_CREATE_FAILED"></span><span id="dns_warning_ptr_create_failed"></span>**\_error de \_ creación de PTR de advertencia de DNS \_ \_**
</dt> <dd> <dl> <dt>

9715 (0x25F3)
</dt> <dt>



No se pudo crear el registro de puntero (PTR).


</dt> </dl> </dd> <dt>

<span id="DNS_WARNING_DOMAIN_UNDELETED"></span><span id="dns_warning_domain_undeleted"></span>**dominio de advertencia de DNS no \_ \_ \_ eliminado**
</dt> <dd> <dl> <dt>

9716 (0x25F4)
</dt> <dt>



Se ha cancelado la eliminación del dominio DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_UNAVAILABLE"></span><span id="dns_error_ds_unavailable"></span>**ERROR de DNS \_ \_ DS \_ no disponible**
</dt> <dd> <dl> <dt>

9717 (0x25F5)
</dt> <dt>



El servicio de directorio no está disponible.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DS_ZONE_ALREADY_EXISTS"></span><span id="dns_error_ds_zone_already_exists"></span>**la \_ zona DS error de DNS \_ \_ \_ ya \_ existe**
</dt> <dd> <dl> <dt>

9718 (0x25F6)
</dt> <dt>



La zona DNS ya existe en el servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_BOOTFILE_IF_DS_ZONE"></span><span id="dns_error_no_bootfile_if_ds_zone"></span>**ERROR de DNS \_ \_ no de \_ arranque si la \_ \_ \_ zona DS**
</dt> <dd> <dl> <dt>

9719 (0x25F7)
</dt> <dt>



El servidor DNS no está creando o leyendo el archivo de arranque para la zona DNS integrada del servicio de directorio.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NODE_IS_DNAME"></span><span id="dns_error_node_is_dname"></span>**el \_ nodo de error de DNS \_ \_ es \_ dname**
</dt> <dd> <dl> <dt>

9720 (0x25F8)
</dt> <dt>



El nodo es un registro DNS DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DNAME_COLLISION"></span><span id="dns_error_dname_collision"></span>**\_ \_ colisión dname de error de DNS \_**
</dt> <dd> <dl> <dt>

9721 (0x25F9)
</dt> <dt>



Ya existe un registro DNAME para el nombre especificado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_ALIAS_LOOP"></span><span id="dns_error_alias_loop"></span>**\_bucle de \_ alias de error de DNS \_**
</dt> <dd> <dl> <dt>

9722 (0x25FA)
</dt> <dt>



Se ha detectado un bucle de alias con registros CNAME o DNAME.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_AXFR_COMPLETE"></span><span id="dns_info_axfr_complete"></span>**información de DNS \_ \_ AXFR \_ completada**
</dt> <dd> <dl> <dt>

9751 (0x2617)
</dt> <dt>



DNS AXFR (transferencia de zona) completo.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_AXFR"></span><span id="dns_error_axfr"></span>**ERROR de DNS \_ \_ AXFR**
</dt> <dd> <dl> <dt>

9752 (0x2618)
</dt> <dt>



No se pudo realizar la transferencia de zona DNS.


</dt> </dl> </dd> <dt>

<span id="DNS_INFO_ADDED_LOCAL_WINS"></span><span id="dns_info_added_local_wins"></span>**información de DNS \_ \_ agregada en el \_ \_ servidor WINS local**
</dt> <dd> <dl> <dt>

9753 (0x2619)
</dt> <dt>



Se ha agregado el servidor WINS local.


</dt> </dl> </dd> <dt>

<span id="DNS_STATUS_CONTINUE_NEEDED"></span><span id="dns_status_continue_needed"></span>**el \_ Estado de DNS \_ continúa siendo \_ necesario**
</dt> <dd> <dl> <dt>

9801 (0x2649)
</dt> <dt>



La llamada de actualización segura debe continuar con la solicitud de actualización.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_TCPIP"></span><span id="dns_error_no_tcpip"></span>**ERROR de DNS \_ \_ sin \_ TCPIP**
</dt> <dd> <dl> <dt>

9851 (0x267B)
</dt> <dt>



El protocolo de red TCP/IP no está instalado.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_NO_DNS_SERVERS"></span><span id="dns_error_no_dns_servers"></span>**ERROR de DNS \_ \_ sin \_ \_ servidores DNS**
</dt> <dd> <dl> <dt>

9852 (0x267C)
</dt> <dt>



No hay servidores DNS configurados para el sistema local.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_DOES_NOT_EXIST"></span><span id="dns_error_dp_does_not_exist"></span>**el DP de error de DNS no \_ \_ \_ \_ \_ existe**
</dt> <dd> <dl> <dt>

9901 (0x26AD)
</dt> <dt>



La partición de directorio especificada no existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_EXISTS"></span><span id="dns_error_dp_already_exists"></span>**el \_ error de DNS \_ DP \_ ya \_ existe**
</dt> <dd> <dl> <dt>

9902 (0x26AE)
</dt> <dt>



La partición de directorio especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_ENLISTED"></span><span id="dns_error_dp_not_enlisted"></span>**no se ha dado de \_ alta el DP de error de DNS \_ \_ \_**
</dt> <dd> <dl> <dt>

9903 (0x26AF)
</dt> <dt>



Este servidor DNS no está dado de alta en la partición de directorio especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_ALREADY_ENLISTED"></span><span id="dns_error_dp_already_enlisted"></span>**ERROR de DNS \_ \_ DP ya dado de \_ \_ alta**
</dt> <dd> <dl> <dt>

9904 (0x26B0)
</dt> <dt>



Este servidor DNS ya está dado de alta en la partición de directorio especificada.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_NOT_AVAILABLE"></span><span id="dns_error_dp_not_available"></span>**el \_ DP de error de DNS \_ \_ no \_ está disponible**
</dt> <dd> <dl> <dt>

9905 (0x26B1)
</dt> <dt>



La partición de directorio no está disponible en este momento. Espere unos minutos y vuelva a intentarlo.


</dt> </dl> </dd> <dt>

<span id="DNS_ERROR_DP_FSMO_ERROR"></span><span id="dns_error_dp_fsmo_error"></span>**error \_ de \_ FSMO de DP de error de \_ DNS \_**
</dt> <dd> <dl> <dt>

9906 (0x26B2)
</dt> <dt>



No se pudo realizar la operación porque no se pudo alcanzar el rol FSMO del maestro de nomenclatura de dominios. El controlador de dominio que contiene el rol FSMO del maestro de nombres de dominio está inactivo o no puede atender la solicitud o no está ejecutando Windows Server 2003 o posterior.


</dt> </dl> </dd> <dt>

<span id="WSAEINTR"></span><span id="wsaeintr"></span>**WSAEINTR**
</dt> <dd> <dl> <dt>

10004 (0x2714)
</dt> <dt>



Una operación de bloqueo fue interrumpida por una llamada a WSACancelBlockingCall.


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



Se intentó tener acceso a un socket de una manera prohibida por sus permisos de acceso.


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



Demasiados Sockets abiertos.


</dt> </dl> </dd> <dt>

<span id="WSAEWOULDBLOCK"></span><span id="wsaewouldblock"></span>**WSAEWOULDBLOCK**
</dt> <dd> <dl> <dt>

10035 (0x2733)
</dt> <dt>



No se pudo completar de inmediato una operación de socket que no sea de bloqueo.


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



Se ha omitido una dirección necesaria de una operación en un socket.


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



Se especificó una opción o un nivel desconocido, no válido o no admitido en una llamada a getsockopt o a un método.


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



Se usó una dirección no compatible con el protocolo solicitado.


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



La conexión se ha interrumpido debido a que la actividad Keep-Alive detecta un error mientras la operación estaba en curso.


</dt> </dl> </dd> <dt>

<span id="WSAECONNABORTED"></span><span id="wsaeconnaborted"></span>**WSAECONNABORTED**
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



No se pudo realizar una operación en un socket porque el sistema no tenía suficiente espacio de búfer o porque la cola estaba llena.


</dt> </dl> </dd> <dt>

<span id="WSAEISCONN"></span><span id="wsaeisconn"></span>**WSAEISCONN**
</dt> <dd> <dl> <dt>

10056 (0x2748)
</dt> <dt>



Se realizó una solicitud de conexión en un socket que ya está conectado.


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



No se pudo realizar un intento de conexión porque la parte conectada no respondió correctamente después de un período de tiempo, o bien se produjo un error en la conexión establecida porque el host conectado no respondió.


</dt> </dl> </dd> <dt>

<span id="WSAECONNREFUSED"></span><span id="wsaeconnrefused"></span>**WSAECONNREFUSED**
</dt> <dd> <dl> <dt>

10061 (0x274D)
</dt> <dt>



No se pudo establecer ninguna conexión porque el equipo de destino la rechazó activamente.


</dt> </dl> </dd> <dt>

<span id="WSAELOOP"></span><span id="wsaeloop"></span>**WSAELOOP**
</dt> <dd> <dl> <dt>

10062 (0x274E)
</dt> <dt>



No se puede convertir el nombre.


</dt> </dl> </dd> <dt>

<span id="WSAENAMETOOLONG"></span><span id="wsaenametoolong"></span>**WSAENAMETOOLONG**
</dt> <dd> <dl> <dt>

10063 (0x274F)
</dt> <dt>



El nombre o el componente de nombre era demasiado largo.


</dt> </dl> </dd> <dt>

<span id="WSAEHOSTDOWN"></span><span id="wsaehostdown"></span>**WSAEHOSTDOWN**
</dt> <dd> <dl> <dt>

10064 (0x2750)
</dt> <dt>



No se pudo realizar una operación de socket porque el host de destino estaba inactivo.


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



Una implementación de Windows Sockets puede tener un límite en cuanto al número de aplicaciones que pueden usarla simultáneamente.


</dt> </dl> </dd> <dt>

<span id="WSAEUSERS"></span><span id="wsaeusers"></span>**WSAEUSERS**
</dt> <dd> <dl> <dt>

10068 (0x2754)
</dt> <dt>



Se agotó la cuota.


</dt> </dl> </dd> <dt>

<span id="WSAEDQUOT"></span><span id="wsaedquot"></span>**WSAEDQUOT**
</dt> <dd> <dl> <dt>

10069 (0x2755)
</dt> <dt>



Se agotó la cuota de disco.


</dt> </dl> </dd> <dt>

<span id="WSAESTALE"></span><span id="wsaestale"></span>**WSAESTALE**
</dt> <dd> <dl> <dt>

10070 (0x2756)
</dt> <dt>



La referencia de identificador de archivo ya no está disponible.


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



WSAStartup no funciona en este momento porque el sistema subyacente que usa para proporcionar servicios de red no está disponible actualmente.


</dt> </dl> </dd> <dt>

<span id="WSAVERNOTSUPPORTED"></span><span id="wsavernotsupported"></span>**WSAVERNOTSUPPORTED**
</dt> <dd> <dl> <dt>

10092 (0x276C)
</dt> <dt>



No se admite la versión de Windows Sockets solicitada.


</dt> </dl> </dd> <dt>

<span id="WSANOTINITIALISED"></span><span id="wsanotinitialised"></span>**WSANOTINITIALISED**
</dt> <dd> <dl> <dt>

10093 (0x276D)
</dt> <dt>



Es posible que la aplicación no haya llamado a WSAStartup o que se haya producido un error en WSAStartup.


</dt> </dl> </dd> <dt>

<span id="WSAEDISCON"></span><span id="wsaediscon"></span>**WSAEDISCON**
</dt> <dd> <dl> <dt>

10101 (0x2775)
</dt> <dt>



Devuelto por WSARecv o WSARecvFrom para indicar que la parte remota ha iniciado una secuencia de cierre estable.


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



Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando. Se canceló la llamada.


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



No se pudo cargar o inicializar el proveedor de servicios solicitado.


</dt> </dl> </dd> <dt>

<span id="WSASYSCALLFAILURE"></span><span id="wsasyscallfailure"></span>**WSASYSCALLFAILURE**
</dt> <dd> <dl> <dt>

10107 (0x277B)
</dt> <dt>



Error en una llamada del sistema.


</dt> </dl> </dd> <dt>

<span id="WSASERVICE_NOT_FOUND"></span><span id="wsaservice_not_found"></span>**\_no \_ se encontró WSASERVICE**
</dt> <dd> <dl> <dt>

10108 (0x277C)
</dt> <dt>



No se conoce este servicio. No se encuentra el servicio en el espacio de nombres especificado.


</dt> </dl> </dd> <dt>

<span id="WSATYPE_NOT_FOUND"></span><span id="wsatype_not_found"></span>**\_no \_ se encontró WSATYPE**
</dt> <dd> <dl> <dt>

10109 (0x277D)
</dt> <dt>



No se encontró la clase especificada.


</dt> </dl> </dd> <dt>

<span id="WSA_E_NO_MORE"></span><span id="wsa_e_no_more"></span>**WSA \_ E \_ no \_ más**
</dt> <dd> <dl> <dt>

10110 (0x277E)
</dt> <dt>



WSALookupServiceNext no puede devolver más resultados.


</dt> </dl> </dd> <dt>

<span id="WSA_E_CANCELLED"></span><span id="wsa_e_cancelled"></span>**WSA \_ E \_ cancelada**
</dt> <dd> <dl> <dt>

10111 (0x277F)
</dt> <dt>



Se realizó una llamada a WSALookupServiceEnd mientras esta llamada todavía se estaba procesando. Se canceló la llamada.


</dt> </dl> </dd> <dt>

<span id="WSAEREFUSED"></span><span id="wsaerefused"></span>**WSAEREFUSED**
</dt> <dd> <dl> <dt>

10112 (0x2780)
</dt> <dt>



Error en una consulta de base de datos porque se rechazó activamente.


</dt> </dl> </dd> <dt>

<span id="WSAHOST_NOT_FOUND"></span><span id="wsahost_not_found"></span>**\_no \_ se encontró WSAHOST**
</dt> <dd> <dl> <dt>

11001 (0x2AF9)
</dt> <dt>



Se desconoce el host.


</dt> </dl> </dd> <dt>

<span id="WSATRY_AGAIN"></span><span id="wsatry_again"></span>**WSATRY de \_ nuevo**
</dt> <dd> <dl> <dt>

11002 (0x2AFA)
</dt> <dt>



Éste es normalmente un error temporal durante la resolución de nombres de host y significa que el servidor local no recibió una respuesta de un servidor autorizado.


</dt> </dl> </dd> <dt>

<span id="WSANO_RECOVERY"></span><span id="wsano_recovery"></span>**recuperación de WSANO \_**
</dt> <dd> <dl> <dt>

11003 (0x2AFB)
</dt> <dt>



Se produjo un error no recuperable durante una búsqueda de base de datos.


</dt> </dl> </dd> <dt>

<span id="WSANO_DATA"></span><span id="wsano_data"></span>**datos de WSANO \_**
</dt> <dd> <dl> <dt>

11004 (0x2AFC)
</dt> <dt>



El nombre solicitado es válido, pero no se encontró ningún dato del tipo solicitado.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RECEIVERS"></span><span id="wsa_qos_receivers"></span>**\_receptores de QoS WSA \_**
</dt> <dd> <dl> <dt>

11005 (0x2AFD)
</dt> <dt>



Ha llegado al menos una reserva.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_SENDERS"></span><span id="wsa_qos_senders"></span>**\_remitentes de QoS WSA \_**
</dt> <dd> <dl> <dt>

11006 (0x2AFE)
</dt> <dt>



Ha llegado al menos una ruta de acceso.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_SENDERS"></span><span id="wsa_qos_no_senders"></span>**\_calidad de QoS WSA \_ sin \_ remitentes**
</dt> <dd> <dl> <dt>

11007 (0x2AFF)
</dt> <dt>



No hay remitentes.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_NO_RECEIVERS"></span><span id="wsa_qos_no_receivers"></span>**\_QoS WSA \_ sin \_ destinatarios**
</dt> <dd> <dl> <dt>

11008 (0x2B00)
</dt> <dt>



No hay ningún receptor.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_REQUEST_CONFIRMED"></span><span id="wsa_qos_request_confirmed"></span>**\_solicitud de QoS WSA \_ \_ confirmada**
</dt> <dd> <dl> <dt>

11009 (0x2B01)
</dt> <dt>



Se ha confirmado la reserva.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ADMISSION_FAILURE"></span><span id="wsa_qos_admission_failure"></span>**\_error de \_ admisión de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11010 (0x2B02)
</dt> <dt>



Error debido a la falta de recursos.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_POLICY_FAILURE"></span><span id="wsa_qos_policy_failure"></span>**error de la \_ Directiva de QoS WSA \_ \_**
</dt> <dd> <dl> <dt>

11011 (0x2B03)
</dt> <dt>



Rechazado por motivos administrativos: Credenciales incorrectas.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_STYLE"></span><span id="wsa_qos_bad_style"></span>**\_ \_ estilo incorrecto de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11012 (0x2B04)
</dt> <dt>



Estilo desconocido o en conflicto.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_BAD_OBJECT"></span><span id="wsa_qos_bad_object"></span>**\_ \_ objeto incorrecto de QoS de WSA \_**
</dt> <dd> <dl> <dt>

11013 (0x2B05)
</dt> <dt>



Problema con alguna parte del búfer de FILTERSPEC o ProviderSpecific en general.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_TRAFFIC_CTRL_ERROR"></span><span id="wsa_qos_traffic_ctrl_error"></span>**\_error de \_ control de tráfico de QoS WSA \_ \_**
</dt> <dd> <dl> <dt>

11014 (0x2B06)
</dt> <dt>



Problema con alguna parte del elemento FLOWSPEC.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_GENERIC_ERROR"></span><span id="wsa_qos_generic_error"></span>**\_ \_ error genérico de QoS WSA \_**
</dt> <dd> <dl> <dt>

11015 (0x2B07)
</dt> <dt>



Error general de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESERVICETYPE"></span><span id="wsa_qos_eservicetype"></span>**\_ESERVICETYPE de QoS WSA \_**
</dt> <dd> <dl> <dt>

11016 (0x2B08)
</dt> <dt>



Se encontró un tipo de servicio no válido o no reconocido en el FLOWSPEC.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWSPEC"></span><span id="wsa_qos_eflowspec"></span>**\_EFLOWSPEC de QoS WSA \_**
</dt> <dd> <dl> <dt>

11017 (0x2B09)
</dt> <dt>



Se encontró un FLOWSPEC no válido o incoherente en la estructura de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPROVSPECBUF"></span><span id="wsa_qos_eprovspecbuf"></span>**\_EPROVSPECBUF de QoS WSA \_**
</dt> <dd> <dl> <dt>

11018 (0x2B0A)
</dt> <dt>



Búfer específico del proveedor QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERSTYLE"></span><span id="wsa_qos_efilterstyle"></span>**\_EFILTERSTYLE de QoS WSA \_**
</dt> <dd> <dl> <dt>

11019 (0x2B0B)
</dt> <dt>



Se usó un estilo de filtro QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERTYPE"></span><span id="wsa_qos_efiltertype"></span>**\_EFILTERTYPE de QoS WSA \_**
</dt> <dd> <dl> <dt>

11020 (0x2B0C)
</dt> <dt>



Se usó un tipo de filtro QOS no válido.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFILTERCOUNT"></span><span id="wsa_qos_efiltercount"></span>**\_EFILTERCOUNT de QoS WSA \_**
</dt> <dd> <dl> <dt>

11021 (0x2B0D)
</dt> <dt>



Se especificó un número incorrecto de FILTERSPECs de QOS en FLOWDESCRIPTOR.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EOBJLENGTH"></span><span id="wsa_qos_eobjlength"></span>**\_EOBJLENGTH de QoS WSA \_**
</dt> <dd> <dl> <dt>

11022 (0x2B0E)
</dt> <dt>



Se especificó un objeto con un campo ObjectLength no válido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWCOUNT"></span><span id="wsa_qos_eflowcount"></span>**\_EFLOWCOUNT de QoS WSA \_**
</dt> <dd> <dl> <dt>

11023 (0x2B0F)
</dt> <dt>



Se especificó un número incorrecto de descriptores de flujo en la estructura de QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EUNKOWNPSOBJ"></span><span id="wsa_qos_eunkownpsobj"></span>**\_EUNKOWNPSOBJ de QoS WSA \_**
</dt> <dd> <dl> <dt>

11024 (0x2B10)
</dt> <dt>



Se encontró un objeto desconocido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPOLICYOBJ"></span><span id="wsa_qos_epolicyobj"></span>**\_EPOLICYOBJ de QoS WSA \_**
</dt> <dd> <dl> <dt>

11025 (0x2B11)
</dt> <dt>



Se encontró un objeto de Directiva no válido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EFLOWDESC"></span><span id="wsa_qos_eflowdesc"></span>**\_EFLOWDESC de QoS WSA \_**
</dt> <dd> <dl> <dt>

11026 (0x2B12)
</dt> <dt>



Se encontró un descriptor de flujo de QOS no válido en la lista de descriptores de flujo.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFLOWSPEC"></span><span id="wsa_qos_epsflowspec"></span>**\_EPSFLOWSPEC de QoS WSA \_**
</dt> <dd> <dl> <dt>

11027 (0x2B13)
</dt> <dt>



Se encontró un FLOWSPEC no válido o incoherente en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_EPSFILTERSPEC"></span><span id="wsa_qos_epsfilterspec"></span>**\_EPSFILTERSPEC de QoS WSA \_**
</dt> <dd> <dl> <dt>

11028 (0x2B14)
</dt> <dt>



Se encontró un FILTERSPEC no válido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESDMODEOBJ"></span><span id="wsa_qos_esdmodeobj"></span>**\_ESDMODEOBJ de QoS WSA \_**
</dt> <dd> <dl> <dt>

11029 (0x2B15)
</dt> <dt>



Se encontró un objeto de modo discard de forma no válido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_ESHAPERATEOBJ"></span><span id="wsa_qos_eshaperateobj"></span>**\_ESHAPERATEOBJ de QoS WSA \_**
</dt> <dd> <dl> <dt>

11030 (0x2B16)
</dt> <dt>



Se encontró un objeto de frecuencia de forma no válido en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_QOS_RESERVED_PETYPE"></span><span id="wsa_qos_reserved_petype"></span>**\_ \_ clave reservada de QoS WSA \_ PETYPE**
</dt> <dd> <dl> <dt>

11031 (0x2B17)
</dt> <dt>



Se encontró un elemento de directiva reservado en el búfer específico del proveedor QOS.


</dt> </dl> </dd> <dt>

<span id="WSA_SECURE_HOST_NOT_FOUND"></span><span id="wsa_secure_host_not_found"></span>**\_ \_ \_ no \_ se encontró el host seguro WSA**
</dt> <dd> <dl> <dt>

11032 (0x2B18)
</dt> <dt>



No se conoce este host de forma segura.


</dt> </dl> </dd> <dt>

<span id="WSA_IPSEC_NAME_POLICY_ERROR"></span><span id="wsa_ipsec_name_policy_error"></span>**\_error de \_ Directiva de nombre de IPSec WSA \_ \_**
</dt> <dd> <dl> <dt>

11033 (0x2B19)
</dt> <dt>



No se pudo agregar la directiva IPSEC basada en nombres.


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

 

 




