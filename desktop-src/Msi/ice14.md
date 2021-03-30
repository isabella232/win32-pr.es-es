---
description: ICE14 valida la tabla de características de una base de datos Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360864"
---
# <a name="ice14"></a>ICE14

ICE14 valida las características siguientes:

-   Dichas características principales de raíz no tienen el bit msidbFeatureAttributesFollowParent establecido en la columna Attributes de la [tabla de características](feature-table.md). Una característica raíz no tiene un elemento primario.
-   No hay ninguna característica que tenga la misma entrada en las \_ columnas primarias de características y características de la [tabla de características](feature-table.md). Ninguna característica puede ser su propio elemento primario.

## <a name="result"></a>Resultado

ICE14 envía un mensaje de error si encuentra una característica raíz con el conjunto de bits msidbFeatureAttributesFollowParent o una característica con entradas idénticas en las \_ columnas primarias de características y características de la tabla de características.

## <a name="example"></a>Ejemplo

ICE14 devolverá los siguientes errores en el ejemplo siguiente:

-   La característica deporte tiene el mismo valor en las columnas principales característica y característica \_ de la tabla archivo.
-   El deporte de la característica raíz tiene establecido el bit msidbFeatureAttributesFollowParent.

En el árbol de características de este ejemplo, deporte es la característica raíz y una principal de las características de natación y fútbol. Freestyle es una característica secundaria de natación. TouchFootball es una característica secundaria de fútbol.

[Tabla de características](feature-table.md) (parcial)



| Característica       | Atributos | Característica \_ principal |
|---------------|------------|-----------------|
| Deporte         | 4          | Deporte           |
| Estiliza      | 1          | Deporte           |
| Balón      | 4          | Deporte           |
| Freestyle     | 1          | Estiliza        |
| TouchFootball | 4          | Balón        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



