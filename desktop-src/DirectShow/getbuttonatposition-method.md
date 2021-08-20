---
description: El método GetButtonAtPosition recupera el número del botón en las coordenadas especificadas sin seleccionarlo ni activarlo.
ms.assetid: ac933d0d-db2e-488f-b661-2fdc9f5acb39
title: GetButtonAtPosition (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ad30e3cc9bb9b3f93d731c19f4418d8e567a0cb80e63832dfe27b8c4553921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118000277"
---
# <a name="getbuttonatposition-method"></a>GetButtonAtPosition (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetButtonAtPosition` método recupera el número del botón en las coordenadas especificadas sin seleccionarlo ni activarlo.

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

Especifica la coordenada Y del puntero del mouse como un entero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que especifica el botón, si lo hay, en la posición especificada.

## <a name="remarks"></a>Comentarios

Este método devuelve cero si no hay ningún botón en las coordenadas dadas. Use este método al implementar el control personalizado del mouse después de establecer [**DisableAutoMouseProcessing en**](disableautomouseprocessing-property.md) **true.**

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActivateButton**](activatebutton-method.md)
</dt> <dt>

[**Botones Disponibles**](buttonsavailable-property.md)
</dt> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



