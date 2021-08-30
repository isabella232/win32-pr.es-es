---
description: Explica cómo crear un \_ hash DE CALG SSL3 \_ SHAMD5.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Creación de un hash CALG_SSL3_SHAMD5 datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567d7fa640c836790265214a7ae99e0ce1a70d925dd0d6c05b3deb1f6bcc81ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876674"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a>Creación de un \_ hash CALG SSL3 \_ SHAMD5

**Para crear un \_ hash CALG SSL3 \_ SHAMD5**

1.  Mediante la metodología estándar de CryptoAPI, cree un hash MD5 y [*SHA*](../secgloss/s-gly.md) [*de*](../secgloss/h-gly.md) los datos de destino.
2.  Concatene los dos hashes, con el valor MD5 más a la izquierda y el valor SHA más a la derecha. Esto da como resultado un valor de 36 bytes (16 bytes + 20 bytes).
3.  Obtenga un identificador para un [*objeto hash*](../secgloss/h-gly.md) mediante una llamada a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con CALG \_ SSL3 SHAMD5 pasado en el \_ parámetro *Algid.*
4.  Establezca el valor hash con una llamada a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam). Los valores hash concatenados se pasan como **BYTE** en el parámetro pbData y el valor HASHVAL de HP debe pasarse \* en el parámetro  \_ *dwParam.* Se producirá un error al llamar a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mediante el identificador devuelto por [**CryptCreateHash en**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) el paso 3.
5.  Llame [**a CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) para generar la firma.
6.  Llame [**a CryptDestroyHash para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) destruir el objeto hash.

 

 
