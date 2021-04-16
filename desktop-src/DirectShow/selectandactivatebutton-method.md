---
description: El método SelectAndActivateButton selecciona y activa el botón especificado.
ms.assetid: fa6239ea-0478-41f1-9515-d67a7fad11db
title: Método SelectAndActivateButton
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 717af00becd5f00f55b166353246f92ea7dfd1bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686302"
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

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Especifica el botón como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.

Este método resalta el botón especificado y lo activa automáticamente.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
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

 

 



