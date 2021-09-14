---
title: Implementación de In-Place activación
description: Implementación de In-Place activación
ms.assetid: 5fd67d1c-1dc5-4d83-a41e-b64d84cbf212
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c075f143c772fe34de0c494664227e892b998387
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060926"
---
# <a name="implementing-in-place-activation"></a>Implementación de In-Place activación

La activación local permite que un usuario interactúe con un objeto incrustado sin salir del documento contenedor. Cuando un usuario activa el objeto, una barra de menús compuesta que contiene elementos de las barras de menús de la aplicación contenedora y de la aplicación de servidor reemplaza *a* la barra de menús principal del contenedor. Por lo tanto, los comandos y las características de ambas aplicaciones están disponibles para el usuario, incluida la ayuda contextual para el objeto activo. Cuando un usuario comienza a trabajar con alguna parte que no es de objeto del documento, el objeto se desactiva, lo que hace que el menú original del documento contenedor reemplace el menú compuesto.

Esta funcionalidad originalmente era por el nombre de *edición en contexto*. Se cambió el nombre porque la edición es solo una manera de que un usuario interactúe con un objeto en ejecución. Los clips de sonido, por ejemplo, se pueden escuchar en lugar de editarse. Los clips de vídeo se pueden ver en lugar de editarse. La activación en contexto es especialmente adecuada en el caso de los clips de vídeo porque les permite ejecutarse en contexto, sin llamar a una ventana independiente. Esto podría ser crítico si el vídeo se visualizara, por ejemplo, junto con los datos de texto adyacentes en el documento contenedor.

La implementación de la activación en contexto es estrictamente opcional para las aplicaciones de contenedor y servidor. OLE sigue siendo compatible con el modelo en el que la activación de un objeto hace que la aplicación de servidor abra una ventana independiente. Los objetos vinculados siempre se abren en una ventana independiente para resaltar que residen en un documento independiente.

La activación en contexto comienza con el objeto en respuesta a una [**llamada IOleObject::D oVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) desde su contenedor. Esta llamada suele ocurrir en respuesta a un usuario que hace doble clic en el objeto o selecciona un comando (verbo) en el menú Editar de la aplicación contenedora.

La ventana local recibe la entrada del teclado y del mouse mientras el objeto incrustado está activo. Cuando un usuario selecciona comandos en la barra de menús compuesta, el comando y los mensajes de menú asociados se envían al contenedor u aplicación de objeto, en función de cuál sea el propietario del menú desplegable determinado seleccionado. La entrada mediante reglas, barras de herramientas o adornos de marco de un objeto van directamente al objeto incrustado, que posee estas ventanas.

Un objeto incrustado activado en el lugar permanece activo hasta que el contenedor lo desactiva en respuesta a la entrada del usuario o el objeto deja voluntariamente el estado activo, como podría hacer un clip de vídeo, por ejemplo. Un usuario puede desactivar un objeto haciendo clic dentro del documento contenedor, pero fuera de la ventana de activación local del objeto, o simplemente haciendo clic en otro objeto. Sin embargo, un objeto activado en contexto permanece activo si el usuario hace clic en la barra de título del contenedor, en la barra de desplazamiento o, en concreto, en la barra de menús.

Puede implementar un servidor de objetos in-place-activation-object como un servidor en proceso (DLL) o un servidor local (EXE). En ambos casos, la barra de menús compuesta contiene elementos (normalmente menús desplegables) de los procesos de servidor y contenedor. En el caso de un servidor en proceso, la ventana de activación en contexto es simplemente otra ventana secundaria en la jerarquía de ventanas del contenedor, recibiendo su entrada a través del bombeo de mensajes de la aplicación contenedora.

En el caso de un servidor local, la ventana de activación local pertenece al proceso de aplicación de servidor del objeto incrustado, pero su ventana primaria pertenece al contenedor. La entrada de la ventana de activación local aparece en la cola de mensajes del servidor y se envía mediante el bucle de mensajes del servidor. Las bibliotecas OLE son responsables de ver que los comandos de menú y los mensajes se envían correctamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Documentos compuestos](compound-documents.md)
</dt> </dl>

 

 




