---
description: Recupera un valor de la enumeración CAPICOM \_ PROV \_ TYPE que especifica el tipo de proveedor.
ms.assetid: bc6a579f-5532-45e3-97f4-adcde2cd29e5
title: PrivateKey.ProviderType, propiedad
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170902"
---
# <a name="privatekeyprovidertype-property"></a>PrivateKey.ProviderType, propiedad

\[La **propiedad ProviderType** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **propiedad ProviderType** recupera un valor de la enumeración [**CAPICOM \_ PROV \_ TYPE**](capicom-prov-type.md) que especifica el tipo de proveedor.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.ProviderType As CAPICOM_PROV_TYPE
```



## <a name="property-value"></a>Valor de propiedad

Valor de la [**enumeración CAPICOM \_ PROV \_ TYPE**](capicom-prov-type.md) que indica el tipo de proveedor. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ FULL**</dt> </dl>                 | Proveedor completo [*de servicios*](../secgloss/r-gly.md) [*criptográficos*](../secgloss/c-gly.md) RSA (CSP). Este tipo de proveedor admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de [*datos.*](../secgloss/e-gly.md)<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ SIG**</dt> </dl>                    | Subconjunto del CSP de RSA que solo admite las funciones y algoritmos necesarios para hashes y firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ PROV \_ DSS**</dt> </dl>                                 | CSP [*de Digital Signature Standard*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ PROV \_ FORTEZZA**</dt> </dl>                  | CSP que contiene los protocolos criptográficos y algoritmos propiedad del [*Instituto Nacional de Estándares y Tecnología*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ EXCHANGE**</dt> </dl>        | Csp diseñado para las necesidades criptográficas de microsoft Exchange aplicación de correo electrónico y otras aplicaciones compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ PROV \_ SSL**</dt> </dl>                                 | CSP que admite el [*protocolo Capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ SCHANNEL**</dt> </dl>     | CSP que admite los protocolos RSA y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ PROV \_ DSS \_ DH**</dt> </dl>                       | CSP que admite los protocolos [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) y [*Diffie-Hellman.*](../secgloss/d-gly.md)<br/>                                                                                                                                                           |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | Csp que admite las funciones y algoritmos de algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | Csp que admite las funciones y algoritmos de La curva elíptica Nyberg-Rueppel Analog (ECNRA) necesarias para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECDSA \_ FULL**</dt> </dl> | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL**</dt> </dl> | CSP que admite la ECNRA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ PROV \_ DH \_ SCHANNEL**</dt> </dl>        | CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**</dt> </dl>     | CSP que admite el dispositivo de tarjeta SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ PROV \_ RNG**</dt> </dl>                                 | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ PROV \_ INTEL \_ SEC**</dt> </dl>              | CSP que proporciona seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ PROV \_ REPLACE \_ OWF**</dt> </dl>        | CSP que admite el reemplazo de la manera en que se generan formatos un solo sentido (OWF) a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ AES**</dt> </dl>                    | CSP que admite firmas digitales y cifrado de datos mediante [*el algoritmo Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES).<br/>                                                                                                                                                                                                                                                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> </dl>

 

 
