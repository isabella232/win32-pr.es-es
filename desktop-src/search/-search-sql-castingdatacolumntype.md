---
description: 'Más información sobre: Conversión del tipo de datos de una columna'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Conversión del tipo de datos de una columna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad09572ca80ed433ebba63e84d4b7ca8bacdb6bd5cae45c356e358cbe978b04c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094936"
---
# <a name="casting-the-data-type-of-a-column"></a>Conversión del tipo de datos de una columna

En ocasiones, es posible que tenga que convertir los datos de cadena extraídos de los documentos como otro tipo de datos, de modo que se pueda realizar una comparación adecuada. Convertir un identificador o literal como otro tipo de datos mediante la sintaxis siguiente:


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

[Asignaciones de tipo de datos](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



