---
title: Problemas de seguridad de la publicación de servicios
description: El sistema restringe la capacidad de crear, modificar o eliminar objetos de punto de conexión. Tenga en cuenta y controle estas restricciones al publicar un servicio.
ms.assetid: 38e20a47-738d-4951-ad74-249039afeb52
ms.tgt_platform: multiple
keywords:
- Problemas de seguridad de Service Publication AD
- Active Directory, uso, seguridad, problemas de seguridad de publicación de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e4cec29d08a029bca52a99b573eb339964dd42274d3ca2e54795bb80b60897
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024913"
---
# <a name="security-issues-for-service-publication"></a>Problemas de seguridad de la publicación de servicios

El sistema restringe la capacidad de crear, modificar o eliminar objetos de punto de conexión. Tenga en cuenta y controle estas restricciones al publicar un servicio.

Los clientes deben ser capaces de confiar en los datos publicados en un objeto de punto de conexión en el directorio . Por este motivo, el permiso para crear un objeto de punto de conexión normalmente está restringido a los usuarios con privilegios, como los administradores de dominio. Esto evita que los usuarios no autorizados engañen a los clientes mediante la creación de puntos de conexión no válidos para servicios conocidos.

Los servicios no deben ejecutarse con privilegios de administrador de dominio. Esto significa que un servicio normalmente no puede crear su propio punto de conexión. En su lugar, proporcione una aplicación de instalación o configuración de servicio que cree el punto de conexión. Este instalador debe ejecutarlo un usuario con los privilegios necesarios.

Aunque un servicio normalmente no puede crear su punto de conexión, debe ser capaz de actualizar las propiedades del punto de conexión en tiempo de ejecución. Las propiedades del punto de conexión contienen los datos de enlace utilizados por los clientes para conectarse al servicio. Si los datos de enlace cambian, el servicio debe actualizar el punto de conexión; De lo contrario, los clientes no pueden usar el servicio. Esto significa que el instalador también debe modificar el descriptor de seguridad en el objeto de punto de conexión para permitir que el servicio lea y escriba las propiedades adecuadas en tiempo de ejecución. Para obtener más información y un ejemplo de código, vea [Enabling Service Account to Access SCP Properties](enabling-service-account-to-access-scp-properties.md).

Un servicio que se ejecuta en la cuenta LocalSystem puede crear un punto de conexión como un objeto secundario en su propio objeto de equipo en el directorio . Este servicio es una excepción a la regla de servicios que no crea sus propios puntos de conexión. Un servicio LocalSystem también tiene permiso para modificar las propiedades de los objetos de punto de conexión en su propio objeto de equipo. Tenga en cuenta que un servicio debe ejecutarse en la cuenta LocalSystem solo si es absolutamente necesario. Para obtener más información, vea [Directrices para seleccionar una cuenta de inicio de sesión de servicio.](guidelines-for-selecting-a-service-logon-account.md)

La aplicación que crea un objeto de punto de conexión, o cualquier objeto , debe tener permisos secundarios de creación para la clase de objeto que se va a crear en el contenedor donde se creará el objeto. Para quitar un objeto, el proceso que realiza la operación debe tener permisos secundarios de eliminación para la clase de objeto que se va a eliminar en el contenedor que contiene el objeto o tener permisos de eliminación en el propio objeto. Para actualizar un punto de conexión, el proceso que realiza la operación debe tener acceso de escritura a las propiedades que se actualizarán en el objeto .

 

 




