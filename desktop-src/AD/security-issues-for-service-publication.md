---
title: Problemas de seguridad para la publicación de servicio
description: El sistema restringe la capacidad de crear, modificar o eliminar objetos de punto de conexión. Tenga en cuenta las restricciones y, al publicar un servicio, y controlarlas.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problemas de seguridad de AD de publicación de servicio
- Active Directory, uso, seguridad, publicación de servicio, problemas de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fee5be89c490fa938cdc9c7cf3d7d72434a3dffa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773087"
---
# <a name="security-issues-for-service-publication"></a>Problemas de seguridad para la publicación de servicio

El sistema restringe la capacidad de crear, modificar o eliminar objetos de punto de conexión. Tenga en cuenta las restricciones y, al publicar un servicio, y controlarlas.

Los clientes deben poder confiar en los datos publicados en un objeto de punto de conexión en el directorio. Por esta razón, el permiso para crear un objeto de punto de conexión suele estar restringido a los usuarios con privilegios, como los administradores de dominio. Esto evita que los usuarios no autorizados puedan engañar a los clientes mediante la creación de puntos de conexión no válidos para servicios conocidos.

Los servicios no deben ejecutarse con privilegios de administrador de dominio. Esto significa que un servicio normalmente no puede crear su propio punto de conexión. En su lugar, se proporciona una instalación de servicio o una aplicación de configuración que crea el punto de conexión. Este instalador lo debe ejecutar un usuario con los privilegios necesarios.

Aunque un servicio no puede crear normalmente su punto de conexión, debe ser capaz de actualizar las propiedades del punto de conexión en tiempo de ejecución. Las propiedades del punto de conexión contienen los datos de enlace que usan los clientes para conectarse al servicio. Si cambian los datos de enlace, el servicio debe actualizar el punto de conexión. de lo contrario, los clientes no pueden utilizar el servicio. Esto significa que el instalador también debe modificar el descriptor de seguridad en el objeto de punto de conexión para que el servicio pueda leer y escribir las propiedades adecuadas en tiempo de ejecución. Para obtener más información y un ejemplo de código, consulte [habilitación de la cuenta de servicio para acceder a las propiedades de SCP](enabling-service-account-to-access-scp-properties.md).

Un servicio que se ejecuta con la cuenta LocalSystem puede crear un punto de conexión como un objeto secundario bajo su propio objeto de equipo en el directorio. Este tipo de servicio es una excepción a la regla de servicios que no crea sus propios puntos de conexión. Un servicio LocalSystem también tiene permiso para modificar las propiedades de los objetos de punto de conexión bajo su propio objeto de equipo. Tenga en cuenta que un servicio solo debe ejecutarse con la cuenta LocalSystem si es absolutamente necesario. Para obtener más información, consulte [directrices para seleccionar una cuenta de inicio de sesión de servicio](guidelines-for-selecting-a-service-logon-account.md).

La aplicación que crea un objeto de punto de conexión, o cualquier objeto, debe tener permisos create Child para la clase de objeto que se va a crear en el contenedor donde se creará el objeto. Para quitar un objeto, el proceso que realiza la operación debe tener permisos eliminar secundarios para que la clase de objeto se elimine en el contenedor que contiene el objeto, o tener permisos de eliminación en el propio objeto. Para actualizar un punto de conexión, el proceso que realiza la operación debe tener acceso de escritura a las propiedades que se van a actualizar en el objeto.

 

 




