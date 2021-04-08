---
title: Notificaciones de cambio en Active Directory Domain Services
description: Active Directory Domain Services proporcionar un mecanismo para que una aplicación cliente se registre en un controlador de dominio para recibir notificaciones de cambios.
ms.assetid: 27f6c7c1-b32e-457a-9be5-47836d097ab1
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee564727cfbcb2bfdb367f822fdc137bca7c4e37
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077562"
---
# <a name="change-notifications-in-active-directory-domain-services"></a>Notificaciones de cambio en Active Directory Domain Services

Active Directory Domain Services proporcionar un mecanismo para que una aplicación cliente se registre en un controlador de dominio para recibir notificaciones de cambios. Para ello, el cliente especifica el control de notificación de cambio LDAP en una operación de búsqueda LDAP asincrónica. El cliente también especifica los siguientes parámetros de búsqueda.



| Parámetro             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ámbito<br/>      | Especifique una **\_ \_ base de ámbito LDAP** para supervisar solo el objeto o **el \_ ámbito LDAP \_ onelevel** para supervisar los elementos secundarios inmediatos del objeto, sin incluir el propio objeto. No especifique el **\_ \_ subárbol del ámbito LDAP**. Aunque se admite el ámbito de subárbol si el objeto base es la raíz de un contexto de nomenclatura, su uso puede afectar gravemente al rendimiento del servidor, ya que genera un mensaje de resultado de búsqueda LDAP cada vez que se modifica un objeto en el contexto de nomenclatura. No se puede especificar el **\_ \_ subárbol de ámbito LDAP** para un subárbol arbitrario.<br/> |
| Filter<br/>     | Especifique un filtro de búsqueda de "(objectClass = \* )", lo que significa que recibirá notificaciones de cambios en cualquier objeto del ámbito especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| Atributos<br/> | Especifique una lista de atributos que se devolverán cuando se produzca un cambio. Tenga en cuenta que recibirá notificaciones cuando se modifique algún atributo, no solo los atributos especificados.<br/>                                                                                                                                                                                                                                                                                                                                                                               |



 

Puede registrar hasta cinco solicitudes de notificación en una única conexión LDAP. Debe tener un subproceso dedicado que espera las notificaciones y las procesa rápidamente. Cuando se llama a la \_ función ext de búsqueda LDAP \_ para registrar una solicitud de notificación, la función devuelve un identificador de mensaje que identifica esa solicitud. A continuación, se usa la función de [**\_ resultado LDAP**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result) para esperar las notificaciones de cambio. Cuando se produce un cambio, el servidor envía un mensaje LDAP que contiene el identificador de mensaje para la solicitud de notificación que generó la notificación. Esto hace que la función de **\_ resultado LDAP** devuelva los resultados de búsqueda que identifican el objeto que ha cambiado.

La aplicación cliente debe determinar el estado inicial del objeto supervisado. Para ello, primero debe registrar la solicitud de notificación y luego leer el estado actual.

La aplicación cliente también debe determinar la causa del cambio. En una búsqueda de nivel base, se produce una notificación cuando cambia cualquier atributo o cuando se elimina o se mueve el objeto. En una búsqueda de un solo nivel, se produce una notificación cuando se crea, se elimina, se mueve o se modifica un objeto secundario. Tenga en cuenta que al mover o cambiar el nombre de un objeto en la jerarquía sobre un objeto de destino, no se genera una notificación aunque el nombre distintivo del destino cambie como resultado. Por ejemplo, si supervisa los cambios en los objetos secundarios de un contenedor, no recibirá notificaciones si el propio contenedor se mueve o se cambia de nombre.

Cuando el cliente procesa los resultados de la búsqueda, puede usar la \_ función LDAP Get \_ DN para obtener el nombre distintivo del objeto que cambió. No confíe en nombres distintivos para identificar los objetos de los que se realiza un seguimiento, ya que los nombres distintivos pueden cambiar. En su lugar, incluya el atributo **objectGUID** en la lista de atributos que se van a recuperar. **ObjectGUID** de cada objeto permanece sin modificar, independientemente de dónde se mueva el objeto dentro del bosque de la empresa.

Si se elimina un objeto dentro del ámbito de búsqueda, el cliente recibe una notificación de cambio y el atributo **IsDeleted** del objeto se establece en **true**. En este caso, los resultados de la búsqueda informan del nuevo nombre distintivo del objeto en el contenedor de objetos eliminados de su partición. No es necesario especificar el control de marcadores de exclusión ([ \_ servidor LDAP \_ Mostrar \_ \_ OID eliminado](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)) para obtener notificaciones de eliminaciones de objetos. Para obtener más información, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).

Cuando un cliente ha registrado una solicitud de notificación, el cliente sigue recibiendo notificaciones hasta que se interrumpe la conexión o el cliente abandona la búsqueda mediante una llamada a la \_ función de abandono de LDAP. Si el cliente o el servidor se desconectan, por ejemplo, si se produce un error en el servidor, se finaliza la solicitud de notificación. Cuando el cliente se vuelve a conectar, debe registrarse para recibir notificaciones de nuevo y, a continuación, leer el estado actual de los objetos de interés en caso de que se hayan producido cambios mientras se desconectó el cliente.

El cliente puede utilizar el valor del atributo **uSNChanged** de un objeto para determinar si el estado actual del objeto en el servidor refleja los cambios más recientes que el cliente ha recibido. El sistema aumenta el atributo **uSNChanged** de un objeto cuando se mueve o se modifica el objeto. Por ejemplo, si se produce un error en el servidor y la partición de directorio se restaura a partir de una copia de seguridad, es posible que la réplica del servidor de un objeto no refleje los cambios previamente comunicados al cliente, en cuyo caso el valor de **uSNChanged** en el servidor será menor que el valor almacenado por el cliente.

Para obtener más información y un ejemplo de código que usa el control de notificación de cambios de LDAP en una operación de búsqueda LDAP asincrónica, vea el [código de ejemplo para recibir notificaciones de cambios](example-code-for-receiving-change-notifications.md).

Para obtener más información acerca de Cuándo usar el control de notificación de cambios de LDAP, vea [información general sobre las técnicas de Change Tracking](overview-of-change-tracking-techniques.md).

 

