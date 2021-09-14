---
description: ICE14 valida la tabla Feature de una base de Windows Installer.
ms.assetid: fb1970f8-1dba-4b06-aa03-5b33d213fc79
title: ICE14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2e64a6106ae359fe02c6ead271bbae267eeb18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074663"
---
# <a name="ice14"></a>ICE14

ICE14 valida lo siguiente para las características:

-   Las características principales raíz no tienen el bit msidbFeatureAttributesFollowParent establecido en la columna Atributos de la [tabla Característica](feature-table.md). Una característica raíz no tiene un elemento primario.
-   Que ninguna característica tenga la misma entrada en las columnas Característica y Elemento \_ primario de la tabla [Característica](feature-table.md). Ninguna característica puede ser su propio elemento primario.

## <a name="result"></a>Resultado

ICE14 envía un mensaje de error si encuentra una característica raíz con el conjunto de bits msidbFeatureAttributesFollowParent o una característica con entradas idénticas en las columnas Feature y Feature Parent de la tabla \_ Feature.

## <a name="example"></a>Ejemplo

ICE14 devolvería los errores siguientes para el ejemplo siguiente:

-   La característica Sport tiene el mismo valor en las columnas Característica y Elemento \_ primario de la tabla Archivo.
-   La característica raíz Sport tiene el conjunto de bits msidbFeatureAttributesFollowParent.

En el árbol de características de este ejemplo, el deporte es la característica raíz y un elemento primario de las características de la nada y el fútbol. Freestyle es una característica secundaria de La nada. TouchFootball es una característica secundaria del fútbol.

[Tabla de características](feature-table.md) (parcial)



| Característica       | Atributos | Elemento \_ primario de la característica |
|---------------|------------|-----------------|
| Deporte         | 4          | Deporte           |
| Natación      | 1          | Deporte           |
| Fútbol      | 4          | Deporte           |
| Freestyle     | 1          | Natación        |
| TouchFootball | 4          | Fútbol        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



