---
title: Entrar en el estado pasivo
description: Entrar en el estado pasivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9f98a30117174c5953c19cc9e1092ebf79403e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903792"
---
# <a name="entering-the-passive-state"></a>Entrar en el estado pasivo

El cierre de objetos fuerza un objeto incrustado o vinculado en el estado pasivo. Normalmente se inicia desde la interfaz de usuario de la aplicación de servidor OLE, como cuando el usuario selecciona el comando de cierre de archivo. En este caso, la aplicación de servidor OLE notifica al contenedor, que libera su recuento de referencias en el objeto. Cuando se han liberado todas las referencias al objeto, se puede liberar el objeto. Cuando se han liberado todos los objetos, la aplicación de servidor OLE puede terminar de forma segura.

Una aplicación contenedora también puede iniciar el cierre de objetos. Para cerrar un objeto, el contenedor libera su recuento de referencias después de completar una operación de guardar opcional. Puede diseñar contenedores para liberar objetos cuando se desactivan después de una sesión de activación en contexto, lo que permite al usuario hacer clic fuera del objeto sin perder la sesión de edición activa.

 

 




