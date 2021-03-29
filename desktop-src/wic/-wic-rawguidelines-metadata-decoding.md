---
description: Descodificación
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Descodificación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911937"
---
# <a name="decoding"></a>Descodificación

Para admitir correctamente los metadatos, los autores del descodificador deben hacer lo siguiente:

-   Implementar interfaces [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) e [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .
-   Implemente [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) en el descodificador de fotogramas. Si el códec admite metadatos de nivel de contenedor, esta interfaz se debe implementar en el descodificador de nivel de contenedor, así como en el descodificador de Marcos.
-   Al descodificar el flujo de imagen, llame a [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**CreateMetadataReaderFromContainer**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) para crear instancias de un lector de metadatos para cada bloque de metadatos. (Los nuevos lectores de metadatos que implemente el códec deben estar registrados con WIC).

    El descodificador no debe crear lectores de metadatos por sí mismo, sino usar WIC para crearlos en función de los bloques de metadatos de la secuencia. El descodificador debe hacerlo en todos los bloques que encuentra, incluso si no son conocidos de forma nativa por el codificador, porque es posible que los lectores de metadatos futuros estén instalados en el sistema que comprenden cómo administrar estos bloques de metadatos.

-   Si no hay ningún controlador de metadatos para un bloque, cree una instancia del lector de metadatos desconocido mediante las opciones de creación de metadatos.
-   Exponga la colección de lectores de metadatos a través de la interfaz [**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

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

 

 



