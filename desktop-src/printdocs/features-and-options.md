---
description: Obtenga información sobre las características y opciones de un documento PrintCapabilities. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Características y opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6d0918b6237885c2c7240efb0dc0f982b882f
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549413"
---
# <a name="features-and-options"></a>Características y opciones

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las construcciones de características,opciones y parámetros se usan en un documento PrintCapabilities para representar atributos de dispositivo que contribuyen a la definición de la configuración del dispositivo. Para obtener un ejemplo de una construcción de característica o opción, considere un dispositivo de impresión que sea capaz de imprimir en varias resoluciones. El atributo de dispositivo que define la resolución se puede representar como una instancia de característica, con cada uno de los valores de resolución de salida posibles representados como una instancia de opción individual. Una instancia de Option puede representar una resolución de 300 ppp, otra puede representar una resolución de 600 ppp, y así sucesivamente.

Debe tenerse en cuenta que el esquema de impresión requiere que la lista de instancias de Feature, Option y ParameterDef notificadas en cada documento PrintCapabilities debe permanecer constante, independientemente de la configuración. Esto permite que las configuraciones y dependencias de las configuraciones se exprese de forma inequívoca. La implicación de este requisito es que cada característica y subfeature debe tener una configuración bien definida, independientemente de la configuración de cualquier otra característica o subfeature. Por lo tanto, cada subfeature debe tener una opción equivalente a no-op (un valor Desactivado, Deshabilitado o Ninguno), que se selecciona automáticamente para todas las subatures cuando el usuario selecciona la opción no op en la característica primaria. Por el contrario, cuando una de las subatures se establece en una opción habilitada, también se habilitan la característica primaria y otras subatures asociadas. Mientras tanto, el proveedor PrintTicket debe asegurarse (durante la validación de PrintTicket) de que la configuración de todas las instancias de característica y subfeature está definida, independientemente de la configuración del dispositivo, y de que la configuración de subfeature sea coherente con la configuración de la característica primaria. Esto garantiza que el dispositivo no tiene un PrintTicket incoherente en el que algunas subaturísticas indican que, por ejemplo, el estapling está habilitado, pero otras subfeatures indican que el stapling está deshabilitado.

Tenga en cuenta que no es necesario que los autores de PrintCapabilities utilicen las funcionalidades de anidamiento de elementos feature. Si lo prefieren, pueden presentar todas las instancias de características en una estructura plana, como elementos del mismo nivel entre sí. Tenga en cuenta también que una colección anidada de instancias de características se puede aplanar simplemente moviendo todas las subaturizaciones al nivel raíz. La única precaución que se debe tomar es asegurarse de que los atributos de nombre de estas instancias de característica son únicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



