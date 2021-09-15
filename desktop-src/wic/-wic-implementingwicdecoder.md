---
description: 'Más información sobre: Implementación de un descodificador de WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementación de un descodificador WIC-Enabled de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467931"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementación de un descodificador WIC-Enabled de datos


La implementación de un descodificador Windows Imaging Component (WIC) requiere escribir dos clases. Las interfaces de estas clases se corresponden directamente [](-wic-howwicworks.md) con las responsabilidades del descodificador que se describen en la sección Descodificación de Cómo funciona el [componente Windows creación de imágenes.](-wic-howwicworks.md)

Una de las clases proporciona servicios de nivel de contenedor e implementa la [interfaz IWICBitmapDecoder.](-wic-imp-iwicbitmapdecoder.md) Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la [interfaz IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) en esta clase. Se recomienda que admita la interfaz [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) en el descodificador y el codificador para admitir una mejor experiencia del usuario.

La otra clase que implementará proporciona servicios de nivel de fotogramas y realiza la decodificación real de los bits de imagen para cada fotograma del contenedor. Esta clase implementa la [interfaz IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) y la [interfaz IWICMetadataBlockReader.](-wic-imp-iwicmetadatablockreader.md) Si va a escribir un descodificador para un formato sin formato, también implementará la [interfaz IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) en esta clase. Además de las interfaces necesarias, se recomienda encarecidamente implementar la interfaz [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) en esta clase para habilitar el mejor rendimiento posible para el formato de imagen.

Uno de los objetos proporcionados por WIC es [**ImagingFactory.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) Con frecuencia se usa [**la interfaz IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) en este objeto para crear varios componentes. Dado que se usa con frecuencia, debe mantener una referencia a ella como propiedad de miembro tanto en el descodificador como en las clases de codificador.


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

[Funcionamiento del componente Windows imaging](-wic-howwicworks.md)
</dt> <dt>

[Interfaces de descodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Introducción a los metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre codificación](-wic-creating-encoder.md)
</dt> </dl>

 

 



