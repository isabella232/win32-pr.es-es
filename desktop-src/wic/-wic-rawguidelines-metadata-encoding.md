---
description: Encoding
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Codificación (componente de Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716637"
---
# <a name="encoding-windows-imaging-component"></a>Codificación (componente de Windows Imaging)

El autor del codificador debe hacer lo siguiente:

-   Implementar interfaces [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) y [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .
-   Implemente [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) en el codificador de fotogramas. Si el códec admite metadatos de nivel de contenedor, esta interfaz se debe implementar en el codificador de nivel de contenedor, así como en el codificador de fotogramas.
-   Si el formato de contenedor contiene implícitamente cualquier bloque de metadatos obligatorio, cree una instancia de un escritor de metadatos para cada uno de estos bloques. Por ejemplo, el formato TIFF requiere un dispositivo de interfaz (IFD) para cada fotograma, por lo que el escritor de la IFD siempre debe estar expuesto.
-   Implementar la compatibilidad para administrar la colección de escritores de metadatos. El escritor de bloques administra los requisitos de los pedidos o las restricciones de contenedor en los tipos de bloques de metadatos que se pueden codificar. El escritor de bloques debe comprobar que los nuevos escritores de metadatos se pueden insertar en el formato del contenedor.
-   Al codificar el flujo de imagen, llame a [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) para serializar el contenido de cada escritor de metadatos en la secuencia. Si el bloque de metadatos contiene metadatos "críticos", el codificador debe establecer los elementos de metadatos críticos antes de solicitar al escritor de metadatos que serialice el contenido.
-   Busque los controladores de metadatos desconocidos para asegurarse de que los bloques de metadatos redundantes no están presentes. Esto es importante porque, mientras se conservan los metadatos en un escenario de descodificación o codificación, los bloques desconocidos podrían ser un duplicado de bloques de metadatos obligatorios.

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

 

 



