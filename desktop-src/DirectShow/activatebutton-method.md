---
description: El método ActivateButton activa el botón de menú seleccionado.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: ActivateButton (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64853a191f688758deb42061e95c91308ff88c00fe9482cce677f8b00926f26f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873525"
---
# <a name="activatebutton-method"></a>ActivateButton (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método ActivateButton activa el botón de menú seleccionado.

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

Use este método para activar un botón que se ha seleccionado a través del método [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton,**](selectlowerbutton-method.md) [**SelectUpperButton**](selectupperbutton-method.md)o [**SelectRightButton.**](selectrightbutton-method.md)

 

 



