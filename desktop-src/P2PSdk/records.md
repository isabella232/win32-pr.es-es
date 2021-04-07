---
description: Los registros son una manera de comunicarse entre los nodos de un gráfico o los miembros de un grupo.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9c2d3c5ae3bd80bc0b3c0ca100155fc8efd7c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002476"
---
# <a name="records"></a>Registros

Los registros son una manera de comunicarse entre los nodos de un gráfico o los miembros de un grupo. Un registro consta de las dos partes siguientes:

-   Encabezado de registro
-   Contenido de datos opacos específico

El encabezado contiene información sobre el registro, incluida la versión, el creador y el tipo de datos que se publican. El encabezado también contiene un campo de atributos XML que permite a las aplicaciones agregar atributos de nombre y valor que describen los datos, y buscar de forma eficaz en la base de datos de registros los registros específicos que se han publicado previamente. El contenido son los datos definidos por la aplicación y es opaco para la infraestructura del mismo nivel.

Cuando se publica un registro, se inunda (tanto el encabezado como los datos) en el gráfico o el grupo. Los pares sincronizados reciben estos datos y los almacenan en una base de datos local. Los pares no sincronizados y sin conexión reciben los datos la próxima vez que se conectan y se sincronizan con el grafo o el grupo del mismo nivel.

Para obtener información sobre cómo trabajar con registros, vea los temas siguientes:

-   [Dependencias de registro](record-dependencies.md)
-   [Administración de registros](record-management.md)
-   [Esquema de atributo de registro](record-attribute-schema.md)
-   [Formato de consulta de búsqueda de registros](record-search-query-format.md)

 

 



