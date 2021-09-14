---
title: ¿Qué ocurre durante una consulta?
description: En esta sección se describe cómo la red controla la consulta cuando un cliente de 32 bits busca un nombre en su propio dominio.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169013"
---
# <a name="what-happens-during-a-query"></a>¿Qué ocurre durante una consulta?

En esta sección se describe cómo la red controla la consulta cuando un cliente de 32 bits busca un nombre en su propio dominio.

Cuando la aplicación cliente llama [**a RpcNsBindingImportBegin,**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)el localizador que reside en el equipo cliente intentará satisfacer esta solicitud. Si no hay nada en la memoria caché, reenviará la solicitud de RPC a un localizador maestro. Si el localizador maestro no encuentra nada en su caché, envía la solicitud a todos los equipos del dominio mediante una difusión de ranura de correo. Si hay una coincidencia, el localizador de cada equipo responderá mediante una ranura de correo dirigido. (Por ejemplo, si un proceso de ese equipo ha exportado la interfaz). Las respuestas se intercalan y la RPC se completa desde el localizador de procesos del cliente, que responderá al propio proceso del cliente.

En un dominio, el localizador de cliente busca un localizador maestro en los siguientes lugares:

-   En el controlador de dominio principal
-   En cada controlador de dominio de copia de seguridad

Si no se encuentra una coincidencia, el localizador de cliente se declara como el localizador maestro. Por lo tanto, difundirá consultas si no se pueden satisfacer localmente.

En un grupo de trabajo, el localizador de cliente mantiene una memoria caché de los equipos cuyos localizadores tienen difusión. Usa el que más tiempo lleva ejecutándose como localizador maestro. Si ese equipo no está disponible, se usa el siguiente equipo de difusión más largo, y así sucesivamente. Si el cliente necesita un localizador maestro y la memoria caché está vacía, repone la memoria caché mediante el envío de una difusión de ranura de correo especial que solicita a los localizadores maestros que respondan. Si no hay respuestas, el localizador de cliente se declara como el localizador maestro y difunde consultas si no se pueden satisfacer localmente.

Esto cambia si la aplicación cliente es un programa de 16 bits o basado en MS-DOS. En este caso, no hay ningún localizador en ejecución en el equipo cliente y Rpcns1.dll o Rpcnslm.rpc contiene el código para buscar un localizador maestro. Todas las solicitudes se reenvía directamente al localizador maestro.

Estas directrices son válidas para los nombres del dominio del cliente, como los nombres de "/.:/ entryname". Si el cliente solicita un nombre de otro dominio mediante el uso de "/.../DOMAIN/entryname;", el localizador de cliente reenvía la solicitud al dominio especificado, que lo difundirá si no tiene la respuesta. Si el dominio está fuera de servicio o es realmente un grupo de trabajo, se producirá un error en la solicitud.

> [!Note]  
> Recuerde lo siguiente al trabajar con entradas en el servicio de nombres:

 

-   Un cliente no puede usar la sintaxis "/.../DOMAIN/entryname" para buscar una entrada en su propio dominio. Use la sintaxis "/.:/ entryname". Sin embargo, puede usar "/.../DOMAIN/entryname" para buscar una entrada en otro dominio.
-   El nombre de dominio de "/.../DOMAIN/entryname" debe estar en mayúsculas. Al buscar una coincidencia, el localizador distingue mayúsculas de minúsculas.
-   Los nombres de entrada del localizador también distinguen mayúsculas de minúsculas, pero no deben estar en mayúsculas.
-   Cuando el cliente usa "/.:/ entryname", el localizador no buscará entradas en otros dominios, incluso si tienen una relación de confianza con el dominio de inicio de sesión.
-   Las difusión no cruzan segmentos de LAN (por ejemplo, subredes). Por lo tanto, la utilidad del localizador está limitada en una organización con varias subredes.

 

 




