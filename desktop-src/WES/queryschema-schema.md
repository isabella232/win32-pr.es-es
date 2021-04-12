---
title: Esquema de consulta
ms.assetid: 5710231b-5195-413e-8953-e47a411897a6
description: 'Más información acerca de: esquema de consulta'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aa9b6c842ff7acd874e8e467d07c31e298a63564
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278222"
---
# <a name="query-schema"></a>Esquema de consulta

El esquema de consulta define los siguientes elementos y tipos que puede usar para escribir una consulta XML estructurada para recuperar los eventos de un archivo de registro o canal:

-   [Elementos QuerySchema](queryschema-elements.md)
-   [Tipos complejos de QuerySchema](queryschema-complex-types.md)

La sección Elements contiene los nombres de los elementos que se usan en la consulta; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

Una consulta puede contener una o más expresiones XPath que se usan para incluir o excluir eventos en el conjunto de resultados de la consulta. Puede consultar eventos de varios canales o archivos de registro, pero no puede mezclar canales y archivos de registro. Puede usar una consulta en cualquier función que tome una expresión XPath (por ejemplo, las funciones [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) o [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) ). Cada XPath que especifique se limita a 32 expresiones. Para obtener un ejemplo, consulte [consumo de eventos](consuming-events.md).

El Windows SDK incluye el esquema en el \\ \\ archivo. xsd de la consulta de inclusión.

Además del esquema de consulta, el registro de eventos de Windows también define los esquemas siguientes:

-   [Esquema EventManifest](eventmanifestschema-schema.md): define los elementos y tipos que se usan para escribir un manifiesto de instrumentación.
-   [Esquema de eventos](eventschema-schema.md): define los elementos y los tipos que se usan para representar un evento.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Consumir eventos](consuming-events.md)
</dt> </dl>

 

 




