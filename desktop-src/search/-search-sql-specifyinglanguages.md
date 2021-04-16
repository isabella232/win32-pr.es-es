---
description: Puede especificar el idioma que se usa en las consultas de búsqueda.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Especificar idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540662"
---
# <a name="specifying-languages"></a>Especificar idiomas

Puede especificar el idioma que se usa en las consultas de búsqueda. Los predicados FREETEXT y Contains de la cláusula WHERE admiten la especificación de un idioma. Puede indicar el lenguaje de consulta proporcionando un identificador de código de idioma (LCID) numérico en el predicado CONTAINS o FREETEXT. Este LCID especifica el separador de palabras que se va a utilizar para analizar la cadena de consulta. Utiliza la siguiente sintaxis:


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Para obtener más información, vea la sintaxis de los predicados [Contains](-search-sql-contains.md) y [FREETEXT](-search-sql-freetext.md) .

 

 



