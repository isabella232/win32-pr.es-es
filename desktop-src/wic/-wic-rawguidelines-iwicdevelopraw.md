---
description: Compatibilidad con IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Compatibilidad con IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278176"
---
# <a name="support-for-iwicdevelopraw"></a>Compatibilidad con IWICDevelopRaw

Para permitir que las aplicaciones admitan el procesamiento sin procesar, se recomienda encarecidamente a los creadores de códec que implementen todos los parámetros de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). En Windows 7, Windows Imaging Component (WIC) requerirá compatibilidad para todos los [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Si el formato de archivo no admite todos estos parámetros, debe revisar el formato del archivo de imagen.

Para habilitar el procesamiento básico sin procesar en aplicaciones, los códecs deben admitir ajustes para la exposición (ExposureCompensationSupport) y el color (como KelvinWhitePointSupport y TintSupport). Además, se recomienda encarecidamente que se generen los espacios de colores y formatos de píxel específicos. Por supuesto, la compatibilidad con otros ajustes es recomendable, y es necesaria para Windows 7.

El códec sin formato debe proporcionar compatibilidad básica con la rotación de imágenes y la vista previa rápida. La rotación se puede especificar de dos maneras distintas:

-   Método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Este método establece el ángulo de giro deseado para la salida de las llamadas subsiguientes a [**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) (método). El autor de la llamada puede establecer la opción dstTransform para indicar el ángulo de giro deseado.

Estos dos enfoques se diferencian de las siguientes maneras:

-   Solo se puede conservar la configuración de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) entre instancias del objeto descodificador.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) solo se aplica a esa llamada concreta; no hay ninguna persistencia de ningún tipo.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) proporciona un control mucho más preciso en la rotación. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) está restringido a incrementos de 90 grados.

Si el giro se especifica en [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) y en [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), el efecto de giro es acumulativo. Por ejemplo, si [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) especifica una rotación de 25 grados y [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) especifica una rotación de 90 grados, debe ocurrir lo siguiente:

-   Las llamadas a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) deben aplicar una rotación de 25 grados (es decir, solo la cantidad especificada en [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Las llamadas a [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) con una cantidad de dstTransform de 90 producen una rotación de 115 grados (25 + 90).
-   De nuevo, solo se puede guardar la rotación de 25 grados especificada a través de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .

En Windows Vista, los métodos [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**GetThumbnail**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) y [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) permiten a los autores de llamadas obtener miniaturas incrustadas e imágenes de vista previa, respectivamente. Están pensadas para devolver vistas previas y vistas previas precalculadas de la secuencia del archivo de imagen. Generar vistas previas o vistas en miniatura "sobre la marcha" da como resultado un rendimiento deficiente en el explorador de Windows y el visor de fotos. El códec también debe proporcionar una manera de devolver rápidamente una imagen de resolución de pantalla actualizada cuando los usuarios realizan el control interactivo de la configuración de procesamiento.

Las llamadas a [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) determinarán qué llamadas posteriores a [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**copyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) devuelven (con lo que se favorece la velocidad o la calidad). Además, la interfaz IWICBitmapSourceTransform se puede usar para determinar si es necesaria la disminución de la resolución y puede aumentar el rendimiento cuando se puede aplicar. La fidelidad de color de todas las imágenes debe ser comparable. Cuando se realizan cambios en la configuración de procesamiento, todas estas representaciones deben reflejar los cambios.

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

 

 



