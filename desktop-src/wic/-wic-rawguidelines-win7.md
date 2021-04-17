---
description: Requisitos de códecs sin formato para Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Requisitos de códecs sin formato para Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687870"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Requisitos de códecs sin formato para Windows 7

Como mínimo, se necesitan las siguientes características de códec:

Toda la funcionalidad necesaria para la compatibilidad con la Galería fotográfica y el shell de Windows Vista: miniatura, vista previa y rotación (persistente). El procesamiento sin procesar debe tener como valor predeterminado la configuración de as-Shot.

La compatibilidad con los metadatos principales (tanto de lectura como de escritura), los metadatos no EXIFs, así como los metadatos EXIF, deben conservarse dentro de formatos de archivo sin formato sin usar archivos sidecar.

Compatibilidad con la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . En Windows 7, el componente WIC de Windows Imaging (WIC) requiere que se implementen todas las interfaces de parámetro que expone [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .

Compatibilidad con el estado de orientación:

-   90 el uso del método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) se debe aplicar a rotaciones de imagen de paso de grado. Las aplicaciones y Windows usan este método para girar las imágenes (y las vistas en miniatura y las vistas previas almacenadas en caché).
-   El códec también debe conservar la aplicación de giro mediante esta API (consulte más adelante en este documento).
-   Las aplicaciones pueden usar las capacidades de rotación de la API de [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , pero el códec no serializará ninguna configuración de rotación en esta API, por lo que no se conservarán las rotaciones realizadas con [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

Compatibilidad con la extracción en miniatura y vista previa de alta velocidad. Si la dimensión de la vista previa de píxeles máxima (ancho o alto) es inferior a 1024 píxeles de tamaño, Windows Vista solicitará un procesamiento para la vista previa de la pantalla:

-   El método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) debe admitir al menos los modos [**WICRawRenderQualityDraftMode**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) y [**WICRawRenderQualityBestQuality**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) para permitir una representación más rápida de miniaturas y vistas previas que el modo de calidad completa.
-   Windows llamará a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con el tamaño de resolución de pantalla solicitado.
-   Los tamaños de la resolución de pantalla deben ser compatibles con la API anterior.
-   Se requiere un procesamiento de imagen coherente de los bits de miniaturas, vista previa y imagen completa de [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .

Formatos de píxeles de intervalo dinámico alto (HDR).

Impresión de XML Paper Specification (XPS).

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

 

 



