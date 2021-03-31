---
description: Instrucciones para usar la API de administrador de autorización para crear un almacén de directivas de autorización en el script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Creación de un almacén de directivas de autorización en un script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0cb35e8e998f95e99193d1dc5e8a74838b7efc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155501"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Creación de un almacén de directivas de autorización en un script

Cree una directiva de autorización antes o durante la instalación de una aplicación.

Cuando use la API de administrador de autorización para crear una directiva de autorización, siga las instrucciones que se proporcionan en los temas siguientes.



| Tema                                                                                                                  | Descripción                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear un objeto de almacén de directivas de autorización en el script](creating-an-authorization-policy-store-object-in-script.md) | Un almacén de directivas de autorización contiene información sobre la Directiva de seguridad de una aplicación o grupo de aplicaciones.                                                                                                                                       |
| [Crear un objeto de aplicación en el script](creating-an-application-object-in-script.md)                               | Para cada aplicación que usa un almacén de directivas de autorización, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.                                                                                                |
| [Definir operaciones en el script](defining-operations-in-script.md)                                                     | Una operación es una función o un método de bajo nivel de una aplicación.                                                                                                                                                                                              |
| [Agrupar operaciones en tareas en script](grouping-operations-into-tasks-in-script.md)                               | Una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se componen de operaciones, que son funciones de bajo nivel y métodos de la aplicación.                                                                                    |
| [Agrupar tareas en roles en el script](grouping-tasks-into-roles-in-script.md)                                         | Un rol representa una categoría de usuarios y las tareas que pueden realizar los usuarios.                                                                                                                                                                     |
| [Definir grupos de usuarios en el script](defining-groups-of-users-in-script.md)                                           | Un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios. Los roles se pueden asignar a este grupo de usuarios colectivamente. Un objeto **IAzApplicationGroup** también puede incluir otros objetos **IAzApplicationGroup** como miembros. |
| [Agregar usuarios a un grupo de aplicaciones en el script](adding-users-to-an-application-group-in-script.md)                   | Un grupo de aplicación es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios. Un grupo de aplicación se representa mediante un objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) .    |



 

 

 



