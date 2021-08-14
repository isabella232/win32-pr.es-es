---
description: A medida que cada entrada de servicio se lee de la base de datos de servicios instalados, el SCM crea un registro de servicio para el servicio.
ms.assetid: c0ee43e2-af9b-4578-9017-46a5ed50b938
title: Lista de registros de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef0bdebed5e302b1dc59bea6494fd812ec506e7e6d2531634b2a6686b86bc98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888859"
---
# <a name="service-record-list"></a>Lista de registros de servicio

A medida que cada entrada de servicio se lee de la base de datos de servicios instalados, el SCM crea un registro de servicio para el servicio. Un registro de servicio incluye:

-   Nombre del servicio
-   Tipo de inicio (inicio automático o inicio a petición)
-   Estado del servicio (consulte la [**estructura SERVICE \_ STATUS)**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) <dl> Tipo  
    Estado actual  
    Códigos de control aceptables  
    Código de salida  
    Sugerencia de espera  
    </dl>
-   Pointer to dependency list

El nombre de usuario y la contraseña de una cuenta se especifican en el momento en que se instala el servicio. El SCM almacena el nombre de usuario en el registro y la contraseña en una parte segura de la autoridad de seguridad local (LSA). El administrador del sistema puede crear cuentas con contraseñas que nunca expiren. Como alternativa, el administrador del sistema puede crear cuentas con contraseñas que expiren y administrar las cuentas cambiando las contraseñas periódicamente.

El SCM conserva dos copias de la contraseña de una cuenta de usuario, una contraseña actual y una contraseña de copia de seguridad. La contraseña especificada la primera vez que se instala el servicio se almacena como la contraseña actual y la contraseña de copia de seguridad no se inicializa. Cuando el SCM intenta ejecutar el servicio en el contexto de seguridad de la cuenta de usuario, usa la contraseña actual. Si la contraseña actual se usa correctamente, también se guarda como contraseña de copia de seguridad. Si la contraseña se modifica con la función [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o la utilidad del panel de control Servicios, la nueva contraseña se almacena como la contraseña actual y la contraseña anterior se almacena como contraseña de copia de seguridad. Si el SCM intenta iniciar el servicio y se produce un error en la contraseña actual, usa la contraseña de copia de seguridad. Si la contraseña de copia de seguridad se usa correctamente, se guarda como la contraseña actual.

El SCM actualiza el estado del servicio cuando un servicio le envía notificaciones de estado mediante la [**función SetServiceStatus.**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) El SCM mantiene el estado de un servicio de controlador consultando el sistema de E/S, en lugar de recibir notificaciones de estado, como hace desde un servicio.

Un servicio puede registrar información de tipo adicional llamando a la [**función SetServiceBits.**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits) Las [**funciones NetServerGetInfo**](/windows/desktop/api/lmserver/nf-lmserver-netservergetinfo) [**y NetServerEnum**](/windows/desktop/api/lmserver/nf-lmserver-netserverenum) obtienen los tipos de servicio admitidos.

 

 
