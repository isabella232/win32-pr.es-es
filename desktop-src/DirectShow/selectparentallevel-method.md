---
description: El método SelectParentalLevel establece el nivel parental especificado para la reproducción posterior.
ms.assetid: ffd1e204-6ed2-4190-8635-9f3866d38099
title: SelectParentalLevel (método)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95de7e8cbf1fb6fa284eddefa1ba07ebb9268825116fdac9c97fbd5d42bac84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684045"
---
# <a name="selectparentallevel-method"></a>SelectParentalLevel (método)

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `SelectParentalLevel` método establece el nivel parental especificado para la reproducción posterior.

``` syntax
MSWebDVD.SelectParentalLevel(iLevel, sUserName, sPassword)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iLevel"></span><span id="ilevel"></span><span id="ILEVEL"></span>*iLevel*
</dt> <dd>

Especifica el nivel de administración parental como entero. Para habilitar la administración parental, el *parámetro iLevel* debe oscilar entre 1 y 8. Para deshabilitar la administración parental, establezca *iLevel* en -1.

</dd> <dt>

<span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*
</dt> <dd>

Especifica el usuario actual como una cadena. (Actualmente se omite).

</dd> <dt>

<span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*
</dt> <dd>

Especifica la contraseña almacenada actualmente en el Registro como una cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método establece el nivel de acceso en el objeto MSWebDVD, que determina qué contenido puede reproducir el usuario. Los niveles más altos pueden reproducir contenido de nivel inferior, pero los niveles inferiores no pueden reproducir contenido de nivel superior. El significado exacto de los ocho niveles de administración parental de DVD varía en función del país o región. En el Estados Unidos y Canadá, los niveles se asignan a las categorías de clasificación de Motion Picture Association of America (MPAA). La administración parental en el navegador de DVD está deshabilitada de forma predeterminada.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**SeleccioneParentalCountry.**](selectparentalcountry-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**AcceptParentalLevelChange**](acceptparentallevelchange-method.md)
</dt> </dl>

 

 



