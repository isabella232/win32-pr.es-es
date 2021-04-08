---
title: Comandos de script
description: Comandos de script
ms.assetid: b8d7d4d3-c0d3-4b09-b5dd-1c6bbc3f2020
keywords:
- SDK de Windows Media Format, comandos de script
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- SDK de Windows Media Format, secuencias de scripts
- Advanced Systems Format (ASF), secuencias de scripts
- ASF (formato de sistemas avanzados), secuencias de scripts
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- scripts, comandos
- scripts, secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57ab446a216624dc8f844f54298aeeaee358ac3
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/20/2020
ms.locfileid: "104078574"
---
# <a name="script-commands"></a>Comandos de script

Los comandos de script admitidos por el SDK de Windows Media Format son pares de cadena de valor y nombre simple. Por ejemplo, un comando de script común es "URL", que usa Windows Media Player y otras aplicaciones de reproducción para abrir páginas Web. La otra mitad del par de scripts para el comando "URL" contiene un localizador uniforme de recursos (URL) válido, como `https://www.adatum.com` . Los objetos de este SDK no proporcionan compatibilidad para ningún comando específico; la aplicación debe incluir lógica para controlar los comandos que use. Puede usar los comandos admitidos por Windows Media Player para mantener la compatibilidad con la mayoría de los reproductores.

Los comandos de script se pueden entregar de una de estas dos maneras: en una secuencia de script o en el encabezado de archivo.

## <a name="script-streams"></a>Secuencias de script

Puede enviar comandos de script en su propia secuencia en un archivo ASF. Cada ejemplo de una secuencia de script contiene las dos cadenas del par nombre-valor. La ventaja de usar un flujo de script es que los comandos se entregarán en el momento correcto de la presentación.

## <a name="script-commands-in-the-file-header"></a>Comandos de script en el encabezado de archivo

Los comandos de script pueden incluirse en el encabezado de archivo para su recuperación en el momento de la reproducción. La aplicación de reproducción es responsable de ejecutar los comandos de script en el momento adecuado. La ventaja de usar comandos de script en el encabezado de archivo es que todos los comandos de script están disponibles antes de empezar a recibir ejemplos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Usar comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




