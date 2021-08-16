---
description: Instrucciones para usar la API de Authorization Manager para crear un almacén de directivas de autorización en script.
ms.assetid: bd9a995a-4195-4da4-a194-472448a0cb08
title: Creación de un almacén de directivas de autorización en script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cbe8bf5457f36cdb71577ae13c2cc226115d4c968436c84b72ca8e90a3446be9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782541"
---
# <a name="creating-an-authorization-policy-store-in-script"></a>Creación de un almacén de directivas de autorización en script

Cree una directiva de autorización antes o durante la instalación de una aplicación.

Cuando use la API de Authorization Manager para crear una directiva de autorización, siga las instrucciones proporcionadas en los temas siguientes.



| Tema                                                                                                                  | Descripción                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Crear un objeto de almacén de directivas de autorización en script](creating-an-authorization-policy-store-object-in-script.md) | Un almacén de directivas de autorización contiene información sobre la directiva de seguridad de una aplicación o grupo de aplicaciones.                                                                                                                                       |
| [Crear un objeto de aplicación en script](creating-an-application-object-in-script.md)                               | Para cada aplicación que use un almacén de directivas de autorización, debe crear un objeto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) y guardarlo en un almacén de directivas.                                                                                                |
| [Definir operaciones en script](defining-operations-in-script.md)                                                     | Una operación es una función o método de bajo nivel de una aplicación.                                                                                                                                                                                              |
| [Agrupación de operaciones en tareas en script](grouping-operations-into-tasks-in-script.md)                               | Una tarea es una acción de alto nivel que los usuarios de una aplicación deben completar. Las tareas se realizan en operaciones, que son funciones y métodos de bajo nivel de la aplicación.                                                                                    |
| [Agrupación de tareas en roles en script](grouping-tasks-into-roles-in-script.md)                                         | Un rol representa una categoría de usuarios y las tareas que esos usuarios están autorizados a realizar.                                                                                                                                                                     |
| [Definir grupos de usuarios en script](defining-groups-of-users-in-script.md)                                           | Un [**objeto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa un grupo de usuarios. A continuación, los roles se pueden asignar a este grupo de usuarios de forma colectiva. Un **objeto IAzApplicationGroup** también puede incluir otros **objetos IAzApplicationGroup** como miembros. |
| [Agregar usuarios a un grupo de aplicaciones en script](adding-users-to-an-application-group-in-script.md)                   | Un grupo de aplicaciones es un grupo de usuarios y grupos de usuarios. Un grupo de aplicaciones puede contener otros grupos de aplicaciones, por lo que se pueden anidar grupos de usuarios. Un grupo de aplicaciones se representa mediante un [**objeto IAzApplicationGroup.**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup)    |



 

 

 



