---
description: La API de la tabla de enrutamiento distribuida (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: Table API de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082659"
---
# <a name="distributed-routing-table-api"></a>Table API de enrutamiento distribuido

La API de la tabla de enrutamiento distribuida (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.

Una aplicación que usa DRT puede realizar lo siguiente:

-   Cree tablas de enrutamiento distribuido específicas de la aplicación.
-   Registrar claves y asociarlas con direcciones IP y datos de aplicaciones.
-   Busque claves y recupere las direcciones IP y los datos de aplicación asociados a ellas. Esta funcionalidad se puede usar para crear tablas de hash distribuidas (DHTs), sistemas de resolución de nombres sin servidor y redes de malla superpuestas de muchas topologías.

> [!Note]  
> Los administradores y los usuarios de aplicaciones habilitadas para DRT deben tener en cuenta la información que se publica en los usuarios finales. Los servidores de Microsoft no se emplean en esta tecnología y la información no se envía a Microsoft.

 

La documentación proporcionada para esta API se divide en tres secciones.



| Sección                                                                                | Descripción                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)               | Información que detalla el ciclo de vida y los cambios de estado de la API de DRT.<br/>                                    |
| [Usar el Table API de enrutamiento distribuido](using-the-distributed-routing-table-api.md) | Información que detalla el uso general de la API de DRT.<br/>                                                   |
| [Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md) | Información que detalla las funciones, estructuras de datos y constantes enumeradas que componen la API de DRT.<br/> |



 

 

 




