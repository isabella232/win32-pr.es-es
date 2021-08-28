---
description: Los registros son una manera de comunicarse entre los nodos de un grafo o los miembros de un grupo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3066bb6d309ce70a790947f002e1a74eb329c862ffcb0ef2c1766ca315323f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675005"
---
# <a name="records"></a>Registros

Los registros son una manera de comunicarse entre los nodos de un grafo o los miembros de un grupo. Un registro consta de las dos partes siguientes:

-   Encabezado de registro
-   Contenido de datos opacos específico

El encabezado contiene información sobre el registro, incluida la versión, el creador y el tipo de datos que se publican. El encabezado también contiene un campo atributos XML que permite a las aplicaciones agregar atributos de nombre-valor que describen los datos y buscar eficazmente en la base de datos de registros registros específicos que se han publicado previamente. El contenido son los datos definidos por la aplicación y es opaco para la infraestructura del mismo nivel.

Cuando se publica un registro, este (encabezado y datos) se desborda en todo el gráfico o grupo. Los pares sincronizados reciben estos datos y los almacenan en una base de datos local. Los pares sin sincronizar y sin conexión reciben los datos la próxima vez que se conectan y se sincronizan con el grafo o grupo del mismo nivel.

Para obtener información sobre cómo trabajar con registros, vea los temas siguientes:

-   [Dependencias de registros](record-dependencies.md)
-   [Administración de registros](record-management.md)
-   [Esquema de atributo de registro](record-attribute-schema.md)
-   [Formato de consulta de búsqueda de registros](record-search-query-format.md)

 

 



