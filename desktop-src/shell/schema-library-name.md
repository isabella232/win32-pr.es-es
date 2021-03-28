---
description: El <name> elemento especifica el nombre de esta biblioteca. Este elemento es obligatorio y no tiene atributos ni elementos secundarios.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Name (elemento, esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997956"
---
# <a name="name-element-library-schema"></a>Name (elemento, esquema de biblioteca)

El <name> elemento especifica el nombre de esta biblioteca. Este elemento es obligatorio y no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Sintaxis

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Información de elemento



| Elemento primario                                                               | Elementos secundarios |
|------------------------------------------------------------------------------|----------------|
| [Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Observaciones

El nombre es el nombre descriptivo de la biblioteca que se muestra en el explorador de Windows. El nombre se puede especificar en un <dllname> <index> formato, como en el ejemplo siguiente.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Esquema de Descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
