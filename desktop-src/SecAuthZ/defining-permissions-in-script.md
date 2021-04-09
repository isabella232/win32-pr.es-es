---
description: Instrucciones para usar la API de administrador de autorización para definir permisos en el script mediante la creación de un almacén de directivas de autorización.
ms.assetid: 114426e8-03a7-41e2-96c9-e2da91aa7d84
title: Definir permisos en el script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e16f377ffa669da0b686ac28783e9a370efec94d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002542"
---
# <a name="defining-permissions-in-script"></a>Definir permisos en el script

En Administrador de autorización, puede definir qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización.

**Para definir los permisos de acceso**

1.  Cree el almacén en el que se define la Directiva de autorización:<dl>

[Creación de un almacén de directivas de autorización en un script](creating-an-authorization-policy-store-object-in-script.md)  
    </dl>
2.  Cree una sección en el almacén de directivas de autorización para una aplicación específica:<dl>

[Crear un objeto de aplicación en el script](creating-an-application-object-in-script.md)  
    </dl>
3.  Defina las operaciones que implementa la aplicación para obtener acceso a los recursos y modificarlos:<dl>

[Definir operaciones en el script](defining-operations-in-script.md)  
    </dl>
4.  Agrupe las operaciones en tareas de alto nivel que los usuarios quieran realizar:<dl>

[Agrupar operaciones en tareas en script](grouping-operations-into-tasks-in-script.md)  
    </dl>
5.  Definir roles que se componen de grupos de tareas:<dl>

[Agrupar tareas en roles en el script](grouping-tasks-into-roles-in-script.md)  
    </dl>Un usuario que se asigna a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.
6.  Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:<dl>

[Acceso de calificación con lógica de negocios en script](qualifying-access-with-business-logic-in-script.md)  
    </dl>Este paso es opcional.
7.  Definir grupos de usuarios:<dl>

[Definir grupos de usuarios en el script](defining-groups-of-users-in-script.md)  
    </dl>Estos grupos se pueden asignar a los roles para determinar qué tareas pueden realizar.
8.  Agregar usuarios a grupos de usuarios:<dl>

[Agregar usuarios a un grupo de aplicaciones en el script](adding-users-to-an-application-group-in-script.md)  
    </dl>

 

 



