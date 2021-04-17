---
description: El protocolo de enlace de seguridad de la capa de transporte (TLS) es responsable de la autenticación y el intercambio de claves necesarios para establecer o reanudar las sesiones seguras.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocolo de enlace TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7cfa9e9db54a6035abe147ce00bbde59bcc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668248"
---
# <a name="tls-handshake-protocol"></a>Protocolo de enlace TLS

El protocolo de enlace de seguridad de la [*capa de transporte*](../secgloss/t-gly.md) (TLS) es responsable de la autenticación y el intercambio de claves necesarios para establecer o reanudar las sesiones seguras. Al establecer una [*sesión*](../secgloss/s-gly.md)segura, el protocolo de enlace administra lo siguiente:

-   Negociación de conjunto de cifrado
-   Autenticación del servidor y, opcionalmente, el cliente
-   Intercambio de información de claves de sesión.

## <a name="cipher-suite-negotiation"></a>Negociación de conjunto de cifrado

El cliente y el servidor hacen contacto y eligen el conjunto de cifrado que se usará en el intercambio de mensajes.

## <a name="authentication"></a>Autenticación

En TLS, un servidor demuestra su identidad al cliente. Es posible que el cliente también tenga que demostrar su identidad en el servidor. La PKI, el uso de [*pares de claves pública y privada*](../secgloss/p-gly.md), es la base de esta autenticación. El método exacto que se usa para la autenticación viene determinado por el conjunto de cifrado negociado.

## <a name="key-exchange"></a>Intercambio de claves

El cliente y el servidor intercambian los números aleatorios y un número especial denominado secreto anterior al patrón. Estos números se combinan con datos adicionales que permiten al cliente y al servidor crear su secreto compartido, denominado secreto principal. El cliente y el servidor usan el secreto principal para generar el secreto de MAC de escritura, que es la clave de sesión que se usa para el [*hash*](../secgloss/h-gly.md)y la clave de escritura, que es la [*clave de sesión*](../secgloss/s-gly.md) que se usa para el cifrado.

## <a name="establishing-a-secure-session-by-using-tls"></a>Establecer una sesión segura mediante TLS

El protocolo de enlace TLS implica los siguientes pasos:

1.  El cliente envía un mensaje "Hello Client" al servidor, junto con el valor aleatorio del cliente y los conjuntos de cifrado admitidos.
2.  El servidor responde mediante el envío de un mensaje "Hello Server" al cliente, junto con el valor aleatorio del servidor.
3.  El servidor envía su certificado al cliente para la autenticación y puede solicitar un certificado del cliente. El servidor envía el mensaje "Server Hello Done".
4.  Si el servidor ha solicitado un certificado del cliente, el cliente lo envía.
5.  El cliente crea un secreto de maestro previo aleatorio y lo cifra con la [*clave pública*](../secgloss/p-gly.md) del certificado del servidor y envía el secreto del maestro previo cifrado al servidor.
6.  El servidor recibe el secreto del patrón previo. Cada servidor y cliente generan el secreto principal y [*las claves de sesión*](../secgloss/s-gly.md) basadas en el secreto del patrón previo.
7.  El cliente envía una notificación de "cambiar especificación de cifrado" al servidor para indicar que el cliente comenzará a usar las nuevas [*claves de sesión*](../secgloss/s-gly.md) para el [*hash*](../secgloss/h-gly.md) y el cifrado de mensajes. El cliente también envía el mensaje "cliente finalizado".
8.  El servidor recibe "cambiar especificación de cifrado" y cambia el estado de seguridad de la capa de registro al [*cifrado simétrico*](../secgloss/s-gly.md) mediante las [*claves de sesión*](../secgloss/s-gly.md). El servidor envía el mensaje "servidor finalizado" al cliente.
9.  El cliente y el servidor ahora pueden intercambiar datos de aplicación a través del canal seguro que han establecido. Todos los mensajes enviados del cliente al servidor y del servidor al cliente se cifran mediante la clave de sesión.

## <a name="resuming-a-secure-session-by-using-tls"></a>Reanudación de una sesión segura mediante TLS

1.  El cliente envía un mensaje "Hello de cliente" con el identificador de sesión de la sesión que se va a reanudar.
2.  El servidor comprueba si hay un identificador de sesión coincidente en la memoria caché de la sesión. Si se encuentra una coincidencia y el servidor puede reanudar la sesión, envía un mensaje "Hello Server" con el identificador de sesión.
    > [!Note]  
    > Si no se encuentra una coincidencia con el identificador de sesión, el servidor genera un nuevo identificador de sesión y el cliente y el servidor de TLS realizan un protocolo de enlace completo.

     

3.  El cliente y el servidor deben intercambiar los mensajes de "cambiar especificación de cifrado" y enviar mensajes de "cliente finalizado" y "servidor finalizado".
4.  El cliente y el servidor ahora pueden reanudar el intercambio de datos de la aplicación a través del canal seguro.

 

 
