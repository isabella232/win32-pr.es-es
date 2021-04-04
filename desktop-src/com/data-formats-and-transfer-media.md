---
title: Formatos de datos y medios de transferencia
description: Formatos de datos y medios de transferencia
ms.assetid: c6023c42-ce20-40e4-9d88-55fa1d2a4d38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6893fabd776d196cbc7354dde7c330f9caffb0a
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/21/2020
ms.locfileid: "104078591"
---
# <a name="data-formats-and-transfer-media"></a>Formatos de datos y medios de transferencia

La mayoría de las plataformas, incluidas Windows, definen un protocolo estándar para transferir datos entre aplicaciones, en función de un conjunto de funciones denominado portapapeles. Las aplicaciones que usan estas funciones pueden compartir datos incluso si sus formatos de datos nativos son muy diferentes. Por lo general, estos portapapeles tienen dos lagunas significativas que COM ha superado.

En primer lugar, las descripciones de datos usan solo un identificador de formato, como el único identificador de formato del portapapeles de 16 bits en Windows, lo que significa que el portapapeles solo puede describir la estructura de los datos, es decir, el orden de los bits. Puede notificar, "tengo un mapa de bits" o tengo algo de texto ", pero no puede especificar los dispositivos de destino para los que se componen los datos, qué vistas o aspectos de los datos pueden proporcionar, o qué medios de almacenamiento son más adecuados para su transferencia. Por ejemplo, no puede notificar, "tengo una cadena de texto que se almacena en memoria global y con formato para presentación en pantalla o en una impresora" o "tengo un mapa de bits de boceto en miniatura representado para una impresora de matriz de puntos de PPP 100 y se almacena como un archivo de disco".

En segundo lugar, todas las transferencias de datos mediante el portapapeles suelen producirse a través de la memoria global. El uso de memoria global es razonablemente eficaz para pequeñas cantidades de datos, pero horriblemente ineficaz para grandes cantidades, como un objeto multimedia de 20 MB. La memoria global es lenta para un objeto de datos de gran tamaño, cuyo tamaño requiere un intercambio considerable a la memoria virtual en el disco. En los casos en los que los datos que se intercambian van a residir principalmente en el disco, forzarlo a través de este cuello de botella de la memoria virtual es muy ineficaz. Una manera mejor sería omitir completamente la memoria global y simplemente transferir los datos directamente al disco.

Para mitigar estos problemas, COM proporciona dos estructuras de datos: [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) y [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1). Para obtener más información, vea los temas siguientes:

-   [La estructura FORMATETC](the-formatetc-structure.md)
-   [La estructura STGMEDIUM](the-stgmedium-structure.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Transferencia de datos](data-transfer.md)
</dt> </dl>

 

 




