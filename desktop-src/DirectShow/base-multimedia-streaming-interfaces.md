---
description: Base Multimedia Streaming Interfaces
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Base Multimedia Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5268855231169c6c0a7ffab02aa5145a7c1813511421b04b2420773e1588ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662925"
---
# <a name="base-multimedia-streaming-interfaces"></a>Base Multimedia Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Las interfaces de streaming multimedia base proporcionan una manera programática de acceder a las secuencias multimedia. Sin embargo, el uso de una interfaz base para acceder a un tipo específico de datos puede limitar la cantidad de control que tiene sobre los datos, por lo que los desarrolladores de medios deben crear versiones derivadas de estas interfaces que proporcionen un control más eficaz sobre las funcionalidades únicas de su tipo de medio.



| Interfaz                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Define cómo acceder al objeto de flujo multimedia de nivel superior; este objeto contiene y proporciona acceso a otros objetos de secuencia. [**IMultiMediaStream tiene métodos**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) que enumeran o recuperan secuencias específicas, así como la comprobación de la duración total del flujo y la búsqueda dentro de la secuencia.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Define un objeto de secuencia genérico. Use sus métodos para recuperar un puntero a la secuencia, obtener información sobre la secuencia y crear ejemplos a partir de los datos de la secuencia. También puede crear ejemplos de secuencias compartidas, a las que pueden acceder varias secuencias sin duplicar los datos de la muestra.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controla el comportamiento de un ejemplo de secuencia específico. Puede recuperar la secuencia que creó el ejemplo, comprobar las horas de inicio y finalización del ejemplo y el estado de finalización, y realizar una función definida por el usuario en el propio ejemplo (a través del [**método Update).**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) Normalmente, el método Update procesa los datos de ejemplo de una manera adecuada, como la representación de datos de vídeo o la reproducción de datos de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



