---
description: Use la API de administrador de autorización para controlar el acceso a los recursos de la aplicación.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Usar la autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668047"
---
# <a name="using-authorization-in-c"></a>Usar la autorización en C++

Puede usar la API de administrador de autorización para controlar el acceso a los recursos de la aplicación.

Si tiene una solución de control de acceso en función de [*las listas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) y desea evitar la conversión de esta solución para usar administrador de autorización, puede seguir usando ACL para controlar el acceso a los recursos. Para obtener información sobre cómo controlar el acceso a los recursos mediante ACL, vea [definir permisos con ACL en c++](defining-permissions-with-acls-in-c--.md), [establecer un contexto de cliente a partir de un SID en c++](establishing-a-client-context-from-a-sid-in-c--.md)y [comprobar el acceso de cliente con ACL en c++](verifying-client-access-with-acls-in-c--.md).

> [!Note]  
> En el caso de las grandes empresas, existe un equilibrio entre la sobrecarga administrativa y el rendimiento. A medida que aumenta el número de recursos y usuarios protegidos, la administración de las ACL es más complicada. El rendimiento no se ve afectado porque toda la información necesaria sobre los derechos de acceso se distribuye a los recursos protegidos. El rendimiento de administrador de autorización se ve afectado por el escalado.

 

Para obtener información acerca de otras tareas de autorización, consulte [Supporting Tasks for Authorization in C++](supporting-tasks-for-authorization-in-c--.md).



| Tema                                                                                                                | Descripción                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definir permisos en C++](defining-permissions-in-c--.md)                                                       | Defina qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización. |
| [Comprobar el acceso del cliente a un recurso solicitado en C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Compruebe si el cliente tiene acceso a una o varias operaciones.                                           |
| [Delegación de la definición de permisos en C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegue la administración de almacenes de directivas de autorización que se almacenan en Active Directory.          |



 

 

 
