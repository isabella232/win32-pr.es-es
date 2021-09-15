---
description: El sistema de escritura del receptor es un componente para codificar archivos de audio o vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Escritor de receptores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574764"
---
# <a name="sink-writer"></a>Escritor de receptores

El sistema de escritura del receptor es un componente para codificar archivos de audio o vídeo.

En el diagrama siguiente se muestra, en un nivel alto, cómo una aplicación usa el sistema de escritura del receptor para codificar y el archivo de audio y vídeo.

![diagrama que muestra el sistema de escritura del receptor.](images/encoding09.png)

El sistema de escritura del receptor hospeda un receptor multimedia y, opcionalmente, uno o varios codificadores. Los codificadores convierten datos de audio o vídeo sin comprimir en secuencias de bits codificadas. El receptor multimedia genera las secuencias de bits en un archivo. El escritor de receptores realiza las siguientes tareas:

-   Carga el receptor de medios.
-   Busca y carga los codificadores.
-   Administra el flujo de datos a los codificadores y al receptor multimedia.

La aplicación pasa datos de audio y vídeo al sistema de escritura del receptor como entrada. No importa cómo la aplicación obtenga o genere los datos de entrada. Una opción es usar el Lector [de origen](source-reader.md), como se muestra en el diagrama siguiente. Sin embargo, el escritor receptor no requiere el uso del lector de origen. Estos dos componentes son independientes.

![diagrama que muestra el lector de origen y el escritor del receptor.](images/encoding02.png)

## <a name="in-this-section"></a>En esta sección

-   [Uso del escritor de receptores](using-the-sink-writer.md)
-   [Tutorial: Uso del escritor de receptores para codificar vídeo](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Codificación y creación de archivos](encoding-and-file-authoring.md)
</dt> <dt>

[Información general sobre la codificación en Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



