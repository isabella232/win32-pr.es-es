---
description: Un hash de un texto u otra cadena de bytes es un valor de longitud fija, estadísticamente único y asociado.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hashes de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913045"
---
# <a name="data-hashes"></a>Hashes de datos

Un [*hash*](../secgloss/h-gly.md) de un texto u otra cadena de bytes es un valor de longitud fija, estadísticamente único y asociado. En algunos documentos, un *hash* de un texto también se denomina síntesis; sin embargo, en esta documentación se usará siempre el término hash. Las funciones CryptoAPI proporcionan un medio para crear un hash para cualquier texto u otra cadena de bytes. Ese hash, a continuación, se puede usar como identificador único de sus datos asociados.

Para garantizar la [*integridad*](../secgloss/i-gly.md) de un texto, se puede enviar un [*hash*](../secgloss/h-gly.md) de un texto para acompañar el texto. A continuación, el receptor puede calcular un hash en los datos recibidos y comparar el hash calculado con el hash recibido. Si los dos coinciden, los datos recibidos deben ser los mismos que los datos de los que se creó el hash recibido.

Para obtener un valor hash, cree un objeto hash mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Este objeto acumulará los datos que se van a comprobar. A continuación, los datos se agregan al objeto hash con la función [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .

Después de agregar el último bloque de datos al hash, se usa la función [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) para obtener el valor hash de los datos.

Se proporciona una mejor seguridad al destruir el objeto hash con [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) en cuanto se obtiene el valor hash.

 

 
