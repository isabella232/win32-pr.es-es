---
description: Obtiene acceso a un contenedor de claves existente. Este método asocia el contenedor de claves al certificado correspondiente a la clave privada mediante la adición de la propiedad del identificador de la clave de la información de la clave del certificado \_ \_ \_ \_ \_ con la información especificada.
ms.assetid: e5e19452-bfdc-4427-ac1d-cf8aa349bb89
title: PrivateKey. Open (método)
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
ms.openlocfilehash: 7e39738a6e28ebbaffbc867f3098270d5043887a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670701"
---
# <a name="privatekeyopen-method"></a>PrivateKey. Open (método)

\[El método **Open** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Open** obtiene acceso a un [*contenedor de claves*](../secgloss/k-gly.md)existente. Este método asocia el contenedor de claves al [*certificado*](../secgloss/c-gly.md) correspondiente a la [*clave privada*](../secgloss/p-gly.md) mediante la adición de la propiedad del identificador de la clave de la información de la clave del certificado \_ \_ \_ \_ \_ con la información especificada.

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

*ContainerName* \[ de\]
</dt> <dd>

Cadena que contiene el nombre del contenedor de claves.

</dd> <dt>

*ProviderName* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el nombre del proveedor. El valor predeterminado es CAPICOM \_ Prov \_ MS \_ Enhanced \_ Prov. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                      | Significado                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_MS_DEF_PROV"></span><span id="capicom_prov_ms_def_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Def \_**</dt> </dl>                                          | Proveedor de servicios criptográficos básicos de Microsoft.<br/>                            |
| <span id="CAPICOM_PROV_MS_ENHANCED_PROV"></span><span id="capicom_prov_ms_enhanced_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ mejorado \_**</dt> </dl>                           | Proveedor de servicios criptográficos mejorados de Microsoft.<br/>                        |
| <span id="CAPICOM_PROV_MS_STRONG_PROV"></span><span id="capicom_prov_ms_strong_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Strong \_**</dt> </dl>                                 | Proveedor de servicios criptográficos seguros de Microsoft.<br/>                          |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SIG_PROV"></span><span id="capicom_prov_ms_def_rsa_sig_prov"></span><dl> <dt>**CAPICOM \_ de \_ MS \_ Def \_ RSA \_ SIG \_**</dt> </dl>                | Proveedor de servicios criptográficos de firmas RSA de Microsoft.<br/>                   |
| <span id="CAPICOM_PROV_MS_DEF_RSA_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_rsa_schannel_prov"></span><dl> <dt>**\_ \_ MS Def Microsoft \_ \_ RSA \_ Schannel \_ Prov**</dt> </dl> | Proveedor de servicios criptográficos de Microsoft RSA Schannel.<br/>                    |
| <span id="CAPICOM_PROV_MS_DEF_DSS_PROV"></span><span id="capicom_prov_ms_def_dss_prov"></span><dl> <dt>**CAPICOM \_ de \_ MS \_ Def \_ DSS de Microsoft \_**</dt> </dl>                             | Proveedor de servicios criptográficos de Microsoft base DSS.<br/>                        |
| <span id="CAPICOM_PROV_MS_DEF_DSS_DH_PROV"></span><span id="capicom_prov_ms_def_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ de \_ MS \_ Def \_ DSS \_ DH \_ Prov**</dt> </dl>                   | Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos.<br/>     |
| <span id="CAPICOM_PROV_MS_ENH_DSS_DH_PROV"></span><span id="capicom_prov_ms_enh_dss_dh_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Enh \_ DSS \_ DH \_**</dt> </dl>                   | Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos.<br/> |
| <span id="CAPICOM_PROV_MS_DEF_DH_SCHANNEL_PROV"></span><span id="capicom_prov_ms_def_dh_schannel_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Def \_ de \_ Schannel \_**</dt> </dl>    | Proveedor de servicios criptográficos de Microsoft DH Schannel.<br/>                     |
| <span id="CAPICOM_PROV_MS_SCARD_PROV"></span><span id="capicom_prov_ms_scard_prov"></span><dl> <dt>**\_Prov Prov \_ MS \_ de \_ CAPICOM**</dt> </dl>                                    | Proveedor de servicios criptográficos de tarjeta inteligente base de Microsoft.<br/>                 |
| <span id="CAPICOM_PROV_MS_ENH_RSA_AES_PROV"></span><span id="capicom_prov_ms_enh_rsa_aes_prov"></span><dl> <dt>**CAPICOM \_ Prov \_ MS \_ Enh \_ RSA \_ AES \_ Prov**</dt> </dl>                | Proveedor de servicios criptográficos RSA y AES mejorado de Microsoft.<br/>            |



 

</dd> <dt>

*ProviderType* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [**\_ \_ tipo Prov de CAPICOM**](capicom-prov-type.md) que especifica un tipo de proveedor. El valor predeterminado es CAPICOM \_ Prov \_ RSA \_ completo. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_PROV_RSA_FULL"></span><span id="capicom_prov_rsa_full"></span><dl> <dt>**RSA de CAPICOM \_ Prov \_ \_ completo**</dt> </dl>                 | Proveedor de [](../secgloss/r-gly.md) [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) completo de RSA. Este tipo de proveedor es compatible con las [*firmas digitales*](../secgloss/d-gly.md) y el [*cifrado*](../secgloss/e-gly.md)de datos.<br/> |
| <span id="CAPICOM_PROV_RSA_SIG"></span><span id="capicom_prov_rsa_sig"></span><dl> <dt>**\_ \_ \_ firma RSA SIG de CAPICOM**</dt> </dl>                    | Subconjunto del CSP de RSA que admite solo las funciones y algoritmos necesarios para los [*hashes*](../secgloss/h-gly.md) y las [*firmas digitales*](../secgloss/d-gly.md).<br/>                                                                                                                                                                              |
| <span id="CAPICOM_PROV_DSS"></span><span id="capicom_prov_dss"></span><dl> <dt>**CAPICOM \_ Prov \_ DSS**</dt> </dl>                                 | El CSP [*estándar de firma digital*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/>                                                                                     |
| <span id="CAPICOM_PROV_FORTEZZA"></span><span id="capicom_prov_fortezza"></span><dl> <dt>**multiprov de CAPICOM \_ \_**</dt> </dl>                  | El CSP que contiene los protocolos criptográficos y los algoritmos que pertenecen al [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                                                                                                          |
| <span id="CAPICOM_PROV_MS_EXCHANGE"></span><span id="capicom_prov_ms_exchange"></span><dl> <dt>**CAPICOM \_ de \_ MS \_ Exchange**</dt> </dl>        | El CSP que admite la aplicación de correo de Microsoft Exchange y otras aplicaciones compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                                                                                                               |
| <span id="CAPICOM_PROV_SSL"></span><span id="capicom_prov_ssl"></span><dl> <dt>**SSL de CAPICOM \_ \_**</dt> </dl>                                 | CSP que admite el protocolo [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                                                                                                                  |
| <span id="CAPICOM_PROV_RSA_SCHANNEL"></span><span id="capicom_prov_rsa_schannel"></span><dl> <dt>**CAPICOM \_ de \_ RSA \_ Schannel**</dt> </dl>     | El CSP que admite los protocolos RSA y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                                                                                                                                    |
| <span id="CAPICOM_PROV_DSS_DH"></span><span id="capicom_prov_dss_dh"></span><dl> <dt>**CAPICOM \_ de \_ DSS de DSS \_**</dt> </dl>                       | El CSP que admite los protocolos DSS y [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_EC_ECDSA_SIG"></span><span id="capicom_prov_ec_ecdsa_sig"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ ECDSA \_**</dt> </dl>    | El CSP que admite las funciones y los algoritmos del algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_EC_ECNRA_SIG"></span><span id="capicom_prov_ec_ecnra_sig"></span><dl> <dt>**\_ \_ \_ ECNRA \_ SIG de CAPICOM de EC**</dt> </dl>    | El CSP que admite la curva elíptica Nyberg-Rueppel funciones y algoritmos analógicos (ECNRA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="CAPICOM_PROV_EC_ECDSA_FULL"></span><span id="capicom_prov_ec_ecdsa_full"></span><dl> <dt>**CAPICOM \_ Prov \_ EC \_ \_ completo**</dt> </dl> | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_EC_ECNRA_FULL"></span><span id="capicom_prov_ec_ecnra_full"></span><dl> <dt>**ECNRA de CAPICOM de \_ \_ EC \_ \_ completo**</dt> </dl> | CSP que admite el ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_DH_SCHANNEL"></span><span id="capicom_prov_dh_schannel"></span><dl> <dt>**CAPICOM \_ Prov \_ DH \_ Schannel**</dt> </dl>        | El CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_SPYRUS_LYNKS"></span><span id="capicom_prov_spyrus_lynks"></span><dl> <dt>**CAPICOM \_ Prov \_ SPYRUS \_ LYNKS**</dt> </dl>     | El CSP que admite el dispositivo de tarjeta LYNKS de SPYRUS.<br/>                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="CAPICOM_PROV_RNG"></span><span id="capicom_prov_rng"></span><dl> <dt>**no es RNG de CAPICOM \_ \_**</dt> </dl>                                 | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="CAPICOM_PROV_INTEL_SEC"></span><span id="capicom_prov_intel_sec"></span><dl> <dt>**CAPICOM \_ Prov \_ Intel \_ s**</dt> </dl>              | El CSP que proporciona la seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="CAPICOM_PROV_REPLACE_OWF"></span><span id="capicom_prov_replace_owf"></span><dl> <dt>**CAPICOM \_ Prov \_ reemplazar \_ OWF**</dt> </dl>        | El CSP que admite la sustitución de la manera en que se generan los formatos unidireccionales a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="CAPICOM_PROV_RSA_AES"></span><span id="capicom_prov_rsa_aes"></span><dl> <dt>**\_AES de \_ RSA de CAPICOM \_**</dt> </dl>                    | CSP que admite tanto firmas digitales como cifrado de datos mediante el algoritmo Estándar de cifrado avanzado ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

*Especificación de especificación* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la [**\_ \_ especificación de clave CAPICOM**](capicom-key-spec.md) que especifica el tipo de clave privada. El valor predeterminado es la \_ firma de la especificación de clave CAPICOM \_ \_ . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                        | Significado                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <dt>**\_KEYEXCHANGE de \_ especificación de clave CAPICOM \_**</dt> </dl> | La clave se puede utilizar para el cifrado y la firma.<br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <dt>**firma de la \_ especificación de clave CAPICOM \_ \_**</dt> </dl>       | La clave solo se puede utilizar para firmar.<br/>           |



 

</dd> <dt>

*StoreLocation* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de la [**\_ \_ Ubicación del almacén de CAPICOM**](capicom-store-location.md) que especifica la ubicación del almacén en el que reside la clave. El valor predeterminado es el \_ almacén del usuario actual de CAPICOM \_ \_ . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_almacén de memoria CAPICOM \_**</dt> </dl>                                                | El almacén es un almacén de memoria. No se conservan los cambios en el contenido del almacén.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**\_almacén del \_ equipo \_ local de CAPICOM**</dt> </dl>                          | El almacén es un almacén del equipo local. Los almacenes de equipos locales pueden ser almacenes de lectura/escritura solo si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si el almacén está abierto para lectura y escritura, se conservan los cambios en el contenido del almacén.<br/> |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_almacén de \_ usuarios \_ actual de CAPICOM**</dt> </dl>                             | El almacén es un almacén de usuario actual. Un almacén de usuario actual puede ser un almacén de lectura/escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                        |
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**el \_ \_ almacén de \_ usuarios de Active \_ Directory de CAPICOM**</dt> </dl> | El almacén es un almacén de Active Directory. Active Directory almacenes solo se pueden abrir en modo de solo lectura. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                                                                                          |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**el \_ \_ almacén de \_ usuarios de tarjetas inteligentes CAPICOM \_**</dt> </dl>                   | El almacén es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*bCheckExistence* \[ en, opcional\]
</dt> <dd>

Valor booleano que indica si CAPICOM intentará obtener acceso a la clave. Si **es true**, CAPICOM intenta tener acceso a la clave. Si la clave está protegida por el usuario o en una tarjeta inteligente u otro dispositivo, se puede generar un cuadro de diálogo. El valor predeterminado es **False**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método devuelve CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**PrivateKey**](privatekey.md)
</dt> <dt>

[**Certificate. HasPrivateKey**](certificate-hasprivatekey.md)
</dt> </dl>

 

 
