---
description: Parámetros multimedia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parámetros multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37cf7229cac3deb5b31a6c6879fd3b5896e5f4098a4cce64ac42d19970f5c569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119584345"
---
# <a name="media-parameters"></a>Parámetros multimedia

Los parámetros multimedia permiten a una aplicación configurar las propiedades de un objeto para que cambien con el tiempo de forma matemáticamente determinista.

Por ejemplo, suponga que un ingeniero de sonido está mezclando una cinta maestra digital y quiere aplicar un ligero retraso a una sección de voz para rellenar el sonido. El efecto se realizará en jarring si el retraso se reduce repentinamente. En su lugar, el efecto debe comenzar 100 % sin retraso, y la mezcla de efectos y efectos debe aumentar gradualmente hasta que alcance el nivel deseado. Además, esta transición debe seguir una curva suave o una progresión lineal. Para admitir este escenario, un DMO puede exponer las interfaces siguientes:

-   [**IMediaParamInfo contiene métodos**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) para detectar información sobre las propiedades admitidas. Normalmente, el cliente llamará a estos métodos antes de empezar a transmitir datos.
-   [**IMediaParams contiene métodos**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) para establecer las curvas que seguirá un parámetro durante el streaming.

Estas interfaces están diseñadas principalmente para DDO, pero cualquier objeto puede admitirlas. En esta sección, el término *parámetro* hace referencia a cualquier propiedad que admita estas dos interfaces.

Esta sección contiene los siguientes temas:

-   [Curvas de parámetros](parameter-curves.md)
-   [Información de parámetros](parameter-information.md)
-   [Segmentos de sobre](envelope-segments.md)
-   [Cálculo de valores de parámetro](calculating-parameter-values.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos multimedia de DirectX](directx-media-objects.md)
</dt> </dl>

 

 



