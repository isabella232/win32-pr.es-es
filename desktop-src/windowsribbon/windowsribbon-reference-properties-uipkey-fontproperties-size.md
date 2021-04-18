---
title: UI_PKEY_FontProperties_Size
description: Identifica la propiedad de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ .
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685476"
---
# <a name="ui_pkey_fontproperties_size"></a>Tamaño de FontProperties de UI \_ PKEY \_ \_

Identifica la propiedad de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Observaciones

\_ \_ \_ Una aplicación usa el tamaño de FontProperties de PKEY de interfaz de usuario para consultar el valor del control de **tamaño de fuente** .

Los valores válidos para esta propiedad oscilan entre 1 y 9999, ambos incluidos. Si un usuario intenta escribir un valor no válido, se rechaza la entrada y el control de **tamaño de fuente** vuelve al último valor válido.

Si una aplicación intenta establecer un tamaño de fuente mediante programación en un valor fuera del intervalo válido, el marco de la cinta de opciones invalida todas las propiedades de fuente y establece los controles de fuente (**tamaño de fuente** y **fuente**) en blanco o en su estado predeterminado, si es necesario.

El valor predeterminado es 0.

Un valor de 0 especifica que no se selecciona ningún tamaño de punto único (ya sea ningún texto o una ejecución de texto de tamaño heterogéneo).

Un usuario no puede establecer el control de **tamaño de fuente** en 0.

Distinto de 0, los valores válidos para el intervalo de tamaño de la interfaz de usuario \_ PKEY \_ FontProperties \_ entre *MinimumFontSize* y *MaximumFontSize* , tal y como se declara en el marcado de [control de fuentes](windowsribbon-controls-fontcontrol.md) .

> [!Note]  
> El control de **tamaño de fuente** se establece en blanco cuando el tamaño de fuente se establece mediante programación en 0, por ejemplo, cuando se resalta una ejecución de texto de tamaño heterogéneo.

 

Cuando se selecciona una ejecución de texto de tamaño heterogéneo, la aplicación debe consultar la [interfaz de usuario \_ PKEY \_ FontProperties \_ deltas](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar los comandos **aumentar fuente** y **reducir fuente** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




