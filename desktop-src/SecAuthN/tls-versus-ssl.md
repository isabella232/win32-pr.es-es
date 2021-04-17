---
description: TLS es un estándar estrechamente relacionado con SSL 3,0 y a veces se conoce como &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS frente a SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668246"
---
# <a name="tls-vs-ssl"></a>TLS frente a SSL

TLS es un estándar estrechamente relacionado con SSL 3,0 y a veces se denomina "SSL 3,1". TLS reemplaza a SSL 2,0 y debe usarse en el nuevo desarrollo. A partir de Windows 10, versión 1607 y Windows Server 2016, se ha quitado SSL 2,0 y ya no se admite.

Las aplicaciones que requieren un alto nivel de interoperabilidad deben admitir SSL 3,0 y TLS. Debido a las similitudes entre estos dos protocolos, los detalles de SSL no se incluyen en esta documentación, excepto cuando difieren de TLS. A continuación se indican los [documentos RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):

"Las diferencias entre este protocolo y SSL 3,0 no son espectaculares, pero son lo suficientemente importantes como para que TLS 1,0 y SSL 3,0 no interoperen (aunque TLS 1,0 incorpora un mecanismo por el que una implementación de TLS puede hacer una copia de seguridad en SSL 3,0)".

 

 



