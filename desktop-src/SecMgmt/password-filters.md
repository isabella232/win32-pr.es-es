---
description: Filtros de contraseña
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073594"
---
# <a name="password-filters"></a>Filtros de contraseña

Los filtros de contraseña proporcionan una manera de implementar la directiva de contraseñas y la notificación de cambio.

Cuando se realiza una solicitud de cambio de contraseña, la autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) llama a los filtros de contraseña registrados en el sistema. Se llama a cada filtro de contraseña dos veces: primero para validar la nueva contraseña y, después, después de que todos los filtros hayan validado la nueva contraseña, para notificar a los filtros que se ha realizado el cambio. En la siguiente ilustración se muestra este proceso.

![solicitud de cambio de contraseña](images/pswdfilte.png)

La notificación de cambio de contraseña se usa para sincronizar los cambios de contraseña con bases de datos de cuentas externas.

Los filtros de contraseña se usan para aplicar la directiva de contraseñas. Los filtros validan las contraseñas nuevas e indican si la nueva contraseña se ajusta a la directiva de contraseñas implementada.

Para obtener información general sobre el uso de filtros de contraseña, vea [Usar filtros de contraseña.](using-password-filters.md)

Para obtener una lista de las funciones de filtro de contraseñas, vea [Funciones de filtro de contraseña.](management-functions.md)

En los temas siguientes se proporciona más información sobre los filtros de contraseña:

-   [Consideraciones sobre la programación de filtros de contraseñas](password-filter-programming-considerations.md)
-   [Aplicación de contraseñas seguras y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
