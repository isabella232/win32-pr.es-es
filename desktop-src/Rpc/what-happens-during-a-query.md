---
title: Lo que sucede durante una consulta
description: En esta sección se describe cómo la red controla la consulta cuando un cliente de 32 bits busca un nombre en su propio dominio.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268832"
---
# <a name="what-happens-during-a-query"></a>Lo que sucede durante una consulta

En esta sección se describe cómo la red controla la consulta cuando un cliente de 32 bits busca un nombre en su propio dominio.

Cuando la aplicación cliente llama a [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), el localizador que reside en el equipo cliente intentará satisfacer esta solicitud. Si no hay nada en la memoria caché, reenviará la solicitud de RPC a un localizador maestro. Si el localizador principal no encuentra nada en su caché, envía la solicitud a todos los equipos del dominio mediante una difusión de ranura de correo. Si hay una coincidencia, el localizador de cada equipo responderá mediante una ranura de correo dirigido. (Por ejemplo, si un proceso de ese equipo ha exportado la interfaz). Las respuestas se intercalan y la RPC se completa desde el localizador de procesos del cliente, que responderá al propio proceso del cliente.

En un dominio, el localizador de cliente busca un localizador maestro en los lugares siguientes:

-   En el controlador de dominio principal
-   En cada controlador de dominio de copia de seguridad

Si no se encuentra ninguna coincidencia, el localizador del cliente se declara a sí mismo como el localizador maestro. Como tal, difundirá consultas si no se pueden satisfacer localmente.

En un grupo de trabajo, el localizador de cliente mantiene una memoria caché de los equipos cuyos localizadores tienen difusión. Utiliza el que se ha estado ejecutando lo más largo que el localizador maestro. Si el equipo no está disponible, se usa el siguiente equipo de difusión más largo, etc. Si el cliente necesita un localizador maestro y la memoria caché está vacía, la memoria caché se reabastece mediante el envío de una difusión de ranura de correo especial que solicita la respuesta de los localizadores principales. Si no hay ninguna respuesta, el localizador del cliente se declara a sí mismo como el localizador maestro y difundirá las consultas si no se pueden satisfacer localmente.

Esto cambia si la aplicación cliente es un programa basado en MS-dos o de 16 bits. En este caso, no hay ningún localizador en ejecución en el equipo cliente y Rpcns1.dll o Rpcnslm. RPC contiene el código para buscar un localizador maestro. Todas las solicitudes se reenvían directamente al localizador maestro.

Estas instrucciones son válidas para los nombres en el dominio del cliente, como los nombres de "/.:/ nombreentrada ". Si el cliente solicita un nombre de otro dominio mediante el uso de "/.../DOMAIN/entryname;", el localizador del cliente reenvía la solicitud al dominio especificado, que la difundirá si no tiene la respuesta. Si el dominio está inactivo o es realmente un grupo de trabajo, se producirá un error en la solicitud.

> [!Note]  
> Recuerde lo siguiente al trabajar con entradas en el servicio de nombres:

 

-   Un cliente no puede usar la sintaxis "/.../DOMAIN/entryname" para buscar una entrada en su propio dominio. Use la sintaxis "/.:/ nombreentrada ". Sin embargo, puede usar "/.../DOMAIN/entryname" para buscar una entrada en otro dominio.
-   El nombre de dominio en "/.../DOMAIN/entryname" debe estar en mayúsculas. Al buscar una coincidencia, el localizador distingue entre mayúsculas y minúsculas.
-   Los nombres de las entradas del localizador también distinguen mayúsculas de minúsculas, pero no tienen que estar en mayúsculas.
-   Cuando el cliente usa "/.:/ nombreentrada ", el localizador no buscará entradas en otros dominios, aunque tengan una relación de confianza con el dominio de inicio de sesión.
-   Las difusiones no atraviesan segmentos de LAN (por ejemplo, subredes). Por lo tanto, la utilidad del localizador está limitada en una organización con varias subredes.

 

 




