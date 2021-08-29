---
description: Negociación del nivel de autenticación
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negociación del nivel de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525a7830b15451d6af54c2422128ba12dcfb56db10a8c2509298ea0ef9821e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070445"
---
# <a name="negotiation-of-authentication-level"></a>Negociación del nivel de autenticación

Tanto el cliente como el servidor deben participar en la autenticación y cada parte indica que desea realizar un determinado nivel de autenticación. Al principio de una llamada, el nivel de autenticación se negocia entre las dos partes, se elige un servicio adecuado y la llamada se autentica y continúa (con el cifrado posible, dependiendo del nivel de autenticación elegido). El nivel de autenticación negociado entre el cliente y el servidor se determina como Máximo (*Preferencia de cliente*, Preferencia del *servidor*). El efecto de esto significa que el servidor siempre puede dictar un nivel mínimo de autenticación con el que se siente cómodo; es decir, la autenticación se puede dictar administrativamente desde el servidor.

El cliente especifica que quiere realizar la autenticación en un nivel determinado como con cualquier aplicación COM. El nivel de autenticación de cliente se puede indicar de la siguiente manera:

-   Por máquina cliente, con el nivel de autenticación COM de toda la máquina establecido mediante [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) o la herramienta administrativa Servicios de componentes.
-   Por aplicación cliente administrativamente, con [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) o con la herramienta administrativa Servicios de componentes si el cliente debe ser una aplicación COM+.
-   Por proceso de cliente mediante programación, [**con CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   En cualquier momento mediante programación, con [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

La aplicación de servidor COM+ especifica un nivel de autenticación administrativamente mediante la herramienta administrativa Servicios de componentes (o a través de un script administrativo).

La negociación de la autenticación para una llamada continúa en la secuencia siguiente:

1.  El nivel de autenticación se elige como MAX(*cliente*, *servidor*).
2.  Negociación del protocolo de autenticación.
3.  El servidor autentica la identidad de cliente.
4.  Opcionalmente, el cliente autentica la identidad del servidor, según el protocolo de autenticación.
5.  Las llamadas a métodos se comunican con el nivel de autenticación elegido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> </dl>

 

 
