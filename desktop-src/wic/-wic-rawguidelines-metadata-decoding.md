---
description: Descodificación
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Descodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bfef7fe219ae7ff05227bfba48b69188844dc2373bd1c3099737224758fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117667332"
---
# <a name="decoding"></a>Descodificación

Para admitir correctamente los metadatos, los autores del descodificador deben hacer lo siguiente:

-   Implemente [**las interfaces IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) [**e IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)
-   Implemente [**IWICMetadataBlockReader en**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) el descodificador de fotogramas. Si el códec admite metadatos de nivel de contenedor, esta interfaz debe implementarse en el descodificador de nivel de contenedor, así como en el descodificador de marco.
-   Al decodificar el flujo de imagen, llame a [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para crear una instancia de un lector de metadatos para cada bloque de metadatos. (Los nuevos lectores de metadatos que implemente el códec deben registrarse con WIC).

    El descodificador no debe crear lectores de metadatos por sí solo, sino que debe usar WIC para crearlos en función de los bloques de metadatos de la secuencia. El descodificador debe hacerlo en todos los bloques que encuentre, incluso si el docoder no los conoce de forma nativa, ya que es posible que se instalen lectores de metadatos futuros en el sistema que entiendan cómo controlar estos bloques de metadatos.

-   Si no hay ningún controlador de metadatos para un bloque, cree una instancia del lector de metadatos desconocido mediante las opciones de creación de metadatos.
-   Exponga la colección de lectores de metadatos a través [**de la interfaz IWICMetadataBlockReader.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Windows Imaging Component información general](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Directrices de WIC para formatos de imagen sin formato de cámara](-wic-rawguidelines.md)
</dt> <dt>

[Cómo escribir un códec WIC-Enabled datos](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



