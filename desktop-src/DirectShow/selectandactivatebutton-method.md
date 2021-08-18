---
description: El método SelectAndActivateButton selecciona y activa el botón especificado.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Método SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d141616356db5daf2ebcb19579b924f6d4cab956e03d876d0254666d55b5702b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951914"
---
# <a name="selectandactivatebutton-method"></a>Método SelectAndActivateButton

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectAndActivateButton` método selecciona y activa el botón especificado.

``` syntax
MSWebDVD.SelectAndActivateButton(iButton)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*Ibutton*
</dt> <dd>

Especifica el botón como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

Este método resalta el botón especificado y lo activa automáticamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Botones Disponibles**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



