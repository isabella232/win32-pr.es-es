---
description: Más información acerca de cómo implementar un descodificador de WIC-Enabled
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Implementar un descodificador de WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911381"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Implementar un descodificador de WIC-Enabled


La implementación de un descodificador de Windows Imaging Component (WIC) requiere la escritura de dos clases. Las interfaces de estas clases se corresponden directamente con las responsabilidades del descodificador que se describen en la sección [descodificación](-wic-howwicworks.md) de [Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md).

Una de las clases proporciona servicios de nivel de contenedor e implementa la interfaz [IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md) . Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la interfaz [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) en esta clase. Se recomienda que admita la interfaz [IWICBitmapCodecProgressNotification](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) en el descodificador y el codificador para admitir una mejor experiencia del usuario.

La otra clase que se va a implementar proporciona servicios de nivel de marco y realiza la descodificación real de los bits de imagen para cada fotograma del contenedor. Esta clase implementa la interfaz [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) y la interfaz [IWICMetadataBlockReader](-wic-imp-iwicmetadatablockreader.md) . Si está escribiendo un descodificador para un formato sin formato, también debe implementar la interfaz [IWICDevelopRaw](-wic-imp-iwicdevelopraw.md) en esta clase. Además de las interfaces requeridas, se recomienda encarecidamente implementar la interfaz [IWICBitmapSourceTransform](-wic-imp-iwicmetadatablockreader.md) en esta clase para habilitar el mejor rendimiento posible para el formato de imagen.

Uno de los objetos proporcionados por WIC es [**ImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). A menudo se usa la interfaz [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) en este objeto para crear varios componentes. Dado que se usa con frecuencia, debe mantener una referencia a ella como una propiedad de miembro en las clases del descodificador y del codificador.


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

**Vista**
</dt> <dt>

[Cómo funciona el componente de creación de imágenes de Windows](-wic-howwicworks.md)
</dt> <dt>

[Interfaces del descodificador](-wic-decoderinterfaces.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Información general sobre metadatos de WIC](-wic-about-metadata.md)
</dt> <dt>

[Información general sobre la codificación](-wic-creating-encoder.md)
</dt> </dl>

 

 



