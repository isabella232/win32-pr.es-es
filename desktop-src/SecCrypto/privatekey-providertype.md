---
description: Recupera un valor de la \_ enumeración de tipo Prov de CAPICOM \_ que especifica el tipo de proveedor.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: Propiedad PrivateKey. ProviderType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderType
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b38cc9a030bc27a30a66624f1faeca080104e7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670438"
---
# <a name="privatekeyprovidertype-property"></a>Propiedad PrivateKey. ProviderType

\[La propiedad **ProviderType** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **ProviderType** recupera un valor de la enumeración de [**\_ \_ tipo Prov de CAPICOM**](capicom-prov-type.md) que especifica el tipo de proveedor.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Valor de propiedad

Un valor de la enumeración de [**\_ \_ tipo Prov de CAPICOM**](capicom-prov-type.md) que indica el tipo de proveedor. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**RSA de CAPICOM \_ Prov \_ \_ completo**</dt> </dl>                 | Proveedor de [](../secgloss/r-gly.md) [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) completo de RSA. Este tipo de proveedor es compatible con las [*firmas digitales*](../secgloss/d-gly.md) y el [*cifrado*](../secgloss/e-gly.md)de datos.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**\_ \_ \_ firma RSA SIG de CAPICOM**</dt> </dl>                    | Subconjunto del CSP de RSA que admite solo las funciones y algoritmos necesarios para los hashes y las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | El CSP [*estándar de firma digital*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**multiprov de CAPICOM \_ \_**</dt> </dl>                  | El CSP que contiene los protocolos criptográficos y los algoritmos que pertenecen al [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ de \_ MS \_ Exchange**</dt> </dl>        | El CSP diseñado para las necesidades criptográficas de la aplicación de correo de Microsoft Exchange y otras aplicaciones compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**SSL de CAPICOM \_ \_**</dt> </dl>                                 | CSP que admite el protocolo [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ de \_ RSA \_ Schannel**</dt> </dl>     | El CSP que admite los protocolos RSA y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ de \_ DSS de DSS \_**</dt> </dl>                       | El CSP que admite los protocolos [*estándar de firma digital*](../secgloss/d-gly.md) (DSS) y [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_**</dt> </dl>    | El CSP que admite las funciones y los algoritmos del algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**\_ \_ \_ ECNRA \_ SIG de CAPICOM de EC**</dt> </dl>    | El CSP que admite la curva elíptica Nyberg-Rueppel funciones y algoritmos analógicos (ECNRA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ \_ completo**</dt> </dl> | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**ECNRA de CAPICOM de \_ \_ EC \_ \_ completo**</dt> </dl> | CSP que admite el ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ DH \_ Schannel**</dt> </dl>        | El CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ SPYRUS \_ LYNKS**</dt> </dl>     | El CSP que admite el dispositivo de tarjeta LYNKS de SPYRUS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**no es RNG de CAPICOM \_ \_**</dt> </dl>                                 | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ s**</dt> </dl>              | El CSP que proporciona la seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ reemplazar \_ OWF**</dt> </dl>        | El CSP que admite la sustitución de la manera en la que se generan formatos unidireccionales (OWFs) a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**\_AES de \_ RSA de CAPICOM \_**</dt> </dl>                    | CSP que admite tanto firmas digitales como cifrado de datos mediante el algoritmo [*estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
