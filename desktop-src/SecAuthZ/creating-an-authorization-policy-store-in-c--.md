---
description: Instrucciones para usar la API del Administrador de autorización para crear un almacén de directivas de autorización en C++.
ms.assetid: a350f25a-7cda-4879-82d1-151a3da7d8ec
title: Creación de un almacén de directivas de autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fdff3ba26457510440c8d0e603bc993a4878281
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160831"
---
# <a name="creating-an-authorization-policy-store-in-c"></a>Creación de un almacén de directivas de autorización en C++

Cree una directiva de autorización antes o durante la instalación de una aplicación.

Cuando use la API de Authorization Manager para crear una directiva de autorización, siga las instrucciones proporcionadas en los temas siguientes.



| Tema                                                                                                            | Descripción                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear un objeto de almacén de directivas de autorización en C++](creating-an-authorization-policy-store-object-in-c--.md) | Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones. La información incluye las aplicaciones, las operaciones, las tareas, los usuarios y los grupos de usuarios asociados a la tienda.              |
| [Creación de un objeto de aplicación en C++](creating-an-application-object-in-c--.md)                               | Un almacén de directivas de autorización contiene información de directiva de autorización para una o varias aplicaciones. Para cada aplicación que use ese almacén de directivas, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas. |
| [Definir operaciones en C++](defining-operations-in-c--.md)                                                     | En el Administrador de autorización, una operación es una función o un método de bajo nivel de una aplicación.                                                                                                                                                               |
| [Agrupación de operaciones en tareas en C++](grouping-operations-into-tasks-in-c--.md)                               | En el Administrador de autorización, una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se realizan en operaciones, que son funciones y métodos de bajo nivel de la aplicación.                                                     |
| [Agrupación de tareas en roles en C++](grouping-tasks-into-roles-in-c--.md)                                         | En el Administrador de autorización, un rol representa una categoría de usuarios y las tareas que dichos usuarios están autorizados a realizar.                                                                                                                                      |
| [Definir grupos de usuarios en C++](defining-groups-of-users-in-c--.md)                                           | En el Administrador de autorización, [**un objeto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios. Los roles se pueden asignar a este grupo de usuarios colectivamente.                                                                       |
| [Agregar usuarios a un grupo de aplicaciones en C++](adding-users-to-an-application-group-in-c--.md)                   | En el Administrador de autorización, un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que los grupos de usuarios se pueden anidar.                                                                          |



 

 

 



