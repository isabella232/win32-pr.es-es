---
title: Marcadores
description: Marcadores
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK, marcadores
- Advanced Systems Format (ASF), marcadores
- ASF (formato de sistemas avanzados), marcadores
- marcadores, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903848"
---
# <a name="markers"></a>Marcadores

Los marcadores se denominan lugares en la escala de tiempo de un archivo ASF. Cada marcador tiene un nombre y un tiempo de presentación que se asigna. Puede especificar tantos marcadores como necesite para un archivo.

Los marcadores son útiles para dividir archivos ASF grandes en partes lógicas. Una aplicación que usa el objeto lector para reproducir archivos ASF puede proporcionar al usuario la opción de omitir de un marcador a un marcador, lo que simplifica la navegación de medios digitales. Por ejemplo, si va a crear un archivo ASF fuera de una presentación, puede colocar marcadores en la escala de tiempo para cada tema principal que se describe. En la reproducción, en lugar de obtener una escala de tiempo larga y tener que adivinar en la ubicación en la que se va a buscar, un usuario puede elegir simplemente un tema de una lista y ir directamente a la parte pertinente del archivo.

El objeto editor de metadatos manipula los marcadores. Puede Agregar, quitar y ver los marcadores de un archivo en cualquier momento después de que se haya escrito el archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Para buscar marcadores**](to-seek-to-markers.md)
</dt> <dt>

[**Usar marcadores**](using-markers.md)
</dt> </dl>

 

 




