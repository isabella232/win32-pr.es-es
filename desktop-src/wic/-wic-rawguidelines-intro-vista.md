---
description: Formatos de imagen sin procesar en Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formatos de imagen sin procesar en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278179"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formatos de imagen sin procesar en Windows Vista

El explorador de Windows Vista, la Galería fotográfica de Windows Vista, la Galería fotográfica de Windows Live y el visor de fotos de Windows 7 usan Windows Imaging Component (WIC) y, por lo tanto, admiten formatos de imagen sin procesar cuando se instalan los códecs adecuados en el equipo.

Dado que WIC es una arquitectura de creación de imágenes extensible, cualquier aplicación WIC puede consumir nuevos formatos de imagen en cuanto se instalan nuevos códecs en el sistema. Esto hace que WIC sea idóneo como una solución Plug and Play para los formatos de imagen sin procesar que producen las cámaras digitales. A través de WIC, las aplicaciones de Windows pueden obtener soporte técnico para los nuevos modelos de cámara cada vez que estén disponibles códecs actualizados (idealmente, con nuevas cámaras). Los creadores de códecs pueden admitir estos escenarios implementando interfaces WIC que son comunes a todos los tipos de imagen, como se describe más detalladamente en este documento.

En la actualidad, la mayoría de las aplicaciones de consumidor principales no tienen ningún conocimiento especial de los formatos de imagen sin procesar y no exponen una interfaz de usuario para ajustar la configuración de procesamiento sin procesar.

Sin embargo, para admitir aplicaciones de imágenes especializadas, los creadores de códecs sin formato también deben implementar la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Esta interfaz expone características especiales para imágenes sin procesar, como la capacidad de realizar ajustes de imagen comunes y procesar (desarrollar) imágenes sin procesar en espacios de colores rojo-verde-azul (RGB) especificados.

Hay muchas otras interfaces WIC importantes para que los autores de códecs sin formato implementen. Estos se describen con más detalle en esta serie de temas.

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

 

 



