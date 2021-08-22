---
title: AverageLevel
description: El atributo AverageLevel contiene un valor de amplitud de 16 bits que designa el nivel medio de volumen del contenido de audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Formato multimedia de Windows AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd8745c5983eca67a02506b6cdeeabaca0a61a4c3f8b2a6993a73359d87adba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028163"
---
# <a name="averagelevel"></a>AverageLevel

El **atributo AverageLevel** contiene un valor de amplitud de 16 bits que designa el nivel medio de volumen del contenido de audio. Con [**PeakValue**](peakvalue.md), este atributo se usa para la normalización. La normalización es el proceso de ajustar el nivel de volumen de reproducción de los archivos de audio para que las partes más ruidosas de la reproducción de archivos en el mismo nivel y el volumen medio de cada uno sea el mismo.

## <a name="global-constant"></a>Constante global

g \_ wszAverageLevel

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El objeto de escritor establece este atributo en función de la información del códec. Solo las secuencias comprimidas con uno de Windows códecs de Audio multimedia tienen un valor establecido automáticamente.

**AverageLevel** no es de solo lectura. Sin embargo, si el archivo se reproducirá Reproductor de Windows Media, no debe modificar este valor. El Reproductor de Windows Media usa esto para normalizar los niveles de archivos de una lista de reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




