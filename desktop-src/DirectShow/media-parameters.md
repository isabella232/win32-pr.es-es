---
description: Parámetros multimedia
ms.assetid: 48b2bc2e-897d-4aa9-8a50-c2855a17dca5
title: Parámetros multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9276a3d38b9176458299bfd1a47057cac6236e
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "103914090"
---
# <a name="media-parameters"></a>Parámetros multimedia

Los parámetros multimedia permiten a una aplicación configurar las propiedades de un objeto para que cambien a lo largo del tiempo de forma matemática.

Por ejemplo, supongamos que un ingeniero de sonido está mezclando una cinta maestra digital y desea aplicar un ligero retraso a una sección de voz, para rellenar el sonido. El efecto será discordante si el retraso se corta de repente. En su lugar, el efecto debe comenzar el 100 por ciento seco (sin retraso) y la mezcla húmeda/seco debe aumentar gradualmente hasta que alcance el nivel deseado. Además, esta transición debe seguir una curva suave o una progresión lineal. Para admitir este escenario, un DMO puede exponer las siguientes interfaces:

-   [**IMediaParamInfo**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparaminfo) contiene métodos para detectar información sobre las propiedades admitidas. Normalmente, el cliente llamará a estos métodos antes de comenzar a transmitir datos.
-   [**IMediaParams**](/previous-versions/windows/desktop/api/Medparam/nn-medparam-imediaparams) contiene métodos para establecer las curvas que seguirá un parámetro durante el streaming.

Estas interfaces se han diseñado principalmente para DMOs, pero cualquier objeto puede admitirlos. En esta sección, el término *parámetro* hace referencia a cualquier propiedad que admita estas dos interfaces.

Esta sección contiene los siguientes temas:

-   [Curvas de parámetro](parameter-curves.md)
-   [Información de parámetros](parameter-information.md)
-   [Segmentos de sobre](envelope-segments.md)
-   [Calcular valores de parámetros](calculating-parameter-values.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos multimedia de DirectX](directx-media-objects.md)
</dt> </dl>

 

 



