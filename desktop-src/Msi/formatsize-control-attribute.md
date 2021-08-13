---
description: Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Atributo de control FormatSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34df03c87ceb742b543f32b770c201646185ce02df6386e38c9c5af02c6a1a47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636048"
---
# <a name="formatsize-control-attribute"></a>Atributo de control FormatSize

Si este bit se establece para un control de texto estático, el control intenta dar formato automáticamente al texto mostrado como un número que representa un recuento de bytes. Para un formato correcto, el texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes. A continuación, el valor mostrado tiene formato en kilobytes (KB), megabytes (MB) o gigabytes (GB) y se muestra con la cadena adecuada que representa las unidades. Para obtener más información, vea [Control de texto](text-control.md).



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

Para establecer este atributo en un control , incluya los bits FormatSize en la columna Atributos del registro del control en la [tabla de control](control-table.md). El texto del control debe establecerse en una cadena que represente un número expresado en unidades de 512 bytes. El texto de las cadenas de unidad se define en la tabla [UIText](uitext-table.md). La propiedad LeftUnit controla el posicionamiento de la cadena de [**unidad.**](leftunit.md) Si la **propiedad LeftUnit** se define como cualquier valor, la cadena de unidad aparece antes del valor numérico. Si aparece algo distinto de caracteres numéricos en el texto asociado al control , el valor mostrado no está definido.

En tiempo de ejecución, el instalador resuelve la propiedad [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) en el número total de bytes necesarios para la instalación en unidades de 512. Se puede usar un control de texto estático con el bit FormatSize para dar formato y etiquetar automáticamente el número total de bytes necesarios para la instalación en KB, MB o GB según corresponda. Para este ejemplo, suponga que el número total de bytes es 18 336 768. El instalador establece el valor de la propiedad PrimaryVolumeSpaceRequired en 18 336 768 dividido entre 512 o 35 814. El número mostrado por el control de texto con FormatSize sería de 17 MB.

Los valores numéricos del texto original se dan en unidades de 512. En la tabla anterior, la cadena 20 480 corresponde a la cadena KB porque 20 480 veces 512 produce un resultado de 10 485 760 bytes o 10 240 KB.

Las cadenas de unidad enumeradas en la tabla anterior hacen referencia a las claves de la tabla [UIText](uitext-table.md), donde se define el texto de la cadena de unidad.

La propiedad LeftUnit controla el posicionamiento de la cadena de [**unidad.**](leftunit.md) Si la **propiedad LeftUnit** se define como cualquier valor, la cadena de unidad aparece antes del valor numérico.

Si aparece algo distinto de caracteres numéricos en el texto asociado al control , el valor mostrado no está definido.

Para obtener más información, vea [Controlar atributos](control-attributes.md) y [controles](controls.md).

 

 



