---
title: Esquema de consulta
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Más información sobre: Esquema de consulta'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 14beeaf8c4d739e490de972107fedf279e16e75b5401f63a709d43b03c338c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005175"
---
# <a name="query-schema"></a>Esquema de consulta

El esquema de consulta define los siguientes elementos y tipos que puede usar para escribir una consulta XML estructurada para recuperar eventos de un canal o archivo de registro:

-   [Elementos QuerySchema](queryschema-elements.md)
-   [Tipos complejos de QuerySchema](queryschema-complex-types.md)

La sección elements contiene los nombres de los elementos que se usan en la consulta; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

Una consulta puede contener una o varias expresiones XPath que se usan para incluir o excluir eventos en el conjunto de resultados de la consulta. Puede consultar eventos de varios canales o archivos de registro, pero no puede mezclar canales y archivos de registro. Puede usar una consulta en cualquier función que tome un XPath (por ejemplo, las funciones [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe).**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) Cada XPath que especifique se limita a 32 expresiones. Para obtener un ejemplo, vea [Consumo de eventos](consuming-events.md).

El SDK Windows incluye el esquema en el \\ archivo \\ Query.xsd de include.

Además del esquema de consulta, Windows de eventos también define los esquemas siguientes:

-   [Esquema eventManifest:](eventmanifestschema-schema.md)define los elementos y tipos usados para escribir un manifiesto de instrumentación.
-   [Esquema de](eventschema-schema.md)eventos: define los elementos y tipos usados para representar un evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consumo de eventos](consuming-events.md)
</dt> </dl>

 

 




