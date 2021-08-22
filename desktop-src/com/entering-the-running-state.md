---
title: Especificación del estado en ejecución
description: Especificación del estado en ejecución
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91261df578697afef0e33dd8c8ea847eb50cfd546dd96ee0a0085d67100bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501065"
---
# <a name="entering-the-running-state"></a>Especificación del estado en ejecución

Cuando un objeto incrustado realiza la transición al estado en ejecución, el controlador de objetos debe buscar y ejecutar la aplicación de servidor para poder utilizar los servicios que solo proporciona el servidor. Los objetos incrustados se colocan en el estado de ejecución explícitamente a través de una solicitud del contenedor, como la necesidad de dibujar un formato que no se almacena en caché actualmente, o implícitamente mediante OLE en respuesta a la invocación de alguna operación, como cuando un usuario del contenedor hace doble clic en el objeto.

Cuando un objeto vinculado realiza la transición al estado en ejecución, el proceso se conoce como *enlace*. En el proceso de enlace, el controlador de objetos solicita a su moniker almacenado que busque los datos del vínculo y, a continuación, ejecuta la aplicación de servidor.

A primera vista, el enlace de un objeto vinculado parece no ser más complicado que ejecutar un objeto incrustado. Sin embargo, los puntos siguientes complican el proceso:

-   Un vínculo puede hacer referencia a un objeto o a una parte de él que se incrusta en otro contenedor. Esta funcionalidad implica un potencial de inserciones anidadas. La resolución de referencias a dicha jerarquía requiere recorrer de forma recursiva un *moniker* compuesto, empezando por el miembro más a la derecha.
-   Cuando se ejecuta el origen del vínculo, OLE enlaza a la instancia en ejecución del objeto en lugar de ejecutar otra instancia. En el caso de objetos incrustados anidados, uno de los cuales es el origen del vínculo, OLE debe ser capaz de enlazar a un objeto que ya se está ejecutando en cualquier momento.
-   La ejecución de un objeto requiere tener acceso al área de almacenamiento del objeto. Cuando se ejecuta un objeto incrustado, OLE recibe un puntero al almacenamiento durante el proceso de carga, que pasa a la aplicación de servidor OLE. En el caso de los objetos vinculados, sin embargo, no hay ninguna interfaz estándar para acceder al almacenamiento. La aplicación de servidor OLE puede usar la interfaz del sistema de archivos o algún otro mecanismo.

 

 




