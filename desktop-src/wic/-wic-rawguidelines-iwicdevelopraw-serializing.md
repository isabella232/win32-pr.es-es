---
description: Directrices de implementación para serializar IWICDevelopRaw Configuración
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Directrices de implementación para serializar IWICDevelopRaw Configuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709835"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Directrices de implementación para serializar IWICDevelopRaw Configuración

La [**interfaz IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expone la configuración que la aplicación puede usar para modificar el procesamiento de la imagen RAW. La configuración debe poder serializarse para que se conserve entre sesiones. Aunque esto se puede hacer de varias maneras, se recomienda codificar estos datos de una manera coherente con otros metadatos.

Estas son algunas directrices generales de implementación:

-   Cualquier configuración realizada a través de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (como rotación o saldo en blanco) debe evitar sobrescribir la configuración de la cámara o los datos "tal como se toma", a menos que la etiqueta se utilice normalmente como "configuración actual". Por ejemplo, las etiquetas de orientación EXIF se pueden usar para conservar la rotación.
-   Es preferible no tener que guardar todo el archivo (incluidos los datos de píxeles de mosaico) cada vez que se solicita serializar la configuración de [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)
-   El proceso de serializar [**la configuración de IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) generalmente seguirá este orden de eventos. La aplicación:

    1.  Crea instancias de [**un IWICBitmapDecoder en**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) un archivo RAW.
    2.  Llama [**a IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) para obtener un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) para el marco RAW.
    3.  Llama a QueryInterface en la interfaz IWICBitmapFrameDecode para la interfaz IWICDevelopRaw.
    4.  Llama [**a IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), que devuelve una interfaz IPropertyBag2 con todas las propiedades actuales almacenadas en ella.

        En este punto del proceso, el objetivo es serializar la configuración de la interfaz IPropertyBag2 en el archivo RAW. Para ello, es necesario girar un codificador, y así sucesivamente, que se detalla en los pasos siguientes.

    5.  Crea un [**IWICBitmapEncoder para**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) el archivo RAW.
    6.  Llama [**a IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Inicializar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), pasando una nueva secuencia (en blanco) para codificar.
    7.  Llama [**a IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) para crear un nuevo IWICBitmapFrameEncode para el marco RAW.
    8.  Llama [**a IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Inicializa**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)y pasa la interfaz IPropertyBag2 del paso 4.
    9.  Llama [**a IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) desde el marco de imagen RAW del descodificador.
    10. Llama [**a IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). A continuación, el códec serializa las propiedades de IPropertyBag2 del paso 8 en el archivo. Se supone que el método más común para serializar las propiedades es escribirlas como metadatos en el archivo.
    11. Llama [**a IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Confirmar**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Llama a IStream::Commit en la secuencia del paso 6.

    La configuración se serializa en el archivo .

    Este método incurre en el costo de volver a escribir todo el archivo RAW cada vez que se serializa la configuración. Esto se puede evitar si implementa [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) o si el formato de archivo de imagen admite XMP o EXIF, ya que WIC proporciona [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) para ambos formatos. Además, si el códec escribe cambios al final del archivo de imagen, no terminará reescribiendo todo el archivo de imagen.

-   Los conjuntos de parámetros se cargan desde el estado serializado cuando la aplicación establece la enumeración [**WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) en el método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) La marca [**WICRawParameterSet.WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) hace referencia al último conjunto de parámetros guardados, por lo que una carga con esta marca debería dar lugar a la restauración de los parámetros al último estado guardado.
-   Tras la carga inicial, se debe cargar el último conjunto de parámetros guardados, si está disponible. Si no es así, la configuración "tal como se toma" debe usarse como valores preestablecidos en las variables de interfaz [**IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Esta configuración de toma también se puede cargar mediante la marca [**WICRawParameterSet.WICAsShotParameterSet.**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset)
-   El identificador [**WICRawParameterSet.WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) está diseñado para representar una configuración "Auto". El diseñador de códecs puede elegir cualquiera de los enfoques siguientes sobre cómo establecer parámetros [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) cuando se establece esta configuración:

    -   Realice una optimización algorítmica de algunos parámetros, como la exposición o el color. Este es el modo en que Auto funciona en editores de imágenes típicos y se basa principalmente en el análisis de datos de píxeles.
    -   Establezca la configuración de la cámara de forma similar a cómo se habría comportado una configuración automática. Esto resulta útil si la imagen se rodó en una configuración manual y permite al usuario invalidar la configuración manual.
    -   No haga nada. No es necesario establecer todos los controles cuando se selecciona Automático y es correcto dejar la configuración sin cambios.

Las herramientas de edición Windows Vista Galería de fotos y Galería fotográfica de Windows Live y otras aplicaciones de edición usan la carga de parámetros [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Auto cuando el usuario selecciona Corregir automáticamente para todos los ajustes normales de control de códecs, como el color y la exposición, para obtener los mejores resultados.

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

 

 



