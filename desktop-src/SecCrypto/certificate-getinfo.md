---
description: Recupera información del certificado.
ms.assetid: 57f1c6f9-f06d-4ac7-9070-2a2e6afe93d2
title: ICertificate2::GetInfo (método)
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
ms.openlocfilehash: 401aa077e5f736449e0638fd5cf368224485ec8393b8bddaed1f62296ad90297
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127025"
---
# <a name="icertificate2getinfo-method"></a>ICertificate2::GetInfo (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método GetInfo** recupera información del [*certificado*](../secgloss/c-gly.md).

## <a name="syntax"></a>Sintaxis


```VB
Certificate.GetInfo( _
  ByVal InfoType _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InfoType* \[ En\]
</dt> <dd>

Valor de la enumeración [**\_ CAPICOM CERT INFO \_ \_ TYPE**](capicom-cert-info-type.md) que especifica qué tipo de datos se recuperan del certificado. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERT_INFO_SUBJECT_SIMPLE_NAME"></span><span id="capicom_cert_info_subject_simple_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ SIMPLE \_ NAME**</dt> </dl> | Devuelve el nombre para mostrar del sujeto del certificado.<br/>                            |
| <span id="CAPICOM_CERT_INFO_ISSUER_SIMPLE_NAME"></span><span id="capicom_cert_info_issuer_simple_name"></span><dl> <dt>**NOMBRE SIMPLE DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM \_**</dt> </dl>    | Devuelve el nombre para mostrar del emisor del certificado.<br/>                        |
| <span id="CAPICOM_CERT_INFO_SUBJECT_EMAIL_NAME"></span><span id="capicom_cert_info_subject_email_name"></span><dl> <dt>**CAPICOM CERT INFO SUBJECT EMAIL NAME (NOMBRE DE CORREO ELECTRÓNICO DEL ASUNTO DE INFORMACIÓN \_ \_ DE CERTIFICADO \_ \_ CAPICOM) \_**</dt> </dl>    | Devuelve la dirección de correo electrónico del sujeto del certificado.<br/>                             |
| <span id="CAPICOM_CERT_INFO_ISSUER_EMAIL_NAME"></span><span id="capicom_cert_info_issuer_email_name"></span><dl> <dt>**NOMBRE DE CORREO ELECTRÓNICO DEL EMISOR \_ \_ DE INFORMACIÓN \_ DE \_ \_ CERTIFICADO CAPICOM**</dt> </dl>       | Devuelve la dirección de correo electrónico del emisor del certificado.<br/>                       |
| <span id="CAPICOM_CERT_INFO_SUBJECT_UPN"></span><span id="capicom_cert_info_subject_upn"></span><dl> <dt>**UPN DE ASUNTO \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM**</dt> </dl>                          | Devuelve el UPN del firmante del certificado. Introducido en CAPICOM 2.0.<br/>            |
| <span id="CAPICOM_CERT_INFO_ISSUER_UPN"></span><span id="capicom_cert_info_issuer_upn"></span><dl> <dt>**UPN DEL EMISOR \_ DE INFORMACIÓN DE CERTIFICADO \_ \_ \_ CAPICOM**</dt> </dl>                             | Devuelve el UPN del emisor del certificado. Introducido en CAPICOM 2.0.<br/>      |
| <span id="CAPICOM_CERT_INFO_SUBJECT_DNS_NAME"></span><span id="capicom_cert_info_subject_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ DNS \_ NAME**</dt> </dl>          | Devuelve el nombre DNS del sujeto del certificado. Introducido en CAPICOM 2.0.<br/>       |
| <span id="CAPICOM_CERT_INFO_ISSUER_DNS_NAME"></span><span id="capicom_cert_info_issuer_dns_name"></span><dl> <dt>**CAPICOM \_ CERT \_ INFO \_ ISSUER \_ DNS \_ NAME**</dt> </dl>             | Devuelve el nombre DNS del emisor del certificado. Introducido en CAPICOM 2.0.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena que contiene la información solicitada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de criptografía](cryptography-objects.md)
</dt> <dt>

[**Certificado**](certificate.md)
</dt> </dl>

 

 
