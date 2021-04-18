---
title: PeakValue
description: El atributo PeakValue contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue formato de Windows Media
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105704845"
---
# <a name="peakvalue"></a>PeakValue

El atributo **PeakValue** contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio. Con [**AverageLevel**](averagelevel.md), este atributo se usa para la normalización. La normalización es el proceso por el que se ajusta el nivel de volumen de reproducción de los archivos de audio para que las partes más fuertes de los archivos que se reproducen en el mismo nivel y el volumen medio para cada uno sea el mismo.

## <a name="global-constant"></a>Constante global

g \_ wszPeakValue

## <a name="data-type"></a>Tipo de datos

**tipo de WMT \_ \_ DWORD**

## <a name="remarks"></a>Observaciones

Este atributo lo establece el objeto de escritor basándose en la información del códec. Solo las secuencias comprimidas con uno de los códecs Windows Media Audio tienen un valor establecido automáticamente.

**PeakValue** no es de solo lectura. Sin embargo, si el archivo lo reproducirá el Media Player de Windows, no debe modificar este valor. El Media Player de Windows lo usa para normalizar los niveles de los archivos de una lista de reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




