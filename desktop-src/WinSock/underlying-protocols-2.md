---
description: Algunos protocolos de los que depende la aplicación para determinados servicios, como la llamada a procedimiento remoto (RPC), pueden tener estructuras y funciones dependientes de la versión de IP que requieren que se modifique la aplicación en función de su uso.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Protocolos subyacentes para aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275391"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a>Protocolos subyacentes para aplicaciones Winsock de IPv6

Algunos protocolos de los que depende la aplicación para determinados servicios, como la llamada a procedimiento remoto (RPC), pueden tener estructuras y funciones dependientes de la versión de IP que requieren que se modifique la aplicación en función de su uso.

Parte del proceso para modificar el código de forma que admita IPv6 debe incluir la determinación de si el uso de los protocolos subyacentes (desde la perspectiva de la pila, estos protocolos se consideran protocolos de nivel superior) requieren modificaciones para poder usar correctamente IPv6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambiar las estructuras de datos para IPv6 Winsock Appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets de doble pila para aplicaciones Winsock de IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones Winsock de IPv6](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
</dt> </dl>

 

 



