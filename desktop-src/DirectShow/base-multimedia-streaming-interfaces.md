---
description: Interfaces de streaming multimedia de base
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de streaming multimedia de base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003436"
---
# <a name="base-multimedia-streaming-interfaces"></a>Interfaces de streaming multimedia de base

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el filtro de [**enganche de ejemplo**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un gráfico de filtros de DirectShow.

 

Las interfaces de streaming multimedia base proporcionan una manera programática de obtener acceso a las secuencias multimedia. Sin embargo, el uso de una interfaz base para tener acceso a un tipo de datos específico puede limitar la cantidad de control que se obtiene sobre los datos, por lo que los desarrolladores de medios deben crear versiones derivadas de estas interfaces que proporcionen un control más eficaz sobre las funcionalidades únicas de su tipo de medio.



| Interfaz                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Define cómo obtener acceso al objeto de flujo multimedia de nivel superior. Este objeto contiene y proporciona acceso a otros objetos de flujo. [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) tiene métodos que enumeran o recuperan secuencias específicas, así como la comprobación del tiempo total de la secuencia y la búsqueda en la secuencia.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Define un objeto de flujo genérico. Use sus métodos para recuperar un puntero a la secuencia, obtener información sobre la secuencia y crear ejemplos a partir de los datos de la secuencia. También puede crear ejemplos de secuencias compartidas, a los que varias secuencias pueden tener acceso sin duplicar los datos del ejemplo.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controla el comportamiento de un ejemplo de flujo concreto. Puede recuperar la secuencia que creó el ejemplo, comprobar las horas de inicio y finalización del ejemplo, así como el estado de finalización, y realizar una función definida por el usuario en el propio ejemplo (mediante el método [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ). Normalmente, el método Update procesa los datos de ejemplo de manera adecuada, como la representación de datos de vídeo o la reproducción de datos de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



