---
title: Usar comandos de script compatibles con Windows Media Player
description: Usar comandos de script compatibles con Windows Media Player
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- SDK de Windows Media Format, comandos de script
- SDK de Windows Media Format, Windows Media Player
- Advanced Systems Format (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- Advanced Systems Format (ASF), Windows Media Player
- ASF (formato de sistemas avanzados), Windows Media Player
- scripts, comandos
- scripts, Media Player de Windows
- Reproductor de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25302b5f5b6789be0d9e18b0a93e1e781a9dc06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075806"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Usar comandos de script compatibles con Windows Media Player

El SDK de Windows Media Format no proporciona compatibilidad nativa para el análisis y la respuesta a los comandos de script. Debe incluir cualquier lógica relacionada con los comandos de script en la aplicación. Los tipos de script que se usan también deben definirse en la aplicación.

Puede incluir código para controlar los mismos comandos de script que se admiten en Windows Media Player. Mantener la compatibilidad con Windows Media Player hace que los archivos sean más universales que si se incrustan comandos de script personalizados.

En la tabla siguiente se enumeran los tipos de scripts compatibles con Windows Media Player.



| Tipo de script | Descripción                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | El reproductor envía la dirección URL especificada al explorador para mostrarla al usuario. Si se utiliza un control de reproductor incrustado, puede Agregar una referencia de marco específica a la dirección URL mediante la sintaxis de &&*FrameName* .                                                                             |
| EXTENSIÓN    | Una dirección URL a otro archivo multimedia que se va a reproducir.                                                                                                                                                                                                                                                |
| CAPTION     | Cadena de texto que se muestra en el área de título de Windows Media Player. Este tipo admite el formato HTML estándar, por lo que el texto puede tener el formato que desee. Un ejemplo de uso es el subtítulos (CC).                                                                             |
| CESO       | Nombre de un evento que se va a producir. El tipo de evento admite la personalización para sus propios usos. El código para el evento especificado debe definirse en el metarchivo de Windows Media para la secuencia con el fin de que el reproductor realice el evento especificado. Un ejemplo de uso es la inserción de anuncios. |
| OPENEVENT   | Este script precede al evento real. El OPENEVENT permite que el reproductor almacene previamente el contenido de modo que, cuando se produzca el evento, el cambio entre las secuencias parezca que sea sencillo.                                                                                                       |
| TEXT        | Cadena de texto que se muestra en el área de título de Windows Media Player. Puede ser texto sin formato, SAMI o texto con formato HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Usar comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




