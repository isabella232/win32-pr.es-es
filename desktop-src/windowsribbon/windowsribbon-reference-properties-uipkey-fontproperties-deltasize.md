---
title: UI_PKEY_FontProperties_DeltaSize
description: Identifica la propiedad \_ \_ DeltaSize de PKEY de la interfaz de usuario \_ FontProperties.
ms.assetid: 021a6c79-1d3e-47d2-9601-cdaa2e66a50a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67778a710de8f69e0aea1134c12fb9ee3ebe0133
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444396"
---
# <a name="ui_pkey_fontproperties_deltasize"></a>UI \_ PKEY \_ FontProperties \_ DeltaSize

Identifica la propiedad \_ \_ DeltaSize de PKEY de la interfaz de usuario \_ FontProperties.

```
propertyDescription
   name = UI_PKEY_FontProperties_DeltaSize
   shellPKey = UI_PKEY_FontProperties_DeltaSize
   formatID = 00000309-7363-696e-8441798acf5aebb7
   propID = 313
   typeInfo
      type = UI_FONTDELTASIZE
```

## <a name="remarks"></a>Comentarios

La propiedad FontProperties DeltaSize de ui PKEY la usa una aplicación en casos en los que no es posible que la aplicación especifique un valor para Tamaño de fuente, como cuando se selecciona una ejecución de texto de tamaño \_ \_ \_ heterogéneo.  El **control Tamaño de** fuente está establecido en en blanco y la interfaz de usuario PKEY FontProperties DeltaSize se usa para capturar la interacción del usuario con los botones Crecimiento de fuente y \_ \_ \_ **Reducción de** fuente. 

Ui \_ PKEY FontProperties DeltaSize se incluye en la interfaz de usuario \_ \_ [ \_ PKEY \_ FontProperties \_ ChangedProperties](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md).

En la siguiente captura de pantalla se muestran los **botones Crecimiento** de fuente y **Reducción de** fuente del [**control FontControl de la cinta**](windowsribbon-element-fontcontrol.md)de opciones.

![captura de pantalla de los botones de aumento y reducción de fuentes de fuente en el control de fuente.](images/markup/fontcontrol-incdec.png)

En la tabla siguiente se describen los valores de propiedad.



|     Valor                 |  Descripción                    |
|---------------------------|---------------------------------|
| `UI_FONTDELTASIZE_GROW`   | **Haga clic en el** botón Aumentar fuente.   |
| `UI_FONTDELTASIZE_SHRINK` | **Se ha hecho clic en** el botón Reducir fuente. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control de fuentes](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[**\_FONTDELTASIZE de la interfaz de usuario**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_fontdeltasize)
</dt> <dt>

[Control de fuentes](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 