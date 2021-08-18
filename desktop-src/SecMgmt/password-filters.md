---
description: Filtros de contraseña
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Filtros de contraseña
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5771fce0e8cbb2826bcf79344e2813587db6dcedc831d7e879b42ab74698b9a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894011"
---
# <a name="password-filters"></a>Filtros de contraseña

Los filtros de contraseña proporcionan una manera de implementar la directiva de contraseñas y la notificación de cambio.

Cuando se realiza una solicitud de cambio de contraseña, la autoridad de seguridad [*local*](/windows/desktop/SecGloss/l-gly) (LSA) llama a los filtros de contraseña registrados en el sistema. Cada filtro de contraseña se llama dos veces: primero para validar la nueva contraseña y, después de que todos los filtros hayan validado la nueva contraseña, para notificar a los filtros que se ha realizado el cambio. En la siguiente ilustración se muestra este proceso.

![solicitud de cambio de contraseña](images/pswdfilte.png)

La notificación de cambio de contraseña se usa para sincronizar los cambios de contraseña con bases de datos de cuentas externas.

Los filtros de contraseña se usan para aplicar la directiva de contraseñas. Los filtros validan las contraseñas nuevas e indican si la nueva contraseña se ajusta a la directiva de contraseñas implementada.

Para obtener información general sobre el uso de filtros de contraseña, vea [Usar filtros de contraseña.](using-password-filters.md)

Para obtener una lista de las funciones de filtro de contraseñas, vea [Funciones de filtro de contraseñas.](management-functions.md)

En los temas siguientes se proporciona más información sobre los filtros de contraseña:

-   [Consideraciones de programación del filtro de contraseñas](password-filter-programming-considerations.md)
-   [Aplicación de contraseñas seguras y Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
