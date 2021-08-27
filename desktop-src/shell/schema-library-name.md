---
description: El &lt; elemento name especifica el nombre de esta &gt; biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: elemento name (Esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880861"
---
# <a name="name-element-library-schema"></a>elemento name (Esquema de biblioteca)

El &lt; elemento name especifica el nombre de esta &gt; biblioteca. Este elemento es necesario y no tiene atributos ni elementos secundarios.

## <a name="syntax"></a>Syntax

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



 

## <a name="remarks"></a>Comentarios

El nombre es el nombre descriptivo de la biblioteca que se muestra en Windows Explorer. El nombre se puede especificar en un formato &lt; dllname &gt; , &lt; &gt; index, como en el ejemplo siguiente.


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

[Esquema de descripción del conector de búsqueda](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
