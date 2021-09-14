---
title: Esquema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Más información sobre: Esquema EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243368"
---
# <a name="eventmanifest-schema"></a>Esquema EventManifest

El esquema EventManifest define los siguientes elementos y tipos que se usan para escribir un manifiesto de instrumentación:

-   [Elementos EventManifestSchema](eventmanifestschema-elements.md)
-   [Tipos simples de EventManifestSchema](eventmanifestschema-simple-types.md)
-   [Tipos complejos de EventManifestSchema](eventmanifestschema-complex-types.md)

La sección elements contiene los nombres de los elementos que se usan en el manifiesto; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

Un manifiesto de instrumentación es un archivo XML que define un proveedor de eventos, los canales en los que se escriben los eventos, los propios eventos, los criterios de filtrado de eventos, como niveles, tareas y códigos de operación, y las cadenas localizadas que se usan al representar los eventos. La convención es usar .man como extensión para los archivos de manifiesto. Para obtener más información sobre cómo escribir un manifiesto, vea [Escribir un manifiesto de instrumentación.](writing-an-instrumentation-manifest.md)

El SDK Windows incluye el esquema en el \\ archivo \\ Include Eventman.xsd. Puede usar xsd para validar el manifiesto.

Además del esquema EventManifest, Windows registro de eventos también define los siguientes esquemas:

-   [Esquema de](eventschema-schema.md)eventos: define los elementos y tipos usados para representar un evento.
-   [Esquema de](queryschema-schema.md)consulta: define los elementos y tipos usados para escribir una consulta para recuperar eventos de uno o varios canales.

 

 




