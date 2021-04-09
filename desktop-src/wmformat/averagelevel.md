---
title: AverageLevel
description: El atributo AverageLevel contiene un valor de amplitud de 16 bits que designa el nivel de volumen medio del contenido de audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel formato de Windows Media
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076723"
---
# <a name="averagelevel"></a>AverageLevel

El atributo **AverageLevel** contiene un valor de amplitud de 16 bits que designa el nivel de volumen medio del contenido de audio. Con [**PeakValue**](peakvalue.md), este atributo se usa para la normalización. La normalización es el proceso por el que se ajusta el nivel de volumen de reproducción de los archivos de audio para que las partes más fuertes de los archivos que se reproducen en el mismo nivel y el volumen medio para cada uno sea el mismo.

## <a name="global-constant"></a>Constante global

g \_ wszAverageLevel

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Este atributo lo establece el objeto de escritor basándose en la información del códec. Solo las secuencias comprimidas con uno de los códecs Windows Media Audio tienen un valor establecido automáticamente.

**AverageLevel** no es de solo lectura. Sin embargo, si el archivo lo reproducirá el Media Player de Windows, no debe modificar este valor. El Media Player de Windows lo usa para normalizar los niveles de los archivos de una lista de reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




