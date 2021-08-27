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
ms.openlocfilehash: 3e3089ac6d4b789d740f256a5c44c1911eb3501bc654c3b94d0006d405616572
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110265"
---
# <a name="peakvalue"></a>PeakValue

El **atributo PeakValue** contiene un valor de amplitud de 16 bits que designa el nivel de volumen máximo del contenido de audio. Con [**AverageLevel**](averagelevel.md), este atributo se usa para la normalización. La normalización es el proceso de ajustar el nivel de volumen de reproducción de los archivos de audio para que las partes más sonorizas de la reproducción de archivos en el mismo nivel y el volumen medio de cada uno sea el mismo.

## <a name="global-constant"></a>Constante global

g \_ wszPeakValue

## <a name="data-type"></a>Tipo de datos

**DWORD \_ DE TIPO \_ WMT**

## <a name="remarks"></a>Comentarios

El objeto de escritor establece este atributo en función de la información del códec. Solo las secuencias comprimidas con uno de los códecs Windows Media Audio tienen un valor establecido automáticamente.

**PeakValue** no es de solo lectura. Sin embargo, si el archivo se reproducirá mediante Reproductor de Windows Media, no debe modificar este valor. El Reproductor de Windows Media usa para normalizar los niveles de archivos de una lista de reproducción.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Lista de atributos**](attribute-list.md)
</dt> </dl>

 

 




