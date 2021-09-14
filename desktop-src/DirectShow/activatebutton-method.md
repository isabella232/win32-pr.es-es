---
description: El método ActivateButton activa el botón de menú seleccionado.
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: ActivateButton (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162406"
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

## <a name="remarks"></a>Observaciones

Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

Use este método para activar un botón que se ha seleccionado a través del método [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton,**](selectlowerbutton-method.md) [**SelectUpperButton**](selectupperbutton-method.md)o [**SelectRightButton.**](selectrightbutton-method.md)

 

 



