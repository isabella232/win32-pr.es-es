---
title: UI_PKEY_FontProperties_Size
description: Identifica la propiedad PKEY FontProperties Size de la interfaz \_ \_ de \_ usuario.
ms.assetid: bd426910-9852-48e1-91c8-b94be5ef7199
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae991cfe5f91b4aca4fe0b49a7b7c547e71b0fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251721"
---
# <a name="ui_pkey_fontproperties_size"></a>UI \_ PKEY \_ FontProperties \_ Size

Identifica la propiedad PKEY FontProperties Size de la interfaz \_ \_ de \_ usuario.

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

Una aplicación usa FontProperties Size de ui PKEY para \_ consultar el valor del control Tamaño \_ \_ **de** fuente.

Los valores válidos para esta propiedad oscilan entre 1 y 9999, ambos inclusive. Si un usuario intenta escribir un valor no válido, se rechaza la entrada y el control **Tamaño** de fuente vuelve al último valor válido.

Si una aplicación intenta establecer el tamaño de fuente mediante programación en un valor fuera del intervalo válido, el marco de la cinta de opciones invalida todas las propiedades de fuente y establece los controles de fuente **(Tamaño** de fuente y **Fuente)** en blanco o en su estado predeterminado, si procede.

El valor predeterminado es 0.

Un valor de 0 especifica que no se selecciona ningún tamaño de punto único (no se selecciona ningún texto o una ejecución de texto de tamaño heterogéneo).

Un usuario no puede establecer el control **Tamaño de fuente** en 0.

Distintos de 0, los valores válidos para la interfaz de usuario PKEY FontProperties Size oscilan entre \_ \_ \_ *MinimumFontSize* y *MaximumFontSize* [](windowsribbon-controls-fontcontrol.md) tal y como se declara en el marcado de Control de fuentes.

> [!Note]  
> El control **Tamaño de** fuente se establece en blanco cuando el tamaño de fuente se establece mediante programación en 0, como cuando se resalta una ejecución de texto de tamaño heterogéneo.

 

Cuando se selecciona una ejecución de texto de tamaño heterogéneo, la aplicación debe consultar la interfaz de usuario [ \_ PKEY \_ FontProperties \_ DeltaSize](windowsribbon-reference-properties-uipkey-fontproperties-deltasize.md) para capturar los comandos **Grow font** y **Shrink font.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 




