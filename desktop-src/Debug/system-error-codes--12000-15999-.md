---
description: Describe los códigos de error 12000-1599 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Códigos de error del sistema (12000-15999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496246"
---
# <a name="system-error-codes-12000-15999"></a>Códigos de error del sistema (12000-15999)

> [!NOTE]
> Esta información está destinada a los desarrolladores que depuran errores del sistema. En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .

En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 12000 a 15999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones. Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**Error \_ de \_Internet \** _
</dt> <dd> <dl> <dt>

12000-12175 (0x2EE0)
</dt> <dt>



Consulte [códigos de error de Internet](../wininet/wininet-errors.md) y Wininet. h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>_ *error en la \_ \_ \_ directiva \_ IPSec QM**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



La Directiva de modo rápido especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la directiva IPSec del QM**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



No se encontró la Directiva de modo rápido especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR \_ \_ \_ \_ en uso de la directiva IPSec QM \_**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Se está utilizando la Directiva de modo rápido especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR: la \_ Directiva de IPSec \_ mm \_ \_ existe**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



La Directiva de modo principal especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la Directiva de IPSec mm**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



No se encontró la Directiva de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR \_ \_ en el \_ \_ uso de la Directiva de IPSec mm \_**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Se está utilizando la Directiva de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR \_ el \_ filtro de mm de IPSec \_ \_ existe**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



El filtro de modo principal especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro IPSec mm**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



No se encontró el filtro de modo principal especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR \_ de \_ filtro de transporte IPSec \_ \_**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



El filtro de modo de transporte especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro de transporte IPSec**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



El filtro de modo de transporte especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR: \_ IPSec \_ mm \_ auth \_ existe**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



Existe la lista de autenticación de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró la autenticación de IPSec mm**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



No se encontró la lista de autenticación de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR \_ \_ \_ de autenticación de IPSec mm \_ en \_ uso**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Se está utilizando la lista de autenticación de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR \_ \_ \_ \_ \_ no se encontró la directiva \_ mm predeterminada de IPSec**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



No se encontró la Directiva de modo principal predeterminada especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR \_ IPSec \_ predeterminado \_ \_ \_ no \_ se encontró la autenticación mm**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



No se encontró la lista de autenticación de modo principal predeterminada especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR \_ : \_ \_ \_ \_ no \_ se encontró la Directiva de QM predeterminada de IPSec**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



No se encontró la directiva predeterminada de modo rápido especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR: el \_ \_ filtro de túnel IPSec \_ \_ existe**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



El filtro de modo de túnel especificado existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el filtro de túnel IPSec**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



No se encontró el filtro de modo de túnel especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR de \_ filtro de mm de IPsec con \_ \_ \_ \_ eliminación pendiente**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



El filtro de modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR \_ de \_ filtro de transporte IPSec \_ pendiente de \_ \_ eliminación**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



El filtro de transporte está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR \_ de \_ filtro de túnel IPSec \_ pendiente de \_ \_ eliminación**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



El filtro de túnel está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR \_ de \_ directiva IPSec mm de \_ \_ \_ eliminación pendiente**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



La Directiva de modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR \_ de \_ autenticación de IPSec mm de \_ autorización pendiente de \_ \_ eliminación**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



El paquete de autenticación de modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR \_ de \_ \_ \_ eliminación pendiente de directiva IPSec QM \_**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



La Directiva de modo rápido está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**ADVERTENCIA \_ de \_ Directiva de IPSec mm \_ \_ eliminada**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



La Directiva de modo principal se agregó correctamente, pero no se admiten algunas de las ofertas solicitadas.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**ADVERTENCIA \_ de \_ directiva IPSec QM \_ \_ eliminada**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



La Directiva de modo rápido se agregó correctamente, pero no se admiten algunas de las ofertas solicitadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR de \_ Inicio de estado de IPSec de \_ IKE \_ NEG \_ \_**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERROR de \_ Inicio de estado de IPSec de \_ IKE \_ NEG \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR \_ de \_ autenticación IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Las credenciales de autenticación IKE no son aceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR de protocolo \_ \_ IKE IPSec \_ \_ erróneo**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Los atributos de seguridad de IKE son inaceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR \_ de \_ negociación IKE de IPSec \_ \_ pendiente**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Negociación IKE en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**error \_ de \_ \_ procesamiento general de IKE de \_ IPSec \_**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Error de procesamiento general.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR \_ de \_ IKE de IPSec \_ agotó el tiempo de \_ espera**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Se agotó el tiempo de espera de la negociación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR \_ IPSec \_ IKE \_ no \_ CERT**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE no encontró el certificado de equipo válido. Póngase en contacto con el administrador de seguridad de red sobre la instalación de un certificado válido en el almacén de certificados adecuado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR \_ IPSec \_ IKE \_ SA \_ eliminado**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



SA IKE eliminada por el par antes del establecimiento completado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR de \_ IPSec \_ IKE \_ SA \_ cosechado**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



SA de IKE eliminada antes de que se completara el establecimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR de \_ adquisición de adquisición de IPSec \_ IKE \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



La solicitud de negociación SAT en la cola es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR de \_ IPSec \_ IKE de \_ \_ adquisición \_**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



La solicitud de negociación SAT en la cola es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR \_ de \_ \_ eliminación de cola IKE \_ de IPSec \_**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



La solicitud de negociación SAT en la cola es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR \_ de \_ cola IKE de IPSec \_ \_ \_ no entrega no \_ mm**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



La solicitud de negociación SAT en la cola es demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR \_ no se pudo \_ quitar la \_ \_ \_ respuesta IKE de IPSec**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



No hay respuesta del elemento del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR \_ de \_ eliminación de retraso IPSec de IKE \_ mm \_ \_**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



La negociación tardó demasiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR \_ de \_ retraso de IPSec IKE de \_ QM \_ \_**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



La negociación tardó demasiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**error \_ IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Error desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR \_ de \_ CRL IKE de IPSec \_ \_ errónea**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Error en la comprobación de revocación de certificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR \_ de \_ \_ uso de \_ clave no válida IKE de IPSec \_**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Uso de clave de certificado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR \_ de \_ IPSec \_ IKE \_ tipo de certificado no válido \_**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Tipo de certificado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ \_ clave privada**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



Error de negociación IKE porque el certificado de equipo utilizado no tiene una clave privada. Los certificados IPsec requieren una clave privada. Póngase en contacto con el administrador de seguridad de red para reemplazar por un certificado que tenga una clave privada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR \_ de \_ \_ regeneración de \_ claves simultánea de IPSec IKE**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Se detectaron claves simultáneas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR de \_ IPSec \_ DH de IKE \_ \_ erróneo**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Error en el cálculo de Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR \_ : \_ \_ no se \_ reconoce la carga crítica de \_ IKE de IPSec \_**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



No sepa cómo procesar la carga crítica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR \_ de \_ encabezado IPSec IKE \_ no válido \_**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Encabezado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ Directiva**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



No hay ninguna directiva configurada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR \_ de \_ \_ firma IKE no válida de IPSec \_**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



No se pudo comprobar la firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**error \_ de \_ Kerberos IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



No se pudo autenticar con Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR \_ IPSec \_ IKE \_ sin \_ \_ clave pública**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



El certificado del mismo nivel no tenía una clave pública.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR \_ de \_ proceso IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Error al procesar la carga de error.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR \_ IPSec \_ IKE de \_ proceso IKE \_ \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Error al procesar la carga de SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ prop**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Error al procesar la carga de propuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ Trans**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Error al procesar la carga de transformación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR en el \_ \_ proceso IKE de IPSec \_ \_ Err \_ ke**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Error al procesar la carga de la KE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Error al procesar la carga de identificador.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Error al procesar la carga de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR en el \_ proceso IKE de IPSec de \_ \_ \_ Err \_ \_ req**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Error al procesar la carga de la solicitud de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR en el \_ hash de Err del \_ proceso IKE de IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Error al procesar la carga hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ SIG**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Error al procesar la carga de la firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR \_ de \_ IKE de \_ proceso IKE \_ \_ de IPSec**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Error al procesar la carga de nonce.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR en la notificación de ERROR del \_ \_ proceso IKE de IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Error al procesar la carga de notificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR de \_ IPSec \_ IKE de proceso de IKE \_ \_ \_ Delete**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Error al procesar la carga de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR en el proveedor de errores de \_ \_ proceso IKE de IPSec \_ \_ \_**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Error al procesar la carga VendorId.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR de \_ IPSec: \_ \_ carga no válida IKE \_**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Carga no válida recibida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR de \_ IPSec \_ IKE \_ carga \_ software \_ SA**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



SA flexible cargada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR de \_ IPSec \_ IKE temporal de IKE \_ \_ \_ \_ desactivada**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



SA flexible desactivada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR de \_ IPSec \_ IKE \_ no válido \_**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Cookie no válida recibida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR \_ IPSec \_ IKE \_ no \_ peer \_ CERT**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



El par no pudo enviar un certificado de equipo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR \_ de \_ \_ CRL IPSec del mismo nivel \_ \_ no superada**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Error en la comprobación de revocación de certificación del certificado del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR \_ de \_ \_ cambio de directiva IKE de IPSec \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Nueva SAs invalidada de la Directiva con la Directiva antigua.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR \_ de \_ IPSec \_ IKE \_ no \_ Directiva de mm**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



No hay ninguna directiva IKE de modo principal disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR \_ IPSec \_ IKE \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



No se pudo habilitar el privilegio TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR \_ IPSec \_ IKE \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



No se pudo cargar SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR \_ IPSec \_ IKE \_ FAILSSPINIT**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



No se pudo obtener la dirección de envío de la tabla de funciones de seguridad de SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR \_ IPSec \_ IKE \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



No se pudo consultar el paquete Kerberos para obtener el tamaño máximo del token.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR \_ IPSec \_ IKE \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



No se pudieron obtener las credenciales del servidor Kerberos para el \_ servicio IKE/error IPSec \_ IKE. La autenticación Kerberos no funcionará. La razón más probable de esto es la falta de pertenencia a un dominio. Esto es normal si el equipo es miembro de un grupo de trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR \_ IPSec \_ IKE \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



No se pudo determinar el nombre de entidad de seguridad de SSPI para el \_ \_ servicio IKE IKE/error IPSec ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR \_ IPSec \_ IKE \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



No se pudo obtener el SPI nuevo para la SA de entrada del controlador IPsec. La causa más común es que el controlador no tenga el filtro correcto. Compruebe la Directiva para comprobar los filtros.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR \_ de \_ \_ filtro IKE no válido de IPSec \_**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



El filtro especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR \_ \_ \_ \_ de memoria insuficiente de IKE de \_ IPSec**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Se produjo un error de asignación de memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR de \_ IPSec: \_ \_ \_ \_ \_ no se pudo agregar la clave de actualización IKE**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



No se pudo agregar la Asociación de seguridad al controlador IPsec. La causa más común es que la negociación IKE tardó demasiado tiempo en completarse. Si el problema persiste, reduzca la carga en el equipo con errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR \_ de \_ directiva IPSec IKE \_ no válida \_**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Directiva no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR \_ de \_ \_ Doi desconocido de IKE de IPSec \_**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR en la \_ \_ situación IPSec IKE \_ no válida \_**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situación no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR de IPSec: error \_ \_ DH de IKE \_ \_**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Error de Diffie-Hellman.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR \_ de \_ Grupo IPSec IKE \_ no válido \_**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Grupo de Diffie-Hellman no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR \_ IPSec \_ \_ cifrado de IKE**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Error al cifrar la carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR \_ de \_ \_ descifrado IKE de IPSec**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Error al descifrar la carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR \_ de \_ \_ coincidencia de directiva IKE de IPSec \_**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Error de coincidencia de directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR de \_ IPSec \_ IKE \_ no compatible \_ ID**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



IDENTIFICADOR no compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR de \_ IPSec \_ IKE \_ no válido \_**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Error de comprobación de hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR \_ de \_ hash IPSec de IKE \_ no válido \_ \_**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algoritmo hash no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR de \_ IPSec \_ IKE \_ no válido tamaño de \_ hash \_**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Tamaño de hash no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR \_ IPSec \_ IKE \_ no válido \_ cifrado \_ alg**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algoritmo de cifrado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR \_ IPSec \_ IKE \_ de \_ autenticación no válida \_**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algoritmo de autenticación no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR en el \_ \_ SIG IPSec IKE \_ no válido \_**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Firma de certificado no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR \_ de \_ carga IKE de IPSec \_ \_ errónea**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Error de carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR \_ de \_ \_ RPC IKE \_ Delete de IPSec**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Eliminado a través de una llamada RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR \_ de \_ \_ reinicialización benigna de IPSec IKE \_**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Estado temporal creado para realizar la reinicialización. No se trata de un error real.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR \_ de \_ \_ notificación de \_ duración del respondedor no válido IKE \_ de IPSec \_**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



El valor de duración recibido en la notificación de duración del respondedor está por debajo del valor mínimo configurado en Windows 2000. Corrija la Directiva en el equipo del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR \_ de \_ IPSec \_ IKE \_ versión principal no válida \_**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



El destinatario no puede controlar la versión de IKE especificada en el encabezado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR \_ IPSec \_ IKE \_ \_ KEYLEN de certificado no válido \_**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



La longitud de clave del certificado es demasiado pequeña para los requisitos de seguridad configurados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR en el \_ límite de IPSec \_ IKE \_ mm \_**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Número máximo de SA de MM establecidas en el mismo nivel superado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR \_ de \_ negociación IKE IPSec \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE recibió una directiva que deshabilita la negociación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR de \_ IPSec \_ IKE de \_ QM \_ Limit**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Se alcanzó el límite de modo rápido máximo para el modo principal. Se iniciará el nuevo modo principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR de \_ IPSec \_ IKE \_ mm \_ expirado**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



La vigencia de SA de modo principal expiró o el interlocutor envió una eliminación de modo principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR \_ IPSec \_ IKE \_ del mismo nivel \_ \_ asumido \_ no válido**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Se supone que la SA de modo principal no es válida porque el elemento del mismo nivel dejó de responder.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de \_ Directiva de cadena de certificado \_ IKE \_ de IPSec**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



El certificado no está encadenado a una raíz de confianza en la directiva IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR de \_ IPSec \_ IKE \_ inesperado \_ \_ ID. de mensaje**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Se recibió un ID. de mensaje inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR en \_ IPSec: carga de \_ \_ autenticación no válida \_ \_**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Ofertas de autenticación no válidas recibidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR \_ de \_ cookie de dos de IKE de IPSec \_ \_ \_ enviada**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



La cookie DoS enviadas notifica al iniciador.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR \_ de \_ cierre de IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



El servicio IKE se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR \_ IPSec \_ IKE \_ CGA \_ auth \_ no se pudo ejecutar**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



No se pudo comprobar el enlace entre la dirección CGA y el certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR \_ de \_ proceso IKE de IPSec \_ \_ \_ NATOA**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Error al procesar la carga de NatOA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR \_ IPSec \_ IKE \_ no \_ válido \_ para el \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Los parámetros del modo principal no son válidos para este modo rápido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR \_ IPSec \_ IKE \_ QM \_ caducado**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



El controlador IPsec expiró la SA de modo rápido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR \_ IPSec \_ IKE \_ demasiados \_ \_ filtros**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Se detectaron demasiados filtros de IKEEXT agregados dinámicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR de \_ fin de estado de IPSec de \_ IKE \_ NEG \_ \_**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERROR de \_ fin de estado de IPSec de \_ IKE \_ NEG \_ \_


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR \_ del \_ \_ túnel de \_ \_ NAP ficticio \_ de IKE de IPSec Kill**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



La reautenticación NAP se realizó correctamente y debe eliminar el túnel IKEv2 NAP ficticio.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR \_ de \_ \_ asignación de \_ dirección IP interna IKE \_ de IPSec \_**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Error al asignar la dirección IP interna al iniciador en modo de túnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR \_ IPSec \_ IKE \_ requiere \_ \_ falta de carga de CP \_**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Falta la carga de configuración necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR \_ de \_ \_ negociación de \_ suplantación de módulo de clave IPSec \_ \_ pendiente**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Una negociación que se ejecuta como el principio de seguridad que emitió la conexión está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR en la \_ \_ \_ coexistencia IKE de IPSec \_ suprimir**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA eliminado debido a que la coexistencia de IKEv1/AuthIP suprime la comprobación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR \_ IPSec \_ IKE \_ RATELIMIT \_ Drop**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



Se quitó la solicitud SA entrante debido a la limitación de velocidad de direcciones IP del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR \_ IPSec \_ IKE \_ del mismo nivel \_ \_ no admite \_ Mobike**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



El elemento del mismo nivel no es compatible con MOBIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR \_ de \_ autorización IKE de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



El establecimiento de la asociación de seguridad no está autorizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR \_ de \_ \_ autorización de \_ credenciales seguras \_ IKE IKE \_ de IPSec**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



El establecimiento de SA no está autorizado porque no hay una credencial basada en PKINIT suficientemente segura.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR \_ \_ \_ de autorización IKE \_ \_ de IPSec \_ con \_ reintento opcional**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



El establecimiento de la asociación de seguridad no está autorizado. Es posible que tenga que especificar credenciales actualizadas o diferentes, como una tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR \_ \_ \_ \_ de autorización de credenciales sólidas IKE \_ \_ de IPSec y \_ \_ error CERTMAP**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



El establecimiento de SA no está autorizado porque no hay una credencial basada en PKINIT suficientemente segura. Esto puede estar relacionado con un error de asignación de certificado a cuenta para la SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR \_ de \_ \_ servidor de \_ estado \_ extendido \_ de IPSec IKE NEG**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERROR \_ de \_ \_ servidor de \_ estado \_ extendido \_ de IPSec IKE NEG


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR \_ de \_ SPI incorrecto de IPSec \_**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



El SPI en el paquete no coincide con una SA de IPsec válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR: \_ vigencia de SA de IPSec \_ \_ \_ expirada**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



El paquete se recibió en una SA de IPsec cuya duración ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR \_ SA de IPSec \_ incorrecto \_**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



El paquete se recibió en una SA de IPsec que no coincide con las características del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR \_ \_ al comprobar la reproducción de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Error al comprobar el número de secuencia de paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR \_ de \_ paquete IPSec no válido \_**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



El encabezado o el finalizador IPsec del paquete no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR \_ de \_ comprobación de integridad de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Error de comprobación de integridad de IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR \_ de \_ \_ eliminación de texto no cifrado de IPSec \_**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec quitó un paquete de texto no cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR \_ de \_ \_ eliminación de Firewall de autenticación IPSec \_**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec quitó un paquete ESP entrante en modo de Firewall autenticado. Esta caída es benigna.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR en el \_ límite de IPSec \_ \_**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec quitó un paquete debido a la limitación de DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR en el \_ \_ bloque DOSP de IPSec \_**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



La protección de DoS de IPsec coincidía con una regla de bloqueo explícita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR \_ IPSec \_ DOSP \_ de \_ multidifusión recibido**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



La protección de DoS de IPsec recibió un paquete de multidifusión específico de IPsec que no está permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR \_ IPSec \_ DOSP \_ paquete no válido \_**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



La protección DoS de IPsec recibió un paquete con un formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR en la \_ \_ \_ búsqueda de estado DOSP \_ de IPSec \_**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



La protección de DoS de IPsec no pudo buscar el estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**DOSP de ERROR de \_ \_ \_ entradas Max de IPSec \_**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



La protección de DoS de IPsec no pudo crear el estado porque se ha alcanzado el número máximo de entradas permitidas por la Directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR \_ IPSec \_ DOSP \_ KEYMOD \_ \_ permitido**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



La protección DoS de IPsec recibió un paquete de negociación IPsec para un módulo de creación de claves que no está permitido por la Directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR \_ IPSec \_ DOSP \_ no \_ instalado**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



No se ha habilitado la protección de DoS de IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR de \_ IPSec \_ DOSP \_ Max \_ por \_ \_ \_ cola de RATELIMIT IP**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



La protección de DoS de IPsec no pudo crear una cola de límite de tasa de IP por interno porque se ha alcanzado el número máximo de colas permitido por la Directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**\_ \_ \_ no \_ se encontró la sección de error SxS**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



La sección solicitada no estaba presente en el contexto de activación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR SxS no se pudo \_ \_ \_ gen \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



No se pudo iniciar la aplicación porque la configuración en paralelo es incorrecta. Vea el registro de eventos de la aplicación o use la herramienta de sxstrace.exe de línea de comandos para obtener más detalles.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR \_ SxS \_ \_ ACTCTXDATA \_ formato no válido**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



El formato de datos de enlace de la aplicación no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR \_ \_ \_ no \_ se encontró el ensamblado SxS**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



El ensamblado al que se hace referencia no está instalado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**error \_ de \_ formato de manifiesto SxS \_ \_**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



El archivo de manifiesto no comienza con la información de formato y etiqueta necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**error \_ de \_ análisis de manifiestos SxS \_ \_**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



El archivo de manifiesto contiene uno o varios errores de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR en el \_ \_ contexto de activación SxS \_ \_ deshabilitado**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



La aplicación intentó activar un contexto de activación deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**\_ \_ \_ no \_ se encontró la clave SxS**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



No se encontró la clave de búsqueda solicitada en ningún contexto de activación activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR \_ de \_ conflicto de versión de SxS \_**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Una versión de componente requerida por la aplicación entra en conflicto con otra versión de componente que ya está activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR \_ SxS \_ \_ tipo de sección incorrecto \_**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



La sección de contexto de activación solicitado de tipo no coincide con la API de consulta utilizada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR \_ SxS \_ consultas de subproceso \_ \_ deshabilitadas**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



La falta de recursos del sistema requiere una activación aislada para deshabilitarse en el subproceso de ejecución actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR \_ el \_ valor predeterminado del proceso SxS \_ \_ ya está \_ establecido**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Error al tratar de establecer el contexto de activación predeterminado del proceso porque el contexto de activación de proceso predeterminado ya estaba establecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR \_ SxS \_ \_ grupo de codificación desconocido \_**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



No se reconoce el identificador de grupo de codificación especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR \_ de \_ codificación SxS desconocida \_**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



No se reconoce la codificación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR \_ SxS \_ \_ URI de \_ espacio de nombres XML no válido \_**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



El manifiesto contiene una referencia a un URI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR \_ de \_ dependencia del manifiesto raíz SxS \_ \_ \_ no \_ instalada**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



El manifiesto de aplicación contiene una referencia a un ensamblado dependiente que no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR \_ de \_ dependencia de manifiesto de hoja \_ \_ \_ no \_ instalada**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



El manifiesto de un ensamblado utilizado por la aplicación tiene una referencia a un ensamblado dependiente que no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR \_ SxS \_ \_ atributo de identidad de ensamblado no válido \_ \_**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



El manifiesto contiene un atributo para la identidad del ensamblado que no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**el \_ manifiesto de error SxS \_ falta el espacio de \_ \_ \_ nombres predeterminado necesario \_**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



En el manifiesto falta la especificación de espacio de nombres predeterminada necesaria en el elemento de ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR \_ SxS \_ \_ no válido \_ requerido \_ \_ espacio de nombres predeterminado**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



El manifiesto tiene un espacio de nombres predeterminado especificado en el elemento de ensamblado, pero su valor no es "urn: schemas-microsoft-com: ASM. v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR \_ \_ \_ \_ de ruta de acceso cruzada del manifiesto privado SxS \_ \_ con \_ punto de reanálisis \_**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



El manifiesto privado sondeado ha cruzado una ruta de acceso con un punto de reanálisis no admitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR \_ SxS \_ Duplicate \_ dll \_ Name**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen archivos con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR \_ SxS \_ WINDOWCLASS duplicado \_ \_**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen clases de ventana con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR \_ SxS \_ duplicado de \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen los mismos CLSID de servidor COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR \_ SxS \_ duplicado de \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen proxies para la misma interfaz COM IID.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR \_ SxS \_ duplicado \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen la misma biblioteca de tipos COM TLBIDs.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR \_ SxS \_ Duplicate \_ ProgID**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación tienen los mismos ProgID de COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR \_ SxS \_ \_ nombre de ensamblado duplicado \_**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Dos o más componentes a los que se hace referencia directa o indirectamente mediante el manifiesto de aplicación son versiones diferentes del mismo componente, lo cual no está permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR \_ de \_ hash de archivo SxS \_ \_ no coincidente**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



El archivo de un componente no coincide con la información de comprobación presente en el manifiesto del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**error \_ de \_ análisis de directiva SxS \_ \_**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



El manifiesto de Directiva contiene uno o varios errores de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Error de análisis de manifiesto: se esperaba un literal de cadena, pero no se encontró ningún carácter de comilla de apertura.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR \_ SxS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Error de análisis de manifiesto: se usó una sintaxis incorrecta en un comentario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR \_ SxS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Error de análisis de manifiesto: se ha iniciado un nombre con un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR \_ SxS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Error de análisis de manifiesto: un nombre contenía un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR \_ SxS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Error de análisis de manifiesto: un literal de cadena contenía un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR \_ SxS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Error de análisis de manifiesto: sintaxis no válida para una declaración XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR \_ SxS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Error de análisis de manifiesto: se encontró un carácter no válido en el contenido de texto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Error de análisis de manifiesto: falta el espacio en blanco necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR \_ SxS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Error de análisis de manifiesto: se esperaba el carácter ' > '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Error de análisis de manifiesto: se esperaba un carácter de punto y coma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR \_ SxS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Error de análisis de manifiesto: paréntesis desequilibrados.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR \_ SxS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Error de análisis de manifiesto: error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR \_ SxS \_ XML \_ E \_ espacio en blanco inesperado \_**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Error de análisis de manifiesto: no se permite un espacio en blanco en esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR \_ de \_ codificación SxS XML \_ E \_ incompleta \_**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Error de análisis de manifiesto: se alcanzó el final del archivo en un estado no válido para la codificación actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR \_ SxS \_ XML \_ E \_ falta el \_ paréntesis**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Error de análisis de manifiesto: faltan paréntesis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR \_ SxS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Error de análisis de manifiesto: falta un carácter de comilla simple o doble ( \\ ' o ' \\ ).


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR \_ SxS \_ XML \_ E \_ varios \_ signos de dos puntos**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Error de análisis de manifiesto: no se permiten varios signos de dos puntos en un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR \_ SxS \_ XML \_ E \_ decimal no válido \_**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Error de análisis de manifiesto: carácter no válido para el dígito decimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR \_ SxS \_ XML \_ E \_ hexadecimal no válido \_**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Error de análisis de manifiesto: carácter no válido para el dígito hexadecimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR \_ SxS \_ XML \_ E \_ \_ Unicode no válido**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Error de análisis de manifiesto: valor de carácter Unicode no válido para esta plataforma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR \_ SxS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Error de análisis de manifiesto: se esperaba un espacio en blanco o '? '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Error de análisis de manifiesto: no se esperaba una etiqueta de cierre en esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Error de análisis de manifiesto: no se cerraron las siguientes etiquetas: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR \_ SxS \_ XML \_ E \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Error de análisis de manifiesto: atributo duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR \_ SxS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Error de análisis de manifiesto: solo se permite un elemento de nivel superior en un documento XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Error de análisis de manifiesto: no válido en el nivel superior del documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR \_ SxS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Error de análisis de manifiesto: declaración XML no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Error de análisis de manifiesto: el documento XML debe tener un elemento de nivel superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR \_ SxS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Error de análisis de manifiesto: final de archivo inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR \_ SxS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Error de análisis de manifiesto: no se pueden usar entidades de parámetro dentro de las declaraciones de marcado de un subconjunto interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Error de análisis de manifiesto: el elemento no se cerró.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Error en el análisis del manifiesto: falta el carácter ' > ' en el elemento final.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Error de análisis de manifiesto: no se cerró un literal de cadena.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Error de análisis de manifiesto: no se cerró un comentario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Error de análisis de manifiesto: no se cerró una declaración.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR \_ SxS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Error de análisis de manifiesto: no se cerró una sección CDATA.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR \_ SxS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Error de análisis de manifiesto: el prefijo de espacio de nombres no puede comenzar con la cadena reservada "XML".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Error de análisis de manifiesto: el sistema no admite la codificación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR \_ SxS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Error de análisis de manifiesto: no se admite el cambio de la codificación actual a la codificación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR \_ SxS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Error de análisis de manifiesto: el nombre ' XML ' está reservado y debe estar en minúsculas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ independiente no válido \_**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Error de análisis de manifiesto: el atributo Standalone debe tener el valor ' Yes ' o ' no '.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR \_ SxS \_ XML \_ E \_ inesperado \_ independiente**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Error de análisis de manifiesto: no se puede usar el atributo independiente en entidades externas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR \_ de \_ versión de XML SxS \_ E \_ no válida \_**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Error de análisis de manifiesto: número de versión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR \_ SxS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Error de análisis de manifiesto: falta el signo igual entre el atributo y el valor de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR \_ de \_ recuperación de protección SxS \_ \_**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Error de protección del ensamblado: no se puede recuperar el ensamblado especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR \_ SxS: la \_ \_ \_ clave pública \_ es demasiado \_ corta**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Error de protección del ensamblado: la clave pública para un ensamblado era demasiado corta para permitirse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR \_ de \_ Catálogo de protección SxS \_ \_ no \_ válido**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Error de protección del ensamblado: el catálogo de un ensamblado no es válido o no coincide con el manifiesto del ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR SxS no traducible que se va a \_ \_ traducir \_**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



No se pudo traducir un valor HRESULT a un código de error de Win32 correspondiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR \_ SxS \_ \_ falta el archivo de catálogo de protección \_ \_**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Error de protección del ensamblado: falta el catálogo de un ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR \_ SxS \_ falta \_ el \_ atributo de identidad de ensamblado \_**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



En la identidad del ensamblado proporcionado faltan uno o varios atributos que deben estar presentes en este contexto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR \_ SxS \_ \_ nombre de \_ atributo de identidad de ensamblado no \_ válido \_**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



La identidad del ensamblado proporcionada tiene uno o más nombres de atributo que contienen caracteres no permitidos en los nombres XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR \_ \_ no se encuentra el ensamblado SxS \_**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



No se pudo encontrar el ensamblado al que se hace referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR \_ de \_ \_ pila de activación dañada SxS \_**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



La pila de activación del contexto de activación para el subproceso de ejecución en ejecución está dañada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR \_ de \_ daños en SxS**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Los metadatos de aislamiento de la aplicación para este proceso o subproceso se han dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR \_ de \_ \_ desactivación temprana de SxS**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



El contexto de activación que se está desactivando no es el que se activó más recientemente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR \_ SxS \_ \_ desactivación no válida**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



El contexto de activación que se está desactivando no está activo para el subproceso de ejecución actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR \_ de \_ \_ desactivación múltiple SxS**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



El contexto de activación que se está desactivando ya se ha desactivado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR \_ de \_ terminación de proceso SxS \_ \_ solicitada**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Un componente usado por la utilidad de aislamiento ha solicitado terminar el proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**ERROR \_ SxS \_ : \_ contexto de activación de versión \_**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Un componente de modo kernel está liberando una referencia en un contexto de activación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR \_ de \_ \_ contexto de activación predeterminado del sistema SxS \_ \_ \_ vacío**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



No se pudo generar el contexto de activación del ensamblado predeterminado del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR \_ SxS \_ \_ valor de \_ atributo de identidad no válido \_**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



El valor de un atributo de una identidad no está dentro del intervalo legal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR \_ SxS \_ \_ nombre de \_ atributo de identidad no válido \_**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



El nombre de un atributo de una identidad no está dentro del intervalo legal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR \_ de \_ \_ atributo duplicado de identidad SxS \_**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Una identidad contiene dos definiciones para el mismo atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**error \_ de \_ análisis de identidad SxS \_ \_**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



La cadena de identidad tiene un formato incorrecto. Esto puede deberse a una coma final, a más de dos atributos sin nombre, que falta el nombre del atributo o que falta un valor de atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR de \_ cadena de sustitución con formato incorrecto \_ \_**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Una cadena que contiene contenido sustituible localizado tenía un formato incorrecto. No se encontró un signo de dólar ($) seguido de un paréntesis de apertura o de otro signo de dólar o de un paréntesis derecho de sustitución.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR \_ de \_ \_ token de \_ clave \_ pública incorrecto SxS**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



El token de clave pública no se corresponde con la clave pública especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR de \_ cadena de sustitución no asignada \_ \_**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Una cadena de sustitución no tiene ninguna asignación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR \_ de \_ ensamblado SxS \_ no \_ bloqueado**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



El componente debe estar bloqueado antes de realizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR \_ SxS \_ almacén de componentes \_ \_ dañado**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



El almacén de componentes está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR \_ de \_ instalador \_ avanzado**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Error de un instalador avanzado durante la instalación o el servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR \_ de \_ coincidencia de codificación XML \_**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



La codificación de caracteres en la declaración XML no coincidía con la codificación utilizada en el documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR en la \_ identidad del manifiesto SxS, \_ pero el contenido es \_ \_ \_ \_ \_ diferente**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Las identidades de los manifiestos son idénticas, pero su contenido es diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR \_ de \_ identidades SxS \_ diferentes**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Las identidades de los componentes son diferentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**\_el error SxS \_ Assembly \_ no es \_ \_ una \_ implementación**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



El ensamblado no es una implementación de.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR \_ \_ de archivo SxS que \_ no \_ forma parte \_ del \_ ensamblado**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



El archivo no forma parte del ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**el \_ manifiesto de error SxS \_ \_ es demasiado \_ grande**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



El tamaño del manifiesto supera el máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR \_ de \_ configuración de SxS \_ no \_ registrada**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



La configuración no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR \_ de \_ cierre de transacción SxS \_ \_ incompleto**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Uno o varios miembros necesarios de la transacción no están presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR en el \_ \_ \_ instalador \_ primitivo de SMI**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Error del instalador primitivo de SMI durante la instalación o el servicio.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR \_ de \_ comando genérico \_ erróneo**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Un ejecutable de comando genérico devolvió un resultado que indica un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR \_ de \_ hash de archivo SxS \_ \_ ausente**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



Falta la información de comprobación de archivos en un componente en su manifiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR \_ evt \_ \_ ruta de acceso de canal no válida \_**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



La ruta de acceso del canal especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR \_ evt \_ consulta no válida \_**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



La consulta especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR \_ evt \_ metadatos del publicador \_ \_ no \_ encontrados**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



No se encuentran los metadatos del publicador en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la plantilla de evento evt**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



No se encuentra la plantilla para una definición de evento en el recurso (error = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR \_ evt \_ \_ nombre de publicador no válido \_**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



El nombre del publicador especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR \_ evt \_ \_ datos de evento no válidos \_**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Los datos de evento generados por el publicador no son compatibles con la definición de la plantilla de evento en el manifiesto del publicador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**ERROR \_ : \_ \_ no \_ se encontró el canal evt**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



No se pudo encontrar el canal especificado. Compruebe la configuración del canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR \_ evt de \_ \_ texto XML con formato incorrecto \_**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



El texto XML especificado no tiene el formato correcto. Vea error extendido para obtener más detalles.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR \_ \_ de suscripción \_ de EVT a \_ \_ canal directo**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



El autor de la llamada está intentando suscribirse a un canal directo que no está permitido. Los eventos de un canal directo van directamente a un archivo de registro y no se pueden suscribir.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**error \_ : \_ error de configuración de EVT \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Error de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR \_ de \_ consulta evt \_ resultado \_ obsoleto**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



El resultado de la consulta es obsoleto o no es válido. Esto puede deberse a que el registro se borra o se revierte una vez creado el resultado de la consulta. Los usuarios deben controlar este código liberando el objeto de resultado de la consulta y reemitiendo la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR \_ : \_ \_ \_ posición no válida del resultado de la consulta evt \_**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



El resultado de la consulta se encuentra actualmente en una posición no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ evt \_ no \_ validando \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



El MSXML registrado no admite la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ evt \_ filtro \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Una expresión solo puede ir seguida de un cambio de operación de ámbito si se evalúa en sí misma como un conjunto de nodos y aún no forma parte de otro cambio de operación de ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ evt \_ filtro \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



No se puede realizar una operación Step desde un término que no representa un conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR \_ evt \_ filtro \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Los argumentos del lado izquierdo de los operadores binarios deben ser atributos, nodos o variables y los argumentos del lado derecho deben ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR \_ evt \_ filtro \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Una operación Step debe implicar una prueba de nodo o, en el caso de un predicado, una expresión algebraica en la que probar cada nodo en el conjunto de nodos identificado por el conjunto de nodos anterior se puede evaluar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR \_ evt \_ filtro \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Este tipo de datos no se admite actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR \_ evt \_ filtro \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Error de sintaxis en la posición %1! d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR \_ evt \_ filtro \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Este operador no es compatible con esta implementación del filtro.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ evt \_ filtro \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



El token encontrado era inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR \_ evt \_ operación no válida \_ \_ en el \_ \_ canal directo habilitado \_**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



La operación solicitada no se puede realizar a través de un canal directo habilitado. Primero debe deshabilitarse el canal antes de realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR \_ evt \_ \_ valor de \_ propiedad de canal no válido \_**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Propiedad de canal %1! s! contiene un valor no válido. El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR \_ evt \_ \_ valor de propiedad de publicador no válido \_ \_**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Propiedad del publicador %1! s! contiene un valor no válido. El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de publicador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR: el \_ \_ canal evt \_ no se puede \_ activar**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



No se puede activar el canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR \_ : \_ filtro evt \_ demasiado \_ complejo**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



La expresión XPath superó la complejidad admitida. Symplify o divídalo en dos o más expresiones simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**ERROR \_ : \_ mensaje evt \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



el recurso de mensaje está presente pero el mensaje no se encuentra en la tabla de cadena/mensaje.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró el identificador de mensaje evt**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



No se pudo encontrar el ID. de mensaje para el mensaje deseado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR \_ evt: \_ inserción de \_ valor sin resolver \_**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



No se encontró la cadena de sustitución para insertar índice (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR \_ evt: \_ inserción de \_ parámetro sin resolver \_**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



No se pudo encontrar la cadena de descripción para la referencia de parámetro (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR \_ evt se \_ alcanzó el número máximo de \_ inserciones \_**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



Se ha alcanzado el número máximo de reemplazos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la definición del evento evt**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



No se encontró la definición de evento para el ID. de evento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR \_ : \_ \_ \_ no \_ se encontró la configuración regional del mensaje evt**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



El recurso específico de configuración regional para el mensaje deseado no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR \_ evt \_ versión \_ demasiado \_ antigua**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



El recurso es demasiado antiguo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR \_ evt \_ versión \_ demasiado \_ nueva**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



El recurso es demasiado nuevo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR \_ evt \_ no se puede \_ abrir el \_ canal \_ de la \_ consulta**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



El canal en el índice %1! d! no se puede abrir la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR \_ evt \_ publicador \_ deshabilitado**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



El publicador se ha deshabilitado y su recurso no está disponible. Esto suele ocurrir cuando el publicador se está desinstalando o actualizando.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**ERROR \_ \_ de filtro evt \_ fuera \_ del \_ intervalo**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Se intentó crear un tipo numérico que está fuera de su intervalo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR \_ la \_ suscripción de EC \_ no se puede \_ activar**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



La suscripción no se puede activar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR \_ de \_ registro EC \_ deshabilitado**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



El registro de la suscripción está en estado deshabilitado y no se puede usar para reenviar eventos a. Primero se debe habilitar el registro antes de que se pueda activar la suscripción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**ERROR \_ de \_ reenvío circular de EC \_**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Al reenviar eventos del equipo local a sí mismo, la consulta de la suscripción no puede contener el registro de destino de la suscripción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR \_ EC \_ CREDSTORE \_ completo**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



El almacén de credenciales que se usa para guardar las credenciales está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR \_ EC \_ CRED \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



No se encuentra la credencial usada por esta suscripción en el almacén de credenciales.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR \_ EC \_ no hay ningún \_ \_ canal activo**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



No se encuentra ningún canal activo para la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**\_ \_ \_ no \_ se encontró el archivo mui de error**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



El cargador de recursos no encontró el archivo MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR \_ de \_ archivo no válido de MUI \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



El cargador de recursos no pudo cargar el archivo MUI porque el archivo no supera la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR \_ de \_ \_ configuración de RC no válida de MUI \_**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



El manifiesto RC está dañado con datos no utilizados o con una versión no admitida o con un elemento necesario que falta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR \_ en \_ \_ el nombre de configuración regional no válido de MUI \_**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



El manifiesto RC tiene un nombre de referencia cultural no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR \_ : \_ \_ nombre de ULTIMATEFALLBACK no válido de MUI \_**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



El manifiesto RC tiene un nombre ultimatefallback no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR \_ de \_ archivo mui \_ no \_ cargado**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



La caché del cargador de recursos no tiene una entrada de MUI cargada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**\_detención de \_ usuario de enumeración de recurso de \_ error \_**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



El usuario detuvo la enumeración de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR de \_ mui \_ INTLSETTINGS \_ UILANG \_ no \_ instalado**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Error en la instalación del idioma de la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR \_ de \_ mui \_ INTLSETTINGS \_ nombre de configuración regional no válido \_**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Error en la instalación de la configuración regional.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR \_ \_ en el tiempo \_ de ejecución de MRM sin \_ \_ recurso predeterminado o \_ neutro \_**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Un recurso no tiene un valor predeterminado o neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR \_ MRM \_ archivo priconfig no válido \_**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Archivo de configuración de PRI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR \_ MRM \_ \_ tipo de archivo no válido \_**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Tipo de archivo no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR \_ MRM \_ desconocido \_ Qualifier**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Calificador desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR \_ MRM \_ \_ valor de calificador no válido \_**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valor de calificador no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR \_ MRM \_ sin \_ candidato**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



No se encontró ningún candidato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR \_ MRM \_ sin \_ coincidencia \_ o \_ \_ candidato predeterminado**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap o NamedResource tiene un elemento que no tiene recursos predeterminados o neutros.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de tipo de recurso de MRM \_**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Tipo de ResourceCandidate no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR \_ MRM \_ \_ nombre de asignación duplicado \_**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Asignación de recursos duplicada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR \_ de \_ MRM \_ entrada duplicada**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Entrada duplicada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR \_ MRM \_ \_ identificador de recurso no válido \_**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificador de recurso no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR \_ MRM \_ FILEPATH \_ Too \_ Long**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



Filepath es demasiado largo.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR \_ MRM \_ tipo de directorio no compatible \_ \_**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Tipo de directorio no compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR \_ MRM \_ \_ archivo PRI no válido \_**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Archivo PRI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR \_ MRM \_ denominado \_ recurso \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



No se encontró NamedResource.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**\_ \_ \_ no \_ se encontró la asignación de error MRM**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



No se encontró ResourceMap.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR \_ MRM \_ tipo de perfil no admitido \_ \_**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Tipo de Perfil de MRT no compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR \_ MRM \_ \_ operador de calificador no válido \_**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Operador de calificador no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR en el \_ \_ \_ valor de calificador indeterminado \_**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



No se puede determinar el valor de calificador o el valor de calificador no se ha establecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR \_ de \_ fusión mediante combinación automerge \_ habilitada**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



Fusionar mediante combinación automáticamente está habilitado en el archivo PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR \_ MRM \_ demasiados \_ \_ recursos**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Demasiados recursos definidos para el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR \_ de \_ \_ cadena de funcionalidades no válidas MCA \_**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



El monitor devolvió una cadena de funcionalidades DDC/CI que no cumplía con las especificaciones ACCESS. bus 3,0, DDC/CI 1,1 o MCCS 2 revisión 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR \_ MCA \_ \_ versión de VCP no válida \_**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



El código VCP de la versión VCP del monitor (0xDF) devolvió un valor de versión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR: el \_ \_ monitor MCA infringe la \_ \_ especificación de MCCS \_**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



El monitor no cumple con la especificación de MCCS que notifica que es compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR \_ no coincidente de la \_ versión MCCS de MCA \_ \_**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



La versión MCCS de la funcionalidad MCCS ver de un monitor \_ no coincide con la versión MCCS que el monitor notifica cuando se usa el código VCP de la versión VCP (0xDF).


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR \_ MCA \_ versión de MCCS no admitida \_ \_**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



La API de configuración de monitor solo funciona con monitores que admiten la especificación MCCS 1,0, MCCS 2,0 Specification o la especificación MCCS 2,0 revisión 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**error \_ interno de MCA \_ \_**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Se ha producido un error interno de API de configuración de monitor.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR \_ MCA \_ tipo de tecnología no válido \_ \_ \_ devuelto**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



El monitor devolvió un tipo de tecnología de monitor no válido. CRT, plasma y LCD (TFT) son ejemplos de tipos de tecnología de supervisión. Este error implica que el monitor infringió la especificación MCCS 2,0 o MCCS 2,0 revisión 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR \_ : \_ temperatura de color no compatible con MCA \_ \_**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



El autor de la llamada de [**SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) especificó una temperatura de color no compatible con el monitor actual. Este error implica que el monitor infringió la especificación MCCS 2,0 o MCCS 2,0 revisión 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR \_ de \_ dispositivo de sistema ambiguo \_**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



No se puede identificar el dispositivo del sistema solicitado debido a que varios dispositivos indistinguibles coinciden potencialmente con los criterios de identificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR \_ de \_ dispositivo de sistema \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



No se encuentra el dispositivo del sistema solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**\_no se \_ \_ admite el hash de error**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



La generación de hash para la versión hash y el tipo hash especificados no está habilitada en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**HASH de ERROR \_ \_ no \_ presente**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



El hash solicitado desde el servidor no está disponible o ya no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR \_ de \_ proveedor de CI secundario \_ \_ no \_ registrado**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



La instancia de controlador de interrupción secundaria que administra la interrupción especificada no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR \_ de \_ información del cliente GPIO \_ \_ no válida**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



La información proporcionada por el controlador de cliente GPIO no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**\_no se \_ admite la versión de GPIO \_ \_**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



No se admite la versión especificada por el controlador cliente GPIO.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR \_ GPIO \_ : \_ paquete de registro no válido \_**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



El paquete de registro proporcionado por el controlador cliente GPIO no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR \_ de \_ operación de GPIO \_ denegada**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



La operación solicitada no es compatible con el identificador especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR \_ GPIO \_ modo de \_ conexión incompatible \_**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



El modo de conexión solicitado entra en conflicto con un modo existente en uno o varios de los pin especificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR \_ de \_ interrupción de GPIO ya sin \_ \_ máscara**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



La interrupción solicitada para desenmascarar no se enmascara.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR \_ no se puede \_ cambiar \_ nivel**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



No se puede completar correctamente el cambio de nivel de ejecución solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR \_ de \_ configuración de nivel no válida \_**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



El servicio tiene un valor de nivel de ejecución no válido. El nivel de ejecución de un servicio no debe ser mayor que el nivel de ejecución de sus servicios dependientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR \_ de \_ tiempo de espera del modificador nivel \_**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



No se puede completar correctamente el cambio de nivel de ejecución solicitado porque uno o varios servicios no se detendrán o se reiniciarán dentro del tiempo de espera especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR \_ nivel \_ cambiar \_ el \_ tiempo de espera del agente**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Un agente de cambio de nivel de ejecución no respondió dentro del tiempo de espera especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR \_ \_ en el modificador nivel \_ en \_ curso**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



Hay un modificador de nivel de ejecución en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR de los servicios de errores de \_ \_ \_ AUTOSTART**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



No se pudo iniciar uno o varios servicios durante la fase de inicio del servicio de un modificador de nivel de ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR de la \_ tarea com de \_ \_ detención \_ pendiente**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



La solicitud de detención de tarea no se puede completar inmediatamente porque la tarea necesita más tiempo para cerrarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR \_ al instalar el \_ \_ paquete abierto \_**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



No se pudo abrir el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR al \_ instalar el \_ paquete \_ no \_ encontrado**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



No se encontró el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR al \_ instalar el \_ paquete no válido \_**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Los datos del paquete no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR \_ al instalar la \_ dependencia de resolución \_ \_**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Error de actualización del paquete, dependencia o validación de conflictos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR al \_ instalar \_ espacio insuficiente en \_ \_ disco \_**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



No hay suficiente espacio en disco en el equipo. Libere espacio y vuelva a intentarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR de instalación de ERROR de \_ \_ red \_**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Se produjo un problema al descargar el producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR de \_ registro de instalación de error \_ \_**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



No se pudo registrar el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR \_ al \_ anular el registro de la instalación \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



No se pudo anular el registro del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR al \_ instalar \_ cancelar**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



El usuario canceló la solicitud de instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR en la instalación del ERROR \_ \_**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Error de instalación. Póngase en contacto con su proveedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR \_ al quitar errores \_**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



No se pudo quitar. Póngase en contacto con su proveedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**el \_ paquete de error \_ ya \_ existe**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



El paquete proporcionado ya está instalado y se ha bloqueado la reinstalación del paquete. Busque detalles en el registro de eventos de AppXDeployment-Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**el ERROR \_ debe \_ corregirse**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



No se puede iniciar la aplicación. Intente volver a instalar la aplicación para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR \_ al instalar el \_ requisito previo de instalación \_**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



No se pudo satisfacer un requisito previo para una instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**el \_ repositorio del paquete de errores \_ \_ está dañado**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



El repositorio de paquetes está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR al \_ instalar la \_ directiva \_**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Para instalar esta aplicación, necesita una licencia de desarrollador de Windows o un sistema habilitado para instalación de prueba.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**\_actualización de paquetes de errores \_**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



No se puede iniciar la aplicación porque se está actualizando actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**\_implementación \_ de error bloqueada por la \_ \_ Directiva**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



La Directiva bloquea la operación de implementación de paquetes. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**\_paquetes \_ de error en \_ uso**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



No se pudo instalar el paquete porque los recursos modificados están actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**el \_ archivo de recuperación de errores \_ \_ está dañado**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



No se pudo recuperar el paquete porque los datos necesarios para la recuperación están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR \_ de \_ firma preconfigurada no válida \_**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



La firma no es válida. Para registrarse en modo de desarrollador, AppxSignature. p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR \_ al eliminar \_ el \_ almacén de APPLICATIONDATA existente \_ \_**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Se produjo un error al eliminar los datos de aplicación existentes anteriormente del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR al \_ instalar la \_ degradación del paquete \_**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



No se pudo instalar el paquete porque ya hay instalada una versión superior de este paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**el \_ sistema de errores \_ necesita \_ corrección**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Se detectó un error en un archivo binario del sistema. Intente actualizar el equipo para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR de integridad de appx error de \_ \_ \_ \_ CLR \_ ngen**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Se detectó un binario CLR NGEN dañado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**archivo de resistencia de errores \_ \_ \_ dañado**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



No se pudo reanudar la operación porque los datos necesarios para la recuperación están dañados.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR al \_ instalar el \_ servicio de Firewall no se \_ \_ \_ está ejecutando**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



No se pudo instalar el paquete porque el servicio Firewall de Windows no se está ejecutando. Habilite el servicio Firewall de Windows e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**\_ \_ no hay ningún paquete de error de APPMODEL \_**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



El proceso no tiene ninguna identidad de paquete.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**tiempo de ejecución del paquete de errores de APPMODEL \_ \_ \_ \_ dañado**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



La información del tiempo de ejecución del paquete está dañada.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**la \_ identidad del paquete de errores de APPMODEL \_ \_ \_ está dañada**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



La identidad del paquete está dañada.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**APPMODEL \_ error \_ sin \_ aplicación**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



El proceso no tiene identidad de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**error en el almacén de carga de \_ estado \_ \_ \_**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



No se pudo cargar el almacén de estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**error \_ \_ al obtener la \_ versión \_ de estado de error**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Error al recuperar la versión de estado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**error en la versión del conjunto de \_ estado \_ \_ \_**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



No se pudo establecer la versión de estado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**error \_ de \_ restablecimiento estructurado de estado \_ de error \_**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



No se pudo restablecer el estado estructurado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR en el \_ \_ \_ contenedor \_ abierto de estado de error**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



El administrador de estado no pudo abrir el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR \_ \_ al crear el \_ contenedor \_ de estado de error**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



El administrador de estado no pudo crear el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR \_ \_ al eliminar el \_ contenedor \_ de estado de error**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



State Manager no pudo eliminar el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**error \_ de \_ configuración de lectura de estado de \_ error \_**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



El administrador de estado no pudo leer la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**error \_ de \_ configuración de escritura de estado de \_ error \_**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



El administrador de estado no pudo escribir la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**error \_ de \_ configuración de eliminación de estado de \_ error \_**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



El administrador de estado no pudo eliminar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**error \_ al \_ establecer la consulta de estado de \_ error \_**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



El administrador de estado no pudo consultar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**error \_ de \_ \_ configuración compuesta de lectura de \_ Estado de \_ error**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



El administrador de estado no pudo leer la configuración compuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**error \_ de \_ \_ configuración compuesta de escritura de \_ Estado de \_ error**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



El administrador de estado no pudo escribir la configuración compuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**error en el \_ \_ contenedor de enumeración de estado de \_ error \_**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



State Manager no pudo enumerar los contenedores.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**error \_ \_ al enumerar la \_ configuración \_ de estado de error**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



State Manager no pudo enumerar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**Estado de ERROR se \_ \_ \_ \_ \_ \_ superó el límite de tamaño del valor de configuración compuesta \_**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



El tamaño del valor de configuración compuesta del administrador de Estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**se \_ \_ \_ \_ \_ superó el límite de tamaño del valor de \_ Estado de error**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



El tamaño del valor de configuración del administrador de Estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**se \_ \_ \_ \_ \_ superó el límite de \_ tamaño de la configuración de estado de error**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



La longitud del nombre de la configuración del administrador de Estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**Estado de ERROR se \_ \_ \_ \_ \_ superó el límite de tamaño del contenedor \_**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



La longitud del nombre del contenedor del administrador de Estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR de \_ API \_ no disponible**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Esta API no se puede usar en el contexto del tipo de aplicación del llamador.


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

 

 
