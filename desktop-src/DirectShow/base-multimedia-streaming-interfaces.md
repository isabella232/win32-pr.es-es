---
description: Base Multimedia Streaming Interfaces
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Base Multimedia Streaming Interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161696"
---
# <a name="base-multimedia-streaming-interfaces"></a>Base Multimedia Streaming Interfaces

> [!Note]  
> Estas API están en desuso. Las aplicaciones deben usar el [**filtro Sample Grabber**](sample-grabber-filter.md) o implementar un filtro personalizado para obtener datos de un DirectShow gráfico de filtros.

 

Las interfaces de streaming multimedia base proporcionan una manera de acceder mediante programación a las secuencias multimedia. Sin embargo, el uso de una interfaz base para acceder a un tipo específico de datos puede limitar la cantidad de control que tiene sobre los datos, por lo que los desarrolladores de medios deben crear versiones derivadas de estas interfaces que proporcionen un control más eficaz sobre las funcionalidades únicas de su tipo de medio.



| Interfaz                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | Define cómo acceder al objeto de secuencia multimedia de nivel superior; este objeto contiene y proporciona acceso a otros objetos de secuencia. [**IMultiMediaStream tiene**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) métodos que enumeran o recuperan secuencias específicas, así como la comprobación de la duración total del flujo y la búsqueda dentro de la secuencia.                                                                                                       |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | Define un objeto de secuencia genérico. Use sus métodos para recuperar un puntero a la secuencia, obtener información sobre la secuencia y crear ejemplos a partir de los datos del flujo. También puede crear ejemplos de flujo compartido, a los que pueden acceder varias secuencias sin duplicar los datos de la muestra.                                                                                                                                                  |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | Controla el comportamiento de un ejemplo de flujo específico. Puede recuperar la secuencia que creó el ejemplo, comprobar las horas de inicio y finalización del ejemplo y el estado de finalización, y realizar una función definida por el usuario en el propio ejemplo (a través del [**método Update).**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) Normalmente, el método Update procesa los datos de ejemplo de una manera adecuada, como la representación de datos de vídeo o la reproducción de datos de audio. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lista de interfaces de streaming multimedia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



