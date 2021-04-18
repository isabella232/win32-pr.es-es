---
description: Aplicar una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige el modo en que se organizan los bytes de una secuencia cuando se envían entre equipos.
ms.assetid: 674e88f9-4b65-4b42-8c44-d24fc03ae2f3
title: Sintaxis de transferencia DER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12f0ced0c47643db8f0e6e3c8f4ba2a36326e3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560046"
---
# <a name="der-transfer-syntax"></a>Sintaxis de transferencia DER

Aplicar una regla de codificación a las estructuras de datos descritas por una sintaxis abstracta proporciona una sintaxis de transferencia que rige el modo en que se organizan los bytes de una secuencia cuando se envían entre equipos. La sintaxis de transferencia usada por reglas de codificación distinguida siempre sigue un formato de *etiqueta, longitud y valor* . Normalmente, el formato se conoce como un tripledo TLV en el que cada campo (T, L o V) contiene uno o más bytes.

![tipo der, longitud y triple valor (TLV)](images/der-tlv-basic.png)

El campo de *etiqueta* especifica el tipo de la estructura de datos que se va a enviar, el campo de *longitud* especifica el número de bytes de contenido que se va a transferir y el campo de *valor* contiene el contenido. Tenga en cuenta que el campo de *valor* puede ser un triple si contiene un tipo de datos construido, tal y como se muestra en la siguiente ilustración.

![recursividad de tríptico de der TLV](images/der-tlv-recursive.png)

Vea los temas siguientes para obtener información detallada acerca de los componentes de un tripledo TLV.

-   [Bytes de etiqueta codificados](about-encoded-tag-bytes.md)
-   [Bytes de valor y longitud codificados](about-encoded-length-and-value-bytes.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Tipos construidos](about-constructed-types.md)
</dt> <dt>

[reglas de codificación distinguida](distinguished-encoding-rules.md)
</dt> </dl>

 

 



