---
title: Formatos de datos y medios de transferencia
description: Formatos de datos y medios de transferencia
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ccbab96fbaca83330737521f253b3c625e67ea9a024d87d35276da2826a3964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501435"
---
# <a name="data-formats-and-transfer-media"></a>Formatos de datos y medios de transferencia

La mayoría de las plataformas, Windows, definen un protocolo estándar para transferir datos entre aplicaciones, en función de un conjunto de funciones denominado Portapapeles. Las aplicaciones que usan estas funciones pueden compartir datos incluso si sus formatos de datos nativos son muy diferentes. Por lo general, estos portapapeles tienen dos limitaciones importantes que COM ha superado.

En primer lugar, las descripciones de datos solo usan un identificador de formato, como el identificador de formato del Portapapeles de 16 bits único en Windows, lo que significa que el Portapapeles solo puede describir la estructura de sus datos, es decir, la ordenación de los bits. Puede notificar "Tengo un mapa de bits" "o tengo texto", pero no puede especificar los dispositivos de destino para los que se componen los datos, qué vistas o aspectos de sí mismos pueden proporcionar los datos o qué medios de almacenamiento son más adecuados para su transferencia. Por ejemplo, no puede informar: "Tengo una cadena de texto almacenada en memoria global y con formato para presentación en pantalla o en una impresora" o "Tengo un mapa de bits de boceto en miniatura representado para una impresora de matriz de puntos de 100 ppp y almacenado como un archivo de disco".

En segundo lugar, todas las transferencias de datos que usan el Portapapeles suelen producirse a través de la memoria global. El uso de memoria global es razonablemente eficaz para pequeñas cantidades de datos, pero muy ineficaz para grandes cantidades, como un objeto multimedia de 20 MB. La memoria global es lenta para un objeto de datos grande, cuyo tamaño requiere un intercambio considerable de memoria virtual en disco. En los casos en los que los datos que se intercambian van a residir principalmente en el disco de todos modos, forzarlo a través de este cuello de botella de memoria virtual es muy ineficaz. Una mejor manera de omitir la memoria global por completo y simplemente transferir los datos directamente al disco.

Para mitigar estos problemas, COM proporciona dos estructuras de datos: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Para obtener más información, vea los temas siguientes:

-   [Estructura FORMATETC](the-formatetc-structure.md)
-   [La estructura STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

 




