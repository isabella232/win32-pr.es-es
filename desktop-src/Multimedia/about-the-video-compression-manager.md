---
title: Acerca del administrador de compresión de vídeo
description: Acerca del administrador de compresión de vídeo
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows multimedia, administrador de compresión de vídeo (VCM)
- multimedia, administrador de compresión de vídeo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487635"
---
# <a name="about-the-video-compression-manager"></a>Acerca del administrador de compresión de vídeo

Normalmente, los compresores instalables operan con datos de imagen de vídeo almacenados en archivos de audio y vídeo intercalado (AVI). En esta información general se explican las técnicas de programación que se usan para tener acceso a los compresores instalables a través de VCM y se tratan los temas siguientes:

-   VCM y el vídeo para la arquitectura de Windows
-   Comprimir y descomprimir los datos de imagen de la aplicación
-   Usar representadores VCM para dibujar datos desde la aplicación
-   Funciones y estructuras de VCM

Antes de leer esta información general, debe estar familiarizado con los servicios gráficos de Microsoft Win32. En concreto, el uso de los mapas de bits y las estructuras relacionadas con los mapas de bits, como [**bitmapinfo (**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) y [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), se usan en gran medida en VCM. Para obtener información adicional sobre las estructuras **bitmapinfo (** y **BITMAPINFOHEADER** , vea [mapas de bits](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> El administrador de compresión de audio (ACM) proporciona compatibilidad de nivel de sistema para los controladores de compresión y descompresión de audio. Para obtener una descripción de los servicios de compresión de audio, consulte [Administrador de compresión de audio](audio-compression-manager.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de compresión de vídeo](video-compression-manager.md)
</dt> </dl>

 

 