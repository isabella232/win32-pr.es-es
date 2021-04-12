---
description: El método GetButtonRect recupera el rectángulo para el botón especificado, en coordenadas de ventana.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: Método GetButtonRect
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152007"
---
# <a name="getbuttonrect-method"></a>Método GetButtonRect

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetButtonRect` método recupera el rectángulo para el botón especificado, en coordenadas de ventana.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*iButton*
</dt> <dd>

Especifica el número de botón como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto [DVDRect](dvdrect-object.md) que define el rectángulo.

## <a name="remarks"></a>Observaciones

Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



