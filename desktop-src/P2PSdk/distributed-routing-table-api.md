---
description: La API de tabla de enrutamiento distribuido (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.
ms.assetid: 17422d71-4c6d-458b-87b6-b31fc2b5bda5
title: Enrutamiento distribuido Table API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9f8c2b435e1c0c813fb279c40b9bbfa9afb6b23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073942"
---
# <a name="distributed-routing-table-api"></a>Enrutamiento distribuido Table API

La API de tabla de enrutamiento distribuido (DRT) permite a las aplicaciones publicar y resolver claves numéricas en una red del mismo nivel.

Una aplicación que utiliza DRT puede realizar lo siguiente:

-   Cree tablas de enrutamiento distribuido específicas de la aplicación.
-   Registre las claves y asocie estas claves con direcciones IP y datos de aplicación.
-   Busque claves y recupere las direcciones IP y los datos de aplicación asociados a ellas. Esta funcionalidad se puede usar para construir tablas hash distribuidas (DHT), sistemas de resolución de nombres sin servidor y redes de malla superpuestas de muchas topologías.

> [!Note]  
> Los administradores y usuarios de las aplicaciones habilitadas para DRT deben hacer que los usuarios finales de sus aplicaciones conozcan la información que se publica. Esta tecnología no emplea los servidores de Microsoft y la información no se envía a Microsoft.

 

La documentación proporcionada para esta API se divide en tres secciones.



| Sección                                                                                | Descripción                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)               | Información que detalla el ciclo de vida y los cambios de estado de la API de DRT.<br/>                                    |
| [Uso del enrutamiento distribuido Table API](using-the-distributed-routing-table-api.md) | Información que detalla el uso general de la API de DRT.<br/>                                                   |
| [Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md) | Información que detalla las funciones, las estructuras de datos y las constantes enumeradas que componen la API de DRT.<br/> |



 

 

 




