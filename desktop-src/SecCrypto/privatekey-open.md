---
description: Accede a un contenedor de claves existente. Este método asocia el contenedor de claves al certificado que corresponde a la clave privada agregando la propiedad CERT KEY PROV INFO PROP ID con \_ la información \_ \_ \_ \_ especificada.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: Método PrivateKey.Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 289465e46740791341e65dd3864e852f8d0b4d05f753b26ff95b7a97de1951f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977964"
---
# <a name="privatekeyopen-method"></a>Método PrivateKey.Open

\[El **método Open** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use la propiedad [**X509Certificate2.PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Open** tiene acceso a un contenedor de claves [*existente.*](../secgloss/k-gly.md) Este método asocia el contenedor [](../secgloss/c-gly.md) de claves al [](../secgloss/p-gly.md) certificado que corresponde a la clave privada agregando la propiedad CERT KEY PROV INFO PROP ID con \_ la información \_ \_ \_ \_ especificada.

## <a name="syntax"></a>Sintaxis


```VB
PrivateKey.Open( _
  ByVal ContainerName, _
  [ ByVal ProviderName ], _
  [ ByVal ProviderType ], _
  [ ByVal KeySpec ], _
  [ ByVal StoreLocation ], _
  [ ByVal bCheckExistence ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ContainerName* \[ En\]
</dt> <dd>

Cadena que contiene el nombre del contenedor de claves.

</dd> <dt>

*ProviderName* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el nombre del proveedor. El valor predeterminado es CAPICOM \_ PROV \_ MS \_ ENHANCED \_ PROV. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                      | Significado                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ PROV**</dt> </dl>                                          | Proveedor de servicios criptográficos base de Microsoft.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ ENHANCED \_ PROV**</dt> </dl>                           | Proveedor de servicios criptográficos mejorado de Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ STRONG \_ PROV**</dt> </dl>                                 | Proveedor de servicios criptográficos fuerte de Microsoft.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ RSA \_ SIG \_ PROV**</dt> </dl>                | Proveedor criptográfico de firma RSA de Microsoft.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ RSA \_ SCHANNEL \_ PROV**</dt> </dl> | Proveedor de servicios criptográficos Schannel rsa de Microsoft.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ DSS \_ PROV**</dt> </dl>                             | Proveedor criptográfico DSS base de Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ DSS \_ DH \_ PROV**</dt> </dl>                   | DSS base de Microsoft y Diffie-Hellman servicios criptográficos.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ ENH \_ DSS \_ DH \_ PROV**</dt> </dl>                   | Microsoft ha mejorado DSS y Diffie-Hellman servicios criptográficos.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ DEF \_ DH \_ SCHANNEL \_ PROV**</dt> </dl>    | Proveedor criptográfico Schannel de Microsoft DH.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ SCARD \_ PROV**</dt> </dl>                                    | Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ ENH \_ RSA \_ AES \_ PROV**</dt> </dl>                | Proveedor de servicios criptográficos RSA y AES mejorados de Microsoft.<br/>            |



 

</dd> <dt>

*ProviderType* \[ en, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ PROV \_ TYPE**](capicom-prov-type.md) que especifica un tipo de proveedor. El valor predeterminado es CAPICOM \_ PROV \_ RSA \_ FULL. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ FULL**</dt> </dl>                 | Proveedor completo [*de servicios*](../secgloss/r-gly.md) [*criptográficos*](../secgloss/c-gly.md) RSA (CSP). Este tipo de proveedor admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de [*datos.*](../secgloss/e-gly.md)<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ SIG**</dt> </dl>                    | Subconjunto del CSP de RSA que solo admite las funciones y algoritmos necesarios para [*hashes*](../secgloss/h-gly.md) y [*firmas digitales.*](../secgloss/d-gly.md)<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ PROV \_ DSS**</dt> </dl>                                 | CSP [*de Digital Signature Standard*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**CAPICOM \_ PROV \_ FORTEZZA**</dt> </dl>                  | CSP que contiene los protocolos criptográficos y algoritmos propiedad del [*Instituto Nacional de Estándares y Tecnología*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ PROV \_ MS \_ EXCHANGE**</dt> </dl>        | Csp que admite microsoft Exchange aplicación de correo electrónico y otras aplicaciones que son compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**CAPICOM \_ PROV \_ SSL**</dt> </dl>                                 | CSP que admite el [*protocolo Capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ SCHANNEL**</dt> </dl>     | CSP que admite los protocolos RSA y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ PROV \_ DSS \_ DH**</dt> </dl>                       | CSP que admite los protocolos DSS [*y Diffie-Hellman.*](../secgloss/d-gly.md)<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECDSA \_ SIG**</dt> </dl>    | CSP que admite las funciones y algoritmos de algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**</dt> </dl>    | Csp que admite las funciones y algoritmos de La curva elíptica Nyberg-Rueppel Analog (ECNRA) necesarias para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECDSA \_ FULL**</dt> </dl> | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL**</dt> </dl> | CSP que admite la ECNRA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ PROV \_ DH \_ SCHANNEL**</dt> </dl>        | CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**</dt> </dl>     | CSP que admite el dispositivo de tarjeta SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**CAPICOM \_ PROV \_ RNG**</dt> </dl>                                 | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ PROV \_ INTEL \_ SEC**</dt> </dl>              | CSP que proporciona seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ PROV \_ REPLACE \_ OWF**</dt> </dl>        | CSP que admite el reemplazo de la manera en que se generan formatos un solo sentido a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**CAPICOM \_ PROV \_ RSA \_ AES**</dt> </dl>                    | CSP que admite firmas digitales y cifrado de datos mediante el algoritmo Estándar de cifrado avanzado [*(AES).*](../secgloss/a-gly.md)<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*KeySpec* \[ en, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ KEY \_ SPEC**](capicom-key-spec.md) que especifica el tipo de clave privada. El valor predeterminado es CAPICOM \_ KEY \_ SPEC \_ SIGNATURE. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                        | Significado                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**CAPICOM \_ KEY \_ SPEC \_ KEYEXCHANGE**</dt> </dl> | La clave se puede usar para el cifrado y la firma.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**FIRMA DE \_ ESPECIFICACIÓN DE CLAVE \_ \_ CAPICOM**</dt> </dl>       | La clave solo se puede usar para firmar.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ en, opcional\]
</dt> <dd>

Valor de la [**enumeración CAPICOM \_ STORE \_ LOCATION**](capicom-store-location.md) que especifica la ubicación del almacén donde reside la clave. El valor predeterminado es CAPICOM \_ CURRENT \_ USER \_ STORE. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**ALMACÉN DE MEMORIA \_ CAPICOM \_**</dt> </dl>                                                | El almacén es un almacén de memoria. Los cambios en el contenido del almacén no se conservan.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM \_ LOCAL \_ MACHINE \_ STORE**</dt> </dl>                          | El almacén es un almacén de equipos local. Los almacenes de equipos locales solo pueden ser almacenes de lectura y escritura si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si el almacén se abre de lectura y escritura, los cambios en el contenido del almacén se conservan.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS \_ ACTUAL DE CAPICOM \_ \_**</dt> </dl>                             | El almacén es un almacén de usuario actual. Un almacén de usuario actual puede ser un almacén de lectura y escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS DE CAPICOM \_ ACTIVE \_ DIRECTORY \_ \_**</dt> </dl> | El almacén es un Active Directory almacén. Active Directory se pueden abrir solo en modo de solo lectura. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS \_ DE \_ TARJETA INTELIGENTE CAPICOM \_ \_**</dt> </dl>                   | La tienda es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si CAPICOM intentará acceder a la clave. Si **es True,** CAPICOM intenta acceder a la clave. Si la clave está protegida por el usuario o en una tarjeta inteligente u otro dispositivo, se puede generar un cuadro de diálogo. El valor predeterminado es **False**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método devuelve CAPICOM \_ E NOT ALLOWED cuando se crea un script desde una aplicación basada en \_ \_ web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate.HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
