---
description: El método AcceptParentalLevelChange acepta o rechaza el nuevo nivel de administración parental temporal.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: AcceptParentalLevelChange (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162418"
---
# <a name="acceptparentallevelchange-method"></a>AcceptParentalLevelChange (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El método AcceptParentalLevelChange acepta o rechaza el nuevo nivel de administración parental temporal.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Especifica el nuevo nivel parental como un valor booleano.



| Value | Descripción                               |
|-------|-------------------------------------------|
| true  | Acepte el nuevo nivel de administración parental. |
| false | Rechazar el nuevo nivel de administración parental. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a este método en respuesta a una notificación de eventos EC DVD PARENTAL LEVEL CHANGE para especificar si el navegador de DVD debe reproducir el contenido con el nuevo nivel parental o rama donde el disco especifica si se rechaza el nuevo \_ \_ \_ \_ nivel.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Aplicación de los niveles de administración parental](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SeleccioneParentalCountry.**](selectparentalcountry-method.md)
</dt> <dt>

[**SeleccioneParentalLevel.**](selectparentallevel-method.md)
</dt> </dl>

 

 



