---
title: PeakValue
description: El atributo PeakValue contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Formato multimedia de Windows PeakValue
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467077"
---
# <a name="peakvalue"></a>PeakValue

El **atributo PeakValue** contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio. Con [**AverageLevel**](averagelevel.md), este atributo se usa para la normalización. La normalización es el proceso de ajustar el nivel de volumen de reproducción de los archivos de audio para que las partes más ruidosas de la reproducción de archivos en el mismo nivel y el volumen medio de cada uno sea el mismo.

## <a name="global-constant"></a>Constante global

g \_ wszPeakValue

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Observaciones

El objeto de escritor establece este atributo en función de la información del códec. Solo las secuencias comprimidas con uno de Windows códecs de Audio multimedia tienen un valor establecido automáticamente.

**PeakValue** no es de solo lectura. Sin embargo, si el archivo se reproducirá con Reproductor de Windows Media, no debe modificar este valor. El Reproductor de Windows Media usa esto para normalizar los niveles de archivos de una lista de reproducción.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




