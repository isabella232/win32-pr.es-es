---
title: Impacto en las aplicaciones Directory-Enabled
description: En este tema se describe el impacto en las aplicaciones habilitadas para el directorio cuando se producen sesgos de versión, actualizaciones parciales o colisiones.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061818fc791e1c75d440d0c477a321b8c4e5edfb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995077"
---
# <a name="impact-on-directory-enabled-applications"></a>Impacto en las aplicaciones Directory-Enabled

## <a name="version-skew"></a>Sesgo de versión

El sesgo de versiones se produce cuando las aplicaciones leen los mismos objetos de diferentes réplicas antes de que se haya replicado un cambio. Las aplicaciones que leen la réplica remota reconocen el objeto sin modificar. El sesgo de versiones es un problema cuando una aplicación o un conjunto de aplicaciones determinados utilizan los datos del directorio para interoperar.

Por ejemplo, un servicio RPC puede publicar sus extremos en el directorio mediante las API de RPC estándar (como [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta)). Los clientes se conectan al servicio mediante la búsqueda del punto de conexión deseado en el directorio ( [**RpcNsBindingLookupBegin**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext), etc.) y el enlace a él.

Supongamos que un servicio RPC S ₁ publica el extremo es ₁ y, posteriormente, se mueve a otro equipo. El punto de conexión original es ₁ se cambia a E<sub>S2,</sub> que refleja la dirección del nuevo equipo. Los clientes que leen réplicas remotas del servicio de directorio no pueden conectarse al servicio hasta que se replique el punto de conexión actualizado. Sin embargo, es poco frecuente mover un servicio de un equipo a otro. por lo tanto, esta interrupción y retraso no se suelen encontrar, especialmente si el movimiento del servicio está bien planeado.

## <a name="partial-updates"></a>Actualizaciones parciales

En general, la actualización parcial se produce cuando una aplicación Lee un conjunto de datos mientras otra aplicación está escribiendo en el mismo conjunto de datos. Se trata de una situación que puede producirse en cualquier aplicación de un sistema con varios maestros. Esto puede ocurrir de muchas maneras. Puede tener más de una aplicación escribiendo en el mismo conjunto de datos a la vez. Si observa esto de esta manera, el servicio de replicación de directorios es simplemente otra aplicación que podría estar escribiendo en el mismo conjunto de datos que otra aplicación puede estar leyendo. Esto podría ser un problema potencial para una aplicación. Sin embargo, el período de tiempo en el que una actualización parcial puede afectar a la aplicación es relativamente pequeño. En raras ocasiones, debería ser un problema para las aplicaciones que no dependen de la sincronización de varios objetos. Si su aplicación depende en gran medida de la sincronización de un conjunto de objetos relacionado, debe tener en cuenta los efectos de una actualización parcial en el diseño de la aplicación.

En lo que respecta a la replicación de directorios, la actualización parcial se produce cuando las aplicaciones leen el mismo conjunto de objetos de diferentes réplicas mientras la replicación está en curso. Las aplicaciones de la réplica remota ven algunos, pero no todos, los cambios.

> [!Note]  
> La ventana en la que la actualización parcial puede afectar a una aplicación es pequeña: la aplicación debe empezar a leer objetos mientras la replicación entrante está en curso, una vez que se han recibido uno o varios de los objetos cambiados relacionados pero antes de que se hayan recibido todos. El tiempo entre las actualizaciones en la réplica de origen afecta directamente al tamaño de esta ventana, ya que las actualizaciones que se producen cerca del tiempo se replican juntas en el tiempo. La actualización parcial puede ser un problema cuando una aplicación utiliza un conjunto de objetos relacionado.

 

Por ejemplo, un servicio de acceso remoto puede utilizar el directorio para almacenar los datos de la Directiva y del perfil. Los datos de la Directiva se almacenan en un conjunto de objetos y el perfil en otro conjunto. Cuando un usuario se conecta al servicio de acceso remoto, el servicio de acceso remoto lee la Directiva para determinar si el usuario puede conectarse y, en caso afirmativo, qué perfil aplicar a la sesión de usuario. La actualización parcial puede afectar al servicio de acceso remoto de varias maneras:

-   Si la Directiva es compleja y consta de varios objetos, el servicio de acceso remoto podría leer una directiva parcialmente actualizada, lo que provocaría una denegación incorrecta o la concesión del servicio al usuario, imposibilidad de procesar la Directiva debido a una incoherencia interna, etc.
-   Si se han actualizado la Directiva y los perfiles, es posible que el servicio procese correctamente la Directiva, pero aplique un perfil obsoleto, ya que los objetos de Directiva se han replicado pero no los objetos de perfil.
-   Si el perfil es complejo y consta de varios objetos, es posible que el servicio procese correctamente la Directiva pero aplique un perfil parcialmente actualizado, ya que los objetos de Directiva se han replicado, pero solo algunos de los objetos de perfil lo han hecho.

## <a name="collisions"></a>Colisiones

Las colisiones se producen cuando se modifican los mismos atributos de dos o más réplicas de un objeto determinado durante el mismo intervalo de replicación. El proceso de replicación concilia la colisión; debido a la reconciliación, un usuario o una aplicación puede "ver" un valor distinto del que escribió.

Un ejemplo sencillo es la información de dirección de usuario: un usuario cambia una dirección de correo en la réplica R1 y un administrador cambia la misma dirección de correo en la réplica R2. Un valor escrito se propaga hasta que el mecanismo de conciliación de colisiones selecciona otro valor en ese valor. Siempre que un valor siga "ganando" con respecto a otros valores del proceso de resolución de colisiones, el valor seguirá propagando. En última instancia, este valor "ganador" se propagará a R1, R2 y a todas las demás réplicas si no se realiza ningún otro cambio.

La resolución de colisiones es un problema para las aplicaciones que realizan suposiciones sobre la coherencia interna de objetos o conjuntos de objetos. Por ejemplo, un servicio de administración de asignación de ancho de banda de red almacena los datos de ancho de banda de red para un segmento de red determinado en el directorio de un objeto O1. El objeto contiene el ancho de banda disponible en bits por segundo y el ancho de banda máximo que un solo usuario puede reservar. El servicio espera que el ancho de banda Reservable del usuario sea siempre menor o igual que el ancho de banda disponible.

Considere la siguiente secuencia de eventos:

-   El objeto en el estado de replicación completa inicial proporciona el ancho de banda disponible de 56 kilobits por segundo y el ancho de banda Reservable del usuario como 9.600 bits por segundo.
-   Un administrador de la réplica R ₁ cambia los valores a 64k y 19.200, respectivamente.
-   Un administrador de la réplica R ₂ cambia los valores a 10 millones y 1 millón, respectivamente, antes de que llegue la actualización de R ₁.

Suponiendo que los atributos en cuestión tienen números de versión iguales cuando se producen las actualizaciones, hay una posibilidad pequeña, pero real, de que el objeto terminará con un ancho de banda máximo de 64k y un máximo de 1 millón de usuarios, si la aplicación realiza las actualizaciones como operaciones de escritura independientes. La aplicación siempre debe actualizar ambas propiedades en una sola operación.

 

 