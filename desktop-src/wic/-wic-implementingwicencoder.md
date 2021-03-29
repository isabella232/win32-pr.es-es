---
description: Implementación de un codificador WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementación de un codificador WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277774"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementación de un codificador WIC-Enabled

## <a name="introduction"></a>Introducción

La implementación de un codificador de Windows Imaging Component (WIC) requiere la escritura de dos clases, como también se cumple para implementar un descodificador de WIC. Las interfaces de estas clases se corresponden directamente con las responsabilidades del codificador que se describen en la sección [codificación](-wic-howwicworks.md) de cómo funciona el componente de creación de imágenes de Windows.

Una de las clases proporciona servicios de nivel de contenedor y administra la serialización de los fotogramas de imagen individuales dentro del contenedor. Esta clase implementa la interfaz [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) . Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en esta clase.

La otra clase proporciona servicios de nivel de marco y realiza la codificación real de los bits de imagen para cada fotograma del contenedor. También recorre en iteración los bloques de metadatos de cada marco y solicita los escritores de metadatos adecuados para serializar los bloques. Esta clase implementa la interfaz **IWICBitmapFrameEncode** y la interfaz [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) . Esta clase debe tener un miembro IStream que la clase de nivel de contenedor inicialice en la creación de instancias, en la que el método **commit** serializará los datos del marco.

En algunos casos, como los formatos sin procesar, es posible que el autor del códec no quiera que las aplicaciones puedan codificar o volver a codificar en el formato sin procesar, ya que el propósito de un archivo sin formato es contener los datos del sensor exactamente como procede de la cámara. En los casos en los que el autor del códec no desea habilitar la codificación, sigue siendo necesario implementar un codificador rudimentario solo para habilitar la adición de metadatos. En ese caso, el codificador solo necesita admitir los métodos necesarios para escribir metadatos y puede copiar los bits de imagen no tocados desde el descodificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Vista**
</dt> <dt>

[Implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Interfaces del codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Información general sobre componentes de Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



