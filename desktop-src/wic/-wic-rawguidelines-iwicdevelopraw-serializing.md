---
description: Instrucciones de implementación para serializar la configuración de IWICDevelopRaw
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Instrucciones de implementación para serializar la configuración de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48cdc78f68e6d63ee7870b9296ae4cfa4f85547a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816083"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Instrucciones de implementación para serializar la configuración de IWICDevelopRaw

La interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expone valores que la aplicación puede usar para modificar el procesamiento de la imagen sin procesar. La configuración se debe poder serializar para que persistan entre sesiones. Aunque esto se puede hacer de varias maneras, se recomienda codificar estos datos de una manera coherente con otros metadatos.

A continuación se muestran algunas directrices generales de implementación:

-   Cualquier configuración realizada a través de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (por ejemplo, rotación o balance de blanco) debe evitar sobrescribir la configuración de la cámara o los datos "tal cual" a menos que la etiqueta se use normalmente como "valor actual". Por ejemplo, las etiquetas de orientación EXIF se pueden usar para conservar la rotación.
-   Es preferible no tener que guardar todo el archivo (incluidos los datos de píxeles de mosaico) cada vez que se solicita la serialización de la configuración de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .
-   El proceso de serialización de la configuración de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) suele seguir este orden de eventos. La aplicación:

    1.  Crea una instancia de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) en un archivo sin formato.
    2.  Llama a [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) para obtener un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) para el fotograma sin formato.
    3.  Llama a QueryInterface en la interfaz IWICBitmapFrameDecode para la interfaz IWICDevelopRaw.
    4.  Llama a [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), que devuelve una interfaz IPropertyBag2 con todas las propiedades actuales almacenadas en él.

        En este punto del proceso, el objetivo es serializar la configuración de la interfaz IPropertyBag2 en el archivo sin formato. Para ello, se requiere la rotación de un codificador, etc., que se detalla en los pasos siguientes.

    5.  Crea un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) para el archivo sin formato.
    6.  Llama a [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), pasando un nuevo flujo (en blanco) para codificar.
    7.  Llama a [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) para crear un nuevo IWICBitmapFrameEncode para el fotograma sin formato.
    8.  Llama a [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)y pasa la interfaz IPropertyBag2 del paso 4.
    9.  Llama a [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) con [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) desde el fotograma de imagen sin procesar del descodificador.
    10. Llama a [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). A continuación, el códec serializa las propiedades de IPropertyBag2 del paso 8 en el archivo. Se supone que el método más común de serialización de las propiedades se escribe como metadatos en el archivo.
    11. Llama a [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Llama a IStream:: commit en la secuencia del paso 6.

    La configuración se serializa en el archivo.

    Este método incurre en el costo de volver a escribir todo el archivo sin formato cada vez que se serializa la configuración. Esto se puede evitar si implementa [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) o si el formato de archivo de imagen admite XMP o EXIF, ya que WIC proporciona [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) para ambos formatos. Además, si el códec escribe cambios al final del archivo de imagen, no terminará de volver a escribir todo el archivo de imagen.

-   Los conjuntos de parámetros se cargan desde el estado serializado cuando la aplicación establece la enumeración [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) en el método [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) . La marca [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) hace referencia al último conjunto de parámetros guardado, por lo que una carga con esta marca debe tener como resultado la restauración de los parámetros en el último estado guardado.
-   Tras la carga inicial, se debe cargar el conjunto de parámetros guardado por última vez, si está disponible. Si no es así, se debe usar la configuración "as-Shot" como valores preestablecidos en las variables de la interfaz [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Estos valores de as-Shot también se pueden cargar mediante el uso de la marca [**WICRawParameterSet. WICAsShotParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) .
-   El identificador [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) se ha diseñado para representar un valor "auto". El diseñador de códecs puede elegir cualquiera de los siguientes métodos para establecer los parámetros de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) cuando se realiza esta configuración:

    -   Realice una optimización algorítmica de algunos parámetros, como la exposición o el color. Así es como funciona la función auto en los editores de imágenes típicos y se basa principalmente en el análisis de datos de píxeles.
    -   Establezca la configuración de la cámara de manera similar a como se habría comportado la configuración automática. Esto resulta útil si la imagen se ha captado en una configuración manual y permite que el usuario invalide la configuración manual.
    -   No haga nada. No todos los controles deben establecerse cuando se selecciona automático y es correcto dejar la configuración sin cambios.

La Galería fotográfica de Windows Vista y las herramientas de edición de la Galería fotográfica de Windows Live y otras aplicaciones de edición usan la carga automática de parámetros [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) cuando el usuario selecciona corrección automática para todos los ajustes normales del control de códecs, como color y exposición, para obtener los mejores resultados.

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

 

 



