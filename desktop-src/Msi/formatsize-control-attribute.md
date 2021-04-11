---
description: Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formatear atributo de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275927"
---
# <a name="formatsize-control-attribute"></a>Formatear atributo de control

Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes. Para que el formato sea correcto, el texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes. A continuación, se da formato al valor mostrado en kilobytes (KB), megabytes (MB) o gigabytes (GB) y se muestra con la cadena adecuada que representa las unidades. Para obtener más información, vea [control de texto](text-control.md).



| Valor numérico del texto original | Cadena de unidad usada |
|----------------------------------|------------------|
| Menor que 20480                  | KB               |
| Menor que 20971520               | MB               |
| Menor que 10737418240            | GB               |



 

## <a name="valid-controls"></a>Controles válidos



| Decimal | Hexadecimal | Control                          |
|---------|-------------|----------------------------------|
| 524 288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya los bits de formato en la columna Attributes del registro del control en la [tabla de control](control-table.md). El texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes. El texto de las cadenas de unidad se define en la [tabla UIText](uitext-table.md). La posición de la cadena de unidad se controla mediante la propiedad [**LeftUnit**](leftunit.md) . Si la propiedad **LeftUnit** se define como cualquier valor, la cadena de unidad aparece delante del valor numérico. Si en el texto asociado al control aparece algo que no sea un carácter numérico, el valor mostrado es indefinido.

En tiempo de ejecución, el instalador resuelve la propiedad [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) en el número total de bytes necesarios para la instalación en unidades de 512. Se puede usar un control de texto estático con el bit Formatme para dar formato y etiquetar automáticamente el número total de bytes necesarios para la instalación en KB, MB o GB, según corresponda. Para los fines de este ejemplo, suponga que el número total de bytes es 18.336.768. El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en 18.336.768 dividido entre 512 o 35.814. El número que muestra el control de texto con Formatme sería 17MB.

Los valores numéricos del texto original se proporcionan en unidades de 512. En la tabla anterior, la cadena 20.480 corresponde a la cadena de KB porque 20.480 veces 512 produce un resultado de 10.485.760 bytes o de 10.240 KB.

Las cadenas de unidad enumeradas en la tabla anterior hacen referencia a las claves de la [tabla UIText](uitext-table.md), donde se define el texto de la cadena de unidad.

La posición de la cadena de unidad se controla mediante la propiedad [**LeftUnit**](leftunit.md) . Si la propiedad **LeftUnit** se define como cualquier valor, la cadena de unidad aparece delante del valor numérico.

Si en el texto asociado al control aparece algo que no sea un carácter numérico, el valor mostrado es indefinido.

Para obtener más información, vea [controles](controls.md)y [atributos de control](control-attributes.md) .

 

 



