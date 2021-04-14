---
description: En este tema se presenta el descodificador de mapas de bits, un componente de códec básico de Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Información general sobre descodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361573"
---
# <a name="decoding-overview"></a>Información general sobre descodificación

En este tema se presenta el descodificador de mapas de bits, un componente de códec básico de Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [Descodificadores de mapas de bits nativos](#native-bitmap-decoders)
-   [Crear un descodificador de mapa de bits](#creating-a-bitmap-decoder)
-   [Extensibilidad del descodificador](#decoder-extensibility)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Los descodificadores de mapas de bits se pueden ver como el contenedor exterior de una imagen digital y proporcionan acceso a las propiedades globales y a los fotogramas de imagen. Algunos formatos de imagen admiten miniaturas globales, vistas previas, contextos de color o metadatos, mientras que otros proporcionan estas propiedades solo en el nivel de marco. Sin embargo, tenga en cuenta que muchos de los formatos de imagen estándar no admiten estas propiedades globales. Como tal, muchas de las implementaciones de códecs nativas proporcionadas por WIC no admiten la mayoría de estas propiedades globales. Vea la tabla de la sección descodificadores de mapas de bits nativos de este tema para obtener información sobre la compatibilidad de propiedades globales.

En WIC, los descodificadores de mapas de bits se representan mediante la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y proporcionan acceso a estas propiedades globales del mapa de bits y, lo que es más importante, los fotogramas que contiene. La interfaz [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) representa un marco de mapa de bits individual y se describe en detalle en la [información general sobre orígenes de mapas de bits](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Descodificadores de mapas de bits nativos

WIC proporciona varias implementaciones nativas de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para los formatos de imagen web estándar y el formato HD de alta calidad HD. En la tabla siguiente se enumeran los descodificadores nativos disponibles, el nombre del identificador de clase y la compatibilidad con las propiedades globales. Aunque es posible que una característica no admita una propiedad como miniaturas en el nivel global, el formato de la imagen puede admitir tales propiedades en el nivel de marco individual.



| Formato de imágenes | Nombre CLSID            | Miniaturas | Vistas previas | Contextos de color | Metadatos |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | No         | No       | No             | No       |
| GIF          | CLSID \_ WICGifDecoder  | No         | No       | No             | Sí      |
| ICO          | CLSID \_ WICIcoDecoder  | No         | No       | No             | No       |
| JPEG         | CLSID \_ WICJpegDecoder | No         | No       | No             | No       |
| PNG          | CLSID \_ WICPngDecoder  | No         | No       | No             | No       |
| TIFF         | CLSID \_ WICTiffDecoder | No         | No       | No             | No       |
| Foto HD     | CLSID \_ WICWmpDecoder  | No         | Sí      | No             | No       |



 

## <a name="creating-a-bitmap-decoder"></a>Crear un descodificador de mapa de bits

Para descodificar una imagen mediante WIC, primero debe crear una instancia de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para el formato de imagen de destino. La instancia del descodificador permite tener acceso a las propiedades globales y a los metadatos, si se admiten, así como a los fotogramas de imagen. El generador de imágenes WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), proporciona varios métodos para crear descodificadores de mapas de bits. Se proporcionan los siguientes métodos de generador para crear descodificadores de mapas de bits.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

En el código siguiente se muestra cómo crear un descodificador de mapa de bits con un nombre de archivo de imagen y recuperar el primer fotograma de la imagen.


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>Extensibilidad del descodificador

Una de las características principales de WIC es un marco de extensibilidad que permite a los desarrolladores de códec desarrollar sus propios códecs de imagen y obtener la misma compatibilidad con la plataforma que las implementaciones nativas de códecs de imagen. Se usa un único conjunto coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen. Cualquier aplicación que use WIC obtiene la compatibilidad automática con los nuevos formatos de imagen en cuanto se instala el códec. Para obtener más información sobre el desarrollo de códecs, vea los temas del [desarrollo de componentes](-wic-component-development.md). Para obtener más información sobre el desarrollo del descodificador, vea [implementar un descodificador de WIC-Enabled](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre la codificación](-wic-creating-encoder.md)
</dt> <dt>

[Desarrollo de componentes](-wic-component-development.md)
</dt> </dl>

 

 



