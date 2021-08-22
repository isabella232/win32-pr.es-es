---
description: Compatibilidad con IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Compatibilidad con IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6436eb9d9422da6f5a29c196df10c97014df6beff178bb584b70e45d207dd50d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709735"
---
# <a name="support-for-iwicdevelopraw"></a>Compatibilidad con IWICDevelopRaw

Para permitir que las aplicaciones admitan el procesamiento RAW, se recomienda encarecidamente a los autores de códecs que implementen todos los parámetros de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Para Windows 7, Windows Imaging Component (WIC) requerirá compatibilidad con todos los [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Si el formato de archivo no admite todos estos parámetros, debe revisar el formato del archivo de imagen.

Para habilitar el procesamiento RAW básico en aplicaciones, los códecs deben admitir ajustes de exposición (ExposureCompensationSupport) y color (como KelvinWhitePointSupport y TintSupport). Además, se recomienda encarecidamente la salida a espacios de color y formatos de píxel específicos. La compatibilidad con otros ajustes es, por supuesto, fomentada y necesaria para Windows 7.

El códec RAW debe proporcionar compatibilidad básica para la rotación de imágenes y la vista previa rápida. La rotación se puede especificar de dos maneras distintas:

-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**Método SetRotation.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) Este método establece el ángulo de rotación deseado para la salida de las llamadas posteriores a [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**método CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) El autor de la llamada puede establecer la opción dstTransform para indicar el ángulo de rotación deseado.

Estos dos enfoques difieren de las maneras siguientes:

-   Solo se puede conservar la configuración de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) en todas las instancias del objeto descodificador.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) solo se aplica a esa llamada concreta; no hay ninguna persistencia de ningún tipo.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) proporciona un control mucho más preciso en la rotación. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) está restringido a incrementos de 90 grados.

Si se especifica la rotación en [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) e [**IWICBitmapSourceTransform,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)el efecto de rotación es acumulativo. Por ejemplo, si [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) especifica una rotación de 25 grados y [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) especifica una rotación de 90 grados, debería ocurrir lo siguiente:

-   Llamadas a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) debe aplicar una rotación de 25 grados (es decir, solo la cantidad especificada en [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Las llamadas a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con una cantidad dstTransform de 90 y, a continuación, tienen como resultado una rotación de 115 grados (25 + 90).
-   De nuevo, solo se puede conservar la rotación de 25 grados especificada a través de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation)

En Windows Vista, los métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) e [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) permiten a los llamadores obtener miniaturas incrustadas e imágenes de vista previa, respectivamente. Están diseñados para devolver vistas previamente precalculadas y miniaturas de la secuencia de archivos de imagen. La generación de vistas previas o miniaturas "sobre la marcha" da como resultado un rendimiento deficiente en Windows Explorer y Visualizador de fotos. El códec también debe proporcionar una manera de devolver una imagen de resolución de pantalla actualizada rápidamente cuando los usuarios están realizando un control interactivo de la configuración de procesamiento.

Las llamadas [**a IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determinarán qué llamadas posteriores a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devuelven (favoreciendo la velocidad o la calidad). Además, la interfaz IWICBitmapSourceTransform se puede usar para determinar si es necesario realizar un abanicamiento y puede aumentar el rendimiento cuando se puede aplicar. La fidelidad de color de todas las imágenes debe ser comparable. Cuando se realizan cambios en la configuración de procesamiento, todas estas representaciones deben reflejar los cambios.

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

 

 



