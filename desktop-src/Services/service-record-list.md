---
description: A medida que cada entrada de servicio se lee de la base de datos de servicios instalados, el SCM crea un registro de servicio para el servicio.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Lista de registros de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1143625de977c7e5c488c5cc56620adc3a5454db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666493"
---
# <a name="service-record-list"></a>Lista de registros de servicio

A medida que cada entrada de servicio se lee de la base de datos de servicios instalados, el SCM crea un registro de servicio para el servicio. Un registro de servicio incluye:

-   Nombre del servicio
-   Tipo de inicio (inicio automático o inicio a petición)
-   Estado del servicio (consulte la estructura de [**\_ Estado del servicio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) ) <dl> Tipo  
    Estado actual  
    Códigos de control aceptables  
    Código de salida  
    Sugerencia de espera  
    </dl>
-   Pointer to dependency list

El nombre de usuario y la contraseña de una cuenta se especifican en el momento en que se instala el servicio. El SCM almacena el nombre de usuario en el registro y la contraseña en una parte segura de la autoridad de seguridad local (LSA). El administrador del sistema puede crear cuentas con contraseñas que nunca expiran. Como alternativa, el administrador del sistema puede crear cuentas con contraseñas que expiren y administrar las cuentas cambiando las contraseñas periódicamente.

El SCM conserva dos copias de la contraseña de una cuenta de usuario, una contraseña actual y una contraseña de copia de seguridad. La contraseña especificada la primera vez que se instala el servicio se almacena como la contraseña actual y no se inicializa la contraseña de copia de seguridad. Cuando el SCM intenta ejecutar el servicio en el contexto de seguridad de la cuenta de usuario, usa la contraseña actual. Si la contraseña actual se utiliza correctamente, también se guarda como contraseña de copia de seguridad. Si se modifica la contraseña con la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) , o la utilidad servicios del panel de control, la nueva contraseña se almacena como la contraseña actual y la contraseña anterior se almacena como contraseña de copia de seguridad. Si el SCM intenta iniciar el servicio y se produce un error en la contraseña actual, se usa la contraseña de copia de seguridad. Si la contraseña de copia de seguridad se utiliza correctamente, se guarda como la contraseña actual.

El SCM actualiza el estado del servicio cuando un servicio envía notificaciones de estado mediante la función [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) . El SCM mantiene el estado de un servicio de controlador consultando el sistema de e/s, en lugar de recibir notificaciones de estado, como lo hace desde un servicio.

Un servicio puede registrar información de tipo adicional mediante una llamada a la función [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) . Las funciones [**NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) y [**NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) obtienen los tipos de servicio admitidos.

 

 
