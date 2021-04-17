---
description: 'Más información sobre: consideraciones de programación para escribir administradores de recursos'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Consideraciones de programación para escribir administradores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687703"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Consideraciones de programación para escribir administradores de recursos

Al usar la API del administrador de transacciones de kernel para agregar compatibilidad con transacciones a las aplicaciones, tenga en cuenta lo siguiente:

-   Al escribir su propio administrador de recursos, debe tener un buen conocimiento práctico de los protocolos y las técnicas de administración de transacciones.
-   Si no escribe los administradores de recursos correctamente, puede dañar sus propios datos con operaciones de recuperación que se administran de forma incorrecta. También puede anclar el final del registro de transacciones y rellenar el sistema de archivos con registros de transacciones.
-   Si la Directiva de tamaño del registro no está configurada para evitar que el registro aumente de tamaño, el administrador de recursos no detendrá las transacciones. El administrador de recursos debe detener la actualización del sistema para que no desborda los recursos del sistema de archivos.
-   Los administradores de recursos deben utilizar listas de control de acceso (ACL) para controlar el acceso a los archivos de registro. de lo contrario, es posible que se produzcan ataques de denegación de servicio.
-   Cualquier participante de Resource Manager o de transacción que almacene los datos en caché debe darse de alta para las notificaciones previas a la preparación. Cuando se recibe una notificación previa a la preparación, debe vaciar todos los datos para que los administradores de recursos de nivel inferior puedan inscribirse antes de la fase de preparación. Cualquier trabajo adicional en esa transacción no se debe almacenar en caché.
-   No cierre un identificador de inscripción mientras la transacción todavía esté activa; Esto hará que se revierta la transacción.

 

 



