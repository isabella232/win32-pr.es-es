---
title: Tipos percibidos (características heredadas del entorno de Windows)
description: PerceivedType es una propiedad que clasifica un elemento en el índice.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "105695840"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Tipos percibidos (características heredadas del entorno de Windows)

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

`PerceivedType` es una propiedad que clasifica un elemento en el índice. Esta clasificación es diferente de la clasificación "Kind" utilizada por la [Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md) , pero también permite a los usuarios refinar los resultados de la búsqueda. El tipo de AQS permite a los usuarios limitar su consulta de búsqueda, mientras que la propiedad PerceivedType permite a los usuarios filtrar el conjunto de resultados.

## <a name="types"></a>Tipos

Use la propiedad PerceivedType para clasificar el tipo de archivo de forma que los usuarios puedan filtrar sus resultados de búsqueda por tipo. La salida debe ser una de las cadenas siguientes:

-   contact
-   comunicaciones
-   comunicaciones/correo electrónico
-   comunicaciones/calendario
-   comunicaciones/tarea
-   comunicaciones/im
-   documento
-   documento/Nota
-   documento/texto
-   documento/hoja de cálculo
-   documento/presentación
-   music
-   images
-   imágenes/imagen
-   imágenes/vídeo
-   folder
-   programa

Por ejemplo, si desea crear un complemento de filtro para un nuevo tipo de archivo de imagen, debe implementar lo siguiente en la interfaz de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):

-   **GetChunk** para devolver un FULLPROPSPEC que incluye: D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** para devolver un PROPVARIANT que incluye: VT \_ LPWStr = "images/Picture"

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Desarrollo de complementos de IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-2x-wds-phaddins.md)
</dt> <dt>

[Sintaxis de consulta avanzada](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
