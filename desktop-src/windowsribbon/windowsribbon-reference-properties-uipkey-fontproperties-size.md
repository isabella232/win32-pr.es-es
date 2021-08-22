---
title: UI_PKEY_FontProperties_Size
description: Identifica la propiedad \_ FontProperties Size de PKEY \_ de la interfaz de \_ usuario.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c013c41290f6e062b03572a9e3cb848752efcb12f1c779348a0253f94d40e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028633"
---
# <a name="ui_pkey_fontproperties_size"></a>Tamaño \_ de fuente PKEY de la interfaz de \_ \_ usuarioPropiedades

Identifica la propiedad \_ FontProperties Size de PKEY \_ de la interfaz de \_ usuario.

```
propertyDescription
   name = UI_PKEY_FontProperties_Size
   shellPKey = UI_PKEY_FontProperties_Size
   formatID = 00000302-7363-696e-8441798acf5aebb7
   propID = 302
   typeInfo
      type = VT_DECIMAL
```

## <a name="remarks"></a>Comentarios

Una aplicación usa el tamaño de FontProperties PKEY de la interfaz de usuario \_ para consultar el valor del control Tamaño \_ \_ **de** fuente.

Los valores válidos para esta propiedad oscilan entre 1 y 9999, ambos incluidos. Si un usuario intenta escribir un valor no válido, se rechaza la entrada y el control **Tamaño** de fuente vuelve al último valor válido.

Si una aplicación intenta establecer el tamaño de fuente mediante programación en un valor fuera del intervalo válido, el marco de la cinta de opciones invalida todas las propiedades de fuente y establece los controles de fuente **(Tamaño** de fuente y Cara de **fuente)** en blanco o en su estado predeterminado, si procede.

El valor predeterminado es 0.

El valor 0 especifica que no se selecciona ningún tamaño de punto único (no se selecciona ningún texto o una ejecución de texto de tamaño heterogéneo).

Un usuario no puede establecer el control **Tamaño de** fuente en 0.

Aparte de 0, los valores válidos para la interfaz de usuario PKEY FontProperties Size oscilan entre \_ \_ \_ *MinimumFontSize* y *MaximumFontSize,* [](windowsribbon-controls-fontcontrol.md) tal y como se declara en el marcado de control de fuentes.

> [!Note]  
> El control **Tamaño de** fuente se establece en blanco cuando el tamaño de fuente se establece mediante programación en 0, por ejemplo, cuando se resalta una ejecución de texto de tamaño heterogéneo.

 

Cuando se selecciona una ejecución de texto de tamaño heterogéneo, la aplicación debe consultar la interfaz de usuario [ \_ PKEY \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar los comandos **Grow font** y **Shrink font.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




