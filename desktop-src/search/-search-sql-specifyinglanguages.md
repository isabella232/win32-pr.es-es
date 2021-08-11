---
description: Puede especificar el idioma que se usa en las consultas de búsqueda.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Especificar idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ab2b5b5c5da4e9f71e49330d966895415467a671289bd4f5607e1265d22a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118226820"
---
# <a name="specifying-languages"></a>Especificar idiomas

Puede especificar el idioma que se usa en las consultas de búsqueda. Los predicados FREETEXT y CONTAINS de la cláusula WHERE admiten la especificación de un idioma. Puede indicar el lenguaje de consulta proporcionando un identificador numérico de código de idioma (LCID) en el predicado CONTAINS o FREETEXT. Este LCID especifica qué separador de palabras se va a usar para analizar la cadena de consulta. Utiliza la siguiente sintaxis:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Para obtener más información, vea la sintaxis de los predicados [CONTAINS](-search-sql-contains.md) y [FREETEXT.](-search-sql-freetext.md)

 

 



