---
description: El método AcceptParentalLevelChange acepta o rechaza el nuevo nivel de administración parental temporal.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Método AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686416"
---
# <a name="acceptparentallevelchange-method"></a>Método AcceptParentalLevelChange

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
| false | Rechace el nuevo nivel de administración parental. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Llame a este método en respuesta a una \_ notificación de evento de cambio de nivel parental de DVD de EC \_ \_ \_ para especificar si el navegador de DVD debe reproducir el contenido con el nuevo nivel parental, o bien bifurcar a donde el disco especifique si se rechaza el nuevo nivel.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Aplicar niveles de administración parental](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



