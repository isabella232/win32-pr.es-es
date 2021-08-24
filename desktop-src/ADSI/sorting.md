---
title: Ordenación (ADSI)
description: Un cliente puede solicitar un servidor para ordenar el conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555b4b6f1868b2e4fddc1891cdf349ef6f44bc47dca6eb80e021ec49cb91b5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082229"
---
# <a name="sorting-adsi"></a>Ordenación (ADSI)

Un cliente puede solicitar un servidor para ordenar el conjunto de resultados. Puede especificar:

-   Criterio de ordenación: se puede especificar un criterio de ordenación ascendente o descendente.
-   Ordenar atributos: se pueden especificar varios atributos en una cadena de ordenación. Por ejemplo, ordene por apellido y, a continuación, por Nombre.

Al especificar el criterio de ordenación, debe intentar usar uno de los atributos indexados. De lo contrario, el servidor debe calcular un conjunto de resultados completo antes de enviarlo al cliente. Esto es así incluso si ha solicitado una búsqueda paginada y ha especificado un tamaño de página.

> [!Note]  
> No todos los servidores de directorios admiten varios ordenes de atributo o criterio de ordenación.

 

 

 




