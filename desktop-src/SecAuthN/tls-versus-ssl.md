---
description: TLS es un estándar estrechamente relacionado con SSL 3.0 y a veces se conoce como &\# 0034; SSL 3.1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS frente a SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ade696a819f6528ade49ea843340a5b8b43af5427acf6616aeafd1871512c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915735"
---
# <a name="tls-vs-ssl"></a>TLS frente a SSL

TLS es un estándar estrechamente relacionado con SSL 3.0 y a veces se conoce como "SSL 3.1". TLS sustituye a SSL 2.0 y debe usarse en el nuevo desarrollo. A partir Windows 10 versión 1607 y Windows Server 2016, SSL 2.0 se ha quitado y ya no se admite.

Las aplicaciones que requieren un alto nivel de interoperabilidad deben admitir SSL 3.0 y TLS. Debido a las similitudes entre estos dos protocolos, los detalles de SSL no se incluyen en esta documentación, excepto cuando difieren de TLS. Lo siguiente es de [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):

"Las diferencias entre este protocolo y SSL 3.0 no son drásticas, pero son lo suficientemente significativas como para que TLS 1.0 y SSL 3.0 no interoperan (aunque TLS 1.0 incorpora un mecanismo por el que una implementación de TLS puede volver a SSL 3.0)."

 

 



