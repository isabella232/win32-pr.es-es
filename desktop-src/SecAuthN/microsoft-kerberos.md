---
description: El protocolo Kerberos define el modo en que los clientes interactúan con un \[ Kit de desarrollo de software (SDK) de plataforma de servicio de autenticación de red \] .
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001088"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

El [*protocolo Kerberos*](../secgloss/k-gly.md) define el modo en que los clientes interactúan con un servicio de autenticación de red. Los clientes obtienen vales del Centro de distribución de claves Kerberos (KDC) y presentan estos vales a los servidores cuando se establecen las conexiones. Los vales Kerberos representan las [*credenciales*](../secgloss/c-gly.md)de red del cliente.

En esta sección se proporciona información general sobre el uso del protocolo Kerberos en un proceso de autenticación. Se trata de información general que puede Agregar a una experiencia del desarrollador sobre lo que ocurre en segundo plano en un proceso SSPI que usa el protocolo Kerberos versión 5.

El protocolo de autenticación Kerberos proporciona un mecanismo para la autenticación mutua entre entidades antes de que se establezca una conexión de red segura. En esta documentación, las dos entidades reciben el nombre de cliente y el servidor, aunque se puedan establecer conexiones de red seguras entre servidores. Tanto el cliente como el servidor también se pueden denominar [*entidades de seguridad*](../secgloss/s-gly.md).

El protocolo Kerberos presupone que las transacciones entre clientes y servidores tienen lugar en una red abierta en la que la mayoría de los clientes y muchos servidores no están físicamente protegidos, y los paquetes que viajan a lo largo de la red se pueden supervisar y modificar a su vez. El entorno asumido es como Internet de hoy en el que un atacante puede suponer fácilmente como cliente o como servidor, y puede espiar o manipular con facilidad las comunicaciones entre los clientes y servidores legítimos.

En esta sección se proporciona la siguiente información:

-   [Conceptos básicos de autenticación](basic-authentication-concepts.md)
-   [Subprotocolos Kerberos](kerberos-subprotocols.md)
-   [Modelo de Kerberos](kerberos-components.md)
-   [Interoperabilidad de SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

La aplicación no debe tener acceso directamente al [*paquete de seguridad*](../secgloss/s-gly.md) de Kerberos. en su lugar, debe usar el paquete de seguridad [*Negotiate*](../secgloss/n-gly.md) . Negotiate permite que la aplicación aproveche los [*protocolos de seguridad*](../secgloss/s-gly.md) más avanzados si son compatibles con los sistemas implicados en la autenticación. Actualmente, el paquete de seguridad Negotiate selecciona entre [*Kerberos*](../secgloss/k-gly.md) y NTLM. Negotiate selecciona Kerberos a menos que uno de los sistemas implicados en la autenticación no pueda utilizarlo.

 

 
