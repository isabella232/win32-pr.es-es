---
description: El método SelectAtPosition selecciona el botón de menú en las coordenadas de puntero del mouse especificadas.
ms.assetid: 005ec550-e04c-4dae-aa5d-d79afefe48ed
title: Método SelectAtPosition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83cd45bc0d0a532531658a7cd55b6b1fa9a450726f1a00cf358c2db44b3e5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072659"
---
# <a name="selectatposition-method"></a>Método SelectAtPosition

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectAtPosition` método selecciona el botón de menú en las coordenadas de puntero del mouse especificadas.

``` syntax
MSWebDVD.SelectAtPosition(xPos, yPos)
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

## <a name="remarks"></a>Comentarios

Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

Al seleccionar simplemente se resalta el botón. Para enviar el comando asociado a un botón que se ha seleccionado, llame a [**ActivateButton**](activatebutton-method.md).

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
</dt> </dl>

 

 



