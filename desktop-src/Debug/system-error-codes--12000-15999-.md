---
description: Describe los códigos de error 12000-1599 definidos en el archivo de encabezado WinError.h y está pensado para desarrolladores.
ms.assetid: bb3c658d-96db-495a-a0dc-e93949c3835d
title: Códigos de error del sistema (12000-15999) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8cac8adf6d8a4cf8f60fe978eb6f99f5efc1b9fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164602"
---
# <a name="system-error-codes-12000-15999"></a>Códigos de error del sistema (12000-15999)

> [!NOTE]
> Esta información está pensada para los desarrolladores que depuran errores del sistema. Para otros errores, como problemas con Windows Update, hay una lista de recursos en la página [Códigos de](system-error-codes.md) error.

En la lista siguiente se [describen los códigos de error del](system-error-codes.md) sistema (errores 12000 a 15999). La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) los devuelve cuando se producirá un error en muchas funciones. Para recuperar el texto de descripción del error en la aplicación, use la [**función FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con la **marca FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_INTERNET__"></span><span id="error_internet__"></span>**ERROR \_ INTERNET\_\***
</dt> <dd> <dl> <dt>

12000 - 12175 (0x2EE0)
</dt> <dt>



Consulte [Códigos de error de Internet](../wininet/wininet-errors.md) y WinInet.h.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_EXISTS"></span><span id="error_ipsec_qm_policy_exists"></span>**ERROR \_ EXISTE LA DIRECTIVA \_ QM DE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13000 (0x32C8)
</dt> <dt>



La directiva de modo rápido especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_qm_policy_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA DIRECTIVA \_ QM \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13001 (0x32C9)
</dt> <dt>



No se encontró la directiva de modo rápido especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_IN_USE"></span><span id="error_ipsec_qm_policy_in_use"></span>**ERROR IPSEC QM POLICY IN USE (ERROR \_ \_ IPSEC QM \_ POLICY IN \_ \_ USE)**
</dt> <dd> <dl> <dt>

13002 (0x32CA)
</dt> <dt>



Se usa la directiva de modo rápido especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_EXISTS"></span><span id="error_ipsec_mm_policy_exists"></span>**ERROR \_ IPSEC \_ MM \_ POLICY \_ EXISTS**
</dt> <dd> <dl> <dt>

13003 (0x32CB)
</dt> <dt>



La directiva de modo principal especificada ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_mm_policy_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA DIRECTIVA MM \_ \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13004 (0x32CC)
</dt> <dt>



No se encontró la directiva de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_IN_USE"></span><span id="error_ipsec_mm_policy_in_use"></span>**ERROR \_ DIRECTIVA MM DE IPSEC EN \_ \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

13005 (0x32CD)
</dt> <dt>



Se usa la directiva de modo principal especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_EXISTS"></span><span id="error_ipsec_mm_filter_exists"></span>**ERROR \_ EXISTE EL FILTRO MM \_ \_ DE IPSEC \_**
</dt> <dd> <dl> <dt>

13006 (0x32CE)
</dt> <dt>



El filtro de modo principal especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_NOT_FOUND"></span><span id="error_ipsec_mm_filter_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL FILTRO MM \_ \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13007 (0x32CF)
</dt> <dt>



No se encontró el filtro de modo principal especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_EXISTS"></span><span id="error_ipsec_transport_filter_exists"></span>**ERROR \_ EXISTE EL FILTRO DE TRANSPORTE \_ \_ IPSEC \_**
</dt> <dd> <dl> <dt>

13008 (0x32D0)
</dt> <dt>



El filtro de modo de transporte especificado ya existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_NOT_FOUND"></span><span id="error_ipsec_transport_filter_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL FILTRO DE TRANSPORTE \_ \_ \_ \_ IPSEC**
</dt> <dd> <dl> <dt>

13009 (0x32D1)
</dt> <dt>



El filtro de modo de transporte especificado no existe.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_EXISTS"></span><span id="error_ipsec_mm_auth_exists"></span>**ERROR \_ IPSEC \_ MM \_ AUTH \_ EXISTS**
</dt> <dd> <dl> <dt>

13010 (0x32D2)
</dt> <dt>



Existe la lista de autenticación del modo principal especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_mm_auth_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA \_ AUTENTICACIÓN MM \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13011 (0x32D3)
</dt> <dt>



No se encontró la lista de autenticación del modo principal especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_IN_USE"></span><span id="error_ipsec_mm_auth_in_use"></span>**ERROR \_ IPSEC MM AUTH IN USE (AUTENTICACIÓN MM DE IPSEC \_ \_ EN \_ \_ USO)**
</dt> <dd> <dl> <dt>

13012 (0x32D4)
</dt> <dt>



Se usa la lista de autenticación del modo principal especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_mm_policy_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA DIRECTIVA MM PREDETERMINADA \_ \_ \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13013 (0x32D5)
</dt> <dt>



No se encontró la directiva de modo principal predeterminada especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_MM_AUTH_NOT_FOUND"></span><span id="error_ipsec_default_mm_auth_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA \_ \_ AUTENTICACIÓN MM \_ PREDETERMINADA \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13014 (0x32D6)
</dt> <dt>



No se encontró la lista de autenticación del modo principal predeterminado especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DEFAULT_QM_POLICY_NOT_FOUND"></span><span id="error_ipsec_default_qm_policy_not_found"></span>**ERROR \_ NO SE ENCONTRÓ LA DIRECTIVA \_ \_ QM PREDETERMINADA \_ \_ DE \_ IPSEC**
</dt> <dd> <dl> <dt>

13015 (0x32D7)
</dt> <dt>



No se encontró la directiva de modo rápido predeterminada especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_EXISTS"></span><span id="error_ipsec_tunnel_filter_exists"></span>**ERROR \_ EXISTE EL FILTRO DE \_ \_ TÚNEL IPSEC \_**
</dt> <dd> <dl> <dt>

13016 (0x32D8)
</dt> <dt>



Existe el filtro de modo de túnel especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_NOT_FOUND"></span><span id="error_ipsec_tunnel_filter_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL FILTRO DE TÚNEL \_ \_ \_ IPSEC \_**
</dt> <dd> <dl> <dt>

13017 (0x32D9)
</dt> <dt>



No se encontró el filtro de modo de túnel especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_FILTER_PENDING_DELETION"></span><span id="error_ipsec_mm_filter_pending_deletion"></span>**ERROR \_ IPSEC \_ MM \_ FILTER \_ PENDING \_ DELETION**
</dt> <dd> <dl> <dt>

13018 (0x32DA)
</dt> <dt>



El filtro Modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TRANSPORT_FILTER_PENDING_DELETION"></span><span id="error_ipsec_transport_filter_pending_deletion"></span>**ERROR FILTRO \_ DE TRANSPORTE \_ IPSEC PENDIENTE DE \_ \_ \_ ELIMINACIÓN**
</dt> <dd> <dl> <dt>

13019 (0x32DB)
</dt> <dt>



El filtro de transporte está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_TUNNEL_FILTER_PENDING_DELETION"></span><span id="error_ipsec_tunnel_filter_pending_deletion"></span>**ERROR FILTRO \_ DE TÚNEL IPSEC \_ PENDIENTE \_ DE \_ \_ ELIMINACIÓN**
</dt> <dd> <dl> <dt>

13020 (0x32DC)
</dt> <dt>



El filtro de túnel está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_mm_policy_pending_deletion"></span>**ERROR IPSEC MM POLICY PENDING DELETION (DIRECTIVA \_ MM DE IPSEC \_ DE ERROR PENDIENTE DE \_ \_ \_ ELIMINACIÓN)**
</dt> <dd> <dl> <dt>

13021 (0x32DD)
</dt> <dt>



La directiva modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_MM_AUTH_PENDING_DELETION"></span><span id="error_ipsec_mm_auth_pending_deletion"></span>**ERROR \_ IPSEC \_ MM \_ AUTH \_ PENDING \_ DELETION**
</dt> <dd> <dl> <dt>

13022 (0x32DE)
</dt> <dt>



La agrupación de autenticación modo principal está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_QM_POLICY_PENDING_DELETION"></span><span id="error_ipsec_qm_policy_pending_deletion"></span>**ERROR \_ IPSEC \_ QM \_ POLICY \_ PENDING \_ DELETION**
</dt> <dd> <dl> <dt>

13023 (0x32DF)
</dt> <dt>



La directiva modo rápido está pendiente de eliminación.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_MM_POLICY_PRUNED"></span><span id="warning_ipsec_mm_policy_pruned"></span>**ADVERTENCIA \_ IPSEC \_ MM POLICY \_ \_ PRUNED**
</dt> <dd> <dl> <dt>

13024 (0x32E0)
</dt> <dt>



La directiva modo principal se agregó correctamente, pero algunas de las ofertas solicitadas no se admiten.


</dt> </dl> </dd> <dt>

<span id="WARNING_IPSEC_QM_POLICY_PRUNED"></span><span id="warning_ipsec_qm_policy_pruned"></span>**ADVERTENCIA \_ IPSEC \_ QM \_ POLICY \_ PRUNED**
</dt> <dd> <dl> <dt>

13025 (0x32E1)
</dt> <dt>



La directiva de modo rápido se agregó correctamente, pero no se admiten algunas de las ofertas solicitadas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_BEGIN"></span><span id="error_ipsec_ike_neg_status_begin"></span>**ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN**
</dt> <dd> <dl> <dt>

13800 (0x35E8)
</dt> <dt>



ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ BEGIN


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTH_FAIL"></span><span id="error_ipsec_ike_auth_fail"></span>**ERROR \_ ERROR DE \_ AUTENTICACIÓN DE IKE \_ IPSEC \_**
</dt> <dd> <dl> <dt>

13801 (0x35E9)
</dt> <dt>



Las credenciales de autenticación de IKE son inaceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ATTRIB_FAIL"></span><span id="error_ipsec_ike_attrib_fail"></span>**ERROR \_ IPSEC \_ IKE \_ ATTRIB \_ FAIL**
</dt> <dd> <dl> <dt>

13802 (0x35EA)
</dt> <dt>



Los atributos de seguridad de IKE son inaceptables.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_PENDING"></span><span id="error_ipsec_ike_negotiation_pending"></span>**ERROR \_ IPSEC \_ IKE \_ NEGOTIATION \_ PENDING**
</dt> <dd> <dl> <dt>

13803 (0x35EB)
</dt> <dt>



Negociación de IKE en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GENERAL_PROCESSING_ERROR"></span><span id="error_ipsec_ike_general_processing_error"></span>**ERROR \_ IPSEC \_ IKE \_ GENERAL \_ PROCESSING \_ ERROR**
</dt> <dd> <dl> <dt>

13804 (0x35EC)
</dt> <dt>



Error de procesamiento general.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TIMED_OUT"></span><span id="error_ipsec_ike_timed_out"></span>**ERROR \_ IPSEC \_ IKE \_ TIMED \_ OUT**
</dt> <dd> <dl> <dt>

13805 (0x35ED)
</dt> <dt>



Se ha producido un tiempo de espera de negociación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_CERT"></span><span id="error_ipsec_ike_no_cert"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ CERT**
</dt> <dd> <dl> <dt>

13806 (0x35EE)
</dt> <dt>



IKE no pudo encontrar el certificado de equipo válido. Póngase en contacto con el administrador de seguridad de red para instalar un certificado válido en el almacén de certificados adecuado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_DELETED"></span><span id="error_ipsec_ike_sa_deleted"></span>**ERROR \_ IPSEC \_ IKE \_ SA \_ DELETED**
</dt> <dd> <dl> <dt>

13807 (0x35EF)
</dt> <dt>



Sa de IKE eliminado por el mismo nivel antes de que se complete el establecimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SA_REAPED"></span><span id="error_ipsec_ike_sa_reaped"></span>**ERROR \_ IPSEC \_ IKE \_ SA \_ REAPED**
</dt> <dd> <dl> <dt>

13808 (0x35F0)
</dt> <dt>



El sa de IKE se eliminó antes de que se completara el establecimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_mm_acquire_drop"></span>**ERROR \_ IPSEC \_ IKE \_ MM \_ ACQUIRE \_ DROP**
</dt> <dd> <dl> <dt>

13809 (0x35F1)
</dt> <dt>



La solicitud de negociación se sentó en la cola demasiado tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_ACQUIRE_DROP"></span><span id="error_ipsec_ike_qm_acquire_drop"></span>**ERROR \_ IPSEC \_ IKE \_ QM \_ ACQUIRE \_ DROP**
</dt> <dd> <dl> <dt>

13810 (0x35F2)
</dt> <dt>



La solicitud de negociación se sentó en la cola demasiado tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_MM"></span><span id="error_ipsec_ike_queue_drop_mm"></span>**ERROR \_ IPSEC \_ IKE \_ QUEUE \_ DROP \_ MM**
</dt> <dd> <dl> <dt>

13811 (0x35F3)
</dt> <dt>



La solicitud de negociación se sentó en la cola demasiado tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QUEUE_DROP_NO_MM"></span><span id="error_ipsec_ike_queue_drop_no_mm"></span>**ERROR \_ IPSEC \_ IKE \_ QUEUE \_ DROP \_ NO \_ MM**
</dt> <dd> <dl> <dt>

13812 (0x35F4)
</dt> <dt>



La solicitud de negociación se sentó en la cola demasiado tiempo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DROP_NO_RESPONSE"></span><span id="error_ipsec_ike_drop_no_response"></span>**ERROR \_ IPSEC \_ IKE \_ DROP \_ NO \_ RESPONSE**
</dt> <dd> <dl> <dt>

13813 (0x35F5)
</dt> <dt>



No hay respuesta del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_DELAY_DROP"></span><span id="error_ipsec_ike_mm_delay_drop"></span>**ERROR \_ IPSEC \_ IKE \_ MM \_ DELAY \_ DROP**
</dt> <dd> <dl> <dt>

13814 (0x35F6)
</dt> <dt>



La negociación tardó demasiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_DELAY_DROP"></span><span id="error_ipsec_ike_qm_delay_drop"></span>**ERROR \_ IPSEC \_ IKE \_ QM \_ DELAY \_ DROP**
</dt> <dd> <dl> <dt>

13815 (0x35F7)
</dt> <dt>



La negociación tardó demasiado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ERROR"></span><span id="error_ipsec_ike_error"></span>**ERROR \_ IPSEC \_ IKE \_ ERROR**
</dt> <dd> <dl> <dt>

13816 (0x35F8)
</dt> <dt>



Error desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRL_FAILED"></span><span id="error_ipsec_ike_crl_failed"></span>**ERROR \_ IPSEC \_ IKE \_ CRL \_ FAILED**
</dt> <dd> <dl> <dt>

13817 (0x35F9)
</dt> <dt>



Error en la comprobación de revocación de certificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_KEY_USAGE"></span><span id="error_ipsec_ike_invalid_key_usage"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ KEY \_ USAGE**
</dt> <dd> <dl> <dt>

13818 (0x35FA)
</dt> <dt>



Uso de clave de certificado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_TYPE"></span><span id="error_ipsec_ike_invalid_cert_type"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ CERT \_ TYPE**
</dt> <dd> <dl> <dt>

13819 (0x35FB)
</dt> <dt>



Tipo de certificado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PRIVATE_KEY"></span><span id="error_ipsec_ike_no_private_key"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ PRIVATE \_ KEY**
</dt> <dd> <dl> <dt>

13820 (0x35FC)
</dt> <dt>



Error de negociación de IKE porque el certificado de máquina usado no tiene una clave privada. Los certificados IPsec requieren una clave privada. Póngase en contacto con Administrador de seguridad de red para reemplazar por un certificado que tenga una clave privada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SIMULTANEOUS_REKEY"></span><span id="error_ipsec_ike_simultaneous_rekey"></span>**ERROR \_ IPSEC \_ IKE \_ SIMULTANEOUS \_ REKEY**
</dt> <dd> <dl> <dt>

13821 (0x35FD)
</dt> <dt>



Se detectaron reclaves simultáneas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAIL"></span><span id="error_ipsec_ike_dh_fail"></span>**ERROR \_ IPSEC \_ IKE \_ DH \_ FAIL**
</dt> <dd> <dl> <dt>

13822 (0x35FE)
</dt> <dt>



Error en Diffie-Hellman cálculo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CRITICAL_PAYLOAD_NOT_RECOGNIZED"></span><span id="error_ipsec_ike_critical_payload_not_recognized"></span>**ERROR \_ IPSEC \_ IKE \_ CRITICAL \_ PAYLOAD \_ NOT \_ RECOGNIZED**
</dt> <dd> <dl> <dt>

13823 (0x35FF)
</dt> <dt>



No sé cómo procesar la carga crítica.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HEADER"></span><span id="error_ipsec_ike_invalid_header"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ HEADER**
</dt> <dd> <dl> <dt>

13824 (0x3600)
</dt> <dt>



Encabezado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_POLICY"></span><span id="error_ipsec_ike_no_policy"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ POLICY**
</dt> <dd> <dl> <dt>

13825 (0x3601)
</dt> <dt>



No hay ninguna directiva configurada.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIGNATURE"></span><span id="error_ipsec_ike_invalid_signature"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ SIGNATURE**
</dt> <dd> <dl> <dt>

13826 (0x3602)
</dt> <dt>



No se pudo comprobar la firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KERBEROS_ERROR"></span><span id="error_ipsec_ike_kerberos_error"></span>**ERROR \_ IPSEC \_ IKE \_ KERBEROS \_ ERROR**
</dt> <dd> <dl> <dt>

13827 (0x3603)
</dt> <dt>



No se pudo autenticar mediante Kerberos.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PUBLIC_KEY"></span><span id="error_ipsec_ike_no_public_key"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ PUBLIC \_ KEY**
</dt> <dd> <dl> <dt>

13828 (0x3604)
</dt> <dt>



El certificado del mismo nivel no tenía una clave pública.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR"></span><span id="error_ipsec_ike_process_err"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR**
</dt> <dd> <dl> <dt>

13829 (0x3605)
</dt> <dt>



Carga de error de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SA"></span><span id="error_ipsec_ike_process_err_sa"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ SA**
</dt> <dd> <dl> <dt>

13830 (0x3606)
</dt> <dt>



Carga de SA de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_PROP"></span><span id="error_ipsec_ike_process_err_prop"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ PROP**
</dt> <dd> <dl> <dt>

13831 (0x3607)
</dt> <dt>



Carga de propuesta de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_TRANS"></span><span id="error_ipsec_ike_process_err_trans"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ TRANS**
</dt> <dd> <dl> <dt>

13832 (0x3608)
</dt> <dt>



Carga de transformación de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_KE"></span><span id="error_ipsec_ike_process_err_ke"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ KE**
</dt> <dd> <dl> <dt>

13833 (0x3609)
</dt> <dt>



Error al procesar la carga de KE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_ID"></span><span id="error_ipsec_ike_process_err_id"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ ID**
</dt> <dd> <dl> <dt>

13834 (0x360A)
</dt> <dt>



Carga del identificador de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT"></span><span id="error_ipsec_ike_process_err_cert"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ CERT**
</dt> <dd> <dl> <dt>

13835 (0x360B)
</dt> <dt>



Carga del certificado de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_CERT_REQ"></span><span id="error_ipsec_ike_process_err_cert_req"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ CERT \_ REQ**
</dt> <dd> <dl> <dt>

13836 (0x360C)
</dt> <dt>



Error al procesar la carga de solicitud de certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_HASH"></span><span id="error_ipsec_ike_process_err_hash"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ HASH**
</dt> <dd> <dl> <dt>

13837 (0x360D)
</dt> <dt>



Error al procesar la carga hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_SIG"></span><span id="error_ipsec_ike_process_err_sig"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ SIG**
</dt> <dd> <dl> <dt>

13838 (0x360E)
</dt> <dt>



Error al procesar la carga de firma.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NONCE"></span><span id="error_ipsec_ike_process_err_nonce"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ NONCE**
</dt> <dd> <dl> <dt>

13839 (0x360F)
</dt> <dt>



Carga nonce de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NOTIFY"></span><span id="error_ipsec_ike_process_err_notify"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ NOTIFY**
</dt> <dd> <dl> <dt>

13840 (0x3610)
</dt> <dt>



Carga de notificación de procesamiento de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_DELETE"></span><span id="error_ipsec_ike_process_err_delete"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ DELETE**
</dt> <dd> <dl> <dt>

13841 (0x3611)
</dt> <dt>



Error al procesar la carga de eliminación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_VENDOR"></span><span id="error_ipsec_ike_process_err_vendor"></span>**ERROR \_ IPSEC \_ IKE \_ PROCESS \_ ERR \_ VENDOR**
</dt> <dd> <dl> <dt>

13842 (0x3612)
</dt> <dt>



Error al procesar la carga de VendorId.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_PAYLOAD"></span><span id="error_ipsec_ike_invalid_payload"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ PAYLOAD**
</dt> <dd> <dl> <dt>

13843 (0x3613)
</dt> <dt>



Carga no válida recibida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_SOFT_SA"></span><span id="error_ipsec_ike_load_soft_sa"></span>**ERROR \_ IPSEC \_ IKE \_ LOAD \_ SOFT \_ SA**
</dt> <dd> <dl> <dt>

13844 (0x3614)
</dt> <dt>



Soft SA cargado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SOFT_SA_TORN_DOWN"></span><span id="error_ipsec_ike_soft_sa_torn_down"></span>**ERROR \_ IPSEC \_ IKE \_ SOFT \_ SA \_ TORN \_ DOWN**
</dt> <dd> <dl> <dt>

13845 (0x3615)
</dt> <dt>



Soft SA se ha desatrabado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_COOKIE"></span><span id="error_ipsec_ike_invalid_cookie"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ COOKIE**
</dt> <dd> <dl> <dt>

13846 (0x3616)
</dt> <dt>



Cookie no válida recibida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_PEER_CERT"></span><span id="error_ipsec_ike_no_peer_cert"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ PEER \_ CERT**
</dt> <dd> <dl> <dt>

13847 (0x3617)
</dt> <dt>



El mismo nivel no pudo enviar un certificado de máquina válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_CRL_FAILED"></span><span id="error_ipsec_ike_peer_crl_failed"></span>**ERROR \_ IPSEC \_ IKE \_ PEER \_ CRL \_ FAILED**
</dt> <dd> <dl> <dt>

13848 (0x3618)
</dt> <dt>



Error en la comprobación de revocación de certificación del certificado del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_CHANGE"></span><span id="error_ipsec_ike_policy_change"></span>**ERROR \_ CAMBIO DE DIRECTIVA DE \_ IKE DE IPSEC \_ \_**
</dt> <dd> <dl> <dt>

13849 (0x3619)
</dt> <dt>



Las nuevas directivas invalidan las SU formadas con la directiva anterior.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NO_MM_POLICY"></span><span id="error_ipsec_ike_no_mm_policy"></span>**ERROR \_ IPSEC \_ IKE \_ NO \_ MM \_ POLICY**
</dt> <dd> <dl> <dt>

13850 (0x361A)
</dt> <dt>



No hay ninguna directiva de IKE en modo principal disponible.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NOTCBPRIV"></span><span id="error_ipsec_ike_notcbpriv"></span>**ERROR \_ IPSEC \_ IKE \_ NOTCBPRIV**
</dt> <dd> <dl> <dt>

13851 (0x361B)
</dt> <dt>



No se pudo habilitar el privilegio TCB.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SECLOADFAIL"></span><span id="error_ipsec_ike_secloadfail"></span>**ERROR \_ IPSEC \_ IKE \_ SECLOADFAIL**
</dt> <dd> <dl> <dt>

13852 (0x361C)
</dt> <dt>



No se pudo cargar SECURITY.DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILSSPINIT"></span><span id="error_ipsec_ike_failsspinit"></span>**ERROR \_ IPSEC \_ IKE \_ FAILSSPISPISPISPISPI**
</dt> <dd> <dl> <dt>

13853 (0x361D)
</dt> <dt>



No se pudo obtener la dirección de distribución de la tabla de funciones de seguridad de SSPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_FAILQUERYSSP"></span><span id="error_ipsec_ike_failqueryssp"></span>**ERROR \_ IPSEC \_ IKE \_ FAILQUERYSSP**
</dt> <dd> <dl> <dt>

13854 (0x361E)
</dt> <dt>



No se pudo consultar el paquete kerberos para obtener el tamaño máximo del token.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVACQFAIL"></span><span id="error_ipsec_ike_srvacqfail"></span>**ERROR \_ IPSEC \_ IKE \_ SRVACQFAIL**
</dt> <dd> <dl> <dt>

13855 (0x361F)
</dt> <dt>



No se pudieron obtener las credenciales del servidor Kerberos para el servicio \_ \_ IKE de IPSEC ISAKMP/ERROR. La autenticación Kerberos no funcionará. El motivo más probable es la falta de pertenencia a un dominio. Esto es normal si el equipo es miembro de un grupo de trabajo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SRVQUERYCRED"></span><span id="error_ipsec_ike_srvquerycred"></span>**ERROR \_ IPSEC \_ IKE \_ SRVQUERYCRED**
</dt> <dd> <dl> <dt>

13856 (0x3620)
</dt> <dt>



No se pudo determinar el nombre principal de SSPI para el servicio IKE de IPSEC ISAKMP/ERROR \_ \_ ([**QueryCredentialsAttributes**](/windows/win32/api/sspi/nf-sspi-querycredentialsattributesa)).


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_GETSPIFAIL"></span><span id="error_ipsec_ike_getspifail"></span>**ERROR \_ IPSEC \_ IKE \_ GETSPIFAIL**
</dt> <dd> <dl> <dt>

13857 (0x3621)
</dt> <dt>



No se pudo obtener el nuevo SPI para el SA de entrada del controlador IPsec. La causa más común de esto es que el controlador no tiene el filtro correcto. Compruebe la directiva para comprobar los filtros.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_FILTER"></span><span id="error_ipsec_ike_invalid_filter"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ FILTER**
</dt> <dd> <dl> <dt>

13858 (0x3622)
</dt> <dt>



El filtro especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_OUT_OF_MEMORY"></span><span id="error_ipsec_ike_out_of_memory"></span>**ERROR \_ IPSEC \_ IKE \_ OUT \_ OF \_ MEMORY**
</dt> <dd> <dl> <dt>

13859 (0x3623)
</dt> <dt>



Se produjo un error de asignación de memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ADD_UPDATE_KEY_FAILED"></span><span id="error_ipsec_ike_add_update_key_failed"></span>**ERROR \_ IPSEC \_ IKE \_ ADD \_ UPDATE \_ KEY \_ FAILED**
</dt> <dd> <dl> <dt>

13860 (0x3624)
</dt> <dt>



No se pudo agregar la asociación de seguridad al controlador IPsec. La causa más común es si la negociación de IKE tardó demasiado tiempo en completarse. Si el problema persiste, reduzca la carga en la máquina con errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_POLICY"></span><span id="error_ipsec_ike_invalid_policy"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ POLICY**
</dt> <dd> <dl> <dt>

13861 (0x3625)
</dt> <dt>



Directiva no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNKNOWN_DOI"></span><span id="error_ipsec_ike_unknown_doi"></span>**ERROR \_ IPSEC \_ IKE \_ UNKNOWN \_ DOI**
</dt> <dd> <dl> <dt>

13862 (0x3626)
</dt> <dt>



DOI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SITUATION"></span><span id="error_ipsec_ike_invalid_situation"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ SITUATION**
</dt> <dd> <dl> <dt>

13863 (0x3627)
</dt> <dt>



Situación no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DH_FAILURE"></span><span id="error_ipsec_ike_dh_failure"></span>**ERROR \_ IPSEC \_ IKE \_ DH \_ FAILURE**
</dt> <dd> <dl> <dt>

13864 (0x3628)
</dt> <dt>



Diffie-Hellman error.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_GROUP"></span><span id="error_ipsec_ike_invalid_group"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ GROUP**
</dt> <dd> <dl> <dt>

13865 (0x3629)
</dt> <dt>



Grupo Diffie-Hellman no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_ENCRYPT"></span><span id="error_ipsec_ike_encrypt"></span>**ERROR \_ IPSEC \_ IKE \_ ENCRYPT**
</dt> <dd> <dl> <dt>

13866 (0x362A)
</dt> <dt>



Carga de cifrado de errores.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DECRYPT"></span><span id="error_ipsec_ike_decrypt"></span>**ERROR \_ IPSEC \_ IKE \_ DECRYPT**
</dt> <dd> <dl> <dt>

13867 (0x362B)
</dt> <dt>



Error al descifrar la carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_POLICY_MATCH"></span><span id="error_ipsec_ike_policy_match"></span>**ERROR \_ IPSEC \_ IKE \_ POLICY \_ MATCH**
</dt> <dd> <dl> <dt>

13868 (0x362C)
</dt> <dt>



Error de coincidencia de directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNSUPPORTED_ID"></span><span id="error_ipsec_ike_unsupported_id"></span>**ERROR \_ IPSEC \_ IKE \_ UNSUPPORTED \_ ID**
</dt> <dd> <dl> <dt>

13869 (0x362D)
</dt> <dt>



Identificador no admitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH"></span><span id="error_ipsec_ike_invalid_hash"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ HASH**
</dt> <dd> <dl> <dt>

13870 (0x362E)
</dt> <dt>



Error de comprobación de hash.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_ALG"></span><span id="error_ipsec_ike_invalid_hash_alg"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ HASH \_ ALG**
</dt> <dd> <dl> <dt>

13871 (0x362F)
</dt> <dt>



Algoritmo hash no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_HASH_SIZE"></span><span id="error_ipsec_ike_invalid_hash_size"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ HASH \_ SIZE**
</dt> <dd> <dl> <dt>

13872 (0x3630)
</dt> <dt>



Tamaño hash no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_ENCRYPT_ALG"></span><span id="error_ipsec_ike_invalid_encrypt_alg"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ ENCRYPT \_ ALG**
</dt> <dd> <dl> <dt>

13873 (0x3631)
</dt> <dt>



Algoritmo de cifrado no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_ALG"></span><span id="error_ipsec_ike_invalid_auth_alg"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ AUTH \_ ALG**
</dt> <dd> <dl> <dt>

13874 (0x3632)
</dt> <dt>



Algoritmo de autenticación no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_SIG"></span><span id="error_ipsec_ike_invalid_sig"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ SIG**
</dt> <dd> <dl> <dt>

13875 (0x3633)
</dt> <dt>



Firma de certificado no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_LOAD_FAILED"></span><span id="error_ipsec_ike_load_failed"></span>**ERROR \_ IPSEC \_ IKE \_ LOAD \_ FAILED**
</dt> <dd> <dl> <dt>

13876 (0x3634)
</dt> <dt>



Error de carga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RPC_DELETE"></span><span id="error_ipsec_ike_rpc_delete"></span>**ERROR \_ IPSEC \_ IKE \_ RPC \_ DELETE**
</dt> <dd> <dl> <dt>

13877 (0x3635)
</dt> <dt>



Se elimina a través de una llamada RPC.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_BENIGN_REINIT"></span><span id="error_ipsec_ike_benign_reinit"></span>**ERROR \_ IPSEC \_ IKE \_ BENIGN \_ REINIT**
</dt> <dd> <dl> <dt>

13878 (0x3636)
</dt> <dt>



Estado temporal creado para realizar la reinicialización. Esto no es un error real.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_RESPONDER_LIFETIME_NOTIFY"></span><span id="error_ipsec_ike_invalid_responder_lifetime_notify"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ RESPONDER \_ LIFETIME \_ NOTIFY**
</dt> <dd> <dl> <dt>

13879 (0x3637)
</dt> <dt>



El valor de duración recibido en notificación de duración del respondedor está por debajo Windows valor mínimo configurado de 2000. Corrija la directiva en la máquina del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MAJOR_VERSION"></span><span id="error_ipsec_ike_invalid_major_version"></span>**ERROR \_ IPSEC \_ IKE \_ VERSIÓN PRINCIPAL NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

13880 (0x3638)
</dt> <dt>



El destinatario no puede controlar la versión de IKE especificada en el encabezado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_CERT_KEYLEN"></span><span id="error_ipsec_ike_invalid_cert_keylen"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ CERT \_ KEYLEN**
</dt> <dd> <dl> <dt>

13881 (0x3639)
</dt> <dt>



La longitud de clave en el certificado es demasiado pequeña para los requisitos de seguridad configurados.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_LIMIT"></span><span id="error_ipsec_ike_mm_limit"></span>**ERROR \_ IPSEC \_ IKE \_ MM \_ LIMIT**
</dt> <dd> <dl> <dt>

13882 (0x363A)
</dt> <dt>



Se superó el número máximo de MM SAs establecidos para emparejar.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEGOTIATION_DISABLED"></span><span id="error_ipsec_ike_negotiation_disabled"></span>**ERROR \_ IPSEC \_ IKE \_ NEGOTIATION \_ DISABLED**
</dt> <dd> <dl> <dt>

13883 (0x363B)
</dt> <dt>



IKE recibió una directiva que deshabilita la negociación.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_LIMIT"></span><span id="error_ipsec_ike_qm_limit"></span>**ERROR \_ IPSEC \_ IKE \_ QM \_ LIMIT**
</dt> <dd> <dl> <dt>

13884 (0x363C)
</dt> <dt>



Se alcanzó el límite máximo de modo rápido para el modo principal. Se inicia el nuevo modo principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_MM_EXPIRED"></span><span id="error_ipsec_ike_mm_expired"></span>**ERROR \_ IPSEC \_ IKE \_ MM \_ EXPIRED**
</dt> <dd> <dl> <dt>

13885 (0x363D)
</dt> <dt>



La duración de SA del modo principal expiró o el mismo nivel envió una eliminación del modo principal.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_MM_ASSUMED_INVALID"></span><span id="error_ipsec_ike_peer_mm_assumed_invalid"></span>**ERROR \_ IPSEC \_ IKE \_ PEER MM SE SUPONE QUE NO ES \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

13886 (0x363E)
</dt> <dt>



Se supone que sa del modo principal no es válido porque el mismo nivel ha dejado de responder.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CERT_CHAIN_POLICY_MISMATCH"></span><span id="error_ipsec_ike_cert_chain_policy_mismatch"></span>**ERROR \_ IPSEC \_ IKE \_ CERT \_ CHAIN \_ POLICY \_ MISMATCH**
</dt> <dd> <dl> <dt>

13887 (0x363F)
</dt> <dt>



El certificado no se encadena a una raíz de confianza en la directiva de IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_UNEXPECTED_MESSAGE_ID"></span><span id="error_ipsec_ike_unexpected_message_id"></span>**ERROR \_ IPSEC \_ IKE \_ UNEXPECTED \_ MESSAGE \_ ID**
</dt> <dd> <dl> <dt>

13888 (0x3640)
</dt> <dt>



Se ha recibido un identificador de mensaje inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_AUTH_PAYLOAD"></span><span id="error_ipsec_ike_invalid_auth_payload"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ AUTH \_ PAYLOAD**
</dt> <dd> <dl> <dt>

13889 (0x3641)
</dt> <dt>



Se han recibido ofertas de autenticación no válidas.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_DOS_COOKIE_SENT"></span><span id="error_ipsec_ike_dos_cookie_sent"></span>**ERROR \_ IPSEC \_ IKE \_ DOS \_ COOKIE \_ SENT**
</dt> <dd> <dl> <dt>

13890 (0x3642)
</dt> <dt>



Se ha enviado una notificación de cookie de DoS al iniciador.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_SHUTTING_DOWN"></span><span id="error_ipsec_ike_shutting_down"></span>**ERROR \_ IPSEC \_ IKE \_ SHUTTING \_ DOWN**
</dt> <dd> <dl> <dt>

13891 (0x3643)
</dt> <dt>



El servicio IKE se está cerrando.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_CGA_AUTH_FAILED"></span><span id="error_ipsec_ike_cga_auth_failed"></span>**ERROR \_ ERROR AL \_ AUTENTICAR CGA DE IPSEC \_ IKE \_ \_**
</dt> <dd> <dl> <dt>

13892 (0x3644)
</dt> <dt>



No se pudo comprobar el enlace entre la dirección CGA y el certificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PROCESS_ERR_NATOA"></span><span id="error_ipsec_ike_process_err_natoa"></span>**ERROR: \_ ERROR IPSEC \_ IKE PROCESS ERR AND AND A (ERROR: ERROR IPSEC IKE \_ PROCESS ERR AL ERROR DE \_ \_ IPSEC)**
</dt> <dd> <dl> <dt>

13893 (0x3645)
</dt> <dt>



Error al procesar la carga de NatOA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INVALID_MM_FOR_QM"></span><span id="error_ipsec_ike_invalid_mm_for_qm"></span>**ERROR \_ IPSEC \_ IKE \_ INVALID \_ MM \_ FOR \_ QM**
</dt> <dd> <dl> <dt>

13894 (0x3646)
</dt> <dt>



Los parámetros del modo principal no son válidos para este modo rápido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_QM_EXPIRED"></span><span id="error_ipsec_ike_qm_expired"></span>**ERROR \_ IPSEC \_ IKE \_ QM \_ EXPIRED**
</dt> <dd> <dl> <dt>

13895 (0x3647)
</dt> <dt>



El controlador IPsec expiró en el modo rápido SA.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_TOO_MANY_FILTERS"></span><span id="error_ipsec_ike_too_many_filters"></span>**ERROR \_ IPSEC \_ IKE \_ TOO \_ MANY \_ FILTERS**
</dt> <dd> <dl> <dt>

13896 (0x3648)
</dt> <dt>



Se detectaron demasiados filtros IXT agregados dinámicamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_END"></span><span id="error_ipsec_ike_neg_status_end"></span>**ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ END**
</dt> <dd> <dl> <dt>

13897 (0x3649)
</dt> <dt>



ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ END


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_KILL_DUMMY_NAP_TUNNEL"></span><span id="error_ipsec_ike_kill_dummy_nap_tunnel"></span>**ERROR \_ IPSEC \_ IKE \_ KILL \_ DUMMY \_ NAP \_ TUNNEL**
</dt> <dd> <dl> <dt>

13898 (0x364A)
</dt> <dt>



La autenticación de NAP se ha autenticado correctamente y debe eliminar el túnel IKEv2 de NAP ficticio.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_INNER_IP_ASSIGNMENT_FAILURE"></span><span id="error_ipsec_ike_inner_ip_assignment_failure"></span>**ERROR \_ IPSEC \_ IKE \_ INNER \_ IP \_ ASSIGNMENT \_ FAILURE**
</dt> <dd> <dl> <dt>

13899 (0x364B)
</dt> <dt>



Error al asignar la dirección IP interna al iniciador en modo de túnel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_REQUIRE_CP_PAYLOAD_MISSING"></span><span id="error_ipsec_ike_require_cp_payload_missing"></span>**ERROR \_ IPSEC \_ IKE \_ REQUIRE \_ CP \_ PAYLOAD \_ MISSING**
</dt> <dd> <dl> <dt>

13900 (0x364C)
</dt> <dt>



Falta la carga de configuración necesaria.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_KEY_MODULE_IMPERSONATION_NEGOTIATION_PENDING"></span><span id="error_ipsec_key_module_impersonation_negotiation_pending"></span>**ERROR \_ IPSEC \_ KEY \_ MODULE \_ IMPERSONATION \_ NEGOTIATION \_ PENDING**
</dt> <dd> <dl> <dt>

13901 (0x364D)
</dt> <dt>



Una negociación que se ejecuta como el principio de seguridad que emitió la conexión está en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_COEXISTENCE_SUPPRESS"></span><span id="error_ipsec_ike_coexistence_suppress"></span>**ERROR \_ IPSEC \_ IKE \_ COEXISTENCE \_ SUPPRESS**
</dt> <dd> <dl> <dt>

13902 (0x364E)
</dt> <dt>



SA se eliminó debido a la comprobación de supresión de coexistencia de IKEv1/AuthIP.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_RATELIMIT_DROP"></span><span id="error_ipsec_ike_ratelimit_drop"></span>**ERROR \_ IPSEC \_ IKE \_ RATELIMIT \_ DROP**
</dt> <dd> <dl> <dt>

13903 (0x364F)
</dt> <dt>



La solicitud de SA entrante se ha eliminado debido a la limitación de la velocidad de direcciones IP del mismo nivel.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_PEER_DOESNT_SUPPORT_MOBIKE"></span><span id="error_ipsec_ike_peer_doesnt_support_mobike"></span>**ERROR \_ IPSEC \_ IKE \_ PEER \_ DOESNT SUPPORT MO \_ \_ BIKE**
</dt> <dd> <dl> <dt>

13904 (0x3650)
</dt> <dt>



El mismo nivel no admite MO BIKE.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_authorization_failure"></span>**ERROR \_ IPSEC \_ IKE \_ AUTHORIZATION \_ FAILURE**
</dt> <dd> <dl> <dt>

13905 (0x3651)
</dt> <dt>



El establecimiento de la asociación de seguridad no está autorizado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_failure"></span>**ERROR \_ IPSEC \_ IKE \_ STRONG \_ CRED \_ AUTHORIZATION \_ FAILURE**
</dt> <dd> <dl> <dt>

13906 (0x3652)
</dt> <dt>



El establecimiento de SA no está autorizado porque no hay una credencial suficientemente segura basada en PKINIT.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_AUTHORIZATION_FAILURE_WITH_OPTIONAL_RETRY"></span><span id="error_ipsec_ike_authorization_failure_with_optional_retry"></span>**ERROR IPSEC IKE AUTHORIZATION FAILURE WITH OPTIONAL RETRY (ERROR DE AUTORIZACIÓN DE IKE DE \_ \_ IPSEC \_ CON REINTENTO \_ \_ \_ \_ OPCIONAL)**
</dt> <dd> <dl> <dt>

13907 (0x3653)
</dt> <dt>



El establecimiento de la asociación de seguridad no está autorizado. Es posible que tenga que escribir credenciales actualizadas o diferentes, como una tarjeta inteligente.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_STRONG_CRED_AUTHORIZATION_AND_CERTMAP_FAILURE"></span><span id="error_ipsec_ike_strong_cred_authorization_and_certmap_failure"></span>**ERROR \_ IPSEC \_ IKE \_ STRONG \_ CRED \_ AUTHORIZATION \_ AND \_ CERTMAP \_ FAILURE**
</dt> <dd> <dl> <dt>

13908 (0x3654)
</dt> <dt>



El establecimiento de SA no está autorizado porque no hay una credencial suficientemente segura basada en PKINIT. Esto puede estar relacionado con un error de asignación de certificado a cuenta para la sa.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_IKE_NEG_STATUS_EXTENDED_END"></span><span id="error_ipsec_ike_neg_status_extended_end"></span>**ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ EXTENDED \_ END**
</dt> <dd> <dl> <dt>

13909 (0x3655)
</dt> <dt>



ERROR \_ IPSEC \_ IKE \_ NEG \_ STATUS \_ EXTENDED \_ END


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_BAD_SPI"></span><span id="error_ipsec_bad_spi"></span>**ERROR \_ IPSEC \_ BAD \_ SPI**
</dt> <dd> <dl> <dt>

13910 (0x3656)
</dt> <dt>



El SPI del paquete no coincide con un SA de IPsec válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_SA_LIFETIME_EXPIRED"></span><span id="error_ipsec_sa_lifetime_expired"></span>**ERROR \_ IPSEC \_ SA \_ LIFETIME \_ EXPIRED**
</dt> <dd> <dl> <dt>

13911 (0x3657)
</dt> <dt>



El paquete se recibió en un SA de IPsec cuya duración ha expirado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_WRONG_SA"></span><span id="error_ipsec_wrong_sa"></span>**ERROR \_ IPSEC \_ WRONG \_ SA**
</dt> <dd> <dl> <dt>

13912 (0x3658)
</dt> <dt>



El paquete se recibió en un SA de IPsec que no coincide con las características del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_REPLAY_CHECK_FAILED"></span><span id="error_ipsec_replay_check_failed"></span>**ERROR \_ IPSEC \_ REPLAY \_ CHECK \_ FAILED**
</dt> <dd> <dl> <dt>

13913 (0x3659)
</dt> <dt>



Error en la comprobación de la reproducción del número de secuencia de paquetes.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INVALID_PACKET"></span><span id="error_ipsec_invalid_packet"></span>**ERROR \_ IPSEC \_ INVALID \_ PACKET**
</dt> <dd> <dl> <dt>

13914 (0x365A)
</dt> <dt>



El encabezado o finalizador IPsec del paquete no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_INTEGRITY_CHECK_FAILED"></span><span id="error_ipsec_integrity_check_failed"></span>**ERROR ERROR \_ EN LA COMPROBACIÓN DE INTEGRIDAD \_ \_ DE IPSEC \_**
</dt> <dd> <dl> <dt>

13915 (0x365B)
</dt> <dt>



Error en la comprobación de integridad de IPsec.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_CLEAR_TEXT_DROP"></span><span id="error_ipsec_clear_text_drop"></span>**ERROR \_ IPSEC \_ CLEAR \_ TEXT \_ DROP**
</dt> <dd> <dl> <dt>

13916 (0x365C)
</dt> <dt>



IPsec ha eliminado un paquete de texto no cifrado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_AUTH_FIREWALL_DROP"></span><span id="error_ipsec_auth_firewall_drop"></span>**ERROR \_ IPSEC \_ AUTH \_ FIREWALL \_ DROP**
</dt> <dd> <dl> <dt>

13917 (0x365D)
</dt> <dt>



IPsec ha eliminado un paquete ESP entrante en modo de firewall autenticado. Esta caída es benigna.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_THROTTLE_DROP"></span><span id="error_ipsec_throttle_drop"></span>**ERROR \_ IPSEC \_ THROTTLE \_ DROP**
</dt> <dd> <dl> <dt>

13918 (0x365E)
</dt> <dt>



IPsec ha eliminado un paquete debido a la limitación de DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_BLOCK"></span><span id="error_ipsec_dosp_block"></span>**ERROR \_ IPSEC \_ DOSP \_ BLOCK**
</dt> <dd> <dl> <dt>

13925 (0x3665)
</dt> <dt>



IPsec DoS Protection coincidía con una regla de bloque explícita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_RECEIVED_MULTICAST"></span><span id="error_ipsec_dosp_received_multicast"></span>**ERROR \_ IPSEC \_ DOSP \_ RECEIVED \_ MULTICAST**
</dt> <dd> <dl> <dt>

13926 (0x3666)
</dt> <dt>



IPsec DoS Protection recibió un paquete de multidifusión específico de IPsec que no está permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_INVALID_PACKET"></span><span id="error_ipsec_dosp_invalid_packet"></span>**ERROR \_ IPSEC \_ DOSP \_ INVALID \_ PACKET**
</dt> <dd> <dl> <dt>

13927 (0x3667)
</dt> <dt>



IPsec DoS Protection recibió un paquete con formato incorrecto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_STATE_LOOKUP_FAILED"></span><span id="error_ipsec_dosp_state_lookup_failed"></span>**ERROR \_ IPSEC \_ DOSP \_ STATE \_ LOOKUP \_ FAILED**
</dt> <dd> <dl> <dt>

13928 (0x3668)
</dt> <dt>



IPsec DoS Protection no pudo buscar el estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_ENTRIES"></span><span id="error_ipsec_dosp_max_entries"></span>**ERROR \_ IPSEC \_ DOSP \_ MAX \_ ENTRIES**
</dt> <dd> <dl> <dt>

13929 (0x3669)
</dt> <dt>



IPsec DoS Protection no pudo crear el estado porque se ha alcanzado el número máximo de entradas permitido por la directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_KEYMOD_NOT_ALLOWED"></span><span id="error_ipsec_dosp_keymod_not_allowed"></span>**ERROR \_ IPSEC \_ DOSP \_ KEYMOD \_ NOT \_ ALLOWED**
</dt> <dd> <dl> <dt>

13930 (0x366A)
</dt> <dt>



IPsec DoS Protection recibió un paquete de negociación de IPsec para un módulo de claves que la directiva no permite.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_NOT_INSTALLED"></span><span id="error_ipsec_dosp_not_installed"></span>**ERROR \_ IPSEC \_ DOSP \_ NOT \_ INSTALLED**
</dt> <dd> <dl> <dt>

13931 (0x366B)
</dt> <dt>



No se ha habilitado la protección contra IPsec DoS.


</dt> </dl> </dd> <dt>

<span id="ERROR_IPSEC_DOSP_MAX_PER_IP_RATELIMIT_QUEUES"></span><span id="error_ipsec_dosp_max_per_ip_ratelimit_queues"></span>**ERROR \_ IPSEC \_ DOSP \_ MAX \_ PER \_ IP \_ RATELIMIT \_ QUEUES**
</dt> <dd> <dl> <dt>

13932 (0x366C)
</dt> <dt>



IPsec DoS Protection no pudo crear una cola por límite de velocidad ip interna porque se ha alcanzado el número máximo de colas permitido por la directiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SECTION_NOT_FOUND"></span><span id="error_sxs_section_not_found"></span>**NO \_ SE ENCONTRÓ LA SECCIÓN \_ SXS DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

14000 (0x36B0)
</dt> <dt>



La sección solicitada no estaba presente en el contexto de activación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CANT_GEN_ACTCTX"></span><span id="error_sxs_cant_gen_actctx"></span>**ERROR \_ SXS \_ CANT \_ GEN \_ ACTCTX**
</dt> <dd> <dl> <dt>

14001 (0x36B1)
</dt> <dt>



No se pudo iniciar la aplicación porque su configuración en paralelo es incorrecta. Consulte el registro de eventos de la aplicación o use la herramienta de sxstrace.exe comandos para obtener más detalles.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ACTCTXDATA_FORMAT"></span><span id="error_sxs_invalid_actctxdata_format"></span>**ERROR \_ SXS \_ INVALID \_ ACTCTXDATA \_ FORMAT**
</dt> <dd> <dl> <dt>

14002 (0x36B2)
</dt> <dt>



El formato de datos de enlace de aplicaciones no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_FOUND"></span><span id="error_sxs_assembly_not_found"></span>**ERROR \_ ENSAMBLADO SXS \_ NO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

14003 (0x36B3)
</dt> <dt>



El ensamblado al que se hace referencia no está instalado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_FORMAT_ERROR"></span><span id="error_sxs_manifest_format_error"></span>**ERROR \_ SXS \_ MANIFEST \_ FORMAT \_ ERROR**
</dt> <dd> <dl> <dt>

14004 (0x36B4)
</dt> <dt>



El archivo de manifiesto no comienza con la etiqueta y la información de formato necesarias.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_PARSE_ERROR"></span><span id="error_sxs_manifest_parse_error"></span>**ERROR \_ SXS \_ MANIFEST \_ PARSE \_ ERROR**
</dt> <dd> <dl> <dt>

14005 (0x36B5)
</dt> <dt>



El archivo de manifiesto contiene uno o varios errores de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ACTIVATION_CONTEXT_DISABLED"></span><span id="error_sxs_activation_context_disabled"></span>**ERROR \_ SXS \_ ACTIVATION \_ CONTEXT \_ DISABLED**
</dt> <dd> <dl> <dt>

14006 (0x36B6)
</dt> <dt>



La aplicación intentó activar un contexto de activación deshabilitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_KEY_NOT_FOUND"></span><span id="error_sxs_key_not_found"></span>**ERROR \_ CLAVE SXS \_ NO \_ \_ ENCONTRADA**
</dt> <dd> <dl> <dt>

14007 (0x36B7)
</dt> <dt>



La clave de búsqueda solicitada no se encontró en ningún contexto de activación activo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_VERSION_CONFLICT"></span><span id="error_sxs_version_conflict"></span>**ERROR \_ SXS \_ VERSION \_ CONFLICT**
</dt> <dd> <dl> <dt>

14008 (0x36B8)
</dt> <dt>



Una versión de componente requerida por la aplicación entra en conflicto con otra versión de componente ya activa.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_WRONG_SECTION_TYPE"></span><span id="error_sxs_wrong_section_type"></span>**ERROR \_ SXS \_ WRONG \_ SECTION \_ TYPE**
</dt> <dd> <dl> <dt>

14009 (0x36B9)
</dt> <dt>



La sección de contexto de activación solicitada de tipo no coincide con la API de consulta usada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_THREAD_QUERIES_DISABLED"></span><span id="error_sxs_thread_queries_disabled"></span>**ERROR \_ SXS \_ THREAD \_ QUERIES \_ DISABLED**
</dt> <dd> <dl> <dt>

14010 (0x36BA)
</dt> <dt>



La falta de recursos del sistema ha requerido que la activación aislada se deshabilite para el subproceso de ejecución actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_DEFAULT_ALREADY_SET"></span><span id="error_sxs_process_default_already_set"></span>**ERROR \_ SXS \_ PROCESS \_ DEFAULT \_ ALREADY \_ SET**
</dt> <dd> <dl> <dt>

14011 (0x36BB)
</dt> <dt>



Error al intentar establecer el contexto de activación predeterminado del proceso porque ya se estableció el contexto de activación predeterminado del proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING_GROUP"></span><span id="error_sxs_unknown_encoding_group"></span>**ERROR \_ SXS \_ UNKNOWN \_ ENCODING \_ GROUP**
</dt> <dd> <dl> <dt>

14012 (0x36BC)
</dt> <dt>



No se reconoce el identificador de grupo de codificación especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNKNOWN_ENCODING"></span><span id="error_sxs_unknown_encoding"></span>**ERROR \_ SXS \_ UNKNOWN \_ ENCODING**
</dt> <dd> <dl> <dt>

14013 (0x36BD)
</dt> <dt>



No se reconoce la codificación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_XML_NAMESPACE_URI"></span><span id="error_sxs_invalid_xml_namespace_uri"></span>**ERROR \_ SXS \_ INVALID \_ XML \_ NAMESPACE \_ URI**
</dt> <dd> <dl> <dt>

14014 (0x36BE)
</dt> <dt>



El manifiesto contiene una referencia a un URI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ROOT_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_root_manifest_dependency_not_installed"></span>**ERROR \_ SXS \_ ROOT \_ MANIFEST \_ DEPENDENCY \_ NOT \_ INSTALLED**
</dt> <dd> <dl> <dt>

14015 (0x36BF)
</dt> <dt>



El manifiesto de aplicación contiene una referencia a un ensamblado dependiente que no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_LEAF_MANIFEST_DEPENDENCY_NOT_INSTALLED"></span><span id="error_sxs_leaf_manifest_dependency_not_installed"></span>**ERROR \_ SXS \_ LEAF \_ MANIFEST \_ DEPENDENCY \_ NOT \_ INSTALLED**
</dt> <dd> <dl> <dt>

14016 (0x36C0)
</dt> <dt>



El manifiesto de un ensamblado utilizado por la aplicación tiene una referencia a un ensamblado dependiente que no está instalado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_invalid_assembly_identity_attribute"></span>**ERROR \_ SXS \_ INVALID \_ ASSEMBLY \_ IDENTITY \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14017 (0x36C1)
</dt> <dt>



El manifiesto contiene un atributo para la identidad del ensamblado que no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_MISSING_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_missing_required_default_namespace"></span>**ERROR \_ SXS \_ MANIFEST \_ MISSING \_ REQUIRED \_ DEFAULT \_ NAMESPACE**
</dt> <dd> <dl> <dt>

14018 (0x36C2)
</dt> <dt>



El manifiesto no tiene la especificación de espacio de nombres predeterminada necesaria en el elemento de ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_INVALID_REQUIRED_DEFAULT_NAMESPACE"></span><span id="error_sxs_manifest_invalid_required_default_namespace"></span>**ERROR \_ SXS \_ MANIFEST \_ INVALID \_ REQUIRED \_ DEFAULT \_ NAMESPACE**
</dt> <dd> <dl> <dt>

14019 (0x36C3)
</dt> <dt>



El manifiesto tiene un espacio de nombres predeterminado especificado en el elemento de ensamblado, pero su valor no es "urn:schemas-microsoft-com:asm.v1".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PRIVATE_MANIFEST_CROSS_PATH_WITH_REPARSE_POINT"></span><span id="error_sxs_private_manifest_cross_path_with_reparse_point"></span>**ERROR \_ SXS \_ PRIVATE \_ MANIFEST \_ CROSS \_ PATH \_ WITH \_ REPARSE \_ POINT**
</dt> <dd> <dl> <dt>

14020 (0x36C4)
</dt> <dt>



El manifiesto privado sondeado ha cruzado una ruta de acceso con un punto de reanado no admitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_DLL_NAME"></span><span id="error_sxs_duplicate_dll_name"></span>**ERROR \_ SXS \_ DUPLICATE \_ DLL \_ NAME**
</dt> <dd> <dl> <dt>

14021 (0x36C5)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen archivos con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_WINDOWCLASS_NAME"></span><span id="error_sxs_duplicate_windowclass_name"></span>**ERROR \_ SXS \_ DUPLICATE \_ WINDOWCLASS \_ NAME**
</dt> <dd> <dl> <dt>

14022 (0x36C6)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen clases de ventana con el mismo nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_CLSID"></span><span id="error_sxs_duplicate_clsid"></span>**ERROR \_ SXS \_ DUPLICATE \_ CLSID**
</dt> <dd> <dl> <dt>

14023 (0x36C7)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen los mismos CLID de servidor COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_IID"></span><span id="error_sxs_duplicate_iid"></span>**ERROR \_ SXS \_ DUPLICATE \_ IID**
</dt> <dd> <dl> <dt>

14024 (0x36C8)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen servidores proxy para los mismos IID de interfaz COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_TLBID"></span><span id="error_sxs_duplicate_tlbid"></span>**ERROR \_ SXS \_ DUPLICATE \_ TLBID**
</dt> <dd> <dl> <dt>

14025 (0x36C9)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen los mismos TLBID de biblioteca de tipos COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_PROGID"></span><span id="error_sxs_duplicate_progid"></span>**ERROR \_ SXS \_ DUPLICATE \_ PROGID**
</dt> <dd> <dl> <dt>

14026 (0x36CA)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación tienen los mismos ProgID COM.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_DUPLICATE_ASSEMBLY_NAME"></span><span id="error_sxs_duplicate_assembly_name"></span>**ERROR \_ SXS \_ DUPLICATE \_ ASSEMBLY \_ NAME**
</dt> <dd> <dl> <dt>

14027 (0x36CB)
</dt> <dt>



Dos o más componentes a los que hace referencia directa o indirectamente el manifiesto de aplicación son versiones diferentes del mismo componente que no se permiten.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISMATCH"></span><span id="error_sxs_file_hash_mismatch"></span>**ERROR \_ SXS \_ FILE \_ HASH \_ MISMATCH**
</dt> <dd> <dl> <dt>

14028 (0x36CC)
</dt> <dt>



El archivo de un componente no coincide con la información de comprobación presente en el manifiesto del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_POLICY_PARSE_ERROR"></span><span id="error_sxs_policy_parse_error"></span>**ERROR \_ SXS \_ POLICY \_ PARSE \_ ERROR**
</dt> <dd> <dl> <dt>

14029 (0x36CD)
</dt> <dt>



El manifiesto de directiva contiene uno o varios errores de sintaxis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGQUOTE"></span><span id="error_sxs_xml_e_missingquote"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSINGQUOTE**
</dt> <dd> <dl> <dt>

14030 (0x36CE)
</dt> <dt>



Error de análisis del manifiesto: se esperaba un literal de cadena, pero no se encontró ningún carácter de comilla de apertura.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_COMMENTSYNTAX"></span><span id="error_sxs_xml_e_commentsyntax"></span>**ERROR \_ SXS \_ XML \_ E \_ COMMENTSYNTAX**
</dt> <dd> <dl> <dt>

14031 (0x36CF)
</dt> <dt>



Error de análisis del manifiesto: se usó una sintaxis incorrecta en un comentario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADSTARTNAMECHAR"></span><span id="error_sxs_xml_e_badstartnamechar"></span>**ERROR \_ SXS \_ XML \_ E \_ BADSTARTNAMECHAR**
</dt> <dd> <dl> <dt>

14032 (0x36D0)
</dt> <dt>



Error de análisis del manifiesto: se inició un nombre con un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADNAMECHAR"></span><span id="error_sxs_xml_e_badnamechar"></span>**ERROR \_ SXS \_ XML \_ E \_ BADNAMECHAR**
</dt> <dd> <dl> <dt>

14033 (0x36D1)
</dt> <dt>



Error de análisis del manifiesto: un nombre contenía un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARINSTRING"></span><span id="error_sxs_xml_e_badcharinstring"></span>**ERROR \_ SXS \_ XML \_ E \_ BADCHARINSTRING**
</dt> <dd> <dl> <dt>

14034 (0x36D2)
</dt> <dt>



Error de análisis del manifiesto: un literal de cadena contenía un carácter no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_XMLDECLSYNTAX"></span><span id="error_sxs_xml_e_xmldeclsyntax"></span>**ERROR \_ SXS \_ XML \_ E \_ XMLDECLSYNTAX**
</dt> <dd> <dl> <dt>

14035 (0x36D3)
</dt> <dt>



Error de análisis del manifiesto: sintaxis no válida para una declaración xml.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADCHARDATA"></span><span id="error_sxs_xml_e_badchardata"></span>**ERROR \_ SXS \_ XML \_ E \_ BADCHARDATA**
</dt> <dd> <dl> <dt>

14036 (0x36D4)
</dt> <dt>



Error de análisis del manifiesto: se encontró un carácter no válido en el contenido de texto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGWHITESPACE"></span><span id="error_sxs_xml_e_missingwhitespace"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSINGWHITESPACE**
</dt> <dd> <dl> <dt>

14037 (0x36D5)
</dt> <dt>



Error de análisis del manifiesto: faltaba un espacio en blanco necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGTAGEND"></span><span id="error_sxs_xml_e_expectingtagend"></span>**ERROR \_ SXS \_ XML \_ E \_ EXPECTINGTAGEND**
</dt> <dd> <dl> <dt>

14038 (0x36D6)
</dt> <dt>



Error de análisis del manifiesto: se esperaba el carácter ">".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGSEMICOLON"></span><span id="error_sxs_xml_e_missingsemicolon"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSINGSEMICOLON**
</dt> <dd> <dl> <dt>

14039 (0x36D7)
</dt> <dt>



Error de análisis del manifiesto: se esperaba un carácter de punto y coma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNBALANCEDPAREN"></span><span id="error_sxs_xml_e_unbalancedparen"></span>**ERROR \_ SXS \_ XML \_ E \_ UNBALANCEDPAREN**
</dt> <dd> <dl> <dt>

14040 (0x36D8)
</dt> <dt>



Error de análisis del manifiesto: paréntesis desequilibrados.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INTERNALERROR"></span><span id="error_sxs_xml_e_internalerror"></span>**ERROR \_ SXS \_ XML \_ E \_ INTERNALERROR**
</dt> <dd> <dl> <dt>

14041 (0x36D9)
</dt> <dt>



Error de análisis del manifiesto: error interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_WHITESPACE"></span><span id="error_sxs_xml_e_unexpected_whitespace"></span>**ERROR \_ SXS \_ XML \_ E \_ UNEXPECTED \_ WHITESPACE**
</dt> <dd> <dl> <dt>

14042 (0x36DA)
</dt> <dt>



Error de análisis del manifiesto: no se permite el espacio en blanco en esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INCOMPLETE_ENCODING"></span><span id="error_sxs_xml_e_incomplete_encoding"></span>**ERROR \_ SXS \_ XML \_ E \_ INCOMPLETE \_ ENCODING**
</dt> <dd> <dl> <dt>

14043 (0x36DB)
</dt> <dt>



Error de análisis del manifiesto: final del archivo alcanzado en estado no válido para la codificación actual.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSING_PAREN"></span><span id="error_sxs_xml_e_missing_paren"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSING \_ PAREN**
</dt> <dd> <dl> <dt>

14044 (0x36DC)
</dt> <dt>



Error de análisis del manifiesto: faltan paréntesis.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_EXPECTINGCLOSEQUOTE"></span><span id="error_sxs_xml_e_expectingclosequote"></span>**ERROR \_ SXS \_ XML \_ E \_ EXPECTINGCLOSEQUOTE**
</dt> <dd> <dl> <dt>

14045 (0x36DD)
</dt> <dt>



Error de análisis de manifiesto: falta un carácter de comilla de cierre simple o doble ( \\ ' o \\ ").


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLE_COLONS"></span><span id="error_sxs_xml_e_multiple_colons"></span>**ERROR \_ SXS \_ XML \_ E \_ MULTIPLE \_ COLONS**
</dt> <dd> <dl> <dt>

14046 (0x36DE)
</dt> <dt>



Error de análisis de manifiesto: no se permiten varios dos puntos en un nombre.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_DECIMAL"></span><span id="error_sxs_xml_e_invalid_decimal"></span>**ERROR \_ SXS \_ XML E DECIMAL NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

14047 (0x36DF)
</dt> <dt>



Error de análisis del manifiesto: carácter no válido para el dígito decimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_HEXIDECIMAL"></span><span id="error_sxs_xml_e_invalid_hexidecimal"></span>**ERROR \_ SXS \_ XML \_ E \_ INVALID \_ HEXIDECIMAL**
</dt> <dd> <dl> <dt>

14048 (0x36E0)
</dt> <dt>



Error de análisis de manifiesto: carácter no válido para dígito hexadecimal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_UNICODE"></span><span id="error_sxs_xml_e_invalid_unicode"></span>**ERROR \_ SXS \_ XML E UNICODE NO \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

14049 (0x36E1)
</dt> <dt>



Error de análisis de manifiesto: valor de carácter Unicode no válido para esta plataforma.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_WHITESPACEORQUESTIONMARK"></span><span id="error_sxs_xml_e_whitespaceorquestionmark"></span>**ERROR \_ SXS \_ XML \_ E \_ WHITESPACEORQUESTIONMARK**
</dt> <dd> <dl> <dt>

14050 (0x36E2)
</dt> <dt>



Error de análisis del manifiesto: se espera un espacio en blanco o "?".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDENDTAG"></span><span id="error_sxs_xml_e_unexpectedendtag"></span>**ERROR \_ SXS \_ XML \_ E \_ UNEXPECTEDENDTAG**
</dt> <dd> <dl> <dt>

14051 (0x36E3)
</dt> <dt>



Error de análisis del manifiesto: no se esperaba la etiqueta final en esta ubicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDTAG"></span><span id="error_sxs_xml_e_unclosedtag"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDTAG**
</dt> <dd> <dl> <dt>

14052 (0x36E4)
</dt> <dt>



Error de análisis del manifiesto: no se cerraron las siguientes etiquetas: %1.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_DUPLICATEATTRIBUTE"></span><span id="error_sxs_xml_e_duplicateattribute"></span>**ERROR \_ SXS \_ XML \_ E \_ DUPLICATEATTRIBUTE**
</dt> <dd> <dl> <dt>

14053 (0x36E5)
</dt> <dt>



Error de análisis de manifiesto: atributo duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MULTIPLEROOTS"></span><span id="error_sxs_xml_e_multipleroots"></span>**ERROR \_ SXS \_ XML \_ E \_ MULTIPLEROOTS**
</dt> <dd> <dl> <dt>

14054 (0x36E6)
</dt> <dt>



Error de análisis de manifiesto: solo se permite un elemento de nivel superior en un documento XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDATROOTLEVEL"></span><span id="error_sxs_xml_e_invalidatrootlevel"></span>**ERROR \_ SXS \_ XML \_ E \_ INVALIDATROOTLEVEL**
</dt> <dd> <dl> <dt>

14055 (0x36E7)
</dt> <dt>



Error de análisis de manifiesto: no válido en el nivel superior del documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLDECL"></span><span id="error_sxs_xml_e_badxmldecl"></span>**ERROR \_ SXS \_ XML \_ E \_ BADXMLDECL**
</dt> <dd> <dl> <dt>

14056 (0x36E8)
</dt> <dt>



Error de análisis de manifiesto: declaración xml no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGROOT"></span><span id="error_sxs_xml_e_missingroot"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSINGROOT**
</dt> <dd> <dl> <dt>

14057 (0x36E9)
</dt> <dt>



Error de análisis de manifiesto: el documento XML debe tener un elemento de nivel superior.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTEDEOF"></span><span id="error_sxs_xml_e_unexpectedeof"></span>**ERROR \_ SXS \_ XML \_ E \_ UNEXPECTEDEOF**
</dt> <dd> <dl> <dt>

14058 (0x36EA)
</dt> <dt>



Error de análisis de manifiesto: final inesperado del archivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADPEREFINSUBSET"></span><span id="error_sxs_xml_e_badperefinsubset"></span>**ERROR \_ SXS \_ XML \_ E \_ BADPEREFINSUBSET**
</dt> <dd> <dl> <dt>

14059 (0x36EB)
</dt> <dt>



Error de análisis de manifiesto: las entidades de parámetro no se pueden usar dentro de declaraciones de marcado en un subconjunto interno.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTARTTAG"></span><span id="error_sxs_xml_e_unclosedstarttag"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDSTARTTAG**
</dt> <dd> <dl> <dt>

14060 (0x36EC)
</dt> <dt>



Error de análisis del manifiesto: el elemento no se cerró.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDENDTAG"></span><span id="error_sxs_xml_e_unclosedendtag"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDENDTAG**
</dt> <dd> <dl> <dt>

14061 (0x36ED)
</dt> <dt>



Error de análisis del manifiesto: faltaba el carácter ">" en el elemento end.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDSTRING"></span><span id="error_sxs_xml_e_unclosedstring"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDSTRING**
</dt> <dd> <dl> <dt>

14062 (0x36EE)
</dt> <dt>



Error de análisis del manifiesto: no se cerró un literal de cadena.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCOMMENT"></span><span id="error_sxs_xml_e_unclosedcomment"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDCOMMENT**
</dt> <dd> <dl> <dt>

14063 (0x36EF)
</dt> <dt>



Error de análisis del manifiesto: no se ha cerrado un comentario.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDDECL"></span><span id="error_sxs_xml_e_uncloseddecl"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDDECL**
</dt> <dd> <dl> <dt>

14064 (0x36F0)
</dt> <dt>



Error de análisis del manifiesto: no se cerró una declaración.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNCLOSEDCDATA"></span><span id="error_sxs_xml_e_unclosedcdata"></span>**ERROR \_ SXS \_ XML \_ E \_ UNCLOSEDCDATA**
</dt> <dd> <dl> <dt>

14065 (0x36F1)
</dt> <dt>



Error de análisis del manifiesto: no se cerró una sección CDATA.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_RESERVEDNAMESPACE"></span><span id="error_sxs_xml_e_reservednamespace"></span>**ERROR \_ SXS \_ XML \_ E \_ RESERVEDNAMESPACE**
</dt> <dd> <dl> <dt>

14066 (0x36F2)
</dt> <dt>



Error de análisis del manifiesto: no se permite que el prefijo del espacio de nombres comience con la cadena reservada "xml".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDENCODING"></span><span id="error_sxs_xml_e_invalidencoding"></span>**ERROR \_ SXS \_ XML \_ E \_ INVALIDENCODING**
</dt> <dd> <dl> <dt>

14067 (0x36F3)
</dt> <dt>



Error de análisis de manifiesto: el sistema no admite la codificación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALIDSWITCH"></span><span id="error_sxs_xml_e_invalidswitch"></span>**ERROR \_ SXS \_ XML \_ E \_ INVALIDSWITCH**
</dt> <dd> <dl> <dt>

14068 (0x36F4)
</dt> <dt>



Error de análisis de manifiesto: no se admite el cambio de la codificación actual a la codificación especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_BADXMLCASE"></span><span id="error_sxs_xml_e_badxmlcase"></span>**ERROR \_ SXS \_ XML \_ E \_ BADXMLCASE**
</dt> <dd> <dl> <dt>

14069 (0x36F5)
</dt> <dt>



Error de análisis del manifiesto: el nombre 'xml' está reservado y debe estar en minúsculas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_STANDALONE"></span><span id="error_sxs_xml_e_invalid_standalone"></span>**ERROR \_ SXS \_ XML \_ E \_ INVALID \_ STANDALONE**
</dt> <dd> <dl> <dt>

14070 (0x36F6)
</dt> <dt>



Error de análisis del manifiesto: el atributo independiente debe tener el valor "yes" o "no".


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_UNEXPECTED_STANDALONE"></span><span id="error_sxs_xml_e_unexpected_standalone"></span>**ERROR \_ SXS \_ XML \_ E \_ UNEXPECTED \_ STANDALONE**
</dt> <dd> <dl> <dt>

14071 (0x36F7)
</dt> <dt>



Error de análisis del manifiesto: el atributo independiente no se puede usar en entidades externas.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_INVALID_VERSION"></span><span id="error_sxs_xml_e_invalid_version"></span>**ERROR \_ SXS \_ XML E VERSIÓN NO \_ \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

14072 (0x36F8)
</dt> <dt>



Error de análisis del manifiesto: número de versión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_XML_E_MISSINGEQUALS"></span><span id="error_sxs_xml_e_missingequals"></span>**ERROR \_ SXS \_ XML \_ E \_ MISSINGEQUALS**
</dt> <dd> <dl> <dt>

14073 (0x36F9)
</dt> <dt>



Error de análisis del manifiesto: falta el signo igual entre el atributo y el valor del atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_RECOVERY_FAILED"></span><span id="error_sxs_protection_recovery_failed"></span>**ERROR DE \_ RECUPERACIÓN DE PROTECCIÓN DE SXS \_ CON \_ \_ ERROR**
</dt> <dd> <dl> <dt>

14074 (0x36FA)
</dt> <dt>



Error de protección de ensamblados: no se puede recuperar el ensamblado especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_PUBLIC_KEY_TOO_SHORT"></span><span id="error_sxs_protection_public_key_too_short"></span>**ERROR \_ SXS \_ PROTECTION \_ PUBLIC \_ KEY \_ TOO \_ SHORT**
</dt> <dd> <dl> <dt>

14075 (0x36FB)
</dt> <dt>



Error de protección de ensamblados: la clave pública de un ensamblado era demasiado corta para permitirse.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_NOT_VALID"></span><span id="error_sxs_protection_catalog_not_valid"></span>**ERROR \_ EL CATÁLOGO DE PROTECCIÓN DE SXS NO ES \_ \_ \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

14076 (0x36FC)
</dt> <dt>



Error de protección de ensamblados: el catálogo de un ensamblado no es válido o no coincide con el manifiesto del ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_UNTRANSLATABLE_HRESULT"></span><span id="error_sxs_untranslatable_hresult"></span>**ERROR \_ SXS \_ UNTRANSLATABLE \_ HRESULT**
</dt> <dd> <dl> <dt>

14077 (0x36FD)
</dt> <dt>



No se pudo traducir un valor HRESULT a un código de error de Win32 correspondiente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROTECTION_CATALOG_FILE_MISSING"></span><span id="error_sxs_protection_catalog_file_missing"></span>**ERROR FALTA EL ARCHIVO DE CATÁLOGO DE PROTECCIÓN \_ \_ \_ \_ DE SXS \_**
</dt> <dd> <dl> <dt>

14078 (0x36FE)
</dt> <dt>



Error de protección de ensamblados: falta el catálogo de un ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MISSING_ASSEMBLY_IDENTITY_ATTRIBUTE"></span><span id="error_sxs_missing_assembly_identity_attribute"></span>**ERROR \_ SXS \_ MISSING \_ ASSEMBLY \_ IDENTITY \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14079 (0x36FF)
</dt> <dt>



A la identidad de ensamblado proporcionada le faltan uno o varios atributos que deben estar presentes en este contexto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_ASSEMBLY_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_assembly_identity_attribute_name"></span>**ERROR \_ SXS \_ INVALID \_ ASSEMBLY \_ IDENTITY \_ ATTRIBUTE \_ NAME**
</dt> <dd> <dl> <dt>

14080 (0x3700)
</dt> <dt>



La identidad de ensamblado proporcionada tiene uno o varios nombres de atributo que contienen caracteres no permitidos en los nombres XML.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_MISSING"></span><span id="error_sxs_assembly_missing"></span>**ERROR \_ FALTA EL ENSAMBLADO SXS \_ \_**
</dt> <dd> <dl> <dt>

14081 (0x3701)
</dt> <dt>



No se encontró el ensamblado al que se hace referencia.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPT_ACTIVATION_STACK"></span><span id="error_sxs_corrupt_activation_stack"></span>**ERROR \_ SXS \_ CORRUPT \_ ACTIVATION \_ STACK**
</dt> <dd> <dl> <dt>

14082 (0x3702)
</dt> <dt>



La pila de activación del contexto de activación para el subproceso en ejecución de la ejecución está dañada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_CORRUPTION"></span><span id="error_sxs_corruption"></span>**ERROR \_ SXS \_ CORRUPTION**
</dt> <dd> <dl> <dt>

14083 (0x3703)
</dt> <dt>



Los metadatos de aislamiento de aplicación para este proceso o subproceso se han dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_EARLY_DEACTIVATION"></span><span id="error_sxs_early_deactivation"></span>**ERROR \_ SXS \_ EARLY \_ DEACTIVATION**
</dt> <dd> <dl> <dt>

14084 (0x3704)
</dt> <dt>



El contexto de activación que se desactiva no es el activado más recientemente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_DEACTIVATION"></span><span id="error_sxs_invalid_deactivation"></span>**ERROR \_ SXS \_ INVALID \_ DEACTIVATION**
</dt> <dd> <dl> <dt>

14085 (0x3705)
</dt> <dt>



El contexto de activación que se desactiva no está activo para el subproceso actual de ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MULTIPLE_DEACTIVATION"></span><span id="error_sxs_multiple_deactivation"></span>**ERROR \_ SXS \_ MULTIPLE \_ DEACTIVATION**
</dt> <dd> <dl> <dt>

14086 (0x3706)
</dt> <dt>



El contexto de activación que se está desactivando ya se ha desactivado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_PROCESS_TERMINATION_REQUESTED"></span><span id="error_sxs_process_termination_requested"></span>**ERROR \_ SXS \_ PROCESS \_ TERMINATION \_ REQUESTED**
</dt> <dd> <dl> <dt>

14087 (0x3707)
</dt> <dt>



Un componente utilizado por la instalación de aislamiento ha solicitado finalizar el proceso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_RELEASE_ACTIVATION_CONTEXT"></span><span id="error_sxs_release_activation_context"></span>**CONTEXTO DE \_ ACTIVACIÓN DE LA VERSIÓN DE SXS DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

14088 (0x3708)
</dt> <dt>



Un componente de modo kernel está liberando una referencia en un contexto de activación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SYSTEM_DEFAULT_ACTIVATION_CONTEXT_EMPTY"></span><span id="error_sxs_system_default_activation_context_empty"></span>**ERROR \_ SXS \_ SYSTEM \_ DEFAULT \_ ACTIVATION \_ CONTEXT \_ EMPTY**
</dt> <dd> <dl> <dt>

14089 (0x3709)
</dt> <dt>



No se pudo generar el contexto de activación del ensamblado predeterminado del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_VALUE"></span><span id="error_sxs_invalid_identity_attribute_value"></span>**ERROR \_ SXS \_ INVALID \_ IDENTITY \_ ATTRIBUTE \_ VALUE**
</dt> <dd> <dl> <dt>

14090 (0x370A)
</dt> <dt>



El valor de un atributo de una identidad no está dentro del intervalo legal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INVALID_IDENTITY_ATTRIBUTE_NAME"></span><span id="error_sxs_invalid_identity_attribute_name"></span>**ERROR \_ SXS \_ INVALID \_ IDENTITY \_ ATTRIBUTE \_ NAME**
</dt> <dd> <dl> <dt>

14091 (0x370B)
</dt> <dt>



El nombre de un atributo de una identidad no está dentro del intervalo legal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_DUPLICATE_ATTRIBUTE"></span><span id="error_sxs_identity_duplicate_attribute"></span>**ERROR \_ SXS \_ IDENTITY \_ DUPLICATE \_ ATTRIBUTE**
</dt> <dd> <dl> <dt>

14092 (0x370C)
</dt> <dt>



Una identidad contiene dos definiciones para el mismo atributo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITY_PARSE_ERROR"></span><span id="error_sxs_identity_parse_error"></span>**ERROR \_ SXS \_ IDENTITY \_ PARSE \_ ERROR**
</dt> <dd> <dl> <dt>

14093 (0x370D)
</dt> <dt>



La cadena de identidad tiene un formato desaformado. Esto puede deberse a una coma final, más de dos atributos sin nombre, un nombre de atributo que falta o un valor de atributo que falta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MALFORMED_SUBSTITUTION_STRING"></span><span id="error_malformed_substitution_string"></span>**ERROR \_ CADENA DE SUSTITUCIÓN CON \_ \_ FORMATO**
</dt> <dd> <dl> <dt>

14094 (0x370E)
</dt> <dt>



Una cadena que contiene contenido sustituible localizado no tenía el formato. Un signo de dólar ($) estaba seguido de algo distinto de un paréntesis izquierdo u otro signo de dólar o no se encontró el paréntesis derecho de una sustitución.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_INCORRECT_PUBLIC_KEY_TOKEN"></span><span id="error_sxs_incorrect_public_key_token"></span>**ERROR \_ SXS \_ INCORRECT \_ PUBLIC \_ KEY \_ TOKEN**
</dt> <dd> <dl> <dt>

14095 (0x370F)
</dt> <dt>



El token de clave pública no se corresponde con la clave pública especificada.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNMAPPED_SUBSTITUTION_STRING"></span><span id="error_unmapped_substitution_string"></span>**ERROR \_ CADENA DE SUSTITUCIÓN SIN \_ \_ ALA**
</dt> <dd> <dl> <dt>

14096 (0x3710)
</dt> <dt>



Una cadena de sustitución no tenía ninguna asignación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_NOT_LOCKED"></span><span id="error_sxs_assembly_not_locked"></span>**ERROR \_ ENSAMBLADO SXS \_ NO \_ \_ BLOQUEADO**
</dt> <dd> <dl> <dt>

14097 (0x3711)
</dt> <dt>



El componente debe estar bloqueado antes de realizar la solicitud.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_COMPONENT_STORE_CORRUPT"></span><span id="error_sxs_component_store_corrupt"></span>**ERROR \_ SXS \_ COMPONENT \_ STORE \_ CORRUPT**
</dt> <dd> <dl> <dt>

14098 (0x3712)
</dt> <dt>



El almacén de componentes está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADVANCED_INSTALLER_FAILED"></span><span id="error_advanced_installer_failed"></span>**ERROR ERROR \_ DEL \_ INSTALADOR \_ AVANZADO**
</dt> <dd> <dl> <dt>

14099 (0x3713)
</dt> <dt>



Error de un instalador avanzado durante la instalación o el mantenimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_XML_ENCODING_MISMATCH"></span><span id="error_xml_encoding_mismatch"></span>**ERROR \_ DE COINCIDENCIA DE \_ CODIFICACIÓN \_ XML**
</dt> <dd> <dl> <dt>

14100 (0x3714)
</dt> <dt>



La codificación de caracteres en la declaración XML no coincide con la codificación utilizada en el documento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_IDENTITY_SAME_BUT_CONTENTS_DIFFERENT"></span><span id="error_sxs_manifest_identity_same_but_contents_different"></span>**ERROR \_ SXS \_ MANIFEST \_ IDENTITY \_ SAME \_ BUT \_ CONTENTS \_ DIFFERENT**
</dt> <dd> <dl> <dt>

14101 (0x3715)
</dt> <dt>



Las identidades de los manifiestos son idénticas, pero su contenido es diferente.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_IDENTITIES_DIFFERENT"></span><span id="error_sxs_identities_different"></span>**ERROR \_ SXS \_ IDENTITIES \_ DIFFERENT**
</dt> <dd> <dl> <dt>

14102 (0x3716)
</dt> <dt>



Las identidades de componente son diferentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_ASSEMBLY_IS_NOT_A_DEPLOYMENT"></span><span id="error_sxs_assembly_is_not_a_deployment"></span>**ERROR \_ EL ENSAMBLADO SXS \_ NO ES UNA \_ \_ \_ \_ IMPLEMENTACIÓN**
</dt> <dd> <dl> <dt>

14103 (0x3717)
</dt> <dt>



El ensamblado no es una implementación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_NOT_PART_OF_ASSEMBLY"></span><span id="error_sxs_file_not_part_of_assembly"></span>**ERROR \_ SXS FILE NOT PART OF ASSEMBLY (ARCHIVO SXS \_ DE ERROR QUE NO FORMA PARTE DEL \_ \_ \_ \_ ENSAMBLADO)**
</dt> <dd> <dl> <dt>

14104 (0x3718)
</dt> <dt>



El archivo no forma parte del ensamblado.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_MANIFEST_TOO_BIG"></span><span id="error_sxs_manifest_too_big"></span>**MANIFIESTO \_ SXS \_ DE ERROR DEMASIADO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

14105 (0x3719)
</dt> <dt>



El tamaño del manifiesto supera el máximo permitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_SETTING_NOT_REGISTERED"></span><span id="error_sxs_setting_not_registered"></span>**ERROR \_ SXS \_ SETTING \_ NOT \_ REGISTERED**
</dt> <dd> <dl> <dt>

14106 (0x371A)
</dt> <dt>



La configuración no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_TRANSACTION_CLOSURE_INCOMPLETE"></span><span id="error_sxs_transaction_closure_incomplete"></span>**ERROR \_ SXS \_ TRANSACTION \_ CLOSURE \_ INCOMPLETE**
</dt> <dd> <dl> <dt>

14107 (0x371B)
</dt> <dt>



Uno o varios miembros necesarios de la transacción no están presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMI_PRIMITIVE_INSTALLER_FAILED"></span><span id="error_smi_primitive_installer_failed"></span>**ERROR DEL \_ INSTALADOR PRIMITIVO DE SMI \_ \_ \_**
</dt> <dd> <dl> <dt>

14108 (0x371C)
</dt> <dt>



Error del instalador primitivo de SMI durante la instalación o el mantenimiento.


</dt> </dl> </dd> <dt>

<span id="ERROR_GENERIC_COMMAND_FAILED"></span><span id="error_generic_command_failed"></span>**ERROR \_ EN EL COMANDO \_ GENÉRICO \_**
</dt> <dd> <dl> <dt>

14109 (0x371D)
</dt> <dt>



Un ejecutable de comando genérico devolvió un resultado que indica un error.


</dt> </dl> </dd> <dt>

<span id="ERROR_SXS_FILE_HASH_MISSING"></span><span id="error_sxs_file_hash_missing"></span>**ERROR \_ SXS \_ FILE \_ HASH \_ MISSING**
</dt> <dd> <dl> <dt>

14110 (0x371E)
</dt> <dt>



A un componente le falta información de comprobación de archivos en su manifiesto.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PATH"></span><span id="error_evt_invalid_channel_path"></span>**ERROR \_ EVT \_ RUTA DE ACCESO DE CANAL NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

15000 (0x3A98)
</dt> <dt>



La ruta de acceso del canal especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_QUERY"></span><span id="error_evt_invalid_query"></span>**ERROR \_ EVT \_ INVALID \_ QUERY**
</dt> <dd> <dl> <dt>

15001 (0x3A99)
</dt> <dt>



La consulta especificada no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_METADATA_NOT_FOUND"></span><span id="error_evt_publisher_metadata_not_found"></span>**ERROR \_ NO SE ENCONTRARON \_ \_ METADATOS DEL \_ PUBLICADOR EVT \_**
</dt> <dd> <dl> <dt>

15002 (0x3A9A)
</dt> <dt>



Los metadatos del publicador no se pueden encontrar en el recurso.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_TEMPLATE_NOT_FOUND"></span><span id="error_evt_event_template_not_found"></span>**NO SE \_ ENCONTRÓ LA PLANTILLA DE EVENTO \_ EVT DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15003 (0x3A9B)
</dt> <dt>



La plantilla para una definición de evento no se encuentra en el recurso (error = %1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_NAME"></span><span id="error_evt_invalid_publisher_name"></span>**ERROR \_ EVT \_ INVALID \_ PUBLISHER \_ NAME**
</dt> <dd> <dl> <dt>

15004 (0x3A9C)
</dt> <dt>



El nombre del publicador especificado no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_EVENT_DATA"></span><span id="error_evt_invalid_event_data"></span>**ERROR \_ EVT \_ INVALID \_ EVENT \_ DATA**
</dt> <dd> <dl> <dt>

15005 (0x3A9D)
</dt> <dt>



Los datos de evento que genera el publicador no son compatibles con la definición de la plantilla de evento en el manifiesto del publicador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_NOT_FOUND"></span><span id="error_evt_channel_not_found"></span>**NO \_ SE ENCONTRÓ EL CANAL \_ EVT DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15007 (0x3A9F)
</dt> <dt>



No se encontró el canal especificado. Compruebe la configuración del canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MALFORMED_XML_TEXT"></span><span id="error_evt_malformed_xml_text"></span>**ERROR \_ EVT \_ MALFORMED \_ XML \_ TEXT**
</dt> <dd> <dl> <dt>

15008 (0x3AA0)
</dt> <dt>



El texto xml especificado no tenía el formato correcto. Consulte Error extendido para obtener más detalles.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_SUBSCRIPTION_TO_DIRECT_CHANNEL"></span><span id="error_evt_subscription_to_direct_channel"></span>**ERROR \_ DE SUSCRIPCIÓN DE EVT AL CANAL \_ \_ \_ \_ DIRECTO**
</dt> <dd> <dl> <dt>

15009 (0x3AA1)
</dt> <dt>



El autor de la llamada está intentando suscribirse a un canal directo que no está permitido. Los eventos de un canal directo van directamente a un archivo de registro y no se pueden suscribir.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CONFIGURATION_ERROR"></span><span id="error_evt_configuration_error"></span>**ERROR \_ DE CONFIGURACIÓN DE EVT \_ \_**
</dt> <dd> <dl> <dt>

15010 (0x3AA2)
</dt> <dt>



Error de configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_STALE"></span><span id="error_evt_query_result_stale"></span>**ERROR \_ EVT \_ QUERY \_ RESULT \_ STALE**
</dt> <dd> <dl> <dt>

15011 (0x3AA3)
</dt> <dt>



El resultado de la consulta es obsoleto o no es válido. Esto puede deberse a que el registro se borra o se redova después de crear el resultado de la consulta. Para controlar este código, los usuarios deben liberar el objeto de resultado de la consulta y volver a emitir la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_QUERY_RESULT_INVALID_POSITION"></span><span id="error_evt_query_result_invalid_position"></span>**ERROR \_ EVT \_ QUERY \_ RESULT \_ INVALID \_ POSITION**
</dt> <dd> <dl> <dt>

15012 (0x3AA4)
</dt> <dt>



El resultado de la consulta se encuentra actualmente en una posición no válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_NON_VALIDATING_MSXML"></span><span id="error_evt_non_validating_msxml"></span>**ERROR \_ EVT \_ NON \_ VALIDATING \_ MSXML**
</dt> <dd> <dl> <dt>

15013 (0x3AA5)
</dt> <dt>



Los MSXML registrados no admiten la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_ALREADYSCOPED"></span><span id="error_evt_filter_alreadyscoped"></span>**ERROR \_ EVT \_ FILTER \_ ALREADYSCOPED**
</dt> <dd> <dl> <dt>

15014 (0x3AA6)
</dt> <dt>



Una expresión solo puede ir seguida de un cambio de operación de ámbito si se evalúa como un conjunto de nodos y aún no forma parte de algún otro cambio de operación de ámbito.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_NOTELTSET"></span><span id="error_evt_filter_noteltset"></span>**ERROR \_ EVT \_ FILTER \_ NOTELTSET**
</dt> <dd> <dl> <dt>

15015 (0x3AA7)
</dt> <dt>



No se puede realizar una operación de paso a partir de un término que no representa un conjunto de elementos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVARG"></span><span id="error_evt_filter_invarg"></span>**ERROR \_ EVT \_ FILTER \_ INVARG**
</dt> <dd> <dl> <dt>

15016 (0x3AA8)
</dt> <dt>



Los argumentos del lado izquierdo de los operadores binarios deben ser atributos, nodos o variables, y los argumentos del lado derecho deben ser constantes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTEST"></span><span id="error_evt_filter_invtest"></span>**ERROR \_ EVT \_ FILTER \_ INVTEST**
</dt> <dd> <dl> <dt>

15017 (0x3AA9)
</dt> <dt>



Una operación de paso debe implicar una prueba de nodo o, en el caso de un predicado, se puede evaluar una expresión algebraica con la que probar cada nodo del conjunto de nodos identificado por el conjunto de nodos preceptor.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_INVTYPE"></span><span id="error_evt_filter_invtype"></span>**ERROR \_ EVT \_ FILTER \_ INVTYPE**
</dt> <dd> <dl> <dt>

15018 (0x3AAA)
</dt> <dt>



Este tipo de datos no se admite actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_PARSEERR"></span><span id="error_evt_filter_parseerr"></span>**ERROR \_ EVT \_ FILTER \_ PARSEERR**
</dt> <dd> <dl> <dt>

15019 (0x3AAB)
</dt> <dt>



Se produjo un error de sintaxis en la posición %1!d!.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNSUPPORTEDOP"></span><span id="error_evt_filter_unsupportedop"></span>**ERROR \_ EVT \_ FILTER \_ UNSUPPORTEDOP**
</dt> <dd> <dl> <dt>

15020 (0x3AAC)
</dt> <dt>



Esta implementación del filtro no admite este operador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_UNEXPECTEDTOKEN"></span><span id="error_evt_filter_unexpectedtoken"></span>**ERROR \_ EVT \_ FILTER \_ UNEXPECTEDTOKEN**
</dt> <dd> <dl> <dt>

15021 (0x3AAD)
</dt> <dt>



El token encontrado fue inesperado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_OPERATION_OVER_ENABLED_DIRECT_CHANNEL"></span><span id="error_evt_invalid_operation_over_enabled_direct_channel"></span>**ERROR \_ EVT \_ INVALID \_ OPERATION \_ OVER \_ ENABLED \_ DIRECT \_ CHANNEL**
</dt> <dd> <dl> <dt>

15022 (0x3AAE)
</dt> <dt>



La operación solicitada no se puede realizar a través de un canal directo habilitado. El canal debe deshabilitarse primero antes de realizar la operación solicitada.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_CHANNEL_PROPERTY_VALUE"></span><span id="error_evt_invalid_channel_property_value"></span>**ERROR \_ EVT \_ INVALID \_ CHANNEL \_ PROPERTY \_ VALUE**
</dt> <dd> <dl> <dt>

15023 (0x3AAF)
</dt> <dt>



Propiedad de canal %1!s! contiene un valor no válido. El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de canal.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_INVALID_PUBLISHER_PROPERTY_VALUE"></span><span id="error_evt_invalid_publisher_property_value"></span>**ERROR \_ EVT \_ INVALID \_ PUBLISHER \_ PROPERTY \_ VALUE**
</dt> <dd> <dl> <dt>

15024 (0x3AB0)
</dt> <dt>



Publisher propiedad %1!s! contiene un valor no válido. El valor tiene un tipo no válido, está fuera del intervalo válido, no se puede actualizar o no es compatible con este tipo de publicador.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CHANNEL_CANNOT_ACTIVATE"></span><span id="error_evt_channel_cannot_activate"></span>**ERROR \_ EL CANAL EVT NO SE \_ PUEDE \_ \_ ACTIVAR**
</dt> <dd> <dl> <dt>

15025 (0x3AB1)
</dt> <dt>



El canal no se puede activar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_TOO_COMPLEX"></span><span id="error_evt_filter_too_complex"></span>**ERROR \_ EVT FILTER TOO COMPLEX (FILTRO EVT \_ DE ERROR DEMASIADO \_ \_ COMPLEJO)**
</dt> <dd> <dl> <dt>

15026 (0x3AB2)
</dt> <dt>



La expresión xpath superó la complejidad admitida. Simplifique o divida en dos o más expresiones simples.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_NOT_FOUND"></span><span id="error_evt_message_not_found"></span>**MENSAJE \_ EVT \_ DE ERROR NO \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

15027 (0x3AB3)
</dt> <dt>



el recurso de mensaje está presente, pero el mensaje no se encuentra en la tabla de cadenas o mensajes.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_ID_NOT_FOUND"></span><span id="error_evt_message_id_not_found"></span>**ERROR \_ EVT \_ MESSAGE \_ ID \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15028 (0x3AB4)
</dt> <dt>



No se encontró el identificador del mensaje deseado.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_VALUE_INSERT"></span><span id="error_evt_unresolved_value_insert"></span>**ERROR \_ EVT \_ UNRESOLVED \_ VALUE \_ INSERT**
</dt> <dd> <dl> <dt>

15029 (0x3AB5)
</dt> <dt>



No se encontró la cadena de sustitución para el índice de inserción (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_UNRESOLVED_PARAMETER_INSERT"></span><span id="error_evt_unresolved_parameter_insert"></span>**ERROR \_ EVT \_ UNRESOLVED \_ PARAMETER \_ INSERT**
</dt> <dd> <dl> <dt>

15030 (0x3AB6)
</dt> <dt>



No se encontró la cadena de descripción para la referencia de parámetros (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MAX_INSERTS_REACHED"></span><span id="error_evt_max_inserts_reached"></span>**ERROR \_ EVT \_ MAX \_ INSERTS \_ REACHED**
</dt> <dd> <dl> <dt>

15031 (0x3AB7)
</dt> <dt>



Se ha alcanzado el número máximo de reemplazos.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_EVENT_DEFINITION_NOT_FOUND"></span><span id="error_evt_event_definition_not_found"></span>**ERROR \_ EVT \_ EVENT \_ DEFINITION \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15032 (0x3AB8)
</dt> <dt>



No se encontró la definición de evento para el identificador de evento (%1).


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_MESSAGE_LOCALE_NOT_FOUND"></span><span id="error_evt_message_locale_not_found"></span>**ERROR \_ EVT \_ MESSAGE \_ LOCALE \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15033 (0x3AB9)
</dt> <dt>



El recurso específico de la configuración regional para el mensaje deseado no está presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_OLD"></span><span id="error_evt_version_too_old"></span>**ERROR \_ EVT \_ VERSION \_ TOO \_ OLD**
</dt> <dd> <dl> <dt>

15034 (0x3ABA)
</dt> <dt>



El recurso es demasiado antiguo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_VERSION_TOO_NEW"></span><span id="error_evt_version_too_new"></span>**ERROR \_ EVT \_ VERSION \_ TOO \_ NEW**
</dt> <dd> <dl> <dt>

15035 (0x3ABB)
</dt> <dt>



El recurso es demasiado nuevo para ser compatible.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_CANNOT_OPEN_CHANNEL_OF_QUERY"></span><span id="error_evt_cannot_open_channel_of_query"></span>**ERROR \_ EVT \_ NO PUEDE ABRIR EL CANAL DE \_ \_ \_ \_ CONSULTA**
</dt> <dd> <dl> <dt>

15036 (0x3ABC)
</dt> <dt>



El canal en el índice %1!d! de la consulta no se puede abrir.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_PUBLISHER_DISABLED"></span><span id="error_evt_publisher_disabled"></span>**ERROR \_ EVT \_ PUBLISHER \_ DISABLED**
</dt> <dd> <dl> <dt>

15037 (0x3ABD)
</dt> <dt>



El publicador se ha deshabilitado y su recurso no está disponible. Esto suele ocurrir cuando el publicador está en proceso de desinstalación o actualización.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVT_FILTER_OUT_OF_RANGE"></span><span id="error_evt_filter_out_of_range"></span>**FILTRO \_ EVT \_ DE ERROR FUERA \_ DEL \_ \_ INTERVALO**
</dt> <dd> <dl> <dt>

15038 (0x3ABE)
</dt> <dt>



Se intentó crear un tipo numérico que está fuera de su intervalo válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_SUBSCRIPTION_CANNOT_ACTIVATE"></span><span id="error_ec_subscription_cannot_activate"></span>**ERROR LA \_ SUSCRIPCIÓN EC NO SE PUEDE \_ \_ \_ ACTIVAR**
</dt> <dd> <dl> <dt>

15080 (0x3AE8)
</dt> <dt>



La suscripción no se puede activar.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_LOG_DISABLED"></span><span id="error_ec_log_disabled"></span>**ERROR \_ EC \_ LOG \_ DISABLED**
</dt> <dd> <dl> <dt>

15081 (0x3AE9)
</dt> <dt>



El registro de la suscripción está en estado deshabilitado y no se puede usar para reenviar eventos. El registro debe habilitarse primero antes de que se pueda activar la suscripción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CIRCULAR_FORWARDING"></span><span id="error_ec_circular_forwarding"></span>**REENVÍO \_ \_ CIRCULAR DE EC DE \_ ERROR**
</dt> <dd> <dl> <dt>

15082 (0x3AEA)
</dt> <dt>



Al reenviar eventos de la máquina local a sí misma, la consulta de la suscripción no puede contener el registro de destino de la suscripción.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CREDSTORE_FULL"></span><span id="error_ec_credstore_full"></span>**ERROR \_ EC \_ CREDSTORE \_ FULL**
</dt> <dd> <dl> <dt>

15083 (0x3AEB)
</dt> <dt>



El almacén de credenciales que se usa para guardar las credenciales está lleno.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_CRED_NOT_FOUND"></span><span id="error_ec_cred_not_found"></span>**ERROR \_ EC \_ CRED \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15084 (0x3AEC)
</dt> <dt>



La credencial usada por esta suscripción no se encuentra en el almacén de credenciales.


</dt> </dl> </dd> <dt>

<span id="ERROR_EC_NO_ACTIVE_CHANNEL"></span><span id="error_ec_no_active_channel"></span>**ERROR \_ EC \_ NO \_ ACTIVE \_ CHANNEL**
</dt> <dd> <dl> <dt>

15085 (0x3AED)
</dt> <dt>



No se encuentra ningún canal activo para la consulta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_FOUND"></span><span id="error_mui_file_not_found"></span>**NO \_ SE ENCONTRÓ EL ARCHIVO DE MUI DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15100 (0x3AFC)
</dt> <dt>



El cargador de recursos no pudo encontrar el archivo MUI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_FILE"></span><span id="error_mui_invalid_file"></span>**ERROR \_ ARCHIVO NO VÁLIDO DE MUI \_ \_**
</dt> <dd> <dl> <dt>

15101 (0x3AFD)
</dt> <dt>



El cargador de recursos no pudo cargar el archivo DEA porque el archivo no pudo pasar la validación.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_RC_CONFIG"></span><span id="error_mui_invalid_rc_config"></span>**ERROR \_ DE CONFIG RC INVALID \_ \_ RC \_**
</dt> <dd> <dl> <dt>

15102 (0x3AFE)
</dt> <dt>



El manifiesto rc está dañado con datos de elementos no utilizados o con una versión no admitida o falta el elemento necesario.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_LOCALE_NAME"></span><span id="error_mui_invalid_locale_name"></span>**ERROR \_ MUI \_ INVALID \_ LOCALE \_ NAME**
</dt> <dd> <dl> <dt>

15103 (0x3AFF)
</dt> <dt>



El manifiesto RC tiene un nombre de referencia cultural no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INVALID_ULTIMATEFALLBACK_NAME"></span><span id="error_mui_invalid_ultimatefallback_name"></span>**ERROR \_ DE INVALID \_ \_ \_ ULTIMATEFALLBACK NAME**
</dt> <dd> <dl> <dt>

15104 (0x3B00)
</dt> <dt>



El manifiesto rc tiene un nombre ultimatefallback no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_FILE_NOT_LOADED"></span><span id="error_mui_file_not_loaded"></span>**ERROR \_ NO SE HA CARGADO EL ARCHIVO DE \_ \_ \_ CSV**
</dt> <dd> <dl> <dt>

15105 (0x3B01)
</dt> <dt>



La memoria caché del cargador de recursos no tiene la entrada DE LAN cargada.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_ENUM_USER_STOP"></span><span id="error_resource_enum_user_stop"></span>**ERROR \_ RESOURCE \_ ENUM \_ USER \_ STOP**
</dt> <dd> <dl> <dt>

15106 (0x3B02)
</dt> <dt>



El usuario detuvo la enumeración de recursos.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_UILANG_NOT_INSTALLED"></span><span id="error_mui_intlsettings_uilang_not_installed"></span>**ERROR \_ DE \_ INTLSETTINGS \_ UILANG NO \_ \_ INSTALADO**
</dt> <dd> <dl> <dt>

15107 (0x3B03)
</dt> <dt>



Error de instalación del idioma de la interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUI_INTLSETTINGS_INVALID_LOCALE_NAME"></span><span id="error_mui_intlsettings_invalid_locale_name"></span>**ERROR \_ DE \_ INTLSETTINGS \_ NOMBRE DE CONFIGURACIÓN REGIONAL NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

15108 (0x3B04)
</dt> <dt>



Error en la instalación de la configuración regional.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RUNTIME_NO_DEFAULT_OR_NEUTRAL_RESOURCE"></span><span id="error_mrm_runtime_no_default_or_neutral_resource"></span>**ERROR \_ MRM \_ RUNTIME \_ NO \_ DEFAULT \_ OR \_ NEUTRAL \_ RESOURCE**
</dt> <dd> <dl> <dt>

15110 (0x3B06)
</dt> <dt>



Un recurso no tiene un valor predeterminado o neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRICONFIG"></span><span id="error_mrm_invalid_priconfig"></span>**ERROR \_ MRM \_ INVALID \_ PRICONFIG**
</dt> <dd> <dl> <dt>

15111 (0x3B07)
</dt> <dt>



Archivo de configuración de PRI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_FILE_TYPE"></span><span id="error_mrm_invalid_file_type"></span>**ERROR \_ TIPO DE ARCHIVO NO VÁLIDO DE \_ \_ \_ MRM**
</dt> <dd> <dl> <dt>

15112 (0x3B08)
</dt> <dt>



Tipo de archivo no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNKNOWN_QUALIFIER"></span><span id="error_mrm_unknown_qualifier"></span>**ERROR \_ CALIFICADOR DESCONOCIDO DE MRM \_ \_**
</dt> <dd> <dl> <dt>

15113 (0x3B09)
</dt> <dt>



Calificador desconocido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_VALUE"></span><span id="error_mrm_invalid_qualifier_value"></span>**ERROR \_ MRM \_ INVALID \_ QUALIFIER \_ VALUE**
</dt> <dd> <dl> <dt>

15114 (0x3B0A)
</dt> <dt>



Valor de calificador no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_CANDIDATE"></span><span id="error_mrm_no_candidate"></span>**ERROR \_ MRM \_ NO \_ CANDIDATE**
</dt> <dd> <dl> <dt>

15115 (0x3B0B)
</dt> <dt>



No se encontró ningún candidato.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NO_MATCH_OR_DEFAULT_CANDIDATE"></span><span id="error_mrm_no_match_or_default_candidate"></span>**ERROR \_ MRM \_ NO \_ MATCH \_ OR \_ DEFAULT \_ CANDIDATE**
</dt> <dd> <dl> <dt>

15116 (0x3B0C)
</dt> <dt>



ResourceMap o NamedResource tienen un elemento que no tiene un recurso predeterminado o neutro.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_RESOURCE_TYPE_MISMATCH"></span><span id="error_mrm_resource_type_mismatch"></span>**ERROR \_ MRM \_ RESOURCE \_ TYPE \_ MISMATCH**
</dt> <dd> <dl> <dt>

15117 (0x3B0D)
</dt> <dt>



Tipo ResourceCandidate no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_MAP_NAME"></span><span id="error_mrm_duplicate_map_name"></span>**ERROR \_ MRM \_ DUPLICATE \_ MAP \_ NAME**
</dt> <dd> <dl> <dt>

15118 (0x3B0E)
</dt> <dt>



Mapa de recursos duplicado.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_DUPLICATE_ENTRY"></span><span id="error_mrm_duplicate_entry"></span>**ERROR \_ MRM \_ DUPLICATE \_ ENTRY**
</dt> <dd> <dl> <dt>

15119 (0x3B0F)
</dt> <dt>



Entrada duplicada.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_RESOURCE_IDENTIFIER"></span><span id="error_mrm_invalid_resource_identifier"></span>**ERROR \_ MRM \_ INVALID \_ RESOURCE \_ IDENTIFIER**
</dt> <dd> <dl> <dt>

15120 (0x3B10)
</dt> <dt>



Identificador de recurso no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_FILEPATH_TOO_LONG"></span><span id="error_mrm_filepath_too_long"></span>**ERROR \_ MRM \_ FILEPATH \_ TOO \_ LONG**
</dt> <dd> <dl> <dt>

15121 (0x3B11)
</dt> <dt>



Ruta de archivo demasiado larga.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_DIRECTORY_TYPE"></span><span id="error_mrm_unsupported_directory_type"></span>**ERROR \_ TIPO DE DIRECTORIO NO ADMITIDO DE \_ \_ \_ MRM**
</dt> <dd> <dl> <dt>

15122 (0x3B12)
</dt> <dt>



Tipo de directorio no admitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_PRI_FILE"></span><span id="error_mrm_invalid_pri_file"></span>**ERROR \_ MRM \_ INVALID \_ PRI \_ FILE**
</dt> <dd> <dl> <dt>

15126 (0x3B16)
</dt> <dt>



Archivo PRI no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_NAMED_RESOURCE_NOT_FOUND"></span><span id="error_mrm_named_resource_not_found"></span>**ERROR \_ MRM \_ NAMED \_ RESOURCE \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15127 (0x3B17)
</dt> <dt>



No se encontró NamedResource.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_MAP_NOT_FOUND"></span><span id="error_mrm_map_not_found"></span>**ERROR \_ MRM \_ MAP \_ NOT \_ FOUND**
</dt> <dd> <dl> <dt>

15135 (0x3B1F)
</dt> <dt>



No se encontró ResourceMap.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_UNSUPPORTED_PROFILE_TYPE"></span><span id="error_mrm_unsupported_profile_type"></span>**ERROR TIPO DE PERFIL NO ADMITIDO \_ \_ DE \_ \_ MRM**
</dt> <dd> <dl> <dt>

15136 (0x3B20)
</dt> <dt>



Tipo de perfil de MRT no admitido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INVALID_QUALIFIER_OPERATOR"></span><span id="error_mrm_invalid_qualifier_operator"></span>**ERROR \_ MRM \_ INVALID \_ QUALIFIER \_ OPERATOR**
</dt> <dd> <dl> <dt>

15137 (0x3B21)
</dt> <dt>



Operador calificador no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_INDETERMINATE_QUALIFIER_VALUE"></span><span id="error_mrm_indeterminate_qualifier_value"></span>**ERROR \_ MRM \_ INDETERMINATE \_ QUALIFIER \_ VALUE**
</dt> <dd> <dl> <dt>

15138 (0x3B22)
</dt> <dt>



No se puede determinar el valor del calificador o el valor del calificador no se ha establecido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_AUTOMERGE_ENABLED"></span><span id="error_mrm_automerge_enabled"></span>**ERROR \_ MRM \_ AUTOMERGE \_ ENABLED**
</dt> <dd> <dl> <dt>

15139 (0x3B23)
</dt> <dt>



La opción Automerge está habilitada en el archivo PRI.


</dt> </dl> </dd> <dt>

<span id="ERROR_MRM_TOO_MANY_RESOURCES"></span><span id="error_mrm_too_many_resources"></span>**ERROR \_ MRM \_ TOO \_ MANY \_ RESOURCES**
</dt> <dd> <dl> <dt>

15140 (0x3B24)
</dt> <dt>



Demasiados recursos definidos para el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_CAPABILITIES_STRING"></span><span id="error_mca_invalid_capabilities_string"></span>**ERROR \_ MCA \_ INVALID \_ CAPABILITIES \_ STRING**
</dt> <dd> <dl> <dt>

15200 (0x3B60)
</dt> <dt>



El monitor devolvió una cadena de funcionalidades de DDC/CI que no se ajustaba a la especificación ACCESS.bus 3.0, DDC/CI 1.1 o MCCS 2 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_VCP_VERSION"></span><span id="error_mca_invalid_vcp_version"></span>**ERROR \_ MCA \_ INVALID \_ VCP \_ VERSION**
</dt> <dd> <dl> <dt>

15201 (0x3B61)
</dt> <dt>



El código VCP versión de VCP (0xDF) del monitor devolvió un valor de versión no válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MONITOR_VIOLATES_MCCS_SPECIFICATION"></span><span id="error_mca_monitor_violates_mccs_specification"></span>**ERROR \_ QUE MCA \_ MONITOR INFRINGE LA \_ \_ ESPECIFICACIÓN DE \_ MCCS**
</dt> <dd> <dl> <dt>

15202 (0x3B62)
</dt> <dt>



El monitor no cumple con la especificación MCCS que dice admitir.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_MCCS_VERSION_MISMATCH"></span><span id="error_mca_mccs_version_mismatch"></span>**ERROR \_ MCA \_ MCCS \_ VERSION \_ MISMATCH**
</dt> <dd> <dl> <dt>

15203 (0x3B63)
</dt> <dt>



La versión de MCCS en la funcionalidad mccs ver de un monitor no coincide con la versión de MCCS que el monitor notifica cuando se usa el código VCP de la versión de \_ VCP (0xDF).


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_MCCS_VERSION"></span><span id="error_mca_unsupported_mccs_version"></span>**ERROR \_ MCA \_ NO COMPATIBLE CON LA VERSIÓN DE \_ \_ MCCS**
</dt> <dd> <dl> <dt>

15204 (0x3B64)
</dt> <dt>



Monitor Configuration API solo funciona con monitores que admiten la especificación MCCS 1.0, la especificación MCCS 2.0 o la especificación MCCS 2.0 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INTERNAL_ERROR"></span><span id="error_mca_internal_error"></span>**ERROR \_ MCA \_ INTERNAL \_ ERROR**
</dt> <dd> <dl> <dt>

15205 (0x3B65)
</dt> <dt>



Error interno de la API de configuración de Monitor.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_INVALID_TECHNOLOGY_TYPE_RETURNED"></span><span id="error_mca_invalid_technology_type_returned"></span>**ERROR \_ MCA \_ INVALID \_ TECHNOLOGY \_ TYPE \_ RETURNED**
</dt> <dd> <dl> <dt>

15206 (0x3B66)
</dt> <dt>



El monitor devolvió un tipo de tecnología de supervisión no válido. CRT, Crt y CRT (TFT) son ejemplos de tipos de tecnología de supervisión. Este error implica que el monitor infringió la especificación MCCS 2.0 o MCCS 2.0 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_UNSUPPORTED_COLOR_TEMPERATURE"></span><span id="error_mca_unsupported_color_temperature"></span>**ERROR \_ TEMPERATURA DE COLOR NO \_ ADMITIDA DE MCA \_ \_**
</dt> <dd> <dl> <dt>

15207 (0x3B67)
</dt> <dt>



El [**llamador de SetMonitorColorTemperature**](/windows/win32/api/highlevelmonitorconfigurationapi/nf-highlevelmonitorconfigurationapi-setmonitorcolortemperature) especificó una temperatura de color que el monitor actual no admite. Este error implica que el monitor infringió la especificación MCCS 2.0 o MCCS 2.0 Revision 1.


</dt> </dl> </dd> <dt>

<span id="ERROR_AMBIGUOUS_SYSTEM_DEVICE"></span><span id="error_ambiguous_system_device"></span>**ERROR \_ AMBIGUO DEL \_ DISPOSITIVO DEL \_ SISTEMA**
</dt> <dd> <dl> <dt>

15250 (0x3B92)
</dt> <dt>



El dispositivo del sistema solicitado no se puede identificar debido a que varios dispositivos indistinguibles podrían coincidir con los criterios de identificación.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_DEVICE_NOT_FOUND"></span><span id="error_system_device_not_found"></span>**ERROR \_ NO SE ENCONTRÓ EL DISPOSITIVO DEL \_ \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

15299 (0x3BC3)
</dt> <dt>



No se encuentra el dispositivo del sistema solicitado.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_SUPPORTED"></span><span id="error_hash_not_supported"></span>**ERROR \_ HASH \_ NO \_ ADMITIDO**
</dt> <dd> <dl> <dt>

15300 (0x3BC4)
</dt> <dt>



La generación de hash para la versión hash y el tipo hash especificados no está habilitada en el servidor.


</dt> </dl> </dd> <dt>

<span id="ERROR_HASH_NOT_PRESENT"></span><span id="error_hash_not_present"></span>**ERROR \_ HASH \_ NOT \_ PRESENT**
</dt> <dd> <dl> <dt>

15301 (0x3BC5)
</dt> <dt>



El hash solicitado desde el servidor no está disponible o ya no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SECONDARY_IC_PROVIDER_NOT_REGISTERED"></span><span id="error_secondary_ic_provider_not_registered"></span>**ERROR \_ PROVEEDOR DE IC SECUNDARIO NO \_ \_ \_ \_ REGISTRADO**
</dt> <dd> <dl> <dt>

15321 (0x3BD9)
</dt> <dt>



La instancia del controlador de interrupciones secundaria que administra la interrupción especificada no está registrada.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_CLIENT_INFORMATION_INVALID"></span><span id="error_gpio_client_information_invalid"></span>**ERROR \_ GPIO \_ CLIENT \_ INFORMATION \_ INVALID**
</dt> <dd> <dl> <dt>

15322 (0x3BDA)
</dt> <dt>



La información proporcionada por el controlador de cliente GPIO no es válida.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_VERSION_NOT_SUPPORTED"></span><span id="error_gpio_version_not_supported"></span>**ERROR \_ NO SE ADMITE LA VERSIÓN \_ \_ DE GPIO \_**
</dt> <dd> <dl> <dt>

15323 (0x3BDB)
</dt> <dt>



No se admite la versión especificada por el controlador de cliente GPIO.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INVALID_REGISTRATION_PACKET"></span><span id="error_gpio_invalid_registration_packet"></span>**ERROR \_ GPIO \_ INVALID \_ REGISTRATION \_ PACKET**
</dt> <dd> <dl> <dt>

15324 (0x3BDC)
</dt> <dt>



El paquete de registro proporcionado por el controlador de cliente GPIO no es válido.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_OPERATION_DENIED"></span><span id="error_gpio_operation_denied"></span>**ERROR \_ GPIO \_ OPERATION \_ DENIED**
</dt> <dd> <dl> <dt>

15325 (0x3BDD)
</dt> <dt>



La operación solicitada no se admite para el identificador especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INCOMPATIBLE_CONNECT_MODE"></span><span id="error_gpio_incompatible_connect_mode"></span>**ERROR \_ GPIO \_ INCOMPATIBLE \_ CONNECT \_ MODE**
</dt> <dd> <dl> <dt>

15326 (0x3BDE)
</dt> <dt>



El modo de conexión solicitado entra en conflicto con un modo existente en uno o varios de los pines especificados.


</dt> </dl> </dd> <dt>

<span id="ERROR_GPIO_INTERRUPT_ALREADY_UNMASKED"></span><span id="error_gpio_interrupt_already_unmasked"></span>**ERROR \_ GPIO \_ INTERRUPT \_ ALREADY \_ UNMASKED**
</dt> <dd> <dl> <dt>

15327 (0x3BDF)
</dt> <dt>



La interrupción solicitada para desenmascarar no se enmascara.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_SWITCH_RUNLEVEL"></span><span id="error_cannot_switch_runlevel"></span>**ERROR \_ NO SE PUEDE CAMBIAR \_ \_ RUNLEVEL**
</dt> <dd> <dl> <dt>

15400 (0x3C28)
</dt> <dt>



El modificador de nivel de ejecución solicitado no se puede completar correctamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_RUNLEVEL_SETTING"></span><span id="error_invalid_runlevel_setting"></span>**ERROR \_ CONFIGURACIÓN \_ DE RUNLEVEL NO \_ VÁLIDA**
</dt> <dd> <dl> <dt>

15401 (0x3C29)
</dt> <dt>



El servicio tiene una configuración de nivel de ejecución no válida. El nivel de ejecución de un servicio no debe ser mayor que el nivel de ejecución de sus servicios dependientes.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_TIMEOUT"></span><span id="error_runlevel_switch_timeout"></span>**ERROR \_ RUNLEVEL \_ SWITCH \_ TIMEOUT**
</dt> <dd> <dl> <dt>

15402 (0x3C2A)
</dt> <dt>



El modificador de nivel de ejecución solicitado no se puede completar correctamente, ya que uno o varios servicios no se detendrán ni reiniciarán dentro del tiempo de espera especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_AGENT_TIMEOUT"></span><span id="error_runlevel_switch_agent_timeout"></span>**ERROR \_ RUNLEVEL \_ SWITCH \_ AGENT \_ TIMEOUT**
</dt> <dd> <dl> <dt>

15403 (0x3C2B)
</dt> <dt>



Un agente de conmutador de nivel de ejecución no respondió dentro del tiempo de espera especificado.


</dt> </dl> </dd> <dt>

<span id="ERROR_RUNLEVEL_SWITCH_IN_PROGRESS"></span><span id="error_runlevel_switch_in_progress"></span>**ERROR \_ RUNLEVEL \_ SWITCH \_ IN \_ PROGRESS**
</dt> <dd> <dl> <dt>

15404 (0x3C2C)
</dt> <dt>



Actualmente hay un modificador de nivel de ejecución en curso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICES_FAILED_AUTOSTART"></span><span id="error_services_failed_autostart"></span>**ERROR DE \_ INICIO AUTOMÁTICO DE SERVICIOS DE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15405 (0x3C2D)
</dt> <dt>



Uno o varios servicios no se pudieron iniciar durante la fase de inicio del servicio de un conmutador de nivel de ejecución.


</dt> </dl> </dd> <dt>

<span id="ERROR_COM_TASK_STOP_PENDING"></span><span id="error_com_task_stop_pending"></span>**ERROR \_ COM \_ TASK \_ STOP \_ PENDING**
</dt> <dd> <dl> <dt>

15501 (0x3C8D)
</dt> <dt>



La solicitud de detención de tareas no se puede completar inmediatamente, ya que la tarea necesita más tiempo para cerrarse.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OPEN_PACKAGE_FAILED"></span><span id="error_install_open_package_failed"></span>**ERROR AL \_ INSTALAR \_ OPEN PACKAGE \_ \_ FAILED**
</dt> <dd> <dl> <dt>

15600 (0x3CF0)
</dt> <dt>



No se pudo abrir el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_NOT_FOUND"></span><span id="error_install_package_not_found"></span>**ERROR \_ AL INSTALAR EL PAQUETE NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

15601 (0x3CF1)
</dt> <dt>



No se encontró el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_INVALID_PACKAGE"></span><span id="error_install_invalid_package"></span>**ERROR \_ AL INSTALAR UN PAQUETE NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

15602 (0x3CF2)
</dt> <dt>



Los datos del paquete no son válidos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_RESOLVE_DEPENDENCY_FAILED"></span><span id="error_install_resolve_dependency_failed"></span>**ERROR AL \_ INSTALAR \_ RESOLVER \_ \_ DEPENDENCIAS CON ERROR**
</dt> <dd> <dl> <dt>

15603 (0x3CF3)
</dt> <dt>



Actualizaciones de paquete con error, dependencia o validación de conflictos.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_OUT_OF_DISK_SPACE"></span><span id="error_install_out_of_disk_space"></span>**ERROR \_ AL INSTALAR FUERA DEL ESPACIO EN \_ \_ \_ \_ DISCO**
</dt> <dd> <dl> <dt>

15604 (0x3CF4)
</dt> <dt>



No hay suficiente espacio en disco en el equipo. Libera espacio e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_NETWORK_FAILURE"></span><span id="error_install_network_failure"></span>**ERROR AL \_ INSTALAR UN ERROR DE \_ \_ RED**
</dt> <dd> <dl> <dt>

15605 (0x3CF5)
</dt> <dt>



Hubo un problema al descargar el producto.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_REGISTRATION_FAILURE"></span><span id="error_install_registration_failure"></span>**ERROR AL \_ INSTALAR \_ EL \_ REGISTRO**
</dt> <dd> <dl> <dt>

15606 (0x3CF6)
</dt> <dt>



No se pudo registrar el paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_DEREGISTRATION_FAILURE"></span><span id="error_install_deregistration_failure"></span>**ERROR \_ AL INSTALAR EL \_ REGISTRO \_**
</dt> <dd> <dl> <dt>

15607 (0x3CF7)
</dt> <dt>



No se pudo anular el registro del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_CANCEL"></span><span id="error_install_cancel"></span>**ERROR \_ AL INSTALAR \_ CANCEL**
</dt> <dd> <dl> <dt>

15608 (0x3CF8)
</dt> <dt>



El usuario canceló la solicitud de instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FAILED"></span><span id="error_install_failed"></span>**ERROR AL \_ INSTALAR \_**
</dt> <dd> <dl> <dt>

15609 (0x3CF9)
</dt> <dt>



Error de instalación. Póngase en contacto con el proveedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOVE_FAILED"></span><span id="error_remove_failed"></span>**ERROR \_ AL QUITAR \_ ERROR**
</dt> <dd> <dl> <dt>

15610 (0x3CFA)
</dt> <dt>



Error de eliminación. Póngase en contacto con el proveedor de software.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_ALREADY_EXISTS"></span><span id="error_package_already_exists"></span>**EL PAQUETE DE ERROR \_ \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

15611 (0x3CFB)
</dt> <dt>



El paquete proporcionado ya está instalado y se ha bloqueado la reinstalación del paquete. Consulte el registro AppXDeployment-Server eventos para obtener más información.


</dt> </dl> </dd> <dt>

<span id="ERROR_NEEDS_REMEDIATION"></span><span id="error_needs_remediation"></span>**ERROR \_ NEEDS \_ REMEDIATION**
</dt> <dd> <dl> <dt>

15612 (0x3CFC)
</dt> <dt>



No se puede iniciar la aplicación. Intente reinstalar la aplicación para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PREREQUISITE_FAILED"></span><span id="error_install_prerequisite_failed"></span>**ERROR AL \_ INSTALAR \_ EL REQUISITO PREVIO \_**
</dt> <dd> <dl> <dt>

15613 (0x3CFD)
</dt> <dt>



No se pudo cumplir un requisito previo para una instalación.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_REPOSITORY_CORRUPTED"></span><span id="error_package_repository_corrupted"></span>**REPOSITORIO \_ DE \_ PAQUETES DE ERRORES \_ DAÑADO**
</dt> <dd> <dl> <dt>

15614 (0x3CFE)
</dt> <dt>



El repositorio de paquetes está dañado.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_POLICY_FAILURE"></span><span id="error_install_policy_failure"></span>**ERROR AL \_ INSTALAR \_ LA DIRECTIVA \_**
</dt> <dd> <dl> <dt>

15615 (0x3CFF)
</dt> <dt>



Para instalar esta aplicación, necesita una licencia Windows desarrollador o un sistema habilitado para la instalación de instalación local.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGE_UPDATING"></span><span id="error_package_updating"></span>**ACTUALIZACIÓN \_ DEL PAQUETE DE \_ ERROR**
</dt> <dd> <dl> <dt>

15616 (0x3D00)
</dt> <dt>



La aplicación no se puede iniciar porque se está actualizando actualmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPLOYMENT_BLOCKED_BY_POLICY"></span><span id="error_deployment_blocked_by_policy"></span>**IMPLEMENTACIÓN DE \_ ERRORES BLOQUEADA POR LA \_ \_ \_ DIRECTIVA**
</dt> <dd> <dl> <dt>

15617 (0x3D01)
</dt> <dt>



La directiva bloquea la operación de implementación de paquetes. Póngase en contacto con el administrador del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PACKAGES_IN_USE"></span><span id="error_packages_in_use"></span>**PAQUETES \_ DE ERROR EN \_ \_ USO**
</dt> <dd> <dl> <dt>

15618 (0x3D02)
</dt> <dt>



No se pudo instalar el paquete porque los recursos que modifica están actualmente en uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FILE_CORRUPT"></span><span id="error_recovery_file_corrupt"></span>**ARCHIVO DE \_ RECUPERACIÓN \_ DE ERRORES \_ DAÑADO**
</dt> <dd> <dl> <dt>

15619 (0x3D03)
</dt> <dt>



No se pudo recuperar el paquete porque se han dañado los datos necesarios para la recuperación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_STAGED_SIGNATURE"></span><span id="error_invalid_staged_signature"></span>**ERROR \_ DE FIRMA DE FASE NO \_ \_ VÁLIDA**
</dt> <dd> <dl> <dt>

15620 (0x3D04)
</dt> <dt>



La firma no es válida. Para registrarse en modo de desarrollador, AppxSignature.p7x y AppxBlockMap.xml deben ser válidos o no deben estar presentes.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELETING_EXISTING_APPLICATIONDATA_STORE_FAILED"></span><span id="error_deleting_existing_applicationdata_store_failed"></span>**ERROR \_ AL ELIMINAR EL ALMACÉN DE \_ \_ APPLICATIONDATA \_ \_ EXISTENTE**
</dt> <dd> <dl> <dt>

15621 (0x3D05)
</dt> <dt>



Error al eliminar los datos de aplicación existentes anteriormente del paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_PACKAGE_DOWNGRADE"></span><span id="error_install_package_downgrade"></span>**ERROR \_ AL INSTALAR EL PAQUETE \_ \_ DEGRADACIÓN**
</dt> <dd> <dl> <dt>

15622 (0x3D06)
</dt> <dt>



No se pudo instalar el paquete porque ya está instalada una versión superior de este paquete.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_NEEDS_REMEDIATION"></span><span id="error_system_needs_remediation"></span>**ERROR SYSTEM NEEDS REMEDIATION (EL \_ SISTEMA DE ERRORES NECESITA \_ \_ CORRECCIÓN)**
</dt> <dd> <dl> <dt>

15623 (0x3D07)
</dt> <dt>



Se detectó un error en un archivo binario del sistema. Intente actualizar el equipo para corregir el problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPX_INTEGRITY_FAILURE_CLR_NGEN"></span><span id="error_appx_integrity_failure_clr_ngen"></span>**ERROR \_ APPX \_ INTEGRITY \_ FAILURE \_ CLR \_ NGEN**
</dt> <dd> <dl> <dt>

15624 (0x3D08)
</dt> <dt>



Se detectó un binario clr NGEN dañado en el sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESILIENCY_FILE_CORRUPT"></span><span id="error_resiliency_file_corrupt"></span>**ARCHIVO \_ DE RESISTENCIA DE ERRORES \_ \_ DAÑADO**
</dt> <dd> <dl> <dt>

15625 (0x3D09)
</dt> <dt>



No se pudo reanudar la operación porque se han dañado los datos necesarios para la recuperación.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTALL_FIREWALL_SERVICE_NOT_RUNNING"></span><span id="error_install_firewall_service_not_running"></span>**ERROR AL \_ INSTALAR EL SERVICIO FIREWALL NO EN \_ \_ \_ \_ EJECUCIÓN**
</dt> <dd> <dl> <dt>

15626 (0x3D0A)
</dt> <dt>



No se pudo instalar el paquete porque el Windows firewall no se está ejecutando. Habilite el servicio Windows Firewall e inténtelo de nuevo.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_PACKAGE"></span><span id="appmodel_error_no_package"></span>**ERROR DE APPMODEL \_ \_ SIN \_ PAQUETE**
</dt> <dd> <dl> <dt>

15700 (0x3D54)
</dt> <dt>



El proceso no tiene ninguna identidad de paquete.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_RUNTIME_CORRUPT"></span><span id="appmodel_error_package_runtime_corrupt"></span>**TIEMPO DE EJECUCIÓN DEL PAQUETE DE ERROR DE APPMODEL \_ \_ \_ \_ DAÑADO**
</dt> <dd> <dl> <dt>

15701 (0x3D55)
</dt> <dt>



La información en tiempo de ejecución del paquete está dañada.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_PACKAGE_IDENTITY_CORRUPT"></span><span id="appmodel_error_package_identity_corrupt"></span>**IDENTIDAD DEL PAQUETE DE ERROR DE APPMODEL \_ \_ \_ \_ DAÑADA**
</dt> <dd> <dl> <dt>

15702 (0x3D56)
</dt> <dt>



La identidad del paquete está dañada.


</dt> </dl> </dd> <dt>

<span id="APPMODEL_ERROR_NO_APPLICATION"></span><span id="appmodel_error_no_application"></span>**ERROR DE APPMODEL \_ \_ SIN \_ APLICACIÓN**
</dt> <dd> <dl> <dt>

15703 (0x3D57)
</dt> <dt>



El proceso no tiene ninguna identidad de aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_LOAD_STORE_FAILED"></span><span id="error_state_load_store_failed"></span>**ERROR \_ EN EL ALMACÉN DE CARGA DE \_ \_ \_ ESTADO**
</dt> <dd> <dl> <dt>

15800 (0x3DB8)
</dt> <dt>



Error al cargar el almacén de estado.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_GET_VERSION_FAILED"></span><span id="error_state_get_version_failed"></span>**ERROR AL \_ OBTENER LA VERSIÓN DEL ESTADO DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15801 (0x3DB9)
</dt> <dt>



Error al recuperar la versión de estado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SET_VERSION_FAILED"></span><span id="error_state_set_version_failed"></span>**ERROR \_ EN LA VERSIÓN DEL CONJUNTO DE \_ \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15802 (0x3DBA)
</dt> <dt>



Error al establecer la versión de estado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_STRUCTURED_RESET_FAILED"></span><span id="error_state_structured_reset_failed"></span>**ERROR DE \_ RESTABLECIMIENTO \_ ESTRUCTURADO DEL ESTADO \_ DE \_ ERROR**
</dt> <dd> <dl> <dt>

15803 (0x3DBB)
</dt> <dt>



Error al restablecer el estado estructurado de la aplicación.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_OPEN_CONTAINER_FAILED"></span><span id="error_state_open_container_failed"></span>**ERROR AL \_ ABRIR \_ CONTENEDOR DE \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15804 (0x3DBC)
</dt> <dt>



State Manager no pudo abrir el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CREATE_CONTAINER_FAILED"></span><span id="error_state_create_container_failed"></span>**ERROR AL \_ CREAR CONTENEDOR DE ESTADO DE \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15805 (0x3DBD)
</dt> <dt>



State Manager no pudo crear el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_CONTAINER_FAILED"></span><span id="error_state_delete_container_failed"></span>**ERROR AL \_ ELIMINAR \_ CONTENEDOR DE \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15806 (0x3DBE)
</dt> <dt>



State Manager no pudo eliminar el contenedor.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_SETTING_FAILED"></span><span id="error_state_read_setting_failed"></span>**ERROR EN \_ LA CONFIGURACIÓN DE LECTURA DE \_ \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15807 (0x3DBF)
</dt> <dt>



State Manager no pudo leer la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_SETTING_FAILED"></span><span id="error_state_write_setting_failed"></span>**ERROR EN \_ LA CONFIGURACIÓN DE ESCRITURA DE \_ \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15808 (0x3DC0)
</dt> <dt>



State Manager no pudo escribir la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_DELETE_SETTING_FAILED"></span><span id="error_state_delete_setting_failed"></span>**ERROR AL \_ ESTABLECER \_ LA \_ ELIMINACIÓN DEL ESTADO \_**
</dt> <dd> <dl> <dt>

15809 (0x3DC1)
</dt> <dt>



State Manager no pudo eliminar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_QUERY_SETTING_FAILED"></span><span id="error_state_query_setting_failed"></span>**ERROR AL \_ ESTABLECER LA CONSULTA DE \_ \_ ESTADO \_**
</dt> <dd> <dl> <dt>

15810 (0x3DC2)
</dt> <dt>



State Manager no pudo consultar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_READ_COMPOSITE_SETTING_FAILED"></span><span id="error_state_read_composite_setting_failed"></span>**ERROR EN \_ LA CONFIGURACIÓN COMPUESTA DE LECTURA DE ESTADO DE \_ \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15811 (0x3DC3)
</dt> <dt>



State Manager no pudo leer la configuración compuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_WRITE_COMPOSITE_SETTING_FAILED"></span><span id="error_state_write_composite_setting_failed"></span>**ERROR EN \_ LA CONFIGURACIÓN COMPUESTA DE ESCRITURA DE ESTADO DE \_ \_ \_ \_ ERROR**
</dt> <dd> <dl> <dt>

15812 (0x3DC4)
</dt> <dt>



State Manager no pudo escribir la configuración compuesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_CONTAINER_FAILED"></span><span id="error_state_enumerate_container_failed"></span>**ERROR \_ AL \_ ENUMERAR CONTENEDOR DE \_ \_ ESTADO**
</dt> <dd> <dl> <dt>

15813 (0x3DC5)
</dt> <dt>



State Manager no pudo enumerar los contenedores.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_ENUMERATE_SETTINGS_FAILED"></span><span id="error_state_enumerate_settings_failed"></span>**ERROR AL \_ \_ ENUMERAR LA \_ CONFIGURACIÓN \_**
</dt> <dd> <dl> <dt>

15814 (0x3DC6)
</dt> <dt>



State Manager no pudo enumerar la configuración.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_COMPOSITE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_composite_setting_value_size_limit_exceeded"></span>**ERROR \_ STATE \_ COMPOSITE \_ SETTING \_ VALUE \_ SIZE \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

15815 (0x3DC7)
</dt> <dt>



El tamaño del valor de configuración compuesto del administrador de estados ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_VALUE_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_value_size_limit_exceeded"></span>**ERROR \_ STATE \_ SETTING \_ VALUE \_ SIZE \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

15816 (0x3DC8)
</dt> <dt>



El tamaño del valor de configuración del administrador de estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_SETTING_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_setting_name_size_limit_exceeded"></span>**ERROR \_ STATE \_ SETTING \_ NAME \_ SIZE \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

15817 (0x3DC9)
</dt> <dt>



La longitud del nombre de configuración del administrador de estado ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_STATE_CONTAINER_NAME_SIZE_LIMIT_EXCEEDED"></span><span id="error_state_container_name_size_limit_exceeded"></span>**ERROR \_ STATE \_ CONTAINER \_ NAME \_ SIZE \_ LIMIT \_ EXCEEDED**
</dt> <dd> <dl> <dt>

15818 (0x3DCA)
</dt> <dt>



La longitud del nombre del contenedor de State Manager ha superado el límite.


</dt> </dl> </dd> <dt>

<span id="ERROR_API_UNAVAILABLE"></span><span id="error_api_unavailable"></span>**ERROR \_ API \_ NO DISPONIBLE**
</dt> <dd> <dl> <dt>

15841 (0x3DE1)
</dt> <dt>



Esta API no se puede usar en el contexto del tipo de aplicación del autor de la llamada.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de error del sistema](system-error-codes.md)
</dt> </dl>

 

 
