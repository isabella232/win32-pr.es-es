---
title: Implementación de la activación de In-Place
description: Implementación de la activación de In-Place
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676165"
---
# <a name="implementing-in-place-activation"></a>Implementación de la activación de In-Place

La activación en contexto permite al usuario interactuar con un objeto incrustado sin tener que cerrar el documento contenedor. Cuando un usuario activa el objeto, una *barra de menús compuesta* que consta de elementos de las barras de menús de la aplicación contenedora y de la aplicación de servidor reemplaza a la barra de menús principal del contenedor. Por tanto, los comandos y las características de ambas aplicaciones están disponibles para el usuario, incluida la ayuda contextual para el objeto activo. Cuando un usuario empieza a trabajar con alguna parte que no es de objeto del documento, se desactiva el objeto, lo que hace que el menú original del documento contenedor reemplace al menú compuesto.

Esta funcionalidad apareció originalmente por el nombre de la *edición en contexto*. El nombre se cambió porque la edición es solo una forma de que un usuario interactúe con un objeto en ejecución. Los clips de sonido, por ejemplo, se pueden escuchar en lugar de editar. Se pueden ver clips de vídeo en lugar de editarlos. La activación en contexto es particularmente útil en el caso de los clips de vídeo, ya que permite que se ejecuten en su lugar, sin llamar a una ventana independiente. Esto podría ser crítico si el vídeo tuviera que verlo, por ejemplo, junto con los datos de texto adyacentes en el documento contenedor.

La implementación de la activación en contexto es estrictamente opcional para las aplicaciones de contenedor y de servidor. OLE sigue siendo compatible con el modelo en el que la activación de un objeto hace que la aplicación de servidor abra una ventana independiente. Los objetos vinculados siempre se abren en una ventana independiente para resaltar que residen en un documento independiente.

La activación en contexto comienza con el objeto en respuesta a una llamada a [**IOleObject::D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) de su contenedor. Esta llamada suele ocurrir en respuesta a un usuario que hace doble clic en el objeto o selecciona un comando (verbo) en el menú edición de la aplicación contenedora.

La ventana en contexto recibe la entrada del teclado y del mouse mientras el objeto incrustado está activo. Cuando un usuario selecciona comandos en la barra de menús compuesta, el comando y los mensajes de menú asociados se envían a la aplicación de contenedor u objeto, en función de cuál sea el propietario del menú desplegable determinado seleccionado. La entrada por medio de las reglas, las barras de herramientas o los gráficos de marcos de un objeto va directamente al objeto incrustado, que posee estas ventanas.

Un objeto incrustado en contexto permanece activo hasta que el contenedor lo desactiva como respuesta a la entrada del usuario o el objeto proporciona de forma voluntaria el estado activo, por ejemplo, como un clip de vídeo. Un usuario puede desactivar un objeto haciendo clic dentro del documento contenedor pero fuera de la ventana de activación en contexto del objeto, o simplemente haciendo clic en otro objeto. Sin embargo, un objeto activado en contexto permanece activo, si el usuario hace clic en la barra de título, la barra de desplazamiento o, en particular, la barra de menús.

Puede implementar un servidor de objetos de activación en contexto como un servidor en proceso (DLL) o un servidor local (EXE). En ambos casos, la barra de menús compuesta contiene elementos (normalmente menús desplegables) de los procesos de servidor y de contenedor. En el caso de un servidor en proceso, la ventana de activación en contexto es simplemente otra ventana secundaria en la jerarquía de ventanas del contenedor y recibe su entrada a través del bombeo de mensajes de la aplicación contenedora.

En el caso de un servidor local, la ventana de activación en contexto pertenece al proceso de aplicación de servidor del objeto incrustado, pero su ventana primaria pertenece al contenedor. La entrada de la ventana de activación en contexto aparece en la cola de mensajes del servidor y se envía mediante el bucle de mensajes del servidor. Las bibliotecas OLE son responsables de verlos que los comandos de menú y los mensajes se envían correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




