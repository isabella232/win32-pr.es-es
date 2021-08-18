---
description: La aplicación de una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige cómo se organizan los bytes de una secuencia cuando se envían entre equipos.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintaxis de transferencia de DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6757a22743a2c44abb5ef4c46154a08e425e2b1b7045beaacc7fb4f4f206fed3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904527"
---
# <a name="der-transfer-syntax"></a>Sintaxis de transferencia de DER

La aplicación de una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige cómo se organizan los bytes de una secuencia cuando se envían entre equipos. La sintaxis de transferencia que reglas de codificación distinguida siempre sigue un *formato de etiqueta, longitud y* valor. Normalmente, el formato se conoce como un triplete TLV en el que cada campo (T, L o V) contiene uno o varios bytes.

![triplet der type, length y value (tlv)](images/der-tlv-basic.png)

El campo Etiqueta especifica el tipo de la  estructura de datos que se envía, el  *campo* Longitud especifica el número de bytes de contenido que se transfiere y el campo Valor contiene el contenido. Tenga en cuenta *que el campo* Valor puede ser un triplete si contiene un tipo de datos construido, como se muestra en la ilustración siguiente.

![der tlv triplet recursion](images/der-tlv-recursive.png)

Consulte los temas siguientes para obtener información detallada sobre los componentes de un triplete TLV.

-   [Bytes de etiqueta codificados](about-encoded-tag-bytes.md)
-   [Bytes de longitud y valor codificados](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos construidos](about-constructed-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 



