---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows SDK de formato multimedia, marcadores
- Formato de sistemas avanzados (ASF), marcadores
- ASF (formato de sistemas avanzados), marcadores
- markers,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58ddc013b2d8e09fa30ac6a8b7373aaf6733b669f2ccacec6350ee70e0800b20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808235"
---
# <a name="markers"></a>Marcadores

Los marcadores se denominan lugares en la escala de tiempo de un archivo ASF. Cada marcador tiene un nombre y un tiempo de presentación que se asigna. Puede especificar tantos marcadores como necesite para un archivo.

Los marcadores son útiles para dividir archivos ASF grandes en partes lógicas. Una aplicación que usa el objeto de lector para reproducir archivos ASF puede proporcionar al usuario la opción de pasar del marcador al marcador, lo que simplifica la navegación de los medios digitales. Por ejemplo, si va a crear un archivo ASF a la salida de una presentación, puede colocar marcadores en la escala de tiempo de cada tema principal que se describe. En la reproducción, en lugar de obtener una escala de tiempo larga y tener que adivinar la ubicación a la que buscar, un usuario puede simplemente elegir un tema de una lista y ir directamente a la parte pertinente del archivo.

El objeto del editor de metadatos manipula los marcadores. Puede agregar, quitar y ver los marcadores de un archivo en cualquier momento después de escribir el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Para buscar marcadores**](to-seek-to-markers.md)
</dt> <dt>

[**Usar marcadores**](using-markers.md)
</dt> </dl>

 

 




