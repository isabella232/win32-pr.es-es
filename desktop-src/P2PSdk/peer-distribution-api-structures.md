---
description: El servicio de distribución del mismo nivel de Microsoft es compatible con las siguientes estructuras.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Estructuras de API de distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667409"
---
# <a name="peer-distribution-api-structures"></a>Estructuras de API de distribución del mismo nivel

El servicio de distribución del mismo nivel de Microsoft es compatible con las siguientes estructuras.



| Estructura                                                              | Descripción                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ información básica del cliente de PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Indica si hay muchos clientes que descargan simultáneamente el mismo contenido.                                                                                                                                                                                             |
| [**\_etiqueta de contenido de PEERDIST \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Contiene una etiqueta suministrada por el cliente que es un valor de entrada para [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). La etiqueta está asociada con el segmento de contenido y se usa en las API de administración de contenido, como [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**\_Opciones de publicación de PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Contiene opciones de publicación, incluida la información de versión de la API y posibles marcas de opciones.                                                                                                                                                                                           |
| [**\_Opciones de recuperación del mismo nivel \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Contiene la versión de la información de contenido que se va a recuperar.                                                                                                                                                                                                                                 |
| [**\_información de estado de PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Contiene información sobre el estado actual y las capacidades del servicio BranchCache en el equipo local.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de distribución del mismo nivel](peer-distribution-api-reference.md)
</dt> </dl>

 

 



