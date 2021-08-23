---
description: El proveedor criptográfico mejorado de DSS y Diffie-Hellman de Microsoft admite el intercambio de claves Diffie-Hellman, el hash SHA, la firma y comprobación de datos DSA (FIPS 186-2) y los algoritmos de cifrado simétrico RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Proveedor de servicios criptográficos & Diffie-Hellman DSS mejorado de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3eb3e70d90224b2d97612c5d63380171d3239e11915da4cdd8a38a0faea0b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425445"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Proveedor de servicios criptográficos & Diffie-Hellman DSS mejorado de Microsoft

El proveedor criptográfico DSS y [*Diffie-Hellman*](../secgloss/d-gly.md) mejorado de Microsoft admite el intercambio de claves *Diffie-Hellman,* el hash SHA, la firma y comprobación de datos DSA (FIPS 186-2) y los algoritmos de cifrado simétrico RC4.

<dl> Tipo de proveedor: **PROV \_ DSS \_ DH**  
Nombre del proveedor: **MS \_ ENH \_ DSS \_ DH \_ PROV**  
</dl>

Este proveedor criptográfico admite los algoritmos siguientes.

| Id. de algoritmo          | Tipo de algoritmo  | Tamaño predeterminado (bits) | Descripción                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | Cifrado de datos | 40                  | Algoritmo de cifrado de mensajes CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Cifrado de datos | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Cifrado de datos | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ DES**         | Cifrado de datos | 56                  | Estándar de cifrado de datos (DES).                                                                                                                            |
| **CALG \_ 3DES \_ 112**   | Cifrado de datos | 112                 | DES triple de dos claves.                                                                                                                                        |
| **CALG \_ 3DES**        | Cifrado de datos | 168                 | Triple DES de tres claves.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Algoritmo hash seguro 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hash            | 128                 | Resumen del mensaje 5 (MD5).                                                                                                                                    |
| **CALG \_ DSS \_ SIGN**   | Firma       | 1024                | Algoritmo de firma digital (DSA).                                                                                                                         |
| **CALG \_ DH \_ SF**      | Intercambio de claves    | 1024                | Almacene y reenvía el algoritmo de intercambio de claves [*Diffie-Hellman.*](../secgloss/d-gly.md) |
| **CALG \_ DH \_ EPHEM**   | Intercambio de claves    | 1024                | [*Algoritmo efímero Diffie-Hellman.*](../secgloss/d-gly.md)                      |



 

 

 
