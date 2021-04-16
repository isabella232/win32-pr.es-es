---
description: Objetos multimedia de DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos multimedia de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105678622"
---
# <a name="directx-media-objects"></a>Objetos multimedia de DirectX

> [!Note]  
> DMOs se han sustituido por [transformaciones de Media Foundation](/windows/desktop/medfound/media-foundation-transforms) (MFTs). Todavía se admiten las interfaces de DMO. Sin embargo, si está escribiendo un códec personalizado o un complemento de procesamiento de audio y vídeo, considere la posibilidad de implementarlo como MFT.

 

Los objetos multimedia de DirectX (DMOs) son componentes de streaming de datos basados en COM. En algunos aspectos, DMOs son similares a los filtros de Microsoft DirectShow. Como los filtros de DirectShow, DMOs toma los datos de entrada y los usa para generar datos de salida. Sin embargo, las interfaces de programación de aplicaciones (API) para DMOs son mucho más sencillas que las API correspondientes para DirectShow. Como resultado, DMOs son más fáciles de crear, probar y usar. DMOs se puede usar en muchos escenarios:

-   Las aplicaciones basadas en DirectShow pueden usar DMOs a través de un filtro de DirectShow denominado filtro de [contenedor de DMO](dmo-wrapper-filter.md) . La distinción entre filtros y DMOs es transparente para la aplicación. La aplicación no llama directamente a las API de DMO.
-   Las aplicaciones basadas en Microsoft DirectSound pueden usar el efecto de audio DMOs. De nuevo, la aplicación se protege de las API de DMO de bajo nivel mediante las API de DirectSound de nivel superior.
-   Las aplicaciones pueden usar DMOs directamente.

Por lo tanto, al escribir un DMO, se crea un componente que se puede usar en una amplia gama de aplicaciones. Esta documentación contiene las siguientes secciones:

-   [Acerca de DMOs](about-dmos.md)
-   [Usar DMOs](using-dmos.md)
-   [Escritura de DMO](writing-a-dmo.md)
-   [Parámetros multimedia](media-parameters.md)
-   [Referencia de DMO](dmo-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
