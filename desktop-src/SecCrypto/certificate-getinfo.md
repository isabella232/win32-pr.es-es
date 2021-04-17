---
description: Recupera información del certificado.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: 'ICertificate2:: GetInfo (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.GetInfo
- ICertificate2.GetInfo
- ICertificate.GetInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41b3cb6cde796f64ee3a5953ed848d105a10bc5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670577"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2:: GetInfo (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **GetInfo** recupera información del [*certificado*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintaxis


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ de\]
</dt> <dd>

Un valor de la enumeración de tipo de información de certificado de CAPICOM que especifica qué tipo de datos se recupera del certificado. [**\_ \_ \_**](capicom-cert-info-type.md) En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**\_ \_ \_ nombre simple del asunto de información \_ de certificado de CAPICOM \_**</dt> </dl> | Devuelve el nombre para mostrar del asunto del certificado.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**\_ \_ \_ nombre simple del emisor de información de \_ certificado de \_ CAPICOM**</dt> </dl>    | Devuelve el nombre para mostrar del emisor del certificado.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**\_nombre de \_ \_ \_ correo electrónico del asunto de información de certificado de CAPICOM \_**</dt> </dl>    | Devuelve la dirección de correo electrónico del firmante del certificado.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**\_nombre de \_ \_ \_ correo electrónico del emisor de información \_ de certificado de CAPICOM**</dt> </dl>       | Devuelve la dirección de correo electrónico del emisor del certificado.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**\_UPN de \_ asunto de información de certificado de CAPICOM \_ \_**</dt> </dl>                          | Devuelve el UPN del firmante del certificado. Introducido en CAPICOM 2,0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**\_UPN del \_ emisor de información de certificado de \_ CAPICOM \_**</dt> </dl>                             | Devuelve el UPN del emisor del certificado. Introducido en CAPICOM 2,0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**\_ \_ \_ nombre DNS del asunto de información \_ de certificado de CAPICOM \_**</dt> </dl>          | Devuelve el nombre DNS del firmante del certificado. Introducido en CAPICOM 2,0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**\_ \_ \_ nombre DNS del emisor de información de \_ certificado de \_ CAPICOM**</dt> </dl>             | Devuelve el nombre DNS del emisor del certificado. Introducido en CAPICOM 2,0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena que contiene la información solicitada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
