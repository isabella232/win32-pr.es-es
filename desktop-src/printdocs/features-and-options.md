---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 8084fa15-85e5-4c8d-b585-8c349482a6eb
title: Características y opciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866cead02021b8d933ca03483e77de832d8d094a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105707611"
---
# <a name="features-and-options"></a>Características y opciones

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Las construcciones de características, opciones y parámetros se usan en un documento de PrintCapabilities para representar atributos de dispositivo que contribuyen a la definición de la configuración del dispositivo. Para obtener un ejemplo de una construcción de característica/opción, considere la posibilidad de usar un dispositivo de impresión que sea capaz de imprimir en varias resoluciones. El atributo de dispositivo que define la resolución puede representarse como una instancia de característica, y cada uno de los valores de resolución de salida posibles se representa como una instancia de opción individual. Una instancia de opción puede representar una resolución de 300 ppp, otra puede representar una resolución de 600 ppp, etc.

Se debe observar que el esquema de impresión requiere que la lista de instancias de características, opciones y ParameterDef de cada documento de PrintCapabilities debe permanecer constante, independientemente de la configuración. Esto permite que las configuraciones y dependencias de las configuraciones se expresen de forma inequívoca. La implicación de este requisito es que todas las características y subcaracterísticas deben tener una configuración bien definida, independientemente de la configuración de cualquier otra característica o subcaracterística. Por lo tanto, cada subcaracterística debe tener una opción que sea equivalente a un valor no operativo (desactivado, deshabilitado o ninguno), que se selecciona automáticamente para todas las subcaracterísticas cuando el usuario selecciona la opción no OP en la característica primaria. Por el contrario, cuando una de las subcaracterísticas está establecida en una opción habilitada, también se habilitan la característica primaria y otras subcaracterísticas asociadas. Mientras tanto, el proveedor de PrintTicket debe asegurarse (durante la validación de PrintTicket) que la configuración de todas las instancias de características y subcaracterísticas está definida, independientemente de la configuración del dispositivo, y de que la configuración de la subcaracterística sea coherente con la configuración de la característica primaria. Esto garantiza que el dispositivo no tenga un PrintTicket incoherente en el que algunas subcaracterísticas indiquen que, por ejemplo, el grapado está habilitado, pero otras subcaracterísticas indican que el grapado está deshabilitado.

Tenga en cuenta que no es necesario que los autores de PrintCapabilities utilicen las capacidades de anidamiento de los elementos de característica. Si lo prefieren, pueden presentar todas las instancias de características en una estructura plana, como elementos del mismo nivel. Tenga en cuenta también que una colección anidada de instancias de características se puede acoplar simplemente moviendo todas las subcaracterísticas al nivel de raíz. La única precaución que debe tomarse es asegurarse de que los atributos de nombre de estas instancias de características son únicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



