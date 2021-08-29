---
description: 'Más información sobre: Consideraciones de programación para escribir administradores de recursos'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Consideraciones de programación para escribir administradores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a20d84695a5bc0f378c8b93519a35b9a1d95bcc58d718520478e519707553b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388914"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Consideraciones de programación para escribir administradores de recursos

Al usar la API de Kernel Transaction Manager para agregar compatibilidad con transacciones a las aplicaciones, tenga en cuenta lo siguiente:

-   Al escribir su propio administrador de recursos, debe tener un buen conocimiento práctico de las técnicas y protocolos de administración de transacciones.
-   Si no escribe correctamente administradores de recursos, puede dañar sus propios datos con operaciones de recuperación mal manipuladas. También puede anclar el final del registro de transacciones y rellenar el sistema de archivos con registros de transacciones.
-   Si la directiva de tamaño de registro no está establecida para evitar que el registro aumente de tamaño, el administrador de recursos no detendrá las transacciones. El administrador de recursos debe dejar de actualizar el sistema para que no sobresalte los recursos del sistema de archivos.
-   Los administradores de recursos deben usar listas de control de acceso (ACL) para controlar el acceso a los archivos de registro. de lo contrario, se pueden realizar ataques por denegación de servicio.
-   Cualquier administrador de recursos o participante de transacción que almacena en caché los datos debe dar de alta para recibir notificaciones previas a la preparación. Cuando se recibe una notificación de preparación previa, debe vaciar todos los datos para que los administradores de recursos de nivel inferior puedan dar de alta antes de la fase de preparación. Cualquier otro trabajo en esa transacción no se debe almacenar en caché.
-   No cierre un identificador de alta mientras la transacción sigue activa; esto hará que se revierte la transacción.

 

 



