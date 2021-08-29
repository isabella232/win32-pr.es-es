---
description: El servicio Distribución del mismo nivel de Microsoft admite las siguientes estructuras.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Estructuras de API de distribución del mismo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afc985ff7a1e8dccdaf9c26cee8380daeccbf4b803f563510c3524a9d5c0c2c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776035"
---
# <a name="peer-distribution-api-structures"></a>Estructuras de API de distribución del mismo nivel

El servicio Distribución del mismo nivel de Microsoft admite las siguientes estructuras.



| Estructura                                                              | Descripción                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INFORMACIÓN BÁSICA DEL \_ CLIENTE \_ PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Indica si hay o no muchos clientes que descargan simultáneamente el mismo contenido.                                                                                                                                                                                             |
| [**ETIQUETA DE CONTENIDO \_ \_ PEERDIST**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Contiene una etiqueta proporcionada por el cliente que es un valor de entrada [**para PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). La etiqueta está asociada al segmento de contenido y se usa en las API de administración de contenido, como [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**OPCIONES DE PUBLICACIÓN \_ \_ PEERDIST**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Contiene opciones de publicación, incluida la información de la versión de la API y las posibles marcas de opción.                                                                                                                                                                                           |
| [**OPCIONES DE \_ RECUPERACIÓN \_ DEL MISMO NIVEL**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Contiene la versión de la información de contenido que se recuperará.                                                                                                                                                                                                                                 |
| [**INFORMACIÓN DE ESTADO \_ DE PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Contiene información sobre el estado actual y las funcionalidades del servicio BranchCache en el equipo local.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de distribución del mismo nivel](peer-distribution-api-reference.md)
</dt> </dl>

 

 



