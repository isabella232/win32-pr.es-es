---
description: Introducción (instrucciones WIC para formatos de imagen RAW de cámara)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introducción (instrucciones WIC para formatos de imagen RAW de cámara)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278178"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introducción (instrucciones WIC para formatos de imagen RAW de cámara)

El componente de creación de imágenes de Windows (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imágenes. WIC permite que los proveedores de software y hardware desarrollen códecs para que sus propios formatos de imagen puedan obtener la misma compatibilidad de plataforma que los formatos de imagen nativa, como el formato de archivo de imagen etiquetado (TIFF), el grupo de expertos fotográficos (JPEG) o la foto HD.

WIC proporciona un conjunto único y coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen. Por lo tanto, cualquier aplicación que use WIC recibirá compatibilidad automática con los nuevos formatos de imagen en cuanto se instale el códec. WIC también proporciona un marco de metadatos extensible que permite que las aplicaciones lean y escriban sus propios metadatos de propiedad directamente en archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.

WIC se incluye con Windows Presentation Foundation (WPF) y está integrado en Windows Vista y versiones posteriores de Windows. También está disponible como componente redistribuible independiente para Windows XP.

Estas instrucciones están diseñadas para ayudar a los fabricantes de formatos sin formato en su desarrollo de códecs WIC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Instrucciones de WIC para formatos de imagen RAW de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



