---
description: El método GetButtonRect recupera el rectángulo del botón especificado, en coordenadas de ventana.
ms.assetid: 359e9483-d7ba-45b0-882b-5a4c56dc0350
title: GetButtonRect (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 752c90637ee58aaa862245b29536dc71ad8e9a1c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061146"
---
# <a name="getbuttonrect-method"></a>GetButtonRect (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método recupera el rectángulo del botón especificado, en coordenadas `GetButtonRect` de ventana.

``` syntax
[ oButton = ] MSWebDVD.GetButtonRect(iButton)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iButton"></span><span id="ibutton"></span><span id="IBUTTON"></span>*Ibutton*
</dt> <dd>

Especifica el número de botón como entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un [objeto DVDRect](dvdrect-object.md) que define el rectángulo.

## <a name="remarks"></a>Observaciones

Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Botones Disponibles**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



