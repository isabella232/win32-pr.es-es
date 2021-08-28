---
description: Se usa para identificar algoritmos de cifrado estándar en varias funciones y estructuras de CNG, como la estructura CRYPT \_ INTERFACE \_ REG.
ms.assetid: a05ae7e6-d882-4287-9990-23e4cd340b05
title: Identificadores de algoritmo CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e853d7cd0d1dd34104d3cffa20f301c11e45304c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481891"
---
# <a name="cng-algorithm-identifiers"></a>Identificadores de algoritmo CNG

Los identificadores siguientes se usan para identificar algoritmos de cifrado estándar en varias funciones y estructuras de CNG, como la estructura [**CRYPT \_ INTERFACE \_ REG.**](/windows/desktop/api/Bcrypt/ns-bcrypt-crypt_interface_reg) Los proveedores de terceros pueden tener algoritmos adicionales que admitan.




| Constante o valor | Descripción | 
|----------------|-------------|
| <span id="BCRYPT_3DES_ALGORITHM"></span><span id="bcrypt_3des_algorithm"></span><dl><dt><strong>BCRYPT_3DES_ALGORITHM</strong></dt><dt>"3DES"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado de datos triple.<br /> Estándar: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_3DES_112_ALGORITHM"></span><span id="bcrypt_3des_112_algorithm"></span><dl><dt><strong>BCRYPT_3DES_112_ALGORITHM</strong></dt><dt>"3DES_112"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado de datos triple de 112 bits.<br /> Estándar: SP800-67, SP800-38A<br /> | 
| <span id="BCRYPT_AES_ALGORITHM"></span><span id="bcrypt_aes_algorithm"></span><dl><dt><strong>BCRYPT_AES_ALGORITHM</strong></dt><dt>"AES"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado avanzado.<br /> Estándar: FIPS 197<br /> | 
| <span id="BCRYPT_AES_CMAC_ALGORITHM"></span><span id="bcrypt_aes_cmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_CMAC_ALGORITHM</strong></dt><dt>"AES-CMAC"</dt></dl> | Algoritmo de cifrado simétrico basado en código de autenticación de mensajes (CMAC) basado en cifrado estándar de cifrado avanzado (AES).<br /> Estándar: SP 800-38B<br /><strong>Windows 8:</strong> Comienza la compatibilidad con este algoritmo.<br /><br /> | 
| <span id="BCRYPT_AES_GMAC_ALGORITHM"></span><span id="bcrypt_aes_gmac_algorithm"></span><dl><dt><strong>BCRYPT_AES_GMAC_ALGORITHM</strong></dt><dt>"AES-GMAC"</dt></dl> | El algoritmo de cifrado simétrico de código de autenticación de mensajes (GMAC) de Galois estándar de cifrado avanzado (AES).<br /> Estándar: SP800-38D<br /><strong>Windows Vista:</strong> Este algoritmo se admite a partir de Windows Vista con SP1.<br /> | 
| <span id="BCRYPT_CAPI_KDF_ALGORITHM"></span><span id="bcrypt_capi_kdf_algorithm"></span><dl><dt><strong>BCRYPT_CAPI_KDF_ALGORITHM</strong></dt><dt>L"CAPI_KDF"</dt></dl> | Algoritmo de función de derivación de claves de crypto API (CAPI). Usado por <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>las funciones BCryptKeyDerivation</strong></a> y <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_DES_ALGORITHM"></span><span id="bcrypt_des_algorithm"></span><dl><dt><strong>BCRYPT_DES_ALGORITHM</strong></dt><dt>"DES"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado de datos.<br /> Estándar: FIPS 46-3, FIPS 81<br /> | 
| <span id="BCRYPT_DESX_ALGORITHM"></span><span id="bcrypt_desx_algorithm"></span><dl><dt><strong>BCRYPT_DESX_ALGORITHM</strong></dt><dt>"DESX"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado de datos extendido.<br /> Estándar: Ninguno<br /> | 
| <span id="BCRYPT_DH_ALGORITHM"></span><span id="bcrypt_dh_algorithm"></span><dl><dt><strong>BCRYPT_DH_ALGORITHM</strong></dt><dt>"DH"</dt></dl> | Algoritmo Diffie-Hellman de intercambio de claves.<br /> Estándar: pkcs #3<br /> | 
| <span id="BCRYPT_DSA_ALGORITHM"></span><span id="bcrypt_dsa_algorithm"></span><dl><dt><strong>BCRYPT_DSA_ALGORITHM</strong></dt><dt>"DSA"</dt></dl> | Algoritmo de firma digital.<br /> Estándar: FIPS 186-2<br /><strong>Windows 8:</strong> A partir Windows 8, este algoritmo admite FIPS 186-3. Las claves menores o iguales que 1024 bits se adhieren a FIPS 186-2 y las claves mayores que 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_ECDH_P256_ALGORITHM"></span><span id="bcrypt_ecdh_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P256_ALGORITHM</strong></dt><dt>"ECDH_P256"</dt></dl> | La curva elíptica prime de 256 bits Diffie-Hellman de intercambio de claves.<br /> Estándar: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P384_ALGORITHM"></span><span id="bcrypt_ecdh_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P384_ALGORITHM</strong></dt><dt>"ECDH_P384"</dt></dl> | La curva elíptica prime de 384 bits Diffie-Hellman algoritmo de intercambio de claves.<br /> Estándar: SP800-56A<br /> | 
| <span id="BCRYPT_ECDH_P521_ALGORITHM"></span><span id="bcrypt_ecdh_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_P521_ALGORITHM</strong></dt><dt>"ECDH_P521"</dt></dl> | La curva elíptica prime de 521 bits Diffie-Hellman de intercambio de claves.<br /> Estándar: SP800-56A<br /> | 
| <span id="BCRYPT_ECDSA_P256_ALGORITHM"></span><span id="bcrypt_ecdsa_p256_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P256_ALGORITHM</strong></dt><dt>"ECDSA_P256"</dt></dl> | Algoritmo de firma digital de curva elíptica prime de 256 bits (FIPS 186-2).<br /> Estándar: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P384_ALGORITHM"></span><span id="bcrypt_ecdsa_p384_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P384_ALGORITHM</strong></dt><dt>"ECDSA_P384"</dt></dl> | Algoritmo de firma digital de curva elíptica prime de 384 bits (FIPS 186-2).<br /> Estándar: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_ECDSA_P521_ALGORITHM"></span><span id="bcrypt_ecdsa_p521_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_P521_ALGORITHM</strong></dt><dt>"ECDSA_P521"</dt></dl> | Algoritmo de firma digital de curva elíptica prime de 521 bits (FIPS 186-2).<br /> Estándar: FIPS 186-2, X9.62<br /> | 
| <span id="BCRYPT_MD2_ALGORITHM"></span><span id="bcrypt_md2_algorithm"></span><dl><dt><strong>BCRYPT_MD2_ALGORITHM</strong></dt><dt>"MD2"</dt></dl> | Algoritmo hash MD2.<br /> Estándar: RFC 1319<br /> | 
| <span id="BCRYPT_MD4_ALGORITHM"></span><span id="bcrypt_md4_algorithm"></span><dl><dt><strong>BCRYPT_MD4_ALGORITHM</strong></dt><dt>"MD4"</dt></dl> | Algoritmo hash MD4.<br /> Estándar: RFC 1320<br /> | 
| <span id="BCRYPT_MD5_ALGORITHM"></span><span id="bcrypt_md5_algorithm"></span><dl><dt><strong>BCRYPT_MD5_ALGORITHM</strong></dt><dt>"MD5"</dt></dl> | Algoritmo hash MD5.<br /> Estándar: RFC 1321<br /> | 
| <span id="BCRYPT_RC2_ALGORITHM"></span><span id="bcrypt_rc2_algorithm"></span><dl><dt><strong>BCRYPT_RC2_ALGORITHM</strong></dt><dt>"RC2"</dt></dl> | Algoritmo de cifrado simétrico de bloque RC2.<br /> Estándar: RFC 2268<br /> | 
| <span id="BCRYPT_RC4_ALGORITHM"></span><span id="bcrypt_rc4_algorithm"></span><dl><dt><strong>BCRYPT_RC4_ALGORITHM</strong></dt><dt>"RC4"</dt></dl> | Algoritmo de cifrado simétrico RC4.<br /> Estándar: varios<br /> | 
| <span id="BCRYPT_RNG_ALGORITHM"></span><span id="bcrypt_rng_algorithm"></span><dl><dt><strong>BCRYPT_RNG_ALGORITHM</strong></dt><dt>"RNG"</dt></dl> | Algoritmo generador de números aleatorios.<br /> Estándar: FIPS 186-2, FIPS 140-2, NIST SP 800-90<br /><blockquote>[!Note]<br />A partir de Windows Vista con SP1 y Windows Server 2008, el generador de números aleatorios se basa en el modo de contador AES especificado en el estándar NIST SP 800-90.</blockquote><br /><strong>Windows Vista:</strong> El generador de números aleatorios se basa en el generador de números aleatorios basado en hash especificado en el estándar FIPS 186-2.<br /><strong>Windows 8:</strong> A partir Windows 8, el algoritmo RNG admite FIPS 186-3. Las claves menores o iguales que 1024 bits se adhieren a FIPS 186-2 y las claves mayores que 1024 a FIPS 186-3.<br /> | 
| <span id="BCRYPT_RNG_DUAL_EC_ALGORITHM"></span><span id="bcrypt_rng_dual_ec_algorithm"></span><dl><dt><strong>BCRYPT_RNG_DUAL_EC_ALGORITHM</strong></dt><dt>"DUALECRNG"</dt></dl> | Algoritmo generador de números aleatorios de curva elíptica dual. <br /> Estándar: SP800-90.<br /><strong>Windows 8:</strong> A partir Windows 8, el algoritmo ec RNG admite FIPS 186-3. Las claves menores o iguales que 1024 bits se adhieren a FIPS 186-2 y las claves mayores que 1024 a FIPS 186-3.<br /><strong>Windows 10:</strong> A partir Windows 10, se ha quitado el algoritmo de generador de números aleatorios de curva elíptica dual. Los usos existentes de este algoritmo seguirán funcionando; sin embargo, el generador de números aleatorios se basa en el modo de contador AES especificado en el estándar NIST SP 800-90. El nuevo código debe <strong>BCRYPT_RNG_ALGORITHM</strong>y se recomienda cambiar el código existente para usar <strong>BCRYPT_RNG_ALGORITHM</strong>. <br /> | 
| <span id="BCRYPT_RNG_FIPS186_DSA_ALGORITHM"></span><span id="bcrypt_rng_fips186_dsa_algorithm"></span><dl><dt><strong>BCRYPT_RNG_FIPS186_DSA_ALGORITHM</strong></dt><dt>"FIPS186DSARNG"</dt></dl> | Algoritmo generador de números aleatorios adecuado para DSA (algoritmo de firma digital). <br /> Estándar: FIPS 186-2.<br /><strong>Windows 8:</strong> Comienza la compatibilidad con FIPS 186-3.<br /> | 
| <span id="BCRYPT_RSA_ALGORITHM"></span><span id="bcrypt_rsa_algorithm"></span><dl><dt><strong>BCRYPT_RSA_ALGORITHM</strong></dt><dt>"RSA"</dt></dl> | Algoritmo de clave pública RSA. <br /> Estándar: PKCS #1 v1.5 y v2.0.<br /> | 
| <span id="BCRYPT_RSA_SIGN_ALGORITHM"></span><span id="bcrypt_rsa_sign_algorithm"></span><dl><dt><strong>BCRYPT_RSA_SIGN_ALGORITHM</strong></dt><dt>"RSA_SIGN"</dt></dl> | Algoritmo de firma RSA. Este algoritmo no se admite actualmente. Puede usar el algoritmo de <strong>BCRYPT_RSA_ALGORITHM</strong> para realizar operaciones de firma RSA. <br /> Estándar: PKCS #1 v1.5 y v2.0.<br /> | 
| <span id="BCRYPT_SHA1_ALGORITHM"></span><span id="bcrypt_sha1_algorithm"></span><dl><dt><strong>BCRYPT_SHA1_ALGORITHM</strong></dt><dt>"SHA1"</dt></dl> | Algoritmo hash seguro de 160 bits. <br /> Estándar: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA256_ALGORITHM"></span><span id="bcrypt_sha256_algorithm"></span><dl><dt><strong>BCRYPT_SHA256_ALGORITHM</strong></dt><dt>"SHA256"</dt></dl> | Algoritmo hash seguro de 256 bits.<br /> Estándar: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA384_ALGORITHM"></span><span id="bcrypt_sha384_algorithm"></span><dl><dt><strong>BCRYPT_SHA384_ALGORITHM</strong></dt><dt>"SHA384"</dt></dl> | Algoritmo hash seguro de 384 bits. <br /> Estándar: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SHA512_ALGORITHM"></span><span id="bcrypt_sha512_algorithm"></span><dl><dt><strong>BCRYPT_SHA512_ALGORITHM</strong></dt><dt>"SHA512"</dt></dl> | Algoritmo hash seguro de 512 bits. <br /> Estándar: FIPS 180-2, FIPS 198.<br /> | 
| <span id="BCRYPT_SP800108_CTR_HMAC_ALGORITHM"></span><span id="bcrypt_sp800108_ctr_hmac_algorithm"></span><dl><dt><strong>BCRYPT_SP800108_CTR_HMAC_ALGORITHM</strong></dt><dt>L"SP800_108_CTR_HMAC"</dt></dl> | Modo de contador, algoritmo de función de derivación de claves de código de autenticación de mensajes basado en hash (HMAC). Usado por <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>las funciones BCryptKeyDerivation</strong></a> y <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_SP80056A_CONCAT_ALGORITHM"></span><span id="bcrypt_sp80056a_concat_algorithm"></span><dl><dt><strong>BCRYPT_SP80056A_CONCAT_ALGORITHM</strong></dt><dt>L"SP800_56A_CONCAT"</dt></dl> | Algoritmo de función de derivación de claves SP800-56A. Usado por <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>las funciones BCryptKeyDerivation</strong></a> y <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation.</strong></a><br /> | 
| <span id="_BCRYPT_PBKDF2_ALGORITHM"></span><span id="_bcrypt_pbkdf2_algorithm"></span><dl><dt><strong>BCRYPT_PBKDF2_ALGORITHM</strong></dt><dt>L"PBKDF2"</dt></dl> | Algoritmo de función de derivación de claves basada en contraseña 2 (PBKDF2). Usado por <a href="/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptkeyderivation"><strong>las funciones BCryptKeyDerivation</strong></a> y <a href="/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptkeyderivation"><strong>NCryptKeyDerivation.</strong></a><br /> | 
| <span id="BCRYPT_ECDSA_ALGORITHM"></span><span id="bcrypt_ecdsa_algorithm"></span><dl><dt><strong>BCRYPT_ECDSA_ALGORITHM</strong></dt><dt>"ECDSA"</dt></dl> | Algoritmo de firma digital de curva elíptica primo genérico (vea <strong>Comentarios</strong> para obtener más información). <br /> Estándar: ANSI X9.62.<br /> | 
| <span id="BCRYPT_ECDH_ALGORITHM"></span><span id="bcrypt_ecdh_algorithm"></span><dl><dt><strong>BCRYPT_ECDH_ALGORITHM</strong></dt><dt>"ECDH"</dt></dl> | Curva elíptica prime genérica Diffie-Hellman algoritmo de intercambio de claves (vea <strong>Comentarios</strong> para obtener más información). <br /> Estándar: SP800-56A.<br /> | 
| <span id="BCRYPT_XTS_AES_ALGORITHM"></span><span id="bcrypt_xts_aes_algorithm"></span><dl><dt><strong>BCRYPT_XTS_AES_ALGORITHM</strong></dt><dt>"XTS-AES"</dt></dl> | Algoritmo de cifrado simétrico estándar de cifrado avanzado en modo XTS. <br /> Estándar: SP-800-38E, IEEE Std 1619-2007.<br /><strong>Windows 10:</strong> Comienza la compatibilidad con este algoritmo.<br /> | 




## <a name="remarks"></a>Comentarios

Para usar **BCRYPT \_ ECDSA \_ ALGORITM** o **BCRYPT \_ ECDH \_ ALGORITHM,** llame a [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) con **BCRYPT \_ ECDSA \_ ALGORITHM** o **BCRYPT \_ ECDH \_ ALGORITHM** como *pszAlgId*. A [**continuación, use BCryptSetProperty para**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) establecer la propiedad **\_ BCRYPT ECC \_ CURVE \_ NAME** en un algoritmo con nombre enumerado en Curvas con nombre de CNG.

Para obtener directamente los parámetros de curva elíptica definidos por el usuario del proveedor, use [**BCryptSetProperty para**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) establecer la propiedad **\_ BCRYPT ECC \_ PARAMETERS.** Descargue el kit Windows 10 desarrollador del proveedor de servicios criptográficos [(CPDK)](https://www.microsoft.com/download/details.aspx?id=30688) para obtener más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




