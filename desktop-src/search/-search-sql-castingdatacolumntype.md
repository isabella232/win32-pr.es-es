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
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="93383-103">Conversión del tipo de datos de una columna</span><span class="sxs-lookup"><span data-stu-id="93383-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="93383-104">En ocasiones, puede que necesite convertir los datos de cadena extraídos de los documentos como otro tipo de datos, de modo que se pueda realizar una comparación adecuada.</span><span class="sxs-lookup"><span data-stu-id="93383-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="93383-105">Convierta un identificador o un literal como otro tipo de datos con la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="93383-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="93383-106">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="93383-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="93383-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="93383-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93383-108">Asignaciones de tipos de datos</span><span class="sxs-lookup"><span data-stu-id="93383-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



