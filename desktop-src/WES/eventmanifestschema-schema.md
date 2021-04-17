---
title: Esquema EventManifest
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 'Más información acerca de: esquema de EventManifest'
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697161"
---
# <a name="eventmanifest-schema"></a>Esquema EventManifest

El esquema EventManifest define los siguientes elementos y tipos que se usan para escribir un manifiesto de instrumentación:

-   [Elementos EventManifestSchema](eventmanifestschema-elements.md)
-   [EventManifestSchema tipos simples](eventmanifestschema-simple-types.md)
-   [Tipos complejos de EventManifestSchema](eventmanifestschema-complex-types.md)

La sección Elements contiene los nombres de los elementos que se usan en el manifiesto; sin embargo, para obtener los detalles de cada elemento, vea el tipo complejo que contiene el elemento.

Un manifiesto de instrumentación es un archivo XML que define un proveedor de eventos, los canales en los que se escriben los eventos, los propios eventos, los criterios de filtrado de eventos, como niveles, tareas y códigos de acceso, y las cadenas localizadas que se utilizan al representar los eventos. La Convención es usar. man como extensión para los archivos de manifiesto. Para obtener más información sobre cómo escribir un manifiesto, consulte [escribir un manifiesto de instrumentación](writing-an-instrumentation-manifest.md).

El Windows SDK incluye el esquema en el \\ \\ archivo. xsd del evento include. Puede usar el XSD para validar el manifiesto.

Además del esquema EventManifest, el registro de eventos de Windows también define los esquemas siguientes:

-   [Esquema de eventos](eventschema-schema.md): define los elementos y los tipos que se usan para representar un evento.
-   [Esquema de consulta](queryschema-schema.md): define los elementos y tipos que se usan para escribir una consulta para recuperar eventos de uno o más canales.

 

 




