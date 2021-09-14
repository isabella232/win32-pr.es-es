---
description: Formatos de imagen RAW en Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagen RAW en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256454"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formatos de imagen RAW en Windows Vista

Windows Vista Explorer , Windows Vista Galería de fotos, Window Live Galería de fotos y Windows 7 Visualizador de fotos usan Windows Imaging Component (WIC) y, por tanto, admiten formatos de imagen RAW cuando se instalan códecs adecuados en el equipo.

Dado que WIC es una arquitectura de creación de imágenes extensible, cualquier aplicación WIC puede consumir nuevos formatos de imagen en cuanto se instalen nuevos códecs en el sistema. Esto hace que WIC sea ideal como solución Plug and Play para los formatos de imagen RAW que producen las cámaras digitales. A través de WIC, Windows aplicaciones pueden obtener compatibilidad con nuevos modelos de cámara cada vez que los códecs actualizados estén disponibles (lo ideal es que estén integrados con nuevas cámaras). Los autores de códecs pueden admitir estos escenarios mediante la implementación de interfaces WIC que son comunes a todos los tipos de imagen, como se describe con más detalle en este documento.

En la actualidad, la mayoría de las aplicaciones de consumidor estándar no tienen ningún conocimiento especial de los formatos de imagen RAW y no exponen una interfaz de usuario para ajustar la configuración de procesamiento RAW.

Sin embargo, para admitir aplicaciones de creación de imágenes especializadas, los autores de códecs RAW también deben implementar la [**interfaz IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Esta interfaz expone características especiales para imágenes RAW, como la capacidad de realizar ajustes de imagen comunes y procesar (desarrollar) imágenes RAW en espacios de color rojo-verde-azul (RGB) especificados.

Otras interfaces WIC son importantes para que los autores de códecs RAW los implementen. Estos temas se tratan con más detalle en esta serie de temas.

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

 

 



