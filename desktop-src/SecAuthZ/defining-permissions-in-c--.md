---
description: Instrucciones para usar la API de Authorization Manager para definir permisos en C++ mediante la creación de un almacén de directivas de autorización.
ms.assetid: 8a3bf625-7973-4905-a63c-e42e6682b7c2
title: Definir permisos en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc398d811f44b69dbde8d30f135fd4f30a552bbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073699"
---
# <a name="defining-permissions-in-c"></a>Definir permisos en C++

En el Administrador de autorización, puede definir qué usuarios tienen acceso a qué recursos de aplicación mediante la creación de un almacén de directivas de autorización.

Para obtener información sobre cómo definir permisos con ACL, vea [Definición de permisos con ACL en C++.](defining-permissions-with-acls-in-c--.md)

**Para definir permisos de acceso**

1.  Cree el almacén donde se define la directiva de autorización:<dl>

[Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md)  
    </dl>
2.  Cree una sección en el almacén de directivas de autorización para una aplicación específica:<dl>

[Crear un objeto de aplicación en C++](creating-an-application-object-in-c--.md)  
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

[Acceso apto con lógica de negocios en C++](qualifying-access-with-business-logic-in-c--.md)  
    </dl>Este paso es opcional.
7.  Definir grupos de usuarios:<dl>

[Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)  
    </dl>A continuación, estos grupos se pueden asignar a roles para determinar qué tareas pueden realizar.
8.  Agregar usuarios a grupos de usuarios:<dl>

[Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)  
    </dl>

 

 



