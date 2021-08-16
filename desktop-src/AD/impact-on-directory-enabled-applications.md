---
title: Impacto en Directory-Enabled aplicaciones
description: En este tema se describe el impacto en las aplicaciones habilitadas para directorios cuando se producen asimetrías de versiones, actualizaciones parciales o colisiones.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601a5bbffda08f0789875176193977cbecfc34596a9900c870f81cfd677b9ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187680"
---
# <a name="impact-on-directory-enabled-applications"></a>Impacto en Directory-Enabled aplicaciones

## <a name="version-skew"></a>Sesgo de versión

La asimetría de versiones se produce cuando las aplicaciones leen los mismos objetos de diferentes réplicas antes de que se replique un cambio. Las aplicaciones que leen la réplica remota reconocen el objeto sin cambios. La asimetría de versiones es un problema cuando una aplicación o un conjunto de aplicaciones determinados usan los datos del directorio para interoperar.

Por ejemplo, un servicio RPC puede publicar sus puntos de conexión en el directorio mediante api RPC estándar (como [**RpcNsBindingExport).**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta) Los clientes se conectan al servicio buscando el punto de conexión deseado en el directorio [**(RpcNsBindingLookupBegin,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina) [**RpcNsBindingLookupNext,**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)y así sucesivamente) y enlazando a él.

Suponga que un servicio RPC S₁ publica el punto de conexión Es₁ y, posteriormente, se mueve a otro equipo. El punto de conexión ₁ cambia a E<sub>s2, lo</sub> que refleja la dirección del nuevo equipo. Los clientes que leen réplicas remotas del servicio de directorio no pueden conectarse al servicio hasta que se replique el punto de conexión actualizado. Sin embargo, mover un servicio de un equipo a otro es algo poco frecuente. Por lo tanto, esta interrupción o retraso rara vez se debe encontrar, especialmente si el movimiento del servicio está bien planeado.

## <a name="partial-updates"></a>Actualizaciones parciales

En general, la actualización parcial se produce cuando una aplicación lee un conjunto de datos mientras otra está escribiendo en ese mismo conjunto de datos. Se trata de una situación que puede producirse con cualquier aplicación en un sistema con varios maestros. Esto puede ocurrir de muchas maneras. Podría tener más de una aplicación escribiendo en el mismo conjunto de datos a la vez. Si lo observa de esta manera, el servicio de replicación de directorios es simplemente otra aplicación que podría estar escribiendo en el mismo conjunto de datos que otra aplicación puede leer. Esto podría ser un posible problema para una aplicación. Sin embargo, la ventana de tiempo en la que una actualización parcial puede afectar a la aplicación es relativamente pequeña. Esto rara vez debería ser un problema para las aplicaciones que no dependen de la sincronización de varios objetos. Si la aplicación depende en gran medida de la sincronización de un conjunto de objetos relacionado, debe tener en cuenta los efectos de una actualización parcial en el diseño de la aplicación.

En cuanto a la replicación de directorios, la actualización parcial se produce cuando las aplicaciones leen el mismo conjunto de objetos de diferentes réplicas mientras la replicación está en curso. Las aplicaciones de la réplica remota ven algunos de los cambios, pero no todos.

> [!Note]  
> La ventana en la que la actualización parcial puede afectar a una aplicación es pequeña: la aplicación debe empezar a leer objetos mientras la replicación entrante está en curso, después de que se hayan recibido uno o varios de los objetos modificados relacionados, pero antes de que se hayan recibido todos. El tiempo entre las actualizaciones de la réplica de origen afecta directamente al tamaño de esta ventana: las actualizaciones que se producen juntos en el tiempo se replican juntas en el tiempo. La actualización parcial puede ser un problema cuando una aplicación usa un conjunto de objetos relacionado.

 

Por ejemplo, un servicio de acceso remoto puede usar el directorio para almacenar datos de perfil y directiva. Los datos de directiva se almacenan en un conjunto de objetos y el perfil en otro conjunto. Cuando un usuario se conecta al servicio de acceso remoto, el servicio de acceso remoto lee la directiva para determinar si el usuario puede conectarse y, si es así, qué perfil se va a aplicar a la sesión de usuario. La actualización parcial puede afectar al servicio de acceso remoto de varias maneras:

-   Si la directiva es compleja y consta de varios objetos, el servicio de acceso remoto podría leer una directiva parcialmente actualizada, lo que da lugar a una denegación o concesión de servicio incorrectas al usuario, la incapacidad de procesar la directiva debido a una incoherencia interna, y así sucesivamente.
-   Si se han actualizado la directiva y los perfiles, el servicio podría procesar correctamente la directiva pero aplicar un perfil obsoleto, porque los objetos de directiva se han replicado, pero los objetos de perfil no lo han hecho.
-   Si el perfil es complejo y consta de varios objetos, el servicio podría procesar correctamente la directiva pero aplicar un perfil parcialmente actualizado porque los objetos de directiva se han replicado, pero solo algunos de los objetos de perfil lo han hecho.

## <a name="collisions"></a>Colisiones

Las colisiones se producen cuando se cambian los mismos atributos de dos o más réplicas de un objeto determinado durante el mismo intervalo de replicación. El proceso de replicación concilia la colisión; debido a la conciliación, un usuario o aplicación puede "ver" un valor distinto del que escribió.

Un ejemplo sencillo es la información de dirección de usuario: un usuario cambia una dirección de correo en la réplica R1 y un administrador cambia la misma dirección de correo en la réplica R2. Un valor escrito se propaga hasta que el mecanismo de conciliación de colisión selecciona otro valor sobre ese valor. Siempre que un valor siga "ganando" con otros valores en el proceso de resolución de colisiones, el valor continúa prorpropagación. En última instancia, este valor "ganador" se propagará a R1, R2 y todas las demás réplicas si no se realizan otros cambios.

La resolución de colisiones es un problema para las aplicaciones que hacen suposiciones sobre la coherencia interna de objetos o conjuntos de objetos. Por ejemplo, un servicio de administración de asignación de ancho de banda de red almacena datos de ancho de banda de red para un segmento de red determinado en el directorio de un objeto O1. El objeto contiene el ancho de banda disponible en bits por segundo y el ancho de banda máximo que cualquier usuario puede reservar. El servicio espera que el ancho de banda reservable del usuario siempre sea menor o igual que el ancho de banda disponible.

Considere la siguiente secuencia de eventos:

-   El objeto en el estado inicial totalmente replicado proporciona el ancho de banda disponible como 56 kilobits por segundo y el ancho de banda reservable del usuario como 9600 bits por segundo.
-   Un administrador de la réplica R₁ cambia los valores a 64 000 y 19 200, respectivamente.
-   Un administrador de la réplica R3 cambia los valores a 10 millones y 1 millón, respectivamente, antes de que llegue la actualización de R₁.

Suponiendo que los atributos en cuestión tienen números de versión iguales cuando se producen las actualizaciones, existe una posibilidad pequeña, pero real, de que el objeto termine con un ancho de banda máximo de 64 000 y un máximo reservable del usuario de 1 millón, si la aplicación realiza las actualizaciones como operaciones de escritura independientes. La aplicación siempre debe actualizar ambas propiedades en una sola operación.

 

 