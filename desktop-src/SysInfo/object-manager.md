---
description: Un objeto consta de un encabezado estándar y atributos específicos del objeto. Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Administrador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3a74581650828a77c6423825d3c557a13075a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002457"
---
# <a name="object-manager"></a>Administrador de objetos

Un objeto consta de un encabezado estándar y atributos específicos del objeto. Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.

El encabezado del objeto incluye elementos como el nombre del objeto, de modo que otros procesos puedan hacer referencia al objeto por nombre, y un descriptor de seguridad, para que el administrador de objetos pueda controlar qué procesos tienen acceso al recurso del sistema.

Entre las tareas que realiza el administrador de objetos se incluyen las siguientes:

-   Creación de objetos
-   Comprobar que un proceso tiene el derecho a usar el objeto
-   Crear identificadores de objeto y devolverlos al autor de la llamada
-   Mantenimiento de cuotas de recursos
-   Crear identificadores duplicados
-   Controladores de cierre de objetos

 

 



