---
description: Una clave de cifrado masivo se genera mediante el algoritmo hash de una de las claves MAC mediante CryptHashSessionKey junto con el contenido del mensaje y otros datos. El mensaje se cifra o descifra con una de las claves de cifrado masivo de la manera habitual.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Cifrado masivo de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb50e156a2e689d01afba2cb383a08dad0b005377e2e745e013adde4b685d882
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879485"
---
# <a name="bulk-data-encryption"></a>Cifrado masivo de datos

Una [*clave de cifrado masivo*](../secgloss/b-gly.md) se genera mediante el algoritmo [*hash*](../secgloss/h-gly.md) de una de las claves MAC mediante [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) junto con el contenido del mensaje y otros datos. El mensaje se cifra o descifra con una de las claves de cifrado masivo de la manera habitual.

Cuando se usa un [*cifrado de bloques,*](../secgloss/b-gly.md)el motor del protocolo [*Schannel*](../secgloss/s-gly.md) realiza todo el relleno de *cifrado de bloques* [*necesario.*](../secgloss/p-gly.md) Cuando se llama a [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) y [**CryptDecrypt,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) la marca Final siempre es **FALSE** y la longitud de los datos es un múltiplo de longitudes de bloques completos.

> [!Note]  
> El CSP nunca debe almacenar en búfer los datos internamente. Después de cifrar (o descifrar) los datos, el tamaño del texto no cifrado siempre debe coincidir exactamente con el tamaño del [*texto cifrado*](../secgloss/c-gly.md). [](../secgloss/p-gly.md)

 

 

 
