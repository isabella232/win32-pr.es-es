---
description: El protocolo Kerberos define cómo interactúan los clientes con un servicio de autenticación de red \[ Platform Software Development Kit (SDK). \]
ms.assetid: e7870e72-1386-4818-bf6f-73430ae942a8
title: Microsoft Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03787bcc65959838ea02c49958d9ca4e0405649
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173470"
---
# <a name="microsoft-kerberos"></a>Microsoft Kerberos

El [*protocolo Kerberos define*](../secgloss/k-gly.md) cómo interactúan los clientes con un servicio de autenticación de red. Los clientes obtienen vales del Centro de distribución de claves Kerberos (KDC) y presentan estos vales a los servidores cuando se establecen las conexiones. Los vales de Kerberos representan las credenciales de red del [*cliente.*](../secgloss/c-gly.md)

La información de esta sección proporciona información teórica sobre el uso del protocolo Kerberos en un proceso de autenticación. Se trata de información en segundo plano que puede agregar a la comprensión de un desarrollador de lo que sucede en segundo plano en un proceso SSPI que usa el protocolo Kerberos versión 5.

El protocolo de autenticación Kerberos proporciona un mecanismo para la autenticación mutua entre entidades antes de establecer una conexión de red segura. En esta documentación, las dos entidades se denominan cliente y servidor, aunque se pueden realizar conexiones de red seguras entre servidores. Tanto el cliente como el servidor también se pueden denominar entidades [*de seguridad.*](../secgloss/s-gly.md)

El protocolo Kerberos supone que las transacciones entre clientes y servidores tienen lugar en una red abierta donde la mayoría de los clientes y muchos servidores no están físicamente seguros, y los paquetes que viajan a lo largo de la red se pueden supervisar y modificar a su ansía. El entorno asumido es como el de Internet de hoy en día, donde un atacante puede plantearse fácilmente como un cliente o un servidor, y puede escuchar o alterar fácilmente las comunicaciones entre clientes y servidores legítimos.

En esta sección se proporciona la siguiente información:

-   [Conceptos básicos de autenticación](basic-authentication-concepts.md)
-   [Subprotocolos de Kerberos](kerberos-subprotocols.md)
-   [Modelo kerberos](kerberos-components.md)
-   [Interoperabilidad de SSPI/Kerberos con GSSAPI](sspi-kerberos-interoperability-with-gssapi.md)

La aplicación no debe acceder directamente al paquete [*de seguridad de*](../secgloss/s-gly.md) Kerberos; en su lugar, debe usar el [*paquete de seguridad Negotiate.*](../secgloss/n-gly.md) Negotiate permite que la aplicación aproveche los protocolos de seguridad más avanzados si son compatibles con los sistemas [*implicados*](../secgloss/s-gly.md) en la autenticación. Actualmente, el paquete de seguridad Negotiate selecciona entre [*Kerberos*](../secgloss/k-gly.md) y NTLM. Negotiate selecciona Kerberos a menos que uno de los sistemas implicados en la autenticación no pueda usarlo.

 

 
