---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la \_ propiedad PKEY FontProperties de la interfaz de usuario \_ \_ .
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c0046edf41fa61382d45a0662119d8fda237a0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077768"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>PKEY de IU \_ \_ FontProperties \_ deltas

Identifica la \_ propiedad PKEY FontProperties de la interfaz de usuario \_ \_ .

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Observaciones

La interfaz de usuario \_ PKEY \_ FontProperties \_ deltas se usa en una aplicación en los casos en los que la aplicación no puede especificar un valor para el **tamaño de fuente**, como cuando se selecciona una ejecución de texto de tamaño heterogéneo. El control de **tamaño de fuente** se establece en Blank y la interfaz de \_ \_ usuario PKEY FontProperties \_ se usa para capturar la interacción del usuario con los botones **aumentar tamaño de fuente** y **reducir fuente** .

La \_ interfaz \_ de usuario PKEY FontProperties \_ deltas se incluye en la [interfaz de usuario \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

En la captura de pantalla siguiente se muestran los botones de **expansión de fuente** y **reducción de fuente** de la cinta de opciones [**FontControl**](windowsribbon-element-fontcontrol.md).

![captura de pantalla de los botones de expansión de fuente y reducción de fuente en fontcontrol.](images/markup/fontcontrol-incdec.png)

En la tabla siguiente se describen los valores de propiedad.



|                           |                                 |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | Botón **aumentar fuente** , haga clic en él.   |
| `UI_FONTDELTASIZE_SHRINK` | Botón **reducir fuente** en el que se hizo clic. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades de control de fuente](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**UI \_ FONTDELTASIZE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Control de fuente](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 