---
description: El protocolo de enlace de seguridad de la capa de transporte (TLS) es responsable de la autenticación y el intercambio de claves necesarios para establecer o reanudar sesiones seguras.
ms.assetid: 65fb4db3-e505-457a-9159-dba0b506ea0b
title: Protocolo de protocolo de enlace TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe32e11127bf46088aa04e58dd6444620cea327c08d2609e01749efcb1e00df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915823"
---
# <a name="tls-handshake-protocol"></a>Protocolo de protocolo de enlace TLS

El [*protocolo de enlace de*](../secgloss/t-gly.md) seguridad de la capa de transporte (TLS) es responsable de la autenticación y el intercambio de claves necesarios para establecer o reanudar sesiones seguras. Al establecer una sesión [*segura,*](../secgloss/s-gly.md)el protocolo de enlace administra lo siguiente:

-   Negociación del conjunto de cifrado
-   Autenticación del servidor y, opcionalmente, el cliente
-   Intercambio de información de clave de sesión.

## <a name="cipher-suite-negotiation"></a>Negociación del conjunto de cifrado

El cliente y el servidor se pondrán en contacto y elijan el conjunto de cifrado que se usará a lo largo de su intercambio de mensajes.

## <a name="authentication"></a>Autenticación

En TLS, un servidor demuestra su identidad al cliente. Es posible que el cliente también tenga que demostrar su identidad al servidor. PKI, el uso de [*pares de claves*](../secgloss/p-gly.md)públicas y privadas, es la base de esta autenticación. El método exacto utilizado para la autenticación viene determinado por el conjunto de cifrado negociado.

## <a name="key-exchange"></a>Intercambio de claves

El cliente y el servidor intercambian números aleatorios y un número especial denominado Secreto maestro previo. Estos números se combinan con datos adicionales que permiten al cliente y al servidor crear su secreto compartido, denominado secreto maestro. El cliente y el servidor usan el secreto maestro para generar el secreto MAC de escritura, que [](../secgloss/s-gly.md) es la clave de sesión utilizada para el [*hash,*](../secgloss/h-gly.md)y la clave de escritura, que es la clave de sesión que se usa para el cifrado.

## <a name="establishing-a-secure-session-by-using-tls"></a>Establecimiento de una sesión segura mediante TLS

El protocolo de enlace TLS implica los pasos siguientes:

1.  El cliente envía un mensaje "Client hello" al servidor, junto con el valor aleatorio del cliente y los conjuntos de cifrado admitidos.
2.  El servidor responde mediante el envío de un mensaje "Server hello" al cliente, junto con el valor aleatorio del servidor.
3.  El servidor envía su certificado al cliente para la autenticación y puede solicitar un certificado al cliente. El servidor envía el mensaje "Server hello done" (Hola al servidor listo).
4.  Si el servidor ha solicitado un certificado al cliente, el cliente lo envía.
5.  El cliente crea un secreto maestro previo aleatorio [](../secgloss/p-gly.md) y lo cifra con la clave pública del certificado del servidor, enviando el secreto maestro previo cifrado al servidor.
6.  El servidor recibe el secreto maestro previo. El servidor y el cliente generan el secreto maestro y las claves [*de sesión*](../secgloss/s-gly.md) en función del secreto maestro previo.
7.  El cliente envía la notificación "Cambiar especificación de cifrado" [](../secgloss/s-gly.md) al servidor para indicar que el cliente comenzará a usar las nuevas claves de sesión para el [*hash y*](../secgloss/h-gly.md) el cifrado de mensajes. El cliente también envía el mensaje "Cliente finalizado".
8.  El servidor recibe "Cambiar especificación de cifrado" y cambia su estado de seguridad de la capa de registro al cifrado simétrico [*mediante*](../secgloss/s-gly.md) las [*claves de sesión*](../secgloss/s-gly.md). El servidor envía el mensaje "Servidor finalizado" al cliente.
9.  El cliente y el servidor ahora pueden intercambiar datos de aplicación a través del canal protegido que han establecido. Todos los mensajes enviados de cliente a servidor y de servidor a cliente se cifran mediante la clave de sesión.

## <a name="resuming-a-secure-session-by-using-tls"></a>Reanudación de una sesión segura mediante TLS

1.  El cliente envía un mensaje "Client hello" con el identificador de sesión de la sesión que se va a reanudar.
2.  El servidor comprueba si su caché de sesiones tiene un identificador de sesión correspondiente. Si se encuentra una coincidencia y el servidor puede reanudar la sesión, envía un mensaje "Server hello" con el identificador de sesión.
    > [!Note]  
    > Si no se encuentra una coincidencia de identificador de sesión, el servidor genera un nuevo identificador de sesión y el cliente y el servidor TLS realizan un protocolo de enlace completo.

     

3.  El cliente y el servidor deben intercambiar los mensajes "Cambiar especificación de cifrado" y enviar los mensajes "Cliente finalizado" y "Servidor finalizado".
4.  El cliente y el servidor ahora pueden reanudar el intercambio de datos de aplicación a través del canal seguro.

 

 
