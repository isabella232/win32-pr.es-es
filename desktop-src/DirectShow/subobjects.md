---
description: Subobjetos
ms.assetid: 03cbd590-b573-4a98-9ab7-fe548800cfcb
title: Subobjetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaf828d0049816c0cbf932b96344b0270c4c9dbfb835a0750736551ff67b319b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633485"
---
# <a name="subobjects"></a>Subobjetos

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los orígenes, efectos y transiciones tienen punteros internos a otros objetos COM, *denominados subobjetos*. El subobjeto realiza el trabajo real del objeto . El subobjeto de un origen es el componente que crea los datos de audio o vídeo. El subobjeto de un efecto o transición es el componente que transforma los datos; Por ejemplo, en un efecto de vídeo, crea el efecto visual en la secuencia de vídeo.

El tipo de subobjeto depende del tipo de objeto:

-   Origen: cualquier DirectShow de origen o analizador que admita la búsqueda y produzca un formato compatible con DES. Puede ser un formato comprimido si DirectShow filtros para descodificarlo.
-   Efecto: para vídeo, cualquier objeto 2D de entrada de Microsoft® DirectX® transform. En el caso del audio, DirectShow filtro de efecto de audio.
-   Transición: para vídeo, cualquier objeto de transformación de DirectX de dos entradas 2D. El audio no admite transiciones.

Los grupos, las composiciones y las pistas no tienen subobjetos.

La aplicación no establece directamente el puntero del subobjeto. Para efectos y transiciones, la aplicación llama al método [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) para especificar el GUID del subobjeto. Para los objetos de origen, una aplicación normalmente llama a [**IAMTimelineSrc::SetMediaName**](iamtimelinesrc-setmedianame.md) para especificar el nombre de un archivo de origen. Sin embargo, **el método SetSubObjectGUID** también se puede usar para los objetos de origen, para especificar el identificador de clase (CLSID) de un filtro.

Para obtener más información, [vea Trabajar con orígenes y](working-with-sources.md) Trabajar con efectos y [transiciones.](working-with-effects-and-transitions.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de los componentes de escala de tiempo](overview-of-the-timeline-components.md)
</dt> </dl>

 

 



