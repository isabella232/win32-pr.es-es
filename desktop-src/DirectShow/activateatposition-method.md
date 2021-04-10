---
description: El método ActivateAtPosition activa el botón de menú en la posición especificada.
ms.assetid: eddc4880-dd78-4d96-8bff-c5c883a19927
title: Método ActivateAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64a83e7fcbc00990c7be7d1a99638a1b4a3de14b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152605"
---
# <a name="activateatposition-method"></a>Método ActivateAtPosition

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método ActivateAtPosition activa el botón de menú en la posición especificada.

``` syntax
        MSWebDVD.ActivateAtPosition(xPos, yPos)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="xPos"></span><span id="xpos"></span><span id="XPOS"></span>*xPos*
</dt> <dd>

Especifica la coordenada x como un entero.

</dd> <dt>

<span id="yPos"></span><span id="ypos"></span><span id="YPOS"></span>*yPos*
</dt> <dd>

Especifica la coordenada y como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ButtonsAvailable**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



