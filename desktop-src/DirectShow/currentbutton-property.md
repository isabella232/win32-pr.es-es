---
description: La propiedad CurrentButton recupera el número del botón de menú seleccionado.
ms.assetid: bd9720bc-068a-4f29-aa2d-1c6b550f789c
title: Propiedad CurrentButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b246b77283a2632f2feac4c2b374075ef9d9a205bcb71813856b9847df21b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053145"
---
# <a name="currentbutton-property"></a>Propiedad CurrentButton

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentButton` propiedad recupera el número del botón de menú seleccionado.

``` syntax
[ iButton = ] MSWebDVD.CurrentButton
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el botón.

## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura sin ningún valor predeterminado. Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**Botones Disponibles**](buttonsavailable-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



