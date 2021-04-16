---
description: Establecer la velocidad de reproducción
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Establecer la velocidad de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8a3297ca376b0cc55e4df4884b22d1cb2df81b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686266"
---
# <a name="setting-the-playback-rate"></a>Establecer la velocidad de reproducción

Para cambiar la velocidad de reproducción, llame al método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) . Especifique la nueva tasa como una fracción de la tasa original. Por ejemplo, para reproducir dos veces la velocidad normal, use lo siguiente:


```C++
pSeek->SetRate(2.0)
```



Las velocidades mayores que uno son más rápidas que las normales. Las velocidades entre cero y uno son más lentas que las normales. Las tasas negativas se definen como reproducción hacia atrás, pero en la práctica la mayoría de los filtros no la admiten. Actualmente ninguno de los filtros de DirectShow estándar admite la reproducción inversa.

Independientemente de la velocidad de reproducción, la posición actual y la posición de detención siempre se expresan en relación con el origen original. Por ejemplo, si un archivo de origen tiene una duración de 20 segundos a una velocidad de reproducción normal, al establecer la posición actual en 10 segundos, se buscará en el medio del archivo. Si la velocidad de reproducción es 2,0, la posición de detención es de 20 segundos y se busca en la posición de 10 segundos, el archivo se reproducirá durante 5 segundos de tiempo real: 10 segundos, como mínimo, la velocidad de reproducción normal. En una velocidad de reproducción de 2,0, la posición actual aumenta al doble de la velocidad del reloj de referencia.

 

 



