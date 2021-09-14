---
description: Objetos multimedia de DirectX
ms.assetid: e4424740-31b9-4317-8791-6a9aebb0c7e6
title: Objetos multimedia de DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2119fc8cce602bc1cc085886edd6852320aca180
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061693"
---
# <a name="directx-media-objects"></a>Objetos multimedia de DirectX

> [!Note]  
> Las DMO se han reemplazado [por Media Foundation transformaciones](/windows/desktop/medfound/media-foundation-transforms) (MTA). Todavía DMO las interfaces de configuración. Sin embargo, si está escribiendo un códec personalizado o un complemento de procesamiento de audio y vídeo, considere la posibilidad de implementarlo como MFT.

 

DirectX Media Objects (DMO) son componentes de streaming de datos basados en COM. En algunos aspectos, las DDO son similares a los filtros DirectShow Microsoft. Al igual DirectShow filtros, las DDO toman los datos de entrada y los usan para generar datos de salida. Sin embargo, las interfaces de programación de aplicaciones (API) para las DDO son mucho más sencillas que las API correspondientes para DirectShow. Como resultado, las DDO son más fáciles de crear, probar y usar. Las DDO se pueden usar en muchos escenarios:

-   Las aplicaciones basadas DirectShow pueden usar DDO a través de DirectShow filtro denominado [DMO wrapper.](dmo-wrapper-filter.md) La distinción entre los filtros y las DDO es transparente para la aplicación. La aplicación no llama directamente a DMO API.
-   Las aplicaciones basadas en Microsoft Direct Sound pueden usar DDO con efecto de audio. Una vez más, la aplicación está blindada de las API de DMO de nivel inferior mediante las API direct Sound de nivel superior.
-   Las aplicaciones pueden usar las DDO directamente.

Por lo tanto, al escribir DMO, se crea un componente que se puede usar en una amplia gama de aplicaciones. Esta documentación contiene las secciones siguientes:

-   [Acerca de las DDO](about-dmos.md)
-   [Uso de DDO](using-dmos.md)
-   [Escribir un DMO](writing-a-dmo.md)
-   [Parámetros multimedia](media-parameters.md)
-   [DMO Referencia](dmo-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow](directshow.md)
</dt> </dl>

 

 
