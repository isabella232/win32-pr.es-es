---
description: La API CNG proporciona un conjunto de funciones que realizan operaciones criptográficas básicas, como la creación de hashes o el cifrado y descifrado de datos. Para obtener más información sobre estas funciones, vea funciones primitivas criptográficas de CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitivos criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539846"
---
# <a name="cryptographic-primitives"></a>Primitivos criptográficos

La API CNG proporciona un conjunto de funciones que realizan operaciones criptográficas básicas, como la creación de hashes o el cifrado y descifrado de datos. Para obtener más información sobre estas funciones, vea [funciones primitivas criptográficas de CNG](cng-cryptographic-primitive-functions.md).

CNG implementa numerosos algoritmos criptográficos. Cada algoritmo o clase de algoritmos expone su propia API primitiva. Se pueden instalar varias implementaciones de un algoritmo determinado al mismo tiempo; sin embargo, solo una implementación será el valor predeterminado en un momento dado.

Cada clase de algoritmo en CNG se representa mediante un enrutador primitivo. Las aplicaciones que usan las funciones primitivas de CNG se vincularán al archivo binario del enrutador Bcrypt.dll en modo de usuario o Ksecdd.sys en modo kernel antes de llamar a las funciones. Varias rutinas de enrutador administran todos los primitivos de algoritmo. Estos enrutadores realizan el seguimiento de cada implementación de algoritmo instalada en el sistema y enrutan cada llamada de función al módulo de proveedor primitivo adecuado.

CNG proporciona primitivas para las clases de algoritmos siguientes.



| Clase Algorithm                                                                                                                                                  | Descripción                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Generador de números aleatorios<br/> | Generación de números aleatorios (RNG) conectable.<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Algoritmos que se usan para el hash, como SHA1 y SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Cifrado simétrico<br/>             | Algoritmos usados para el cifrado simétrico, como AES, 3DES y RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Cifrado asimétrico<br/>         | Algoritmos asimétricos (clave pública) que admiten el cifrado, como RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signatura<br/>                                                         | Algoritmos de firma como DSA y ECDSA. Esta clase también se puede usar con RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Acuerdo secreto<br/>                             | Algoritmos de acuerdo secreto como Diffie-Hellman (DH) y Diffie-Hellman de curva elíptica (ECDH).<br/> |



 

En la ilustración siguiente se muestra el diseño y la función de las primitivas criptográficas de CNG.

![diseño y función de primitivas criptográficas CNG](images/ssdk-cng1c.png)

El archivo de encabezado bcrypt. h define la constante del **\_ \_ proveedor primitivo de MS** como "proveedor primitivo de Microsoft". Para usar el proveedor primitivo de Microsoft, pase este valor a [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




