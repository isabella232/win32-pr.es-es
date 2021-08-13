---
description: Formatos de imagen RAW en Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagen RAW en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709863"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formatos de imagen RAW en Windows Vista

Windows Vista Explorer , Windows Vista Galería de fotos, Window Live Galería de fotos y Windows 7 Visualizador de fotos usan Windows Imaging Component (WIC) y, por tanto, admiten formatos de imagen RAW cuando se instalan códecs adecuados en el equipo.

Dado que WIC es una arquitectura de creación de imágenes extensible, cualquier aplicación WIC puede consumir nuevos formatos de imagen en cuanto se instalen nuevos códecs en el sistema. Esto hace que WIC sea ideal como Plug and Play solución para los formatos de imagen RAW que producen las cámaras digitales. A través de WIC, Windows aplicaciones pueden obtener compatibilidad con nuevos modelos de cámara cada vez que los códecs actualizados estén disponibles (idealmente en la caja con nuevas cámaras). Los autores de códecs pueden admitir estos escenarios mediante la implementación de interfaces WIC que son comunes a todos los tipos de imagen, como se describe con más detalle en este documento.

En la actualidad, la mayoría de las aplicaciones de consumidor estándar no tienen ningún conocimiento especial de los formatos de imagen RAW y no exponen una interfaz de usuario para ajustar la configuración de procesamiento RAW.

Sin embargo, para admitir aplicaciones de creación de imágenes especializadas, los autores de códecs RAW también deben implementar la [**interfaz IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Esta interfaz expone características especiales para las imágenes RAW, como la capacidad de realizar ajustes de imagen comunes y procesar (desarrollar) imágenes RAW en espacios de color rojo-verde-azul (RGB) especificados.

Otras interfaces WIC son importantes para que los autores de códecs RAW implementen. Estos temas se tratan con más detalle en esta serie de temas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen sin formato de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



