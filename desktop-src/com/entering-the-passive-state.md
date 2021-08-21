---
title: Especificación del estado pasivo
description: Especificación del estado pasivo
ms.assetid: 544760e6-1706-4384-8e17-8971f0e0c5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a0a3a93b0ff0bd1c16701c82f271847ee435375112a8e7a03120155928fe1ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736859"
---
# <a name="entering-the-passive-state"></a>Especificación del estado pasivo

El cierre de objetos fuerza a un objeto incrustado o vinculado al estado pasivo. Normalmente se inicia desde la interfaz de usuario de la aplicación de servidor OLE, como cuando el usuario selecciona el comando Cerrar archivo. En este caso, la aplicación de servidor OLE notifica al contenedor, que libera su recuento de referencias en el objeto . Cuando se han liberado todas las referencias al objeto, el objeto se puede liberar. Cuando se han liberado todos los objetos, la aplicación de servidor OLE puede finalizar de forma segura.

Una aplicación contenedora también puede iniciar el cierre de objetos. Para cerrar un objeto, el contenedor libera su recuento de referencias después de completar una operación de guardado opcional. Puede diseñar contenedores para liberar objetos cuando se desactivan después de una sesión de activación local, lo que permite al usuario hacer clic fuera del objeto sin perder la sesión de edición activa.

 

 




