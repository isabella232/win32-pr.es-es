---
title: Entrar en el estado de ejecución
description: Entrar en el estado de ejecución
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994167"
---
# <a name="entering-the-running-state"></a>Entrar en el estado de ejecución

Cuando un objeto incrustado realiza la transición al estado en ejecución, el controlador de objetos debe localizar y ejecutar la aplicación de servidor para poder utilizar los servicios que solo proporciona el servidor. Los objetos incrustados se colocan en el estado de ejecución explícitamente a través de una solicitud del contenedor, como una necesidad de dibujar un formato no almacenado en caché actualmente o implícitamente por OLE en respuesta a la invocación de una operación, como cuando un usuario del contenedor hace doble clic en el objeto.

Cuando un objeto vinculado realiza la transición al estado en ejecución, el proceso se conoce como *enlace*. En el proceso de enlace, el controlador de objetos pide a su moniker almacenado que busque los datos del vínculo y, a continuación, ejecuta la aplicación de servidor.

A primera vista, el enlace de un objeto vinculado parece no ser más complicado que ejecutar un objeto incrustado. Sin embargo, los siguientes puntos complican el proceso:

-   Un vínculo puede hacer referencia a un objeto, o una parte de ella, que está incrustado en otro contenedor. Esta capacidad implica una posibilidad de incrustaciones anidadas. La resolución de referencias a una jerarquía de este tipo requiere atravesar de forma recursiva un *moniker compuesto*, empezando por el miembro situado más a la derecha.
-   Cuando el origen del vínculo se está ejecutando, OLE se enlaza a la instancia en ejecución del objeto en lugar de ejecutar otra instancia. En el caso de los objetos incrustados anidados, uno de los cuales es el origen del vínculo, OLE debe ser capaz de enlazar a un objeto que ya se está ejecutando en cualquier momento.
-   La ejecución de un objeto requiere tener acceso al área de almacenamiento del objeto. Cuando se ejecuta un objeto incrustado, OLE recibe un puntero al almacenamiento durante el proceso de carga, que pasa a la aplicación de servidor OLE. En el caso de los objetos vinculados, sin embargo, no hay ninguna interfaz estándar para tener acceso al almacenamiento. La aplicación de servidor OLE puede utilizar la interfaz del sistema de archivos o algún otro mecanismo.

 

 




