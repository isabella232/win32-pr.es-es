---
description: Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos admite Diffie-Hellman intercambio de claves, hash SHA, firma y comprobación de datos DSA (FIPS 186-2) y algoritmos de cifrado simétrico RC4.
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Proveedor de servicios criptográficos de Microsoft Enhanced DSS & Diffie-Hellman
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c42b4e504c1e5d4cb8ccfea7405580e37362f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686861"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Proveedor de servicios criptográficos de Microsoft Enhanced DSS & Diffie-Hellman

El proveedor de servicios criptográficos Microsoft Enhanced DSS y [*Diffie-Hellman*](../secgloss/d-gly.md) admite el intercambio *de claves Diffie-Hellman* , el algoritmo hash Sha, la firma y comprobación de datos DSA (FIPS 186-2) y los algoritmos de cifrado simétrico RC4.

<dl> Tipo de proveedor: **Prov \_ DSS \_ DH**  
Nombre del proveedor: **MS \_ Enh \_ DSS \_ DH \_ Prov**  
</dl>

Este proveedor de servicios criptográficos admite los siguientes algoritmos.

| IDENTIFICADOR de algoritmo          | Tipo de algoritmo  | Tamaño predeterminado (bits) | Descripción                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ clave MEK** | Cifrado de datos | 40                  | Algoritmo de cifrado de mensajes de CYLINK.                                                                                                                       |
| **CALG \_ RC2**         | Cifrado de datos | 128                 | RSA RC2.                                                                                                                                                   |
| **CALG \_ RC4**         | Cifrado de datos | 128                 | RSA RC4.                                                                                                                                                   |
| **CALG \_ des**         | Cifrado de datos | 56                  | Estándar de cifrado de datos (DES).                                                                                                                            |
| **CALG \_ 3des \_ 112**   | Cifrado de datos | 112                 | Triple DES de clave.                                                                                                                                        |
| **CALG \_ 3DES**        | Cifrado de datos | 168                 | Triple DES de clave.                                                                                                                                      |
| **CALG \_ SHA1**        | Hash            | 160                 | Algoritmo hash seguro 1 (SHA-1).                                                                                                                           |
| **CALG \_ MD5**         | Hash            | 128                 | Síntesis del mensaje 5 (MD5).                                                                                                                                    |
| **\_firma DSS de CALG \_**   | Firma       | 1024                | Algoritmo de firma digital (DSA).                                                                                                                         |
| **CALG \_ DH \_ SF**      | Intercambio de claves    | 1024                | Almacenar y reenviar [*el algoritmo de intercambio de claves Diffie-Hellman*](../secgloss/d-gly.md) . |
| **CALG \_ DH \_ EPHEM**   | Intercambio de claves    | 1024                | Algoritmo efímero [*Diffie-Hellman*](../secgloss/d-gly.md) .                      |



 

 

 
