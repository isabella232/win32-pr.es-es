---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- Windows SDK de formato multimedia, comandos de script
- Formato de sistemas avanzados (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- Windows SDK de formato multimedia, secuencias de script
- Formato de sistemas avanzados (ASF), secuencias de script
- ASF (formato de sistemas avanzados), secuencias de script
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF), secuencias
- ASF (formato de sistemas avanzados), secuencias
- scripts, comandos
- scripts,streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6f6487958db820892f57af2b1348dcd4304031976aaaf56ddeb6233e1b8a87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197537"
---
# <a name="script-commands"></a>Comandos de script

Los comandos de script admitidos por el SDK Windows Media Format son pares de cadenas de nombre y valor simples. Por ejemplo, un comando de script común es "URL", que se usa en Reproductor de Windows Media y otras aplicaciones en reproducción para abrir páginas web. La otra mitad del par de script para el comando "URL" contiene un localizador uniforme de recursos (URL) válido, como `https://www.adatum.com` . Los objetos de este SDK no proporcionan compatibilidad con ningún comando específico; La aplicación debe incluir lógica para controlar los comandos que use. Puede usar los comandos admitidos por Reproductor de Windows Media mantener la compatibilidad con la mayoría de los reproductores.

Los comandos de script se pueden entregar de una de estas dos maneras: en una secuencia de scripts o en el encabezado de archivo.

## <a name="script-streams"></a>Script Secuencias

Puede entregar comandos de script en su propia secuencia en un archivo ASF. Cada ejemplo de una secuencia de scripts contiene las dos cadenas del par nombre-valor. La ventaja de usar una secuencia de scripts es que los comandos se entregarán en el momento de presentación correcto.

## <a name="script-commands-in-the-file-header"></a>Comandos de script en el encabezado de archivo

Los comandos de script se pueden incluir en el encabezado de archivo para su recuperación en el momento de la reproducción. La aplicación en reproducción es responsable de ejecutar los comandos de script en el momento adecuado. La ventaja de usar comandos de script en el encabezado de archivo es que todos los comandos de script están disponibles antes de empezar a recibir ejemplos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Uso de comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




