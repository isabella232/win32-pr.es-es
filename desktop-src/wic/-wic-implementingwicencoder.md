---
description: Implementación de un WIC-Enabled Encoder
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Implementación de un WIC-Enabled Encoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467930"
---
# <a name="implementing-a-wic-enabled-encoder"></a>Implementación de un WIC-Enabled Encoder

## <a name="introduction"></a>Introducción

Implementar un codificador Windows Imaging Component (WIC) requiere escribir dos clases, como también sucede para implementar un descodificador WIC. Las interfaces de estas clases se corresponden directamente [](-wic-howwicworks.md) con las responsabilidades del codificador que se describen en la sección Codificación de Cómo funciona Windows componente de creación de imágenes.

Una de las clases proporciona servicios de nivel de contenedor y administra la serialización de los fotogramas de imagen individuales dentro del contenedor. Esta clase implementa la [**interfaz IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) Si el formato de imagen admite metadatos de nivel de contenedor, también debe implementar la [**interfaz IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en esta clase.

La otra clase proporciona servicios de nivel de marco y realiza la codificación real de los bits de imagen para cada fotograma del contenedor. También recorre en iteración los bloques de metadatos de cada fotograma y solicita a los escritores de metadatos adecuados que serializan los bloques. Esta clase implementa la **interfaz IWICBitmapFrameEncode** y la [**interfaz IWICMetadataBlockWriter.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) Esta clase debe tener un miembro IStream que la clase de nivel de contenedor inicializa en la creación de instancias, en el que el método **Commit** serializará los datos del marco.

En algunos casos, como los formatos sin formato, es posible que el autor del códec no quiera que las aplicaciones puedan codificar o volver a codificar en el formato sin formato, porque el propósito de un archivo sin formato es contener los datos del sensor exactamente como provenían de la cámara. En los casos en los que el autor del códec no quiere habilitar la codificación, todavía es necesario implementar un codificador rudimentario solo para habilitar la adición de metadatos. En ese caso, el codificador solo necesita admitir los métodos necesarios para escribir metadatos y puede copiar los bits de imagen sin tocar del descodificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Implementación de IWICDevelopRaw](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[Interfaces de codificador](-wic-encoderinterfaces.md)
</dt> <dt>

[Cómo escribir un códec de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Información general sobre los componentes de creación de imágenes](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



