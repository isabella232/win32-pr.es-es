---
description: Negociación del nivel de autenticación
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Negociación del nivel de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705389"
---
# <a name="negotiation-of-authentication-level"></a>Negociación del nivel de autenticación

Tanto el cliente como el servidor deben participar en la autenticación y cada parte indica que desea realizar un cierto nivel de autenticación. Al principio de una llamada, el nivel de autenticación se negocia entre las dos partes, se elige un servicio adecuado y la llamada se autentica y continúa (con posible cifrado, según el nivel de autenticación elegido). El nivel de autenticación negociado entre el cliente y el servidor se determina como máximo (*preferencia de cliente*, *preferencia de servidor*). El efecto de esto significa que el servidor siempre puede dictar un nivel mínimo de autenticación con el que se sienta cómodo; es decir, la autenticación se puede dictar administrativamente desde el servidor.

El cliente especifica que desea realizar la autenticación en cierto nivel como con cualquier aplicación COM. El nivel de autenticación del cliente se puede indicar de la siguiente manera:

-   Por equipo cliente, con el nivel de autenticación COM en todo el equipo establecido mediante [dcomcnfg](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) o la herramienta administrativa Servicios de componentes.
-   Por aplicación cliente administrativamente, con [dcomcnfg](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) o con la herramienta administrativa Servicios de componentes si el cliente debe ser una aplicación com+.
-   Por proceso de cliente mediante programación, con [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   En cualquier momento mediante programación, usando [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

La aplicación de servidor COM+ especifica un nivel de autenticación administrativa mediante la herramienta administrativa Servicios de componentes (o a través de un script administrativo).

La negociación de la autenticación para una llamada continúa en la secuencia siguiente:

1.  El nivel de autenticación se elige como MAX (*cliente*, *servidor*).
2.  Negociación del Protocolo de autenticación.
3.  El servidor autentica la identidad del cliente.
4.  Opcionalmente, el cliente autentica la identidad del servidor, según el protocolo de autenticación.
5.  Las llamadas a métodos se comunican con el nivel de autenticación elegido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Autenticación de cliente](client-authentication.md)
</dt> </dl>

 

 
