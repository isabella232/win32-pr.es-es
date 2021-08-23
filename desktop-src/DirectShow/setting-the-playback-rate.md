---
description: Establecimiento de la velocidad de reproducción
ms.assetid: 74ae45d3-4fea-491c-af1f-46768df41c5f
title: Establecimiento de la velocidad de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0404e67d716616a4c383c134a4fb4e75060e3094023abec52df1d38099b92b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583325"
---
# <a name="setting-the-playback-rate"></a>Establecimiento de la velocidad de reproducción

Para cambiar la velocidad de reproducción, llame al [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) Especifique la nueva velocidad como una fracción de la velocidad original. Por ejemplo, para reproducir a una velocidad dos veces normal, use lo siguiente:


```C++
pSeek->SetRate(2.0)
```



Las tasas mayores que una son más rápidas de lo normal. Las tasas entre cero y uno son más lentas de lo normal. Las tasas negativas se definen como reproducción con versiones anteriores, pero en la práctica la mayoría de los filtros no la admiten. Actualmente, ninguno de los filtros de DirectShow estándar admite la reproducción inversa.

Independientemente de la velocidad de reproducción, la posición actual y la posición de detenerse siempre se expresan en relación con el origen original. Por ejemplo, si un archivo de origen tiene una duración de 20 segundos con una velocidad de reproducción normal, al establecer la posición actual en 10 segundos se buscará en el centro del archivo. Si la velocidad de reproducción es 2,0, la posición de detenerse es de 20 segundos y se busca en la posición de 10 segundos, el archivo se reproducirá durante 5 segundos en tiempo real: 10 segundos, con el doble de velocidad de reproducción normal. A una velocidad de reproducción de 2,0, la posición actual aumenta al doble de la velocidad del reloj de referencia.

 

 



