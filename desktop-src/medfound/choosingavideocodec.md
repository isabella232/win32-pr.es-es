---
description: Elección de un códec de vídeo
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Elección de un códec de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275145"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a>Elección de un códec de vídeo (Microsoft Media Foundation)

El codificador de Windows Media Video 9 admite tres categorías de salida codificada: perfil principal, perfil avanzado e imagen. La categoría principal de perfil proporciona compresión de vídeo general para contenido de vídeo complejo, como películas o vídeos musicales. Las características del perfil principal proporcionan una amplia gama de opciones de codificación. Puede usar el perfil principal para crear vídeo con velocidades de bits muy bajas para la entrega en dispositivos de mano o, en el otro extremo del espectro, puede usarlo para crear vídeo de alta definición para cine digital.

El énfasis de los algoritmos de codificación en el perfil principal se encuentra en el contenido de vídeo dinámico, pero también es adecuado para otro contenido de vídeo. El perfil principal debe ser la categoría predeterminada para el contenido de vídeo. Para satisfacer necesidades específicas, puede usar la categoría de perfil avanzado, la categoría de imagen o un codificador independiente denominado codificador de pantalla de Windows Media Video 9. En la tabla siguiente se enumeran las cuatro opciones.



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
<td><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a><dl> Perfil Main<br />
</dl></td>
</tr>
<tr class="even">
<td>Vídeo o vídeo de alta definición de codificación que se ajusta al estándar de SMPTE del perfil avanzado de VC-1</td>
<td><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a><dl> Perfil avanzado<br />
</dl></td>
</tr>
<tr class="odd">
<td>Convertir imágenes de mapa Dete en vídeo dinámico</td>
<td><a href="windowsmediavideo9encoder.md">Codificador de Windows Media Video 9</a><dl> Imagen<br />
</dl></td>
</tr>
<tr class="even">
<td>Encoding: vídeo de aplicación (captura de pantalla) u otro vídeo muy estático</td>
<td><a href="windowsmediavideo9screenencoder.md"><strong>Codificador de pantalla de Windows Media Video 9</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con vídeo](workingwithvideo.md)
</dt> </dl>

 

 



