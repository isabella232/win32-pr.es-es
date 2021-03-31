---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8b427a315231577f1608a168629bc8b77d2cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911701"
---
# <a name="subobjects"></a>Subobjetos

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los orígenes, los efectos y las transiciones tienen punteros internos a otros objetos COM, denominados *subobjetos*. El subobjeto realiza el trabajo real del objeto. El subobjeto de un origen es el componente que crea los datos de vídeo o audio. El subobjeto de un efecto o transición es el componente que transforma los datos. por ejemplo, en un efecto de vídeo, crea el efecto visual en el flujo de vídeo.

El tipo de subobjeto depende del tipo de objeto:

-   Origen: cualquier filtro de origen de DirectShow o filtro de analizador que admita búsquedas y genere un formato compatible con DES. Puede ser un formato comprimido si existen filtros de DirectShow para descodificarlo.
-   Efecto: para el vídeo, cualquier objeto de transformación de® de Microsoft® DirectX de una entrada de una sola entrada. En audio, cualquier filtro de efecto de audio de DirectShow.
-   Transición: para vídeo, cualquier objeto de transformación de DirectX de dos entradas 2D. Audio no admite transiciones.

Los grupos, las composiciones y las pistas no tienen subobjetos.

La aplicación no establece directamente el puntero de subobjeto. En el caso de los efectos y las transiciones, la aplicación llama al método [**IAMTimelineObj:: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar el GUID del subobjeto. En el caso de los objetos de origen, una aplicación normalmente llama a [**IAMTimelineSrc:: SetMediaName**](iamtimelinesrc-setmedianame.md) para especificar el nombre de un archivo de código fuente. Sin embargo, el método **SetSubObjectGUID** también se puede usar para los objetos de origen, para especificar el identificador de clase (CLSID) de un filtro.

Para obtener más información, vea [trabajar con orígenes](working-with-sources.md) y [trabajar con efectos y transiciones](working-with-effects-and-transitions.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de la escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



