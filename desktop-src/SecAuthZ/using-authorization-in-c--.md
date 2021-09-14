---
description: Use la API de Authorization Manager para controlar el acceso a los recursos de la aplicación.
ms.assetid: 2485056c-b860-4247-9e7b-0157ca85d05d
title: Uso de la autorización en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b6771d16748d3c04680b545a83e382fa3d5ce78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253640"
---
# <a name="using-authorization-in-c"></a>Uso de la autorización en C++

Puede usar la API de Authorization Manager para controlar el acceso a los recursos de la aplicación.

Si tiene una solución de control de acceso existente basada en listas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) y desea evitar convertir esta solución para que use el Administrador de autorización, puede seguir usando acl para controlar el acceso a los recursos. Para obtener información sobre cómo controlar el acceso a recursos mediante ACL, vea Definir permisos con ACL en [C++,](defining-permissions-with-acls-in-c--.md)Establecer un contexto de cliente desde un SID en [C++](establishing-a-client-context-from-a-sid-in-c--.md)y Comprobar el acceso de cliente con ACL en [C++.](verifying-client-access-with-acls-in-c--.md)

> [!Note]  
> En el caso de las grandes empresas, hay un equilibrio entre la sobrecarga administrativa y el rendimiento. A medida que aumenta el número de usuarios y recursos protegidos, la administración de ACL se complica. El rendimiento no se ve afectado porque toda la información necesaria sobre los derechos de acceso se distribuye a los recursos protegidos. El rendimiento del Administrador de autorización se ve afectado por el escalado.

 

Para obtener información sobre otras tareas de autorización, vea [Tareas de compatibilidad para la autorización en C++.](supporting-tasks-for-authorization-in-c--.md)



| Tema                                                                                                                | Descripción                                                                                              |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [Definir permisos en C++](defining-permissions-in-c--.md)                                                       | Defina qué usuarios tienen acceso a los recursos de la aplicación mediante la creación de un almacén de directivas de autorización. |
| [Comprobar el acceso de cliente a un recurso solicitado en C++](verifying-client-access-to-a-requested-resource-in-c--.md) | Compruebe si el cliente tiene acceso a una o varias operaciones.                                           |
| [Delegación de la definición de permisos en C++](delegating-the-defining-of-permissions-in-c--.md)                   | Delegue la administración de almacenes de directivas de autorización almacenados en Active Directory.          |



 

 

 
