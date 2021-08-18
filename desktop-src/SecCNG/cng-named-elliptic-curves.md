---
description: A partir Windows 10, CNG proporciona compatibilidad con las siguientes curvas elípticas con nombre (ANSI X9.62, X9.63, FIPS 186-2).
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: Curvas elípticas con nombre de CNG (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691f1211b56abc41d622d20857653723be37681014a9bf72b91c1384c8f4b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908256"
---
# <a name="cng-named-elliptic-curves"></a>Curvas elípticas con nombre CNG

A partir Windows 10, CNG proporciona compatibilidad con las siguientes curvas elípticas con nombre (ANSI X9.62, X9.63, FIPS 186-2).

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ CURVE \_ 25519**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------|
| Nombre              | curve25519                                                  |
| Estándar          | [Curva 25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| Tamaño de la clave (bits)   | 255                                                         |
| Compatible con TLS       |                                                             |
| Identificador de objeto | Ninguno                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP160r1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 160                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP160T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP160t1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 160                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP192r1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 192                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP192T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP192t1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 192                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP224r1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 224                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP224T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP224t1                                                                                                   |
| Estándar          | [Generación de curvas y curvas estándar de ECC Brainpool](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 224                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP256r1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 256                                                                                                               |
| Compatible con TLS       | Sí                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP256T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP256t1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 256                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP320R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP320r1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 320                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP320t1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 320                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP384r1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 384                                                                                                               |
| Compatible con TLS       | Sí                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP384T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP384t1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 384                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP512r1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 512                                                                                                               |
| Compatible con TLS       | Sí                                                                                                               |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ CURVE \_ BRAINPOOLP512T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| Nombre              | brainpoolP512t1                                                                                                   |
| Estándar          | [ECC Brainpool Standard Curves and Curve Generation](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| Tamaño de la clave (bits)   | 512                                                                                                               |
| Compatible con TLS       | No                                                                                                                |
| Identificador de objeto | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ ECC \_ CURVE \_ EC192WAPI**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|----------------------------------------------------------------|
| Nombre              | ec192wapi                                                      |
| Estándar          | Estándar nacional chino para LAN inalámbricas (GB 15629.11-2003) |
| Tamaño de la clave (bits)   | 192                                                            |
| Compatible con TLS       | No                                                             |
| Identificador de objeto | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP192**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | nistP192                                                                                                                     |
| Estándar          | [Curvas elípticas recomendadas para uso del Gobierno Federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamaño de la clave (bits)   | 192                                                                                                                          |
| Compatible con TLS       | Sí                                                                                                                          |
| Identificador de objeto | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP224**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | nistP224                                                                                                                     |
| Estándar          | [Curvas elípticas recomendadas para uso del Gobierno Federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamaño de la clave (bits)   | 224                                                                                                                          |
| Compatible con TLS       | Sí                                                                                                                          |
| Identificador de objeto | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP256**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | nistP256                                                                                                                     |
| Estándar          | [Curvas elípticas recomendadas para uso del Gobierno Federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamaño de la clave (bits)   | 256                                                                                                                          |
| Compatible con TLS       | Sí                                                                                                                          |
| Identificador de objeto | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP384**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | nistP384                                                                                                                     |
| Estándar          | [Curvas elípticas recomendadas para uso del Gobierno Federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamaño de la clave (bits)   | 384                                                                                                                          |
| Compatible con TLS       | Sí                                                                                                                          |
| Identificador de objeto | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ CURVE \_ NISTP521**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | nistP521                                                                                                                     |
| Estándar          | [Curvas elípticas recomendadas para uso del Gobierno Federal](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| Tamaño de la clave (bits)   | 521                                                                                                                          |
| Compatible con TLS       | Sí                                                                                                                          |
| Identificador de objeto | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ ECC \_ CURVE \_ NUMSP256T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | numsP256t1                                                                                                                              |
| Estándar          | [Especificación de la selección de curva y los parámetros de curva admitidos en MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamaño de la clave (bits)   | 256                                                                                                                                     |
| Compatible con TLS       | No                                                                                                                                      |
| Identificador de objeto | Ninguno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ ECC \_ CURVE \_ NUMSP384T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | numsP384t1                                                                                                                              |
| Estándar          | [Especificación de la selección de curva y los parámetros de curva admitidos en MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamaño de la clave (bits)   | 384                                                                                                                                     |
| Compatible con TLS       | No                                                                                                                                      |
| Identificador de objeto | Ninguno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ CURVE \_ NUMSP512T1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Nombre              | numsP512t1                                                                                                                              |
| Estándar          | [Especificación de la selección de curva y los parámetros de curva admitidos en MSR ECCLib](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| Tamaño de la clave (bits)   | 512                                                                                                                                     |
| Compatible con TLS       | No                                                                                                                                      |
| Identificador de objeto | Ninguno                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ CURVA ECC \_ \_ SECP160K1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP160k1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 160                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ CURVA ECC \_ \_ SECP160R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP160r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 160                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ CURVA ECC \_ \_ SECP160R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP160r2                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 160                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP192K1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP192k1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 192                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ CURVA ECC \_ \_ SECP192R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP192r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 192                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP224K1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP224k1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 224                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP224R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP224r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 224                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP256K1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP256k1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 256                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP256R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP256r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 256                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ CURVA ECC \_ \_ SECP384R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP384r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 384                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ CURVE \_ SECP521R1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------|
| Nombre              | secP521r1                                                                       |
| Estándar          | [Parámetros de dominio de curva elíptica recomendados](https://www.secg.org/sec2-v2.pdf) |
| Tamaño de la clave (bits)   | 521                                                                             |
| Compatible con TLS       | Sí                                                                             |
| Identificador de objeto | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ CURVE \_ WTLS12**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|--------------|
| Nombre              | wtls12       |
| Estándar          | Wtls         |
| Tamaño de la clave (bits)   | 224          |
| Compatible con TLS       | No           |
| Identificador de objeto | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ CURVE \_ WTLS7**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|--------------|
| Nombre              | wtls7        |
| Estándar          | Wtls         |
| Tamaño de la clave (bits)   | 160          |
| Compatible con TLS       | No           |
| Identificador de objeto | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ CURVA ECC \_ \_ WTLS9**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------|
| Nombre              | wtls9         |
| Estándar          | Wtls          |
| Tamaño de la clave (bits)   | 160           |
| Compatible con TLS       | No            |
| Identificador de objeto | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P192v1          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 192                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P192V2**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P192v2          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 192                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P192V3**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P192v3          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 192                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P239v1          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 239                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V2**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P239v2          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 239                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ CURVA ECC \_ \_ X962P239V3**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P239v3          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 239                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ CURVE \_ X962P256V1**</dt> <dd> <dl> <dt> 

| Requisito | Value |
|-------------------|---------------------|
| Nombre              | x962P256v1          |
| Estándar          | ANSI X9.62          |
| Tamaño de la clave (bits)   | 256                 |
| Compatible con TLS       | No                  |
| Identificador de objeto | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Para usar una curva con nombre, llame a [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) mediante **BCRYPT \_ ECDSA \_ ALGORITHM** o **BCRYPT \_ ECDH \_ ALGORITHM** como identificador del algoritmo. A continuación, llame a [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) y establezca la propiedad **\_ BCRYPT ECC \_ CURVE \_ NAME** en una de las curvas anteriores o en cualquier curva con nombre registrada en el equipo, como se muestra en el `certutil -displayEccCurve` comando .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




