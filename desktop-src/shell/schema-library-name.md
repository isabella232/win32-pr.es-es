---
description: El &lt; elemento name especifica el nombre de esta &gt; biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: elemento name (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574520"
---
# <a name="name-element-library-schema"></a>elemento name (esquema de biblioteca)

El &lt; elemento name especifica el nombre de esta &gt; biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.

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
| [elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Observaciones

El nombre es el nombre descriptivo de la biblioteca que se muestra en Windows Explorer. El nombre se puede especificar en formato &lt; de índice &gt; dllname, como en el ejemplo &lt; &gt; siguiente.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
