---
description: Explica cómo crear un hash CALG \_ de \_ SHAMD5 SSL3.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Crear un hash de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667716"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Creación de un \_ hash CALG de \_ SHAMD5 SSL3

**Para crear un \_ \_ hash SHAMD5 de CALG SSL3**

1.  Mediante la metodología estándar de CryptoAPI, cree un hash MD5 y un [*algoritmo hash*](../secgloss/h-gly.md) [*Sha*](../secgloss/s-gly.md) de los datos de destino.
2.  Concatene los dos hashes, con el valor MD5 a la izquierda y el valor SHA a la derecha. Esto da como resultado un valor de 36 byte (16 bytes + 20 bytes).
3.  Obtener un identificador de un [*objeto hash*](../secgloss/h-gly.md) llamando a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con CALG \_ SSL3 \_ SHAMD5 pasado en el parámetro *algid* .
4.  Establezca el valor hash con una llamada a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam). Los valores hash concatenados se pasan como **bytes** \* en el parámetro *pbData* y el \_ valor HASHVAL de HP se debe pasar en el parámetro *dwParam* . Se producirá un error al llamar a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mediante el identificador devuelto por [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) en el paso 3.
5.  Llame a [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) para generar la firma.
6.  Llame a [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) para destruir el objeto hash.

 

 
