---
description: Un objeto consta de un encabezado estándar y atributos específicos del objeto. Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.
ms.assetid: 104113f3-bfd1-4ff7-b92f-2f753c0f5185
title: Administrador de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b87b239d685d53b29243212e06ba2fd5af20e1249794355ed2169278c7f46c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885353"
---
# <a name="object-manager"></a>Administrador de objetos

Un objeto consta de un encabezado estándar y atributos específicos del objeto. Dado que todos los objetos tienen la misma estructura, hay un único administrador de objetos en Windows que mantiene todos los objetos.

El encabezado de objeto incluye elementos como el nombre del objeto, para que otros procesos puedan hacer referencia al objeto por nombre y un descriptor de seguridad, para que el administrador de objetos pueda controlar qué procesos acceden al recurso del sistema.

Entre las tareas que realiza el administrador de objetos se incluyen las siguientes:

-   Creación de objetos
-   Comprobación de que un proceso tiene derecho a usar el objeto
-   Creación de identificadores de objeto y devolución al autor de la llamada
-   Mantenimiento de cuotas de recursos
-   Creación de identificadores duplicados
-   Cierre de identificadores a objetos

 

 



