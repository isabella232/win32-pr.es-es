---
title: Ordenar (ADSI)
description: Un cliente puede solicitar a un servidor que ordene el conjunto de resultados.
ms.assetid: 795d27f0-0bfa-417e-aa1f-f2471f92dc45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e4ee790a646367366afe33639abd8f5aa57ed4f
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105656303"
---
# <a name="sorting-adsi"></a>Ordenar (ADSI)

Un cliente puede solicitar a un servidor que ordene el conjunto de resultados. Puede especificar:

-   Criterio de ordenación: se puede especificar el criterio de ordenación ascendente o descendente.
-   Atributos de ordenación: se pueden especificar varios atributos en una cadena de ordenación. Por ejemplo, ordene por Apellido y luego por nombre.

Al especificar el criterio de ordenación, debe intentar usar uno de los atributos indizados. De lo contrario, el servidor debe calcular un conjunto de resultados completo antes de enviarlo al cliente. Esto es así incluso si ha solicitado una búsqueda paginada y ha especificado un tamaño de página.

> [!Note]  
> No todos los servidores de directorio admiten varias ordenaciones de atributos o criterios de ordenación.

 

 

 




