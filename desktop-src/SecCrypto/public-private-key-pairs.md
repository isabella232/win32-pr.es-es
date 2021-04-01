---
description: Las claves asimétricas, también conocidas como pares de claves pública y privada, se usan para el cifrado asimétrico. El cifrado asimétrico se usa principalmente para cifrar y descifrar las claves de sesión y las firmas digitales. El cifrado asimétrico utiliza algoritmos de cifrado de clave pública.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Claves asimétricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c475b1d0260bd20495d28ab542ca18c0d1cefa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817862"
---
# <a name="asymmetric-keys"></a>Claves asimétricas

[*Las claves asimétricas*](../secgloss/a-gly.md), también conocidas como [*pares de claves pública y privada*](../secgloss/p-gly.md), se usan para el cifrado asimétrico. El cifrado asimétrico se usa principalmente para cifrar y descifrar [*las claves de sesión y las*](../secgloss/s-gly.md) [*firmas digitales*](../secgloss/d-gly.md). El cifrado asimétrico utiliza algoritmos de [*cifrado de clave pública*](../secgloss/p-gly.md) .

Los algoritmos de clave pública utilizan dos claves diferentes: una [*clave pública*](../secgloss/p-gly.md) y una [*clave privada*](../secgloss/p-gly.md). El miembro de clave privada del par debe mantenerse privado y seguro. La clave pública, sin embargo, se puede distribuir a cualquier persona que la solicite. La clave pública de un par de claves suele distribuirse por medio de un [*certificado digital*](../secgloss/c-gly.md). Cuando se usa una clave de un par de claves para cifrar un mensaje, se requiere la otra clave de ese par para descifrar el mensaje. Por lo tanto, si se utiliza la clave pública del usuario a para cifrar los datos, solo el usuario A (o alguien que tenga acceso a la clave privada de un usuario) puede descifrar los datos. Si se utiliza la clave privada de usuario a para cifrar una parte de los datos, solo la clave pública del usuario a descifrará los datos, lo que indicará que el usuario A (o alguien con acceso a la clave privada de usuario a) lo ha cifrado.

Si se utiliza la clave privada para firmar un mensaje, se debe usar la clave pública de ese par para validar la firma. Por ejemplo, si Alicia desea enviar a alguien un mensaje firmado digitalmente, firmaría el mensaje con su clave privada y la otra persona podría comprobar su firma con su clave pública. Dado que supuestamente solo Alicia tiene acceso a su clave privada, el hecho de que la firma se pueda comprobar con la clave pública de Alice indica que Alice creó la firma.

Desafortunadamente, los algoritmos de clave pública son muy lentos, aproximadamente 1.000 veces más lentos que los algoritmos simétricos. No es práctico usarlas para cifrar grandes cantidades de datos. En la práctica, los algoritmos de clave pública se utilizan para cifrar [*las claves de sesión*](../secgloss/s-gly.md). Los [*algoritmos simétricos*](../secgloss/s-gly.md) se utilizan para cifrar y descifrar la mayoría de los datos.

Del mismo modo, dado que la firma de un mensaje, en efecto, cifra el mensaje, no es práctico usar algoritmos de firma de clave pública para firmar mensajes de gran tamaño. En su lugar, se crea un [*hash*](../secgloss/h-gly.md) de longitud fija del mensaje y el valor hash está firmado. Para obtener más información, consulte [hashes y firmas digitales](hashes-and-digital-signatures.md).

Generalmente, cada usuario tiene dos [*pares de claves pública y privada*](../secgloss/p-gly.md). Se usa un par de claves para cifrar las claves de sesión y el otro para crear [*firmas digitales*](../secgloss/d-gly.md). Estos se conocen como el [*par de claves de intercambio de claves*](../secgloss/k-gly.md) y el [*par de claves de firma*](../secgloss/s-gly.md), respectivamente.

Tenga en cuenta que, aunque los contenedores de claves creados por la mayoría de los [*proveedores de servicios de cifrado*](../secgloss/c-gly.md) (CSP) contienen dos pares de claves, esto no es necesario. Algunos CSP no almacenan ningún [*par de claves*](../secgloss/k-gly.md) mientras otros CSP almacenan más de dos pares.

Todas las claves de CryptoAPI se almacenan en CSP. Los CSP también son responsables de crear las claves, destruirlas y usarlas para realizar diversas operaciones criptográficas. Exportar claves fuera del CSP para que se puedan enviar a otros usuarios se describe en almacenamiento de [claves criptográficas y Exchange](cryptographic-key-storage-and-exchange.md).

 

 
