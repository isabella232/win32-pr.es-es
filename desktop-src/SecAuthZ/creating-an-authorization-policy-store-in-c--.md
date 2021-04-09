---
description: Instrucciones para usar la API de administrador de autorización para crear un almacén de directivas de autorización en C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Crear un almacén de directivas de autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155100"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Crear un almacén de directivas de autorización en C++

Cree una directiva de autorización antes o durante la instalación de una aplicación.

Cuando use la API de administrador de autorización para crear una directiva de autorización, siga las instrucciones que se proporcionan en los temas siguientes.



| Tema                                                                                                            | Descripción                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md) | Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, operaciones, tareas, usuarios y grupos de usuarios asociados a la tienda.              |
| [Crear un objeto de aplicación en C++](creating-an-application-object-in-c--.md)                               | Un almacén de directivas de autorización contiene información de directiva de autorización para una o más aplicaciones. Para cada aplicación que usa ese almacén de directivas, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas. |
| [Definir operaciones en C++](defining-operations-in-c--.md)                                                     | En Administrador de autorización, una operación es una función o método de bajo nivel de una aplicación.                                                                                                                                                               |
| [Agrupar operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)                               | En Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se componen de operaciones, que son funciones de bajo nivel y métodos de la aplicación.                                                     |
| [Agrupar tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)                                         | En Administrador de autorización, un rol representa una categoría de usuarios y las tareas a las que están autorizados los usuarios.                                                                                                                                      |
| [Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)                                           | En el administrador de autorización, un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios. Los roles se pueden asignar a este grupo de usuarios colectivamente.                                                                       |
| [Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)                   | En el administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios.                                                                          |



 

 

 



