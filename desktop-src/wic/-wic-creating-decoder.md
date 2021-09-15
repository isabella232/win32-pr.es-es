---
description: En el tema se presenta el descodificador de mapa de bits, un componente de códec Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Información general sobre lacoding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247599"
---
# <a name="decoding-overview"></a>Información general sobre lacoding

En el tema se presenta el descodificador de mapa de bits, un componente de códec Windows Imaging Component (WIC) que se usa para descodificar archivos de imagen de una secuencia.

En este tema se incluyen las siguientes secciones.

-   [Introducción](#introduction)
-   [Descodificadores de mapa de bits nativos](#native-bitmap-decoders)
-   [Crear un descodificador de mapa de bits](#creating-a-bitmap-decoder)
-   [Extensibilidad del descodificador](#decoder-extensibility)
-   [Temas relacionados](#related-topics)

## <a name="introduction"></a>Introducción

Los descodificadores de mapa de bits se pueden ver como el contenedor externo de una imagen digital y proporciona acceso a las propiedades globales y los marcos de imagen. Algunos formatos de imagen admiten miniaturas globales, vistas previas, contextos de color o metadatos, mientras que otros proporcionan estas propiedades solo en el nivel de fotograma. Sin embargo, tenga en cuenta que muchos de los formatos de imagen estándar no admiten estas propiedades globales. Por lo tanto, muchas de las implementaciones de códec nativo proporcionadas por WIC no admiten la mayoría de estas propiedades globales. Vea la tabla de la sección Descodificadores de mapa de bits nativos de este tema para obtener información sobre la compatibilidad con propiedades globales.

En WIC, los descodificadores de mapa de bits se representan mediante la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) y proporcionan acceso a estas propiedades globales del mapa de bits y, lo que es más importante, a los marcos que contiene. La [**interfaz IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) representa un marco de mapa de bits individual y se describe en detalle en Información general sobre orígenes [de mapa de bits](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Descodificadores de mapa de bits nativos

WIC proporciona varias implementaciones nativas de la interfaz [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para los formatos de imagen web estándar y el formato HD Photo de alto rango dinámico. En la tabla siguiente se enumeran los descodificadores nativos disponibles, el nombre del identificador de clase y la compatibilidad con las propiedades globales. Aunque una característica puede no admitir una propiedad como miniaturas en el nivel global, el formato de imagen puede admitir dichas propiedades en el nivel de fotograma individual.



| Formato de imágenes | Nombre de CLSID            | Miniaturas | Vistas previas | Contextos de color | Metadatos |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | CLSID \_ WICBmpDecoder  | No         | No       | No             | No       |
| GIF          | CLSID \_ WICGifDecoder  | No         | No       | No             | Sí      |
| ICO          | CLSID \_ WICIcoDecoder  | No         | No       | No             | No       |
| JPEG         | CLSID \_ WICMidegDecoder | No         | No       | No             | No       |
| PNG          | CLSID \_ WICPngDecoder  | No         | No       | No             | No       |
| TIFF         | CLSID \_ WICTiffDecoder | No         | No       | No             | No       |
| HD Photo     | CLSID \_ WICWmpDecoder  | No         | Sí      | No             | No       |



 

## <a name="creating-a-bitmap-decoder"></a>Crear un descodificador de mapa de bits

Para descodificar una imagen mediante WIC, primero debe crear una instancia de [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) para el formato de imagen de destino. La instancia del descodificador permite acceder a las propiedades globales y los metadatos, si se admiten, así como a los marcos de imagen. La factoría de creación de imágenes de WIC, [**IWICImagingFactory,**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)proporciona varios métodos para crear descodificadores de mapa de bits. Se proporcionan los siguientes métodos de generador para crear descodificadores de mapa de bits.

-   [**CreateDecoder**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**CreateDecoderFromFileHandle**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**CreateDecoderFromFilename**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**CreateDecoderFromStream**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

En el código siguiente se muestra cómo crear un descodificador de mapa de bits mediante un nombre de archivo de imagen y recuperar el primer fotograma de la imagen.


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

Una de las características principales de WIC es un marco de extensibilidad que permite a los desarrolladores de códecs desarrollar sus propios códecs de imagen y obtener la misma compatibilidad de plataforma que las implementaciones nativas de códecs de imagen. Se usa un conjunto único y coherente de interfaces para todo el procesamiento de imágenes, independientemente del formato de imagen. Cualquier aplicación que use WIC obtiene compatibilidad automática con nuevos formatos de imagen en cuanto se instala el códec. Para obtener más información sobre el desarrollo de códecs, vea los temas de [Desarrollo de componentes](-wic-component-development.md). Para obtener más información sobre el desarrollo de descodificadores, vea [Implementing a WIC-Enabled Decoder](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre codificación](-wic-creating-encoder.md)
</dt> <dt>

[Desarrollo de componentes](-wic-component-development.md)
</dt> </dl>

 

 



