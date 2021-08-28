---
description: Encoding
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificación (Windows de creación de imágenes)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b3d6eef499379bbdc668e70d5d0ec4326b390372da910934a6e7c7f547d177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964654"
---
# <a name="encoding-windows-imaging-component"></a>Codificación (Windows de creación de imágenes)

El autor del codificador debe hacer lo siguiente:

-   Implemente [**las interfaces IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) [**e IWICBitmapFrameEncode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)
-   Implemente [**IWICMetadataBlockWriter en**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) el codificador de fotogramas. Si el códec admite metadatos de nivel de contenedor, esta interfaz debe implementarse en el codificador de nivel de contenedor, así como en el codificador de fotogramas.
-   Si el formato del contenedor contiene implícitamente cualquier bloque de metadatos obligatorio, cree una instancia de un escritor de metadatos para cada uno de estos bloques. Por ejemplo, el formato TIFF requiere un dispositivo de interfaz (IFD) para cada fotograma, por lo que el escritor IFD siempre debe exponerse.
-   Implemente compatibilidad para administrar la colección de escritores de metadatos. El escritor de bloques administra los requisitos de pedido o las restricciones de contenedor en los tipos de bloques de metadatos que se pueden codificar. El escritor de bloques debe comprobar que los nuevos escritores de metadatos se pueden incrustar en el formato de contenedor.
-   Al codificar el flujo de imágenes, llame a [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar el contenido de cada escritor de metadatos en la secuencia. Si el bloque de metadatos contiene metadatos "críticos", el codificador debe establecer los elementos de metadatos críticos antes de solicitar al escritor de metadatos que deserialice el contenido.
-   Compruebe si hay controladores de metadatos desconocidos para asegurarse de que los bloques de metadatos redundantes no están presentes. Esto es importante porque, a la vez que se conservan los metadatos en un escenario de descodificación o codificación, los bloques desconocidos pueden ser un duplicado de bloques de metadatos obligatorios.

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

 

 



