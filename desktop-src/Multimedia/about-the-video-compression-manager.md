---
title: Acerca del Administrador de compresión de vídeo
description: Acerca del Administrador de compresión de vídeo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows multimedia, administrador de compresión de vídeo (VCM)
- multimedia, administrador de compresión de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063014"
---
# <a name="about-the-video-compression-manager"></a>Acerca del Administrador de compresión de vídeo

Normalmente, los módulos instalables funcionan con datos de imágenes de vídeo almacenados en archivos intercalados de audio y vídeo (AVI). En esta introducción se explican las técnicas de programación que se usan para acceder a los procedimientos instalables a través de VCM y se tratan los temas siguientes:

-   VCM y el vídeo para Windows arquitectura
-   Comprimir y descomprimir datos de imagen de la aplicación
-   Uso de representadores de VCM para dibujar datos de la aplicación
-   Funciones y estructuras de VCM

Antes de leer esta introducción, debe estar familiarizado con los servicios gráficos de Microsoft Win32. En concreto, VCM usa ampliamente mapas de bits y estructuras relacionadas con mapas de bits, como [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) y [**BITMAPINFOHEADER.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) Para obtener información adicional sobre las **estructuras BITMAPINFO** y **BITMAPINFOHEADER,** vea [Mapas de bits.](/previous-versions//ms532349(v=vs.85))

> [!Note]  
> El administrador de compresión de audio (ACM) proporciona compatibilidad de nivel de sistema con controladores de compresión y descompresión de audio. Para obtener una descripción de los servicios de compresión de audio, vea [Administrador de compresión de audio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> </dl>

 

 