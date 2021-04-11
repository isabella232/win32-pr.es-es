---
description: GetPlayerParentalLevel recupera el nivel de administración parental establecido en el objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: Método GetPlayerParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151995"
---
# <a name="getplayerparentallevel-method"></a>Método GetPlayerParentalLevel

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

`GetPlayerParentalLevel`Recupera el nivel de administración parental establecido en el objeto **MSWebDVD** .

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que especifica el nivel parental actual en el navegador de DVD o-1 si la administración parental está deshabilitada.

## <a name="remarks"></a>Observaciones

Una aplicación de reproducción es responsable de aplicar controles parentales. El nivel parental del reproductor es un valor establecido por una aplicación que se puede usar para indicar el nivel parental más alto que puede ver el usuario actual. Cuando el navegador de DVD encuentra un nuevo nivel parental, use este método para determinar si el nuevo nivel es mayor que el nivel establecido por la aplicación a través de [**SelectParentalLevel**](selectparentallevel-method.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



