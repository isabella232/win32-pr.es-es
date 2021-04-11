---
description: Filtros de contraseña
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278984"
---
# <a name="password-filters"></a>Filtros de contraseña

Los filtros de contraseñas proporcionan una manera de implementar la Directiva de contraseñas y la notificación de cambios.

Cuando se realiza una solicitud de cambio de contraseña, la [*autoridad de seguridad local*](/windows/desktop/SecGloss/l-gly) (LSA) llama a los filtros de contraseña registrados en el sistema. Cada filtro de contraseña se llama dos veces: primero para validar la nueva contraseña y después, después de que todos los filtros hayan validado la nueva contraseña, para notificar a los filtros que se ha realizado el cambio. En la siguiente ilustración se muestra este proceso.

![solicitud de cambio de contraseña](images/pswdfilte.png)

La notificación de cambio de contraseña se usa para sincronizar los cambios de contraseña en las bases de datos de cuentas externas.

Los filtros de contraseñas se utilizan para exigir la Directiva de contraseñas. Los filtros validan nuevas contraseñas e indican si la nueva contraseña se ajusta a la Directiva de contraseñas implementadas.

Para obtener información general sobre el uso de filtros de contraseñas, consulte [uso de filtros de contraseñas](using-password-filters.md).

Para obtener una lista de las funciones de filtro de contraseñas, consulte [funciones de filtro de contraseñas](management-functions.md).

En los temas siguientes se proporciona más información acerca de los filtros de contraseñas:

-   [Consideraciones sobre la programación de filtros de contraseña](password-filter-programming-considerations.md)
-   [Aplicación segura de contraseñas y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
