---
description: Instrucciones para usar la API de administrador de autorización para definir permisos en C++ mediante la creación de un almacén de directivas de autorización.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definir permisos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653095"
---
# <a name="defining-permissions-in-c"></a>Definir permisos en C++

En Administrador de autorización, puede definir qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización.

Para obtener información sobre cómo definir permisos con ACL, vea [definir permisos con ACL en C++](defining-permissions-with-acls-in-c--.md).

**Para definir los permisos de acceso**

1.  Cree el almacén en el que se define la Directiva de autorización:<dl>

[Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Cree una sección en el almacén de directivas de autorización para una aplicación específica:<dl>

[Crear un objeto de aplicación en C++](creating-an-application-object-in-c--.md)  
    </dl>
3.  Defina las operaciones que implementa la aplicación para obtener acceso a los recursos y modificarlos:<dl>

[Definir operaciones en C++](defining-operations-in-c--.md)  
    </dl>
4.  Agrupe las operaciones en tareas de alto nivel que los usuarios quieran realizar:<dl>

[Agrupar operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)  
    </dl>
5.  Definir roles que se componen de grupos de tareas:<dl>

[Agrupar tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)  
    </dl>Un usuario que se asigna a un rol tiene permiso para realizar cualquier tarea asignada a ese rol.
6.  Cree scripts para calificar el acceso a las tareas en tiempo de ejecución:<dl>

[Calificar el acceso con la lógica de negocios en C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Este paso es opcional.
7.  Definir grupos de usuarios:<dl>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)  
    </dl>Estos grupos se pueden asignar a los roles para determinar qué tareas pueden realizar.
8.  Agregar usuarios a grupos de usuarios:<dl>

[Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



