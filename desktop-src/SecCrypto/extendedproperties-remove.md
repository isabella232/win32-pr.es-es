---
description: Quita una propiedad extendida de la colección.
ms.assetid: 0329a158-758d-4e73-95a5-bab7307e7d70
title: ExtendedProperties. Remove (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1774ce0fc8b03bed621c58b0f7a9a0f16a7d4156
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671043"
---
# <a name="extendedpropertiesremove-method"></a>ExtendedProperties. Remove (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a la función de la API de Win32 [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) y obtener las propiedades. Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx). También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]

El método **Remove** quita una propiedad extendida de la colección.

## <a name="syntax"></a>Sintaxis


```VB
ExtendedProperties.Remove( _
  ByVal propID _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*propID* \[ de\]
</dt> <dd>

Un valor de la enumeración de [**CAPICOM \_ PROPID**](capicom-propid.md) que define los identificadores de propiedad de CAPICOM de la propiedad extendida que se va a quitar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                           | Significado                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROPID_UNKNOWN"></span><span id="capicom_propid_unknown"></span><dl> <dt>**no se \_ conoce el PROPID de CAPICOM \_**</dt> </dl>                                                                       | No se conoce el tipo de la propiedad.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_KEY_PROV_HANDLE"></span><span id="capicom_propid_key_prov_handle"></span><dl> <dt>**\_identificador de \_ Prov de clave \_ \_ de CAPICOM PROPID**</dt> </dl>                                             | Identificador de un contenedor de claves dentro de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        |
| <span id="CAPICOM_PROPID_KEY_PROV_INFO"></span><span id="capicom_propid_key_prov_info"></span><dl> <dt>**\_información de \_ Prov de clave \_ \_ de CAPICOM PROPID**</dt> </dl>                                                   | Información sobre un contenedor de claves dentro de un CSP.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_SHA1_HASH"></span><span id="capicom_propid_sha1_hash"></span><dl> <dt>**HASH de SHA1 de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                                | Objeto hash SHA1.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_HASH_PROP"></span><span id="capicom_propid_hash_prop"></span><dl> <dt>**\_ \_ propiedades hash de el PROPID de CAPICOM \_**</dt> </dl>                                                                | Propiedades de un objeto hash.<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_MD5_HASH"></span><span id="capicom_propid_md5_hash"></span><dl> <dt>**\_ \_ Hash MD5 del PROPID de CAPICOM \_**</dt> </dl>                                                                   | Objeto hash MD5.<br/>                                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_KEY_CONTEXT"></span><span id="capicom_propid_key_context"></span><dl> <dt>**contexto de clave de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                          | [*Contexto*](../secgloss/c-gly.md)de la clave.<br/>                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_KEY_SPEC"></span><span id="capicom_propid_key_spec"></span><dl> <dt>**Especificación de clave de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                                   | Especificaciones de una clave.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_IE30_RESERVED"></span><span id="capicom_propid_ie30_reserved"></span><dl> <dt>**CAPICOM \_ PROPID \_ IE30 \_ Reserved**</dt> </dl>                                                    | Información acerca de si el objeto está reservado en Internet Explorer 3,0.<br/>                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_PUBKEY_HASH_RESERVED"></span><span id="capicom_propid_pubkey_hash_reserved"></span><dl> <dt>**se \_ ha \_ \_ reservado el hash de PUBKEY de CAPICOM PROPID \_**</dt> </dl>                              | Información sobre si el hash de la clave pública está reservado.<br/>                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_ENHKEY_USAGE"></span><span id="capicom_propid_enhkey_usage"></span><dl> <dt>**\_uso de \_ ENHKEY del PROPID de CAPICOM \_**</dt> </dl>                                                       | Un [*uso mejorado de clave*](../secgloss/e-gly.md) (EKU).<br/>                                                                                                                                                              |
| <span id="CAPICOM_PROPID_CTL_USAGE"></span><span id="capicom_propid_ctl_usage"></span><dl> <dt>**\_uso de \_ CTL del PROPID de CAPICOM \_**</dt> </dl>                                                                | Un uso de la [*lista de certificados de confianza*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             |
| <span id="CAPICOM_PROPID_NEXT_UPDATE_LOCATION"></span><span id="capicom_propid_next_update_location"></span><dl> <dt>**\_ \_ siguiente ubicación de \_ actualización \_ de CAPICOM PROPID**</dt> </dl>                              | La ubicación de la siguiente actualización de la [*lista de revocación de certificados*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               |
| <span id="CAPICOM_PROPID_FRIENDLY_NAME"></span><span id="capicom_propid_friendly_name"></span><dl> <dt>**\_ \_ nombre descriptivo de CAPICOM PROPID \_**</dt> </dl>                                                    | Un nombre legible.<br/>                                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_PVK_FILE"></span><span id="capicom_propid_pvk_file"></span><dl> <dt>**\_ \_ archivo PVK del PROPID de CAPICOM \_**</dt> </dl>                                                                   | Un archivo que contiene una clave privada.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_DESCRIPTION"></span><span id="capicom_propid_description"></span><dl> <dt>**Descripción de la PROPID de CAPICOM \_ \_**</dt> </dl>                                                           | Una descripción legible.<br/>                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ACCESS_STATE"></span><span id="capicom_propid_access_state"></span><dl> <dt>**Estado de acceso de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                       | Estado del acceso.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SIGNATURE_HASH"></span><span id="capicom_propid_signature_hash"></span><dl> <dt>**HASH de firma de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                 | Un hash de la firma.<br/>                                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SMART_CARD_DATA"></span><span id="capicom_propid_smart_card_data"></span><dl> <dt>**\_datos de \_ \_ tarjeta inteligente \_ de CAPICOM PROPID**</dt> </dl>                                             | Datos de la tarjeta inteligente.<br/>                                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_EFS"></span><span id="capicom_propid_efs"></span><dl> <dt>**\_EFS PROPID de CAPICOM \_**</dt> </dl>                                                                                   | Sistema de cifrado de archivos (EFS).<br/>                                                                                                                                                                                                                                                |
| <span id="CAPICOM_PROPID_FORTEZZA_DATA"></span><span id="capicom_propid_fortezza_data"></span><dl> <dt>**datos de la \_ \_ información Fortezza del PROPID de CAPICOM \_**</dt> </dl>                                                    | Los datos creados mediante los protocolos criptográficos y los algoritmos que pertenecen al [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> |
| <span id="CAPICOM_PROPID_ARCHIVED"></span><span id="capicom_propid_archived"></span><dl> <dt>**CAPICOM \_ PROPID \_ archived**</dt> </dl>                                                                    | Información sobre si el objeto se ha archivado.<br/>                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_KEY_IDENTIFIER"></span><span id="capicom_propid_key_identifier"></span><dl> <dt>**identificador de clave de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                 | Identificador de clave.<br/>                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_AUTO_ENROLL"></span><span id="capicom_propid_auto_enroll"></span><dl> <dt>**\_ \_ inscripción automática de CAPICOM PROPID \_**</dt> </dl>                                                          | Información de inscripción automática de un certificado.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_PUBKEY_ALG_PARA"></span><span id="capicom_propid_pubkey_alg_para"></span><dl> <dt>**CAPICOM \_ PROPID \_ PUBKEY \_ alg \_ para**</dt> </dl>                                             | Parámetros de un algoritmo de clave pública.<br/>                                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_CROSS_CERT_DIST_POINTS"></span><span id="capicom_propid_cross_cert_dist_points"></span><dl> <dt>**\_puntos de \_ distribución de certificados cruzados del PROPID de \_ \_ CAPICOM \_**</dt> </dl>                       | Información utilizada para actualizar los certificados cruzados dinámicos.<br/>                                                                                                                                                                                                                          |
| <span id="CAPICOM_PROPID_ISSUER_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_issuer_public_key_md5_hash"></span><dl> <dt>**\_ \_ \_ \_ Hash MD5 de clave pública \_ del emisor \_ de CAPICOM PROPID**</dt> </dl>          | El hash MD5 de la clave pública del emisor.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_SUBJECT_PUBLIC_KEY_MD5_HASH"></span><span id="capicom_propid_subject_public_key_md5_hash"></span><dl> <dt>**\_Hash MD5 del asunto de la \_ \_ clave pública del sujeto \_ \_ de \_ CAPICOM**</dt> </dl>       | El hash MD5 de la clave pública del sujeto.<br/>                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROPID_ENROLLMENT"></span><span id="capicom_propid_enrollment"></span><dl> <dt>**inscripción de CAPICOM \_ PROPID \_**</dt> </dl>                                                              | Información sobre la inscripción del certificado.<br/>                                                                                                                                                                                                                                 |
| <span id="CAPICOM_PROPID_DATE_STAMP"></span><span id="capicom_propid_date_stamp"></span><dl> <dt>**marca de fecha de CAPICOM \_ PROPID \_ \_**</dt> </dl>                                                             | Una marca de fecha.<br/>                                                                                                                                                                                                                                                                   |
| <span id="CAPICOM_PROPID_ISSUER_SERIAL_NUMBER_MD5_HASH"></span><span id="capicom_propid_issuer_serial_number_md5_hash"></span><dl> <dt>**Número de serie del emisor de CAPICOM del \_ \_ \_ \_ \_ \_ algoritmo hash MD5**</dt> </dl> | El hash MD5 del número de serie del emisor.<br/>                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROPID_SUBJECT_NAME_MD5_HASH"></span><span id="capicom_propid_subject_name_md5_hash"></span><dl> <dt>**Nombre del firmante de CAPICOM \_ PROPID \_ \_ \_ \_ hash MD5**</dt> </dl>                          | El hash MD5 del nombre del sujeto.<br/>                                                                                                                                                                                                                                             |
| <span id="CAPICOM_PROPID_EXTENDED_ERROR_INFO"></span><span id="capicom_propid_extended_error_info"></span><dl> <dt>**\_información de \_ \_ error extendido \_ de CAPICOM PROPID**</dt> </dl>                                 | Información ampliada sobre un error.<br/>                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROPID_RENEWAL"></span><span id="capicom_propid_renewal"></span><dl> <dt>**\_renovación del PROPID de CAPICOM \_**</dt> </dl>                                                                       | Información sobre la renovación de una [*entidad de certificación*](../secgloss/c-gly.md).<br/>                                                                                                                     |
| <span id="CAPICOM_PROPID_ARCHIVED_KEY_HASH"></span><span id="capicom_propid_archived_key_hash"></span><dl> <dt>**\_hash de \_ clave archivada de CAPICOM PROPID \_ \_**</dt> </dl>                                       | Un hash archivado de una clave.<br/>                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROPID_FIRST_RESERVED"></span><span id="capicom_propid_first_reserved"></span><dl> <dt>**se \_ ha \_ reservado primero el PROPID de CAPICOM \_**</dt> </dl>                                                 | Información sobre la primera reserva.<br/>                                                                                                                                                                                                                                        |
| <span id="CAPICOM_PROPID_LAST_RESERVED"></span><span id="capicom_propid_last_reserved"></span><dl> <dt>**se \_ ha \_ reservado por última vez CAPICOM PROPID \_**</dt> </dl>                                                    | Información sobre la reserva más reciente.<br/>                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROPID_FIRST_USER"></span><span id="capicom_propid_first_user"></span><dl> <dt>**\_ \_ primer \_ usuario de CAPICOM PROPID**</dt> </dl>                                                             | Información sobre el primer usuario.<br/>                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROPID_LAST_USER"></span><span id="capicom_propid_last_user"></span><dl> <dt>**\_ \_ último \_ usuario de CAPICOM PROPID**</dt> </dl>                                                                | Información sobre el usuario más reciente.<br/>                                                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
