---
title: Tipos percibidos (características heredadas Windows entorno)
description: PerceivedType es una propiedad que clasifica un elemento en el índice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360724"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Tipos percibidos (características heredadas Windows entorno)

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

`PerceivedType` es una propiedad que clasifica un elemento en el índice. Esta clasificación es diferente de la clasificación [](-search-2x-wds-aqsreference.md) de "tipo" que usa la sintaxis de consulta avanzada, pero de forma similar permite a los usuarios refinar sus resultados de búsqueda. El tipo AQS permite a los usuarios limitar su consulta de búsqueda, mientras que la propiedad PerceivedType permite a los usuarios filtrar su conjunto de resultados.

## <a name="types"></a>Tipos

Use la propiedad PerceivedType para clasificar el tipo de archivo para que los usuarios puedan filtrar los resultados de la búsqueda por tipo. La salida debe ser una de las cadenas siguientes:

-   contact
-   comunicaciones
-   comunicaciones/correo electrónico
-   comunicaciones/calendario
-   comunicaciones/tarea
-   communications/im
-   documento
-   document/note
-   document/text
-   documento/hoja de cálculo
-   documento/presentación
-   music
-   images
-   imágenes/imagen
-   imágenes/vídeo
-   folder
-   programa

Por ejemplo, si desea crear un complemento de filtro para un nuevo tipo de archivo de imagen, debe implementar lo siguiente en la [**interfaz IFilter:**](/windows/desktop/api/filter/nn-filter-ifilter)

-   **GetChunk** para devolver un FULLPROPSPEC que incluye: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** para devolver un PROPVARIANT que incluye: VT \_ LPWSTR = "images/picture"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
