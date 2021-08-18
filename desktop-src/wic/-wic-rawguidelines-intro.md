---
description: Introducción (Directrices de WIC para formatos de imagen raw de cámara)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introducción (Directrices de WIC para formatos de imagen raw de cámara)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d96da37d36fed6af0aef271471eb2a0e5dae44bef71dfe14a4da37eba3f658c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086868"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a>Introducción (Directrices de WIC para formatos de imagen raw de cámara)

El Windows Imaging Component (WIC) proporciona un marco extensible para trabajar con imágenes y metadatos de imagen. WIC permite a los proveedores de software y hardware desarrollar códecs para que sus propios formatos de imagen puedan obtener la misma compatibilidad con la plataforma que los formatos de imagen nativos, como el formato de archivo de imagen etiquetado (TIFF), el grupo de expertos en fotografía conjunta (JPEG) o hd photo.

WIC proporciona un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen. Por lo tanto, cualquier aplicación que use WIC recibe compatibilidad automática con nuevos formatos de imagen en cuanto se instala el códec. WIC también proporciona un marco de metadatos extensible que permite a las aplicaciones leer y escribir sus propios metadatos propietarios directamente en archivos de imagen, por lo que los metadatos nunca se pierden ni se separan de la imagen.

WIC se incluye con Windows Presentation Foundation (WPF) y está integrado en Windows Vista y versiones Windows posteriores. También está disponible como componente redistribuible independiente para Windows XP.

Estas directrices están diseñadas para ayudar a los fabricantes de formato RAW en el desarrollo de códecs WIC.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen raw de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



