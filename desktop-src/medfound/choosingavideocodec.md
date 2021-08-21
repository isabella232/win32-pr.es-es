---
description: Elección de un códec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Elegir un códec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b560666ddeebb88fc3bb720cbc9f1be26308e7ecd8a4ad872fbb1f0991826fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035373"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Elegir un códec de vídeo (Microsoft Media Foundation)

El Windows Media Video 9 admite tres categorías de salida codificada: Perfil principal, Perfil avanzado e Imagen. La categoría Perfil principal proporciona compresión de vídeo general para contenido de vídeo complejo, como películas o vídeos de música. Las características del perfil principal proporcionan una amplia gama de configuraciones de codificación. Puede usar el perfil principal para crear vídeo con velocidades de bits muy bajas para la entrega en dispositivos portátiles o, en el otro extremo del espectro, puede usarlo para crear vídeo de alta definición para digital.

El énfasis de los algoritmos de codificación en el perfil principal se encuentra en el contenido de vídeo dinámico, pero también son adecuados para otro contenido de vídeo. El perfil principal debe ser la categoría predeterminada para el contenido de vídeo. Para satisfacer necesidades específicas, puede usar la categoría Perfil avanzado, la categoría Imagen o un codificador independiente denominado Windows Media Video 9 Screen. En la tabla siguiente se enumeran las cuatro opciones.



<table>
<thead>
<tr class="header">
<th>Propósito</th>
<th>Códec</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Codificación de vídeo de uso general</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificador Media Video 9</a><dl> Perfil Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificación de vídeo o vídeo de alta definición que se ajusta al estándar SMPTE de perfil avanzado de VC-1</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificador Media Video 9</a><dl> Perfil avanzado<br />
</dl></td>
</tr>
<tr class="odd">
<td>Conversión de imágenes de mapa de bits en vídeo dinámico</td>
<td><a href="windowsmediavideo9encoder.md">Windows Codificador Media Video 9</a><dl> Imagen<br />
</dl></td>
</tr>
<tr class="even">
<td>Codificación de vídeo de aplicación de equipo (captura de pantalla) u otro vídeo altamente estático</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Windows Codificador de pantalla de Vídeo multimedia 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



