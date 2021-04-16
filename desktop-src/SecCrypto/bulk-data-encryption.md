---
description: Se genera una clave de cifrado masivo mediante el hash de una de las claves MAC con CryptHashSessionKey junto con el contenido del mensaje y otros datos. El mensaje se cifra/descifra con una de las claves de cifrado masivo de la manera habitual.
ms.assetid: 08174502-3ff1-4c1c-bcd0-46fd85882305
title: Cifrado de datos masivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ecfb55c162e5aa576d8baa3d0ccbc45e9588c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669819"
---
# <a name="bulk-data-encryption"></a>Cifrado de datos masivo

Se genera una [*clave de cifrado masivo*](../secgloss/b-gly.md) mediante el [*hash*](../secgloss/h-gly.md) de una de las claves Mac con [**CryptHashSessionKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey) junto con el contenido del mensaje y otros datos. El mensaje se cifra/descifra con una de las claves de cifrado masivo de la manera habitual.

Cuando se usa un [*cifrado de bloques*](../secgloss/b-gly.md), el motor de protocolo [*Schannel*](../secgloss/s-gly.md) realiza todo el [*relleno*](../secgloss/p-gly.md)de *cifrado de bloques* necesario. Cuando se llama a [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) y [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) , la marca final siempre es **false** y la longitud de los datos es un múltiplo de longitudes de bloque completas.

> [!Note]  
> El CSP nunca debe almacenar en búfer los datos internamente. Una vez cifrados o descifrados los datos, el tamaño del [*texto*](../secgloss/p-gly.md) no cifrado debe coincidir exactamente con el tamaño del [*texto cifrado*](../secgloss/c-gly.md).

 

 

 
