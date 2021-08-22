---
description: Un conjunto de cifrado es un conjunto de algoritmos criptográficos.
ms.assetid: 513e5e73-12f8-4b64-86e4-179518c3582d
title: Conjuntos de cifrado en TLS/SSL (Schannel SSP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 590012b4a1ef0c84b8216fd970d1e60c8ed449294ec110dc566e7c3679b7bb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141228"
---
# <a name="cipher-suites-in-tlsssl-schannel-ssp"></a>Conjuntos de cifrado en TLS/SSL (Schannel SSP)

Un conjunto de cifrado es un conjunto de algoritmos criptográficos. La implementación de SSP de schannel de los protocolos TLS/SSL usa algoritmos de un conjunto de cifrado para crear claves y cifrar información. Un conjunto de cifrado especifica un algoritmo para cada una de las siguientes tareas:

-   Intercambio de claves
-   Cifrado masivo
-   Autenticación de mensajes

[*Los algoritmos de intercambio*](/windows/desktop/SecGloss/k-gly) de claves protegen la información necesaria para crear claves compartidas. Estos algoritmos son [*asimétricos (algoritmos de clave pública)*](/windows/desktop/SecGloss/p-gly)y tienen un buen rendimiento para cantidades relativamente pequeñas de datos.

Los algoritmos de cifrado masivo cifran los mensajes intercambiados entre clientes y servidores. Estos algoritmos son [*simétricos*](/windows/desktop/SecGloss/s-gly) y tienen un buen rendimiento para grandes cantidades de datos.

[Los algoritmos de](message-authentication-codes-in-schannel.md) autenticación de mensajes [*generan hashes*](/windows/desktop/SecGloss/h-gly) de mensajes y firmas que garantizan la [*integridad*](/windows/desktop/SecGloss/i-gly) de un mensaje.

Los desarrolladores especifican estos elementos mediante [**tipos de datos DE \_ ALG ID.**](/windows/desktop/SecCrypto/alg-id) Para obtener más información, vea [Especificar cifrados Schannel y puntos fuertes de cifrado.](specifying-schannel-ciphers-and-cipher-strengths.md)

En versiones anteriores de Windows, los conjuntos de cifrado TLS y las curvas elípticas se configuraban mediante una sola cadena:

![Diagrama que muestra una sola cadena para un conjunto de cifrado.](images/tls-cipher-suite.png)

Las distintas Windows admiten diferentes conjuntos de cifrado TLS y orden de prioridad. Consulte la versión Windows correspondiente para el orden predeterminado en el que el proveedor de Microsoft Schannel las elige.

**Windows Server 2022:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS en Windows Server 2022.](tls-cipher-suites-in-windows-server-2022.md)

**Windows 10, versión 1903:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1903](tls-cipher-suites-in-windows-10-v1903.md)

**Windows 10, versión 1809:** Para obtener información sobre los conjuntos de cifrado admitidos, consulte [Conjuntos de cifrado TLS Windows 10 v1809](tls-cipher-suites-in-windows-10-v1809.md)

**Windows 10, versión 1803:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1803](tls-cipher-suites-in-windows-10-v1803.md)

**Windows 10, versión 1709:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1709](tls-cipher-suites-in-windows-10-v1709.md)

**Windows 10, versión 1703:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1703](tls-cipher-suites-in-windows-10-v1703.md)

**Windows Server 2016 y Windows 10, versión 1607:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1607](tls-cipher-suites-in-windows-10-v1607.md)

**Windows 10, versión 1511:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1511](tls-cipher-suites-in-windows-10-v1511.md)

**Windows 10, versión 1507:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS Windows 10 v1507](./tls-cipher-suites-in-windows-10--version-1507.md)

**Windows Server 2012 R2 y Windows 8.1:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS en Windows 8.1](tls-cipher-suites-in-windows-8-1.md)

**Windows Server 2012 y Windows 8:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS en Windows 8](tls-cipher-suites-in-windows-8.md)

**Windows Server 2008 R2 y Windows 7:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS en Windows 7.](tls-cipher-suites-in-windows-7.md)

**Windows Server 2008 y Windows Vista:** Para obtener información sobre los conjuntos de cifrado admitidos, vea [Conjuntos de cifrado TLS en Windows Vista.](schannel-cipher-suites-in-windows-vista.md)

**Windows Server 2003 y Windows XP:** Para obtener información sobre los conjuntos de cifrado admitidos, consulte los temas siguientes.

| Tema                                                                         | Descripción                                                                                                                        |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [Conjuntos de cifrado TLS](tls-cipher-suites.md)<br/>                         | Información sobre los conjuntos de cifrado disponibles con el protocolo TLS en Windows Server 2003 y Windows XP.<br/>              |
| [Capa de sockets seguros protocolo](secure-sockets-layer-protocol.md)<br/> | Información general sobre SSL 2.0 y 3.0, incluidos los conjuntos de cifrado disponibles en Windows Server 2003 y Windows XP.<br/> |



 

> [!Note]  
> Antes de Windows 10, las cadenas del conjunto de cifrado se anexaban con la curva elíptica para determinar la prioridad de la curva. Windows 10 admite una configuración de orden de prioridad de curva elíptica para que el sufijo de curva elíptica no sea necesario y se invalide por el nuevo orden de prioridad de curva elíptica, cuando se proporciona, para permitir que las organizaciones usen la directiva de grupo para configurar diferentes versiones de Windows con los mismos conjuntos de cifrado.

 

