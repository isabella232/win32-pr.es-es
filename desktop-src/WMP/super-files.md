---
title: Súper archivos
description: Súper archivos
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos de súper archivos
- Aspectos de Windows Media Player Mobile, archivos de superarchivos
- máscaras, súper archivos
- Súper archivos en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714219"
---
# <a name="super-files"></a>Súper archivos

Los súper archivos se usan para almacenar las imágenes deshabilitadas para trackbars. Dado que la imagen principal de la barra de desplazamiento se muestra en el archivo de fondo y el usuario pulsa la imagen Thumb, no la imagen de TrackBar, solo se necesita la imagen deshabilitada para trackbars. Se almacena en el archivo definido por Super en la sección de mapas de bits del archivo de definición de máscara. Un súper archivo también puede almacenar las imágenes insertadas y deshabilitadas para otros botones, como silenciar, que no es necesario que sea un botón de tipo de posicionamiento.

> [!Note]  
> Los archivos de superart no se usan en máscaras para Windows Media Player 10 Mobile o posterior porque las imágenes deshabilitadas para Seek trackbars se encuentran en el archivo seekthumb.

 

La siguiente imagen es un súper archivo típico.

![Super File](images/cesdksup.png)

Esto almacena las imágenes deshabilitadas para los trackbars y el botón silenciar. Estas imágenes se desplazan tal y como se define en la sección de mapas de bits.

El área de fondo de la imagen de TrackBar deshabilitada coincide exactamente con el área correspondiente en el archivo de fondo. Esto es importante, porque el rectángulo completo definido para la imagen de TrackBar deshabilitada reemplazará el área de coincidencia en el archivo de fondo. Esto garantiza que la imagen de TrackBar deshabilitada se mezcle sin problemas en la imagen de fondo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Archivos de imagen**](art-files-mobile.md)
</dt> </dl>

 

 




