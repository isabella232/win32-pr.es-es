---
description: El método GetButtonAtPosition recupera el número del botón en las coordenadas especificadas sin seleccionarlo o activarlo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: Método GetButtonAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9347929946a6f26cac4652a5357bd6454c80446c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152008"
---
# <a name="getbuttonatposition-method"></a>Método GetButtonAtPosition

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetButtonAtPosition` método recupera el número del botón en las coordenadas especificadas sin seleccionarlo o activarlo.

``` syntax
[ iButton = ] MSWebDVD.GetButtonAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Especifica la coordenada x del puntero del mouse como un entero.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Especifica la coordenada y del puntero del mouse como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que especifica el botón, si existe, en la posición especificada.

## <a name="remarks"></a>Observaciones

Este método devuelve cero si no hay ningún botón presente en las coordenadas especificadas. Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



