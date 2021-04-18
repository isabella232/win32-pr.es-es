---
description: Más información acerca de cómo convertir el tipo de datos de una columna
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Conversión del tipo de datos de una columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715005"
---
# <a name="casting-the-data-type-of-a-column"></a>Conversión del tipo de datos de una columna

En ocasiones, puede que necesite convertir los datos de cadena extraídos de los documentos como otro tipo de datos, de modo que se pueda realizar una comparación adecuada. Convierta un identificador o un literal como otro tipo de datos con la siguiente sintaxis:


```
CAST (<identifier> | <literal> AS <datatype>)
```



Por ejemplo:


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignaciones de tipos de datos](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



