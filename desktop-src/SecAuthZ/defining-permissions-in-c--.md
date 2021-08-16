---
description: Instrucciones para usar la API del Administrador de autorización para definir permisos en C++ mediante la creación de un almacén de directivas de autorización.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definir permisos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 008c82e74bcd4b4fec714e43c8beb7d8c7e908baaf569ee260559f64ba5bbc10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913778"
---
# <a name="defining-permissions-in-c"></a>Definir permisos en C++

En el Administrador de autorización, defina qué usuarios tienen acceso a los recursos de aplicación mediante la creación de un almacén de directivas de autorización.

Para obtener información sobre cómo definir permisos con ACL, vea Definir permisos con [ACL en C++.](defining-permissions-with-acls-in-c--.md)

**Para definir permisos de acceso**

1.  Cree el almacén donde se define la directiva de autorización:<dl>

[Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Cree una sección en el almacén de directivas de autorización para una aplicación específica:<dl>

[Creación de un objeto de aplicación en C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Defina las operaciones que implementa la aplicación para acceder a los recursos y modificarlos:<dl>

[Definir operaciones en C++](defining-operations-in-c--.md)  
    </dl>
4.  Agrupa las operaciones en tareas de alto nivel que los usuarios desean realizar:<dl>

[Agrupación de operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Defina roles que constan de grupos de tareas:<dl>

[Agrupación de tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Un usuario asignado a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.
6.  Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:<dl>

[Calificar el acceso con lógica de negocios en C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Este paso es opcional.
7.  Definir grupos de usuarios:<dl>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)  
    </dl>A continuación, estos grupos se pueden asignar a roles para determinar qué tareas pueden realizar.
8.  Agregar usuarios a grupos de usuarios:<dl>

[Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



