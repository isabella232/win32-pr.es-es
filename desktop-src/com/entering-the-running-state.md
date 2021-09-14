---
title: Especificar el estado en ejecución
description: Especificar el estado en ejecución
ms.assetid: 2173eaa9-0e60-4411-81e4-dbabc5fe89b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 959038c8f64fe8750ab1bcf0f06b753371f04136
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889129"
---
# <a name="entering-the-running-state"></a>Especificar el estado en ejecución

Cuando un objeto incrustado realiza la transición al estado en ejecución, el controlador de objetos debe buscar y ejecutar la aplicación de servidor para utilizar los servicios que solo proporciona el servidor. Los objetos incrustados se colocan en el estado en ejecución explícitamente a través de una solicitud del contenedor, como la necesidad de dibujar un formato que no se almacena actualmente en caché, o implícitamente mediante OLE en respuesta a invocar alguna operación, como cuando un usuario del contenedor hace doble clic en el objeto.

Cuando un objeto vinculado realiza la transición al estado en ejecución, el proceso se conoce como *enlace*. En el proceso de enlace, el controlador de objetos solicita a su moniker almacenado que busque los datos del vínculo y, a continuación, ejecuta la aplicación de servidor.

A primera vista, el enlace de un objeto vinculado parece no ser más complicado que ejecutar un objeto incrustado. Sin embargo, los siguientes puntos complican el proceso:

-   Un vínculo puede hacer referencia a un objeto o a una parte de él que se incrusta en otro contenedor. Esta funcionalidad implica un potencial de inserciones anidadas. La resolución de referencias a dicha jerarquía requiere recorrer de forma recursiva un *moniker* compuesto, empezando por el miembro más a la derecha.
-   Cuando el origen del vínculo se está ejecutando, OLE se enlaza a la instancia en ejecución del objeto en lugar de ejecutar otra instancia. En el caso de objetos incrustados anidados, uno de los cuales es el origen del vínculo, OLE debe poder enlazarse a un objeto que ya se está ejecutando en cualquier momento.
-   La ejecución de un objeto requiere tener acceso al área de almacenamiento del objeto. Cuando se ejecuta un objeto incrustado, OLE recibe un puntero al almacenamiento durante el proceso de carga, que pasa a la aplicación de servidor OLE. Sin embargo, en el caso de los objetos vinculados, no hay ninguna interfaz estándar para acceder al almacenamiento. La aplicación de servidor OLE puede usar la interfaz del sistema de archivos o algún otro mecanismo.

 

 




