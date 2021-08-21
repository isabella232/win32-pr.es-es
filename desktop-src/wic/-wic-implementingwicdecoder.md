---
description: 'Más información sobre: Implementación de un descodificador de WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementación de un descodificador WIC-Enabled de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0aa2211c0b21e8f6fc921986406f7079b13c216f0bd7ada684e7748effb6c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205715"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementación de un descodificador WIC-Enabled de datos


Implementar un descodificador Windows Imaging Component (WIC) requiere escribir dos clases. Las interfaces de estas clases se corresponden directamente con las responsabilidades del descodificador que se describen en la sección [Descodificación](-wic-howwicworks.md) de Cómo funciona Windows componente de creación [de imágenes.](-wic-howwicworks.md)

Una de las clases proporciona servicios de nivel de contenedor e implementa la [interfaz IWICBitmapDecoder.](-wic-imp-iwicbitmapdecoder.md) Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la [interfaz IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) en esta clase. Se recomienda que admita la interfaz [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) tanto en el descodificador como en el codificador para admitir una mejor experiencia del usuario.

La otra clase que va a implementar proporciona servicios de nivel de marco y realiza la decodificación real de los bits de imagen para cada fotograma del contenedor. Esta clase implementa la [interfaz IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) y la [interfaz IWICMetadataBlockReader.](-wic-imp-iwicmetadatablockreader.md) Si va a escribir un descodificador para un formato sin formato, también implementa la [interfaz IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) en esta clase. Además de las interfaces necesarias, se recomienda encarecidamente implementar la interfaz [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) en esta clase para habilitar el mejor rendimiento posible para el formato de imagen.

Uno de los objetos proporcionados por WIC es [**ImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) Con frecuencia se usa [**la interfaz IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) en este objeto para crear varios componentes. Dado que se usa con frecuencia, debe mantener una referencia a ella como una propiedad de miembro en las clases de descodificador y codificador.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Funcionamiento del componente Windows creación de imágenes](-wic-howwicworks.md)
</dt> <dt>

[Interfaces de descodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre codificación](-wic-creating-encoder.md)
</dt> </dl>

 

 



