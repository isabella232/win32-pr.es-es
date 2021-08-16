---
description: Instrucciones para usar la API de Authorization Manager para definir permisos en script mediante la creación de un almacén de directivas de autorización.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definir permisos en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 772c55f453a68e3bf1a4933abc4beb7cf3d65380b3bcf5d2e2c4af2832173b73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782106"
---
# <a name="defining-permissions-in-script"></a>Definir permisos en el script

En el Administrador de autorización, puede definir qué usuarios tienen acceso a qué recursos de aplicación mediante la creación de un almacén de directivas de autorización.

**Para definir permisos de acceso**

1.  Cree el almacén donde se define la directiva de autorización:<dl>

[Creación de un almacén de directivas de autorización en script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Cree una sección en el almacén de directivas de autorización para una aplicación específica:<dl>

[Crear un objeto de aplicación en script](creating-an-application-object-in-script.md)  
    </dl>
3.  Defina las operaciones que implementa la aplicación para acceder a los recursos y modificarlos:<dl>

[Definir operaciones en script](defining-operations-in-script.md)  
    </dl>
4.  Agrupa las operaciones en tareas de alto nivel que los usuarios desean realizar:<dl>

[Agrupación de operaciones en tareas en script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Defina roles que constan de grupos de tareas:<dl>

[Agrupación de tareas en roles en script](grouping-tasks-into-roles-in-script.md)  
    </dl>Un usuario asignado a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.
6.  Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:<dl>

[Calificar el acceso con lógica de negocios en el script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Este paso es opcional.
7.  Definir grupos de usuarios:<dl>

[Definir grupos de usuarios en script](defining-groups-of-users-in-script.md)  
    </dl>A continuación, estos grupos se pueden asignar a roles para determinar qué tareas pueden realizar.
8.  Agregar usuarios a grupos de usuarios:<dl>

[Agregar usuarios a un grupo de aplicaciones en script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



