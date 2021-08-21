---
description: Un hash de un texto u otra cadena de bytes es un valor de longitud fija asociado, estadísticamente único.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hashes de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a998c2172f6bd3b48bb3cdc94f1ed2207384606950dd9d6e8b6f3152149eaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767773"
---
# <a name="data-hashes"></a>Hashes de datos

Un [*hash*](../secgloss/h-gly.md) de un texto u otra cadena de bytes es un valor de longitud fija asociado, estadísticamente único. En algunos documentos, un *hash* de un texto también se denomina resumen; sin embargo, en esta documentación siempre se usará el término hash. Las funciones cryptoAPI proporcionan un medio para crear un hash para cualquier texto u otra cadena de bytes. Ese hash, a continuación, se puede usar como identificador único de sus datos asociados.

Para garantizar la [*integridad*](../secgloss/i-gly.md) de un texto, se puede enviar [*un hash*](../secgloss/h-gly.md) de un texto para que lo acompaña. A continuación, el receptor puede calcular un hash en los datos recibidos y comparar el hash calculado con el hash recibido. Si las dos coinciden, los datos recibidos deben ser los mismos que los datos a partir de los cuales se creó el hash recibido.

Para obtener un valor hash, cree un objeto hash mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash). Este objeto acumulará los datos que se van a comprobar. A continuación, los datos se agregan al objeto hash con la [**función CryptHashData.**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata)

Después de agregar el último bloque de datos al hash, se usa la función [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) para obtener el valor hash de los datos.

Se proporciona una mayor seguridad al destruir el objeto hash con [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) en cuanto se ha obtenido el valor hash.

 

 
