---
title: Uso de comandos de script admitidos por Reproductor de Windows Media
description: Uso de comandos de script admitidos por Reproductor de Windows Media
ms.assetid: 7054ce49-c000-4978-891e-825a83bfda5c
keywords:
- Windows SDK de formato multimedia, comandos de script
- Windows SDK de formato multimedia, Reproductor de Windows Media
- Formato de sistemas avanzados (ASF), comandos de script
- ASF (formato de sistemas avanzados), comandos de script
- Formato de sistemas avanzados (ASF), Reproductor de Windows Media
- ASF (formato de sistemas avanzados),Reproductor de Windows Media
- scripts, comandos
- scripts,Reproductor de Windows Media
- Reproductor de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58709af99cb4ebcb4eaba64fa6bb167b0ca80acb3fcb21b34efe4a55e2bacf12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110075"
---
# <a name="using-script-commands-supported-by-windows-media-player"></a>Uso de comandos de script admitidos por Reproductor de Windows Media

El SDK Windows media format no proporciona compatibilidad nativa para analizar y responder a comandos de script. Debe incluir cualquier lógica relacionada con los comandos de script en la aplicación. Los tipos de script que use también deben definirse en la aplicación.

Puede incluir código para controlar los mismos comandos de script que admite Reproductor de Windows Media. Mantener la compatibilidad con Reproductor de Windows Media hace que los archivos sea más universal que si inserta comandos de script personalizados.

En la tabla siguiente se enumeran los tipos de script admitidos por Reproductor de Windows Media.



| Tipo de script | Descripción                                                                                                                                                                                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL         | El reproductor envía la dirección URL especificada al explorador para mostrarla al usuario. Si se usa un control de reproductor incrustado, puede agregar una referencia de fotograma específica a la dirección URL mediante la sintaxis &&*framename.*                                                                             |
| Nombre    | Dirección URL a otro archivo multimedia que se va a reproducir.                                                                                                                                                                                                                                                |
| CAPTION     | Cadena de texto que se muestra en el área de títulos de Reproductor de Windows Media. Este tipo admite el formato HTML estándar, por lo que el texto se puede formatear como desee. Un ejemplo de uso es el subtítulo.                                                                             |
| Evento       | Nombre de un evento que se va a producir. El tipo EVENT admite la personalización para sus propios usos. El código del evento especificado debe definirse en el metarchivo Windows Media de la secuencia para que el reproductor realice el evento especificado. Un ejemplo de uso es la inserción de anuncios. |
| OPENEVENT   | Este script precede al evento real. OPENEVENT permite al reproductor almacenar previamente en búfer el contenido para que, cuando se produce el evento, el cambio entre secuencias parezca ser sin problemas.                                                                                                       |
| TEXT        | Cadena TEXT que se muestra en el área de títulos de Reproductor de Windows Media. Puede ser texto sin formato, SAMI o texto con formato HTML.                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Uso de comandos de script**](using-script-commands.md)
</dt> </dl>

 

 




