---
description: GetPlayerParentalLevel recupera el nivel de administración parental establecido en el objeto MSWebDVD.
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: GetPlayerParentalLevel (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0426c48589449e03b78d894300ff2c83d83d625a269b19f0e985f78d49973f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756485"
---
# <a name="getplayerparentallevel-method"></a>GetPlayerParentalLevel (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

recupera `GetPlayerParentalLevel` el nivel de administración parental establecido en el objeto **MSWebDVD.**

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que especifica el nivel parental actual en el navegador de DVD o -1 si la administración parental está deshabilitada.

## <a name="remarks"></a>Comentarios

Una aplicación de reproductor es responsable de aplicar los controles parentales. El nivel parental del reproductor es un valor establecido por una aplicación que se puede usar para indicar el nivel parental más alto que el usuario actual puede ver. Cuando el navegador de DVD encuentre un nuevo nivel parental, use este método para determinar si el nuevo nivel es mayor que el nivel establecido por la aplicación a través de [**SelectParentalLevel**](selectparentallevel-method.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**SeleccioneParentalCountry.**](selectparentalcountry-method.md)
</dt> <dt>

[**SeleccioneParentalLevel.**](selectparentallevel-method.md)
</dt> </dl>

 

 



